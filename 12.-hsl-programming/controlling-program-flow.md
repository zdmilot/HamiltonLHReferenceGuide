# Controlling Program Flow

## &#x20;Why Control the Flow of Execution?

Often, a program is required to do different things under different conditions. There are several kinds of conditions that can be tested. All conditional tests in HSL are Boolean, so the result of any test is either **true** or **false**. Boolean or numeric type values can be freely tested.&#x20;

HSL provides control structures for a range of possibilities. The simplest control structures are the conditional statements.&#x20;

&#x20;

## Using Conditional Statements&#x20;

HSL supports **if** and **if...else** conditional statements. **if** statements test a condition, and if the condition meets the test, some HSL code written by the programmer is executed. (In the **if...else** statement, different code is executed if the condition fails the test.) The simplest form of an **if** statement can be written entirely on one line, but multi-line **if** and **if...else** statements are much more common.

The following examples demonstrate the syntax which can be used with **if** and **if...else** statements. The first example shows the simplest kind of Boolean test. If (and only if) the item between the parentheses evaluates to **true**, the statement or block of statements after the **if** is executed.&#x20;

&#x20;

```clike
if (v2 != 0)
    v3 = v1 / v2;
else
    Trace("Division by zero !");
```



If only one of several conditions must be true (using || operators), testing stops as soon as any one condition passes the test. An example of the side effect of short-circuiting is that second() will not be executed in the following example if first() returns 0 or **false**.



```
if ((first() == 0) || (second() == 0))
    // some code
```



## Using Repetition, or Loops

There are several ways to execute a statement or block of statements repeatedly. In general, repetitive execution is called _looping_. It is typically controlled by a test of some variable, the value of which is changed each time the loop is executed. HSL supports many types of loops: **for** loops, **while** loops, and the **loop** statement.&#x20;

&#x20;

### Using **for** Loops

The **for** loop specifies a counter variable, a test condition, and an action that updates the counter. Just before each time the loop is executed (this is called one pass or one iteration of the loop), the condition is tested. After the loop is executed, the counter variable is updated before the next iteration begins.&#x20;

If the condition for looping is never met, the loop is never executed at all. If the test condition is always met, an infinite loop results. While the former may be desirable in certain cases, the latter rarely is.

```clike
// The update expression (currentPos = Ml_Star.SourceA++ in the following example)is executed at the end of the loop, after the
// block of statements that forms the body of the loop is executed, and before the condition is tested.
 
device Ml_Star("SystemLayout.lay", "ML_STAR", hslTrue);
variable vol, currentPos;
vol = 10;
 
Initialize();
TipPickUp();
 
for (currentPos = Ml_Star.SourceA.SetCurrentPosition(1);
 currentPos != 0;
 currentPos = Ml_Star.SourceA++)
{
 Aspirate();
 Dispense();
}
 
TipEject();
Ml_Star.StandardTips++;
```



### Using while Loops

The **while** loop is very similar to a **for** loop. The difference is that a **while** loop does not have a built-in counter variable or an update expression. If there are already a changing condition that is reflected in the value assigned to a variable, and if this condition shall be used to control repetitive execution of a statement or block of statements, use a **while** loop.

```clike
device Ml_Star("SystemLayout.lay", "ML_STAR", hslTrue);
variable vol, currentPos;
vol = 10;
 
Initialize();
TipPickUp();
currentPos = Ml_Star.SourceA.SetCurrentPosition(1);
while (currentPos != 0)
{
 Aspirate();
 Dispense();
 currentPos = Ml_Star.SourceA++
}
 
TipEject();
Ml_Star.StandardTips++;
```



### Using break Statements

HSL provides a statement to stop the execution of a loop. The break statement can be used to stop the execution if some (presumably special) condition is met.&#x20;

```clike
for (index = 0; index < length; index++)
    if (nullString.Compare(barcode.Mid(index, 1)) != 0) 
    break; 
```

