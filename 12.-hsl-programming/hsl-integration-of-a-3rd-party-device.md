# HSL Integration of a 3rd party device

**Integration of a 3rd party device (or software) using a HSL library**

The Vector supports the integration of 3rd party software using software automation (COM). COM is the basis for OLE, ActiveX, COM+ and DCOM (Microsoft technologies). Using the Hamilton HSL Method Editor you can write a HSL (Hamilton Standard Language) Library that interfaces to the COM component.

To write a COM wrapper/driver using C#:

* Select the target platform as x86
* Create a class library interface
* Make the project ‘COM-Visible’
* Create an interface definition
  * Add methods as required
  * Use automation types (variant compatible types)
  * Add a GUID to the interface (attribute)
* Create a separate interface for any events (optional event interface for object)
  * Add a GUID to the interface (attribute)
  * Declare as IDispatch (attribute)
  * Add a DispId for each event
* Declare your class as public
  * Derive from the interface definition
  * Add a public constructor with no parameters
  * Add the attributes:
    * ProgId
    * Guid
    * To implement events, ComSourceInterfaces
  * Implement the interface methods
* Finally, expose your object (with interfaces via COM)
  * Register your assembly using ‘regasm /tlb \<assembly name>’

## C# code sample

```csharp
[GuidAttribute("F02C0FA4-dBC8-457b-88D1-31AD24C1C399")]
[InterfaceType(ComInterfaceType.InterfaceIsIDispatch)] public 
interface IHxDriverEvents
{
    [DispId(1)] void ValueChanged();
}

[GuidAttribute("F02C0FA4-dBC8-457b-88D1-31AD5671C399")]
public interface _IHxDriver
{
    int SetValue(string value); int GetValue(ref string value);
}

public delegate void ValueChangedEvt(); 
[ProgId("Driver1.MyDriver")]
[Guid("12E49563-FD68-4589-A52F-6D66B30EFD13")]
[ComSourceInterfaces(typeof(IHxDriverEvents))] 
[ClassInterface(ClassInterfaceType.None)] public 
class MyDriver : _IHxDriver
{
```



**Recommended Implementation Details C# Class Library Interface**

* Do not throw exceptions, instead use a return code (0=success)
* Provide a GetLastError() method
* Provide a GetErrorString(int code) method; provide meaningful error descriptions

**HSL Library Interface**

* Provide a very slim wrapper for the C# interface
* Do not attempt to add error recovery logic; return error codes to the method
* Refer to the (HSL Method Editor) on-line help for writing HSL libraries
