# Fork / Join Parallelization

Fork Splits to Sub-Method

* Sub-Method name (string) is provided
* Somewhat rarely objects will be passed by string name
* Return value is a “handle” used for joining
* Submethod must NOT have parameters

Join...Joins

* Provide the forked “handle” to bring back to the main line

\
Warning: Not all functions are supported in a forked thread (MPE2)

<div>

<figure><img src="../../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

</div>



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
