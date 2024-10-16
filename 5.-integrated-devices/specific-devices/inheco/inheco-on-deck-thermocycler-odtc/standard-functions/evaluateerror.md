# EvaluateError

## Description

This function is used to translate a error number to an explanation string.

### Syntax

```
EvaluateError (variable i_intErrorCode, 
               variable & o_strErrorMessage)
```

### Arguments

| argument                  | value  | description                                   |
| ------------------------- | ------ | --------------------------------------------- |
| i\_intErrorCode \[in]     | int    | The error number returned by a function call. |
| o\_strErrorMessage \[out] | string | Explanation of the error.                     |
