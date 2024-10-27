# Modifying the daily maitenence

If you want to modify the text prompt text the strigs are within `HslDailyMaintMetEnu.hs_`\


```clike
// Language dependant part of the Microlab® STAR IVD Daily Maintenance
// Copyright (C) by HAMILTON Bonaduz AG, CH-7402 Bonaduz.
// All rights reserved.
//
// Modification History
// 2002-05-30	Christian Frehner : Initial file creation.
// 2004-06-01  Urban Bernhard		: add new Id's dlgWarningTitle, dlgCannotRunWithSimulator and dlgMaintenanceAbortText
// 2009-10-26  Claudio Jörg		: add/uppdated Id's for integrated 5ml maintenance
// 2013-03-15  Thomas Benz		   : add Id for easyPunch maintenance

function StringTable()
{
	Insert(IDS::dlgCheckDeckCleaningTitle,          "Daily maintenance - check deck cleaning");
	Insert(IDS::dlgCheckDeckCleaningText,           "Open the flront cover and check if the deck needs to be cleaned.\n\nIf the deck is clean, press OK to continue.\n\nIf the deck needs to be cleaned, press Cancel to abort the daily maintenance.\nInstead, proceed with the weekly maintenance.");
	Insert(IDS::dlgTipWasteTitle,                   "Daily maintenance - tip waste");
	Insert(IDS::dlgTipWasteText,                    "Empty the tip waste and press OK to continue.\n\nCancel will abort the daily maintenance.");
	Insert(IDS::dlgCloseCoverTitle,                 "Daily maintenance - close cover");
	Insert(IDS::dlgCloseCoverText,                  "Close the front cover and press OK to continue.\n\nCancel will abort the daily maintenance.");
	Insert(IDS::dlgSuccessfulTitle,                 "Daily maintenance - successful");
	Insert(IDS::dlgSuccessfulText,                  "Daily maintenance successfully completed.");
	Insert(IDS::dlgFailedTitle,                     "Daily maintenance - failed");
	Insert(IDS::dlgFailedText,                      "The following daily maintenance check failed:\n");
	Insert(IDS::dlgFailedTightnessCheck1000ulText,  "\n   -> Tightness check 1000ul channels");
	Insert(IDS::dlgFailedcLLDCheck1000ulText,       "\n   -> cLLD check 1000ul channels");
	Insert(IDS::dlgFailedTightnessCheck5mlText,  	"\n   -> Tightness check 5ml channels");
	Insert(IDS::dlgFailedcLLDCheck5mlText,       	"\n   -> cLLD check 5ml channels");
	Insert(IDS::dlgErrorTitle,                      "Daily maintenance - error");
	Insert(IDS::dlgWarningTitle,                    "Daily maintenance - warning");
	Insert(IDS::dlgCannotRunWithSimulator,          "Can not run method in simulator mode.");
	Insert(IDS::dlgFailedEasyPunchText,       	   "\n   -> easyPunch ionizer state");
	Insert(IDS::dlgDailyMaintenanceText,       	   "Daily maintenance");
}
// $$author=wbarmettler$$valid=1$$time=2013-06-26 13:55$$checksum=82771ff4$$length=088$$
```

