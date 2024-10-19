# Fork / Join Parallelization

_By Matt Morrison._

_HSL\_Fork\_Join_

**Contact**

For assistance with this library please e-mail:

[MathewMorrison@outlook.com](mailto:MathewMorrison@outlook.com)



```clike
//Matt Morrison's Fork and Join HSL Library. // ******Beta verson1.3 // Questions email: Mathew.Morrison@hamiltoncompany.com
#ifndef HSLForkJoin_hsl #define HSLForkJoin 1
namespace Fork_Join {
////////////////// FUNCTION FORK THREAD
function ForkThread(variable i_strThread) variable { 
    //declare variables
    variable varThreadHandle;
    onerror goto myErrorHandler;
        Trace("$$$$$$$ START FORK INTO", i_strThread, "$$$$$$$$$");
        varThreadHandle = Fork(i_strThread);
        //Trace(varThreadHandle);
        Trace("$$$$$$$ FORK INTO", i_strThread, " COMPLETED SUCCESSFULLY $$$$$$$$$");
        return(varThreadHandle);
    myErrorHandler : {
        variable strErrorDescription;
        Trace("***************** AN ERROR HAS OCCURED DURING FORK FUNCTION. SEE DESCRIPTION BELOW*****************");
        strErrorDescription = err.GetDescription( );
        Trace(strErrorDescription);
        err.Clear( );
        return(hslFalse);
    }//end error handler
} //end function //onerror goto myErrorHandler;
////////////////// FUNCTION JOIN THREAD
function JoinThread(variable i_ThreadHandle) variable{
    //declare variables
    variable varReturnJoin;
    variable currentDeckPath;
    variable strFunctionName;
    strFunctionName = GetFunctionName();
    onerror goto myErrorHandler;
        Trace("$$$$$$$ START *******", strFunctionName," ****** $$$$$$$$$");
        varReturnJoin = Join( i_ThreadHandle, hslInfinite );
        Trace("$$$$$$$ JOIN THREAD COMPLETED SUCCESSFULLY $$$$$$$$$");
        return(hslTrue);
    myErrorHandler : {
        variable strErrorDescription;
        Trace("***************** AN ERROR HAS OCCURED DURING JOIN FUNCTION. SEE DESCRIPTION BELOW*****************");
        strErrorDescription = err.GetDescription( );
        Trace(strErrorDescription);
        err.Clear( );
        return(hslFalse);
        }
}
} // namespace Fork_Join
#endif // valid=0checksum=7706ab1e
```
