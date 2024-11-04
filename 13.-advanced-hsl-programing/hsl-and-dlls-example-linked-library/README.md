# HSL and DLLs Example Linked Library

Below is an example of the HSLAlphaLib which has been made to concatinate two strings to one, this will be the framework of our code to build upon the library of the DLL which converts numbers to letters

```clike
#ifndef __HSLAlphaLib_hsl__
#define __HSLAlphaLib_hsl__ 1

// Interface to library 
#ifndef HSL_RUNTIME
function StrConcat2(variable var1, variable var2) variable { return(0); }
#endif

// Implementation of library 
#ifdef HSL_RUNTIME

namespace StrAlpha
{
   // --------------------------------------------------------------------------------------
	// Error Ids
	// --------------------------------------------------------------------------------------

	namespace IDE
	{
		static const variable first(0);									// guard
		static const variable noError(first);							// No error.
		static const variable unknownType(first + 1);				// Unknown type : 
		static const variable addFieldFailed(first + 2);			// Failed to add field to record.
		static const variable openFileFailed(first + 3);			// Failed to open file: 
		static const variable closeFileFailed(first + 4);			// Failed to close file: 
		static const variable writeRecordFailed(first + 5);		// Failed to write record.
		static const variable shellOutDeleteFailed(first + 6);	// Failed to shell out delete command.
		static const variable last(first + 6);							// guard
	}

	// --------------------------------------------------------------------------------------
	// String Ids
	// --------------------------------------------------------------------------------------

	namespace IDS
	{
		static const variable first(IDE::last + 1);					// guard
		static const variable helpFileName(first + 1);				// help file name
		static const variable last(first + 1);							// guard
	}

	#ifndef __HSLStringTableLib_hsl__
	#include "HSLStringTableLib.hs_"

	#endif
	// --------------------------------------------------------------------------------------
	// Library Initialization 
	// --------------------------------------------------------------------------------------
   static variable initializedLib(hslFalse); // initialization state of the String Library
   static function InitAlphabetLibrary();      // initializes the String Library (only once)

   // --------------------------------------------------------------------------------------
	// Exception handling
	// --------------------------------------------------------------------------------------

	namespace Error
	{
		static function Raise(												// raises a runtime error
			variable errorId,													// i: error id, one of IDE
			variable& fileName,												// i: file name
			variable& funcName,												// i: function name
			variable& lineNumber)											// i: line number
		{
			variable description("");

			// set error description
			description = fileName + "(" + lineNumber + ") : " + funcName + "()\n" + StringTable::Load(errorId);
			err.SetDescription(description);

			// raise error
			err.Raise(errorId, err.GetDescription(), StringTable::Load(IDS::helpFileName));
		}

		static function RaiseEx(
			variable errorId,
			variable errorDetail,
			variable& fileName,
			variable& funcName,
			variable& lineNumber)
		{
			variable description("");

			// set error description
			description = fileName + "(" + lineNumber + ") : " + funcName + "()\n" + StringTable::Load(errorId) + errorDetail;
			err.SetDescription(description);

			// raise error
			err.Raise(errorId, err.GetDescription(), StringTable::Load(IDS::helpFileName));
		}
	}

	// --------------------------------------------------------------------------------------
	// Functions
	// --------------------------------------------------------------------------------------

	static function InitAlphabetLibrary()
	{
		// initialize the Time Library once only
		if (!initializedLib)
		{
			StringTable::Init("HSLAlphaLib");
			//StringTable::Dump();
			initializedLib = hslTrue;
		}
		return(initializedLib);
	}

}


// String Conversion function, used by StrConcat2
static function StrAStr(variable var) {
    // initialize String Library
    StrAlpha::InitAlphabetLibrary();  // Corrected namespace call
    return(var);
}

// Concatenation function - retains only StrConcat2
function StrAlphaConcat2(variable var1, variable var2) variable {
    return(StrAStr(var1) + StrAStr(var2));
}

#endif
#endif
```

