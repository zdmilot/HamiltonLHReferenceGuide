# CheckSpinError Method

Use this method after the Spin() method returns when the return value cannot be checked directly.![](blob:https://app.gitbook.com/e4ea7d1e-82e0-46d3-8400-39c27bf37395)

## Syntax

```
function CheckSpinError(
	variable& spinMessages
) variable
```

## **Parameters**

| Name         | Type                                                                 | Description                                             |
| ------------ | -------------------------------------------------------------------- | ------------------------------------------------------- |
| spinMessages | [System.String](https://docs.microsoft.com/dotnet/api/system.string) | Composite string of all spin messages separated by '\|' |

## **Return Value**

[Int32](https://docs.microsoft.com/dotnet/api/system.int32)\
Zero when no spin errors
