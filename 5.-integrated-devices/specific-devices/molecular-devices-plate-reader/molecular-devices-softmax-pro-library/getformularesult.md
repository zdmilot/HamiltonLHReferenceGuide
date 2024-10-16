# GetFormulaResult

## Description

This function returns the result from the specified formula.

Note This command requires the name of the formula, name of either Notes or Group section, and the name of the Experiment. If the name of the Experiment is not specified, it will search from the first Experiment of the document.

Note The returned value is the calculated value for the formula, not the formula string.

### Syntax

```
GetFormulaResult(i_strFormulaName,
                 o_strResult)
```

### Arguments

\[in] i\_strFormulaNameFully qualified formula name, including section and experiment identifiers. Example: formulaName@sectionName@experimentName\[out] o\_strResultthe calculated value for the formula, as string.
