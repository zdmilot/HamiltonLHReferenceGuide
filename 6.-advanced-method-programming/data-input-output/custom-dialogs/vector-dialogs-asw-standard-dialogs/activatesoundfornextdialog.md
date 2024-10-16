# ActivateSoundForNextDialog

## Syntax

| <p> </p><p>ActivateSoundForNextDialog (</p> | <p> </p><p>variable i_strWaveFileFullName</p> | <p> </p><p> </p> |
| ------------------------------------------- | --------------------------------------------- | ---------------- |
|                                             | variable i\_blnSoundIsLooping) variable       |                  |

## Description

This function activates a sound for the next showing dialog. The playing sound can be stopped by clicking on the dialog header.

&#x20;

## Arguments & Return Values

| argument               | range                                                     | description                                                                  |
| ---------------------- | --------------------------------------------------------- | ---------------------------------------------------------------------------- |
| i\_strWaveFileFullName | string                                                    | Full name of the sound wave file.  The function supports only pcm wav files. |
| i\_blnSoundIsLooping   | <p>ASWGLOBAL::BOOL::TRUE</p><p>ASWGLOBAL::BOOL::FALSE</p> | Flag if the sound has to be repeat endless.                                  |
| return values          | <p>ASWGLOBAL::BOOL::TRUE</p><p>ASWGLOBAL::BOOL::FALSE</p> | <p>Call finished successful</p><p>Call finished unsuccessfull</p>            |
