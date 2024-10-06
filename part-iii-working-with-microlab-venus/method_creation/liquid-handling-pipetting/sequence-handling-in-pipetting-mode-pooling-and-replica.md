# Sequence Handling in Pipetting Mode Pooling and Replica‌

_In these two cases, the aspiration sequence should be selected as controlling. It is possible to choose how to reload a sequence:_

* _If during pipetting a sequence is used up (no more tubes are left to aspirate from), the system asks for a new carrier of tubes to be loaded._
*   _If the “Operator may reduce the sequence by a reload“ Checkbox is ticked, the user has the option of reducing the newly loaded sequence at run time. This is especially helpful if the exact amount of sample tubes varies from run to run (or from tube carrier to tube carrier)._

    \


    _Advanced Buttons_

    _Sequence manipulations can be made (separately for aspiration and dispense sequences) by means of the dialogs invoked by the \[Advanced...] Buttons._
* _If the Smart Step is going to work with sequences that have been used within this method from the preceding steps, the sequence counters can be reset. This is done by using the two checkboxes for initial sequence manipulation._
*   _If other steps are following this Smart Step, the status of the sequence which is passed back can be defined by the \[Final sequence manipulation] Radio Button. Below is an example of the advanced dialog for “Aspirate” Sequence settings._

    \


    ![image](../../../.gitbook/assets/Image\_1470.jpg)

    \


    _The “Error Settings” Dialog allows specifying an error handling approach. The choices are listed on the next page._

    \


    ![image](../../../.gitbook/assets/Image\_1471.jpg)

    _In case of an error, the following choices are:_
* _Abort the method (only abort button on run time error dialog)_
* _Offer choices (in run time) whether to abort or cancel (continue with user-defined error handling if programmed, otherwise abort)_
* _Use the fixed default error recovery (recommended) pre-programmed for the Smart Step. In this case two choices can be made_
*   _“Copy pattern”, means that in case of an error on aspiration, the corresponding well of the dispense sequence will be left out (the pattern is kept). If “Copy pattern“ is not checked, the dispense sequence positions will all be pipetted, leaving a well not pipetted at the end of the sequence._

    \


    ![image](../../../.gitbook/assets/Image\_1472.jpg)

    \

* _“Exclude error positions”, means exclude the erroneous positions from aspiration and dispensation sequences. If this option is enabled and an error occurs during an aspirate or dispense step, the erroneous position will be excluded from the sequence by removing the corresponding element from the aspirate or dispense sequence. The next time these sequences are used, the erroneous well will not be pipetted._
* _In addition, Walk-away mode can be enabled. If this checkbox is ticked, a timeout has to be specified after which the error dialog on run time will automatically close down and continue with the selected error handling: abort, cancel, or default error recovery._

\


![Originalbild anzeigen](../../../.gitbook/assets/Image\_1473.jpg)

_NOTE_

_Exception: If the option “Default error recovery” is chosen and an error occurs for which the default is set to abort (e.g. a hardware error), the walk-away mode is left on and the dialog waits for user interaction._

1.  #### _‌Tip Pick Up and Tip Eject Smart Steps‌_

    \


    _These two Smart Steps allow picking up tips from a rack and then disposing them in the tip waste after use._

    _Below is the dialog for the “Tip Pick Up” Step._

    \


    ![image](../../../.gitbook/assets/Image\_1474.jpg)

    \


    _The dialog is to specify a tip sequence. It is also possible to specify the tip counter. Below is the dialog for the “Tip Eject” Step._

    \


    ![image](../../../.gitbook/assets/Image\_1475.jpg)

    \


    _For “Channel Settings” and “Error Settings_[_”, see the description of the previous Smart Steps found in_ ](sequence-handling-in-pipetting-mode-pooling-and-replica.md#bookmark68)_Section 3.4.2 ML STAR Smart Steps Settings._
