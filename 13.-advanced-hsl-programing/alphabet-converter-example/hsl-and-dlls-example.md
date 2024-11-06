# HSL and DLLs Example

In the following HSL code we see that the ClassLibrary1.AlphabetConverter registered DLL COM object is defined and working well\
\
the Pre-Compiled C# code of the AlphabetConverter is:\


```clike
using System;

namespace ClassLibrary1
{
    public class AlphabetConverter
    {
        /// <summary>
        /// Converts a number to its corresponding letter in the alphabet.
        /// </summary>
        /// <param name="number">The number to convert (1 = A, 2 = B, ...).</param>
        /// <returns>The corresponding letter as a string or an error message for out-of-range numbers.</returns>
        public string NumberToLetter(int number)
        {
            if (number < 1 || number > 26)
                return "Error: Number out of range. Please enter a number between 1 and 26.";

            // Convert number to corresponding letter
            char letter = (char)(number + 64); // 65 is 'A' in ASCII
            return letter.ToString();
        }
    }
}
```

with a CSproj configuration as:\


```clike
<Project Sdk="Microsoft.NET.Sdk">

  <PropertyGroup>
    <TargetFramework>net48</TargetFramework>
    <LangVersion>8.0</LangVersion>
    <ImplicitUsings>disable</ImplicitUsings>
    <Nullable>disable</Nullable>
  </PropertyGroup>

</Project>

```

this needs to be compiled by creating a .net project in visual studio and then building the code by using command + shift + b



this code needs to be registered to get the DLL avalible within the code dynamically. this can be done using\
\


{% code overflow="wrap" %}
```bash
regasm "C:\Users\milot\Documents\Github\CSharpVenusLibrary\ClassLibrary1\ClassLibrary1\bin\Debug\net48\ClassLibrary1.dll" /codebase
```
{% endcode %}

***



To be able to link the code to C# code now we can use this template to dynamically add the DLL and namespace to the HSL code:

```clike
#include "Method1.res"
global device ML_STAR ("Method1.lay", "ML_STAR", hslTrue);
namespace _Method { #include "HSLTrcLib.hsl" }
/* {{ 2 "LibraryInsertLine" "" */ // }} ""
variable xyz;
variable returnVariable;
/* {{ 2 "VariableInsertLine" "" */ // }} ""
// {{ 2 "TemplateIncludeBlock" ""
namespace _Method { #include "HSLMETEDLib.hs_" } 
namespace _Method { #include "HSLMECCLib.hs_" } 
namespace _Method { #include "HSLPTLLib.hsl" } 
// }} ""
// {{{ 2 "LocalSubmethodInclude" ""
namespace _Method { #include __filename__ ".sub" }
// }} ""
namespace hslAlphabet
{
    object comObject;
    variable strReturn;

    // Function declaration with proper syntax
    function convertNumberToLetter(variable xyz) variable
    {
        // Create an instance of the COM object
        comObject.CreateObject("ClassLibrary1.AlphabetConverter");
        
        // Call the NumberToLetter method and store the result in strReturn
        strReturn = comObject.NumberToLetter(xyz);

        // Return the result
        return(strReturn);
    }
}

/* {{ 2 "ProcessInsertLine" "" */ // }} ""
// {{{ 5 "main" "Begin"
namespace _Method { 
    method main() void {
    // }} ""
    // {{ 5 "main" "InitLocals"
    // }} ""

    // {{ 2 "AutoInitBlock" ""
    PTL::SetWashingStateDefault("RinseTime1", 5);
    PTL::SetWashingStateDefault("SoakTime1", 5);
    PTL::SetWashingStateDefault("FlowRate1", 11);
    PTL::SetWashingStateDefault("RinseTime2", 0);
    PTL::SetWashingStateDefault("SoakTime2", 0);
    PTL::SetWashingStateDefault("FlowRate2", 11);
    PTL::SetWashingStateDefault("DrainingTime", 10);
    PTL::SetWashingStateDefault("StartWashLiquid", 0);
    PTL::SetLoadingStateDefault("RecoveryOptionContinue", hslTrue);
    PTL::SetLoadingStateDefault("RecoveryOptionExclude", hslTrue);
    PTL::SetLoadingStateDefault("RecoveryOptionDefault", 0);
    PTL::SetLoadingStateDefault("KitLotCheckEnabled", hslFalse);
    ::RegisterAbortHandler("OnAbort");

    // Initialize the xyz variable with a numeric value
    xyz = 3;                     // Set xyz to 3
    // Declare returnVariable to hold the function output
    returnVariable = hslAlphabet::convertNumberToLetter(xyz);  

    // Output the result using TrcTrace
    TrcTrace("Converted letter:", returnVariable);  // Expected output: "C" if xyz is 3

    // }} ""
    // {{ 5 "main" "End"
    } 
}
// }} ""
// $$author=milot$$valid=0$$time=2024-11-01 21:43$$checksum=6a27ab45$$length=084$$
```





as one would expect this inreversably disables the drag and drop method editor, this is why adding the C# code to its own library is something which is ideal and lets you use the functions without worrying about the requirement of using raw HSL throughout your whole liquid handling method
