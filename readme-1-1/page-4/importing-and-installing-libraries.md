# Importing and Installing Libraries

Although most libraries can be imported by using the HSL method, some specifically require an installer to register the .dll

for instance:\
\
[Lab Automation Forums](https://labautomation.io/)

## [VectorCustomDialogs.dll Error](https://labautomation.io/t/vectorcustomdialogs-dll-error/3032)

[Hamilton (Venus) ](https://labautomation.io/c/hamilton-venus/venus-questions/31)[Venus Questions](https://labautomation.io/c/hamilton-venus/venus-questions/31)[MasonDuran](https://labautomation.io/u/MasonDuran) February 22, 2024, 2:47pm1

> Hello,
>
> I have downloaded the VectorCustomDialogs Library and successfully used some custom dialogs on one PC. However, when I try to initialize the the Custom Dialogs library a different PC I get the following error:
>
> “2024-02-22 09:30:23> LIBRARY: VectorCustomDialogs : Initialize - start; >> Start >> load comvisible library\
> 2024-02-22 09:30:23> SYSTEM : Execute method - error; An error occurred while running Vector. The error description is: C:\Program Files (x86)\HAMILTON\Library\VectorCustomDialogs\VectorCustomDialogs.hsl(533) : Invalid class string (0x23 - 0x2 - 0x39) ,\
> 2024-02-22 09:30:23> LIBRARY: VectorCustomDialogs : Initialize - start; >> Error >> VectorCustomDialogs.dll not registered (please use asmreg.bat to register).\
> 2024-02-22 09:30:23> LIBRARY: VectorCustomDialogs : MessageDialog - start; >> Error >> VectorCustomDialogs is not initialized…”
>
> Any Idea what might be causing this issue? Why is the .dll not registered?
>
> Thanks!



[EricSindelar\_Hamilton](https://labautomation.io/u/EricSindelar\_Hamilton) February 22, 2024, 2:53pm2

> You’ll need to run the installer on each PC. Importing a method with a library will copy over the library files but will not register the dll.
