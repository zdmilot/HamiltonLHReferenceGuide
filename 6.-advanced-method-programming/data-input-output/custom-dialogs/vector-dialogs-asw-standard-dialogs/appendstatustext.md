# AppendStatusText

## Syntax

| AppendStatusText ( | variable i\_strTextToAppend ) variable |   |
| ------------------ | -------------------------------------- | - |

&#x20;

## Description

Appends the given text to the existing content in the status window dialog.\
\
Hints:\
If you turn in more than 100 lines will delete the next word in the oldest.\


## &#x20;Arguments & Return Values

| arguments              | range    | description                  |
| ---------------------- | -------- | ---------------------------- |
| i\_strTextToAppend     | string   | text which should be append. |
| return value           |          |                              |
| ASWGLOBAL::BOOL::TRUE  | boolean  | if successfully              |
| ASWGLOBAL::BOOL::FALSE | boolean  | in case an error occurred    |
