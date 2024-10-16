# GetMessages Method

Returns and clears all messages in the message queue.

## Syntax

```
function GetMessages(
	variable& messages
) variable
```

## **Parameters**

| Name     | Type                                                                 | Description                                        |
| -------- | -------------------------------------------------------------------- | -------------------------------------------------- |
| messages | [System.String](https://docs.microsoft.com/dotnet/api/system.string) | Composite string of all messages separated by '\|' |

## **Return Value**

[Int32](https://docs.microsoft.com/dotnet/api/system.int32)\
Zero on success
