# Activity Logging

## Why Log?

* Trace incomprehensible (parallel processing)
* Trace TL:DR
* Regulatory assistance: Happy QA = Happy Life

## Where to Log?

* **Directly to file** (usually on a Sub)
  * Parallel issues
  * Access issues
* **Status Window**
* An array, then File!
* Final product:
  * Text or Excel
  * Convert to “more” secure, .PDF
  * Force Print

## What to Log?

* **Method information**: Unique RunID, operator, project number
* **RunTime info**: Direct user selections and the result of the selections
* **Method events** (time stamps)
* **Device info**: Serial#’s, responses
* **Critical Volumes**: Hardcoded or calculated
* _**Anything needed to reconstruct the run**_

## How to collect and format Info?

* Most Libraries have **Get** commands – can pull data during runtime
* Time Library and Read Elapsed for timings
* Event Logging:
  * Build a Sub Method Template!
  * Customize event string formats and parameters based on what **YOU** need to know

![](<../.gitbook/assets/0 (1) (1).png>)

## Format Data?

* **HSLString Library** or **APPS** library has functions for wrangling text:
  * Trim Left/Right – keeps selected positions
  * Concatenate – joins multiple variables together (all types)
  * Convert (String ßà Numbers)
  * Find – looks for position of text in a string (wild cards)
  * Get Length – great for formatting lines
  * Fill left/right – adds spaces
* Apps or Math Library for rounding times or responses

![](<../.gitbook/assets/1 (1) (1).png>)

## CAUTION!

* Always make sure that variables logged are at the appropriate **time** and **place**.
* Like recording in a lab notebook, **carelessly logged events can lead to poor conclusions**! Be careful copying and pasting.
* Be mindful of **hard coded** results file entries – ensure that a static value hasn’t turned into a **variable during development**.

## ASW Status Dialog

![](<../.gitbook/assets/2 (1) (1).png>)

### Visual Library

* Opens a **separate** window that’s **selectively** written to (a single string variable)
* Easier for operator interpretation than the trace file
* Parallel friendly – if using variables to write to dialog, **use separate variables per thread**
* Use **string commands** to format text with multiple pieces of information

### Commands

* **Initialize -** Call to show the window and provide a title
* **AppendText –** Adds a text string to the dialog
* **SetStatusText – **_**Clears dialog**_ then displays the text string
* **Terminate –** closes the window
