# Firmware Commands

## Firmware Command Disclaimer

<table data-header-hidden><thead><tr><th width="69"></th><th width="616"></th><th></th></tr></thead><tbody><tr><td><img src="../.gitbook/assets/image (259).png" alt="" data-size="line"></td><td>I UNDERSTAND THAT ACCESSING FIRMWARE COMMANDS IS NOT COVERED UNDER ANY WARRANTY AND CAN SEVERELY DAMAGE THE DEVICE.<br><br>ANY DAMAGE DONE IS OF MY OWN DOING AND I WILL BE HELD RESPONSIBLE FOR ANY DAMAGE DONE UTILIZING THESE COMMANDS.</td><td><img src="../.gitbook/assets/image (260).png" alt="" data-size="line"></td></tr></tbody></table>

\##Firmware Commands Vector allows you to use firmware commands to run the STAR at a low level.

Why would you do this?

* If the current command set doesn’t offer a particular function.
* If you need to change a particular parameter.
* If you need to retrieve information from the STAR.\\

## Firmware Command Dialog Box

Bring in the Firmware Command using the Configuration Editor. The Firmware command dialog box looks like this:

<img src="../.gitbook/assets/image (198).png" alt="" data-size="original">

## Formats

Commands and Parameters must be in quotations. Commands are all capitals; Parameters, lower-case:\\

<img src="../.gitbook/assets/image (199).png" alt="" data-size="original">

## Warnings

**Firmware commands should only be used by programmers having a very good knowledge of the firmware commands and their parameters.**

**The firmware command has no internal error handling implemented, i.e. this step always returns “OK.”**

**It is the programmer’s responsibility to interpret and check the return strings (in the trace) for errors.**

**Damage done to the robot as a result of sending firmware commands not provided by a Hamilton representative for a specific purpose may not be covered under warranty.**

## Firmware Reference Guides

Firmware Reference Guides are documents that describe the commands, parameters, and error codes.

<img src="../.gitbook/assets/image (203).png" alt="" data-size="original">

## Module Names

Firmware modules (please note that those are zeros!):

* C0 – Master
* H0 – 96 head
* I0 – Autoload
* PX – Pipettes
* R0 – iSWAP
* X0 – X-drive
* WX – Wash station

## Command Availability

Not all firmware commands and parameters will work with all versions of software and hardware.

If a firmware command does not seem to work, it could be:

* Hardware is not compatible.
* Software is not compatible.
* Firmware command is subsequently overwritten by another method command and therefore not implemented during run time.
* Command or parameter were incorrectly entered into the command dialog box

## Troubleshooting

To troubleshoot a firmware command, use bind return values and use a User Output to view the returned value.

If you get er00, the command was successful.

If you get a different output, then refer to the Error Messages section of the applicable firmware reference guide.
