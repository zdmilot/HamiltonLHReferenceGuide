# Step Returns - Instrument Feedback

What are Step Returns?

Capturing Run Time Information

## **Returns**

* Is an **optional** output value for a function:
  * Submethod or Library
  * May or may not be present (optional, common for **device libraries**)
  * If present, may or may not use a variable to capture a value (again, optional!)
* Often gives **information** about a function/process:
  * Was it successful or a failure? (0/1, either way)
  * Was a specific error encountered? (non-binary output)
* **Step Returns** are return values for **instrument steps**
  * **Optional!**
  * Often have a consistent, **block format**
  * Can simultaneously report errors and successes, based on the instrument device (individual channels, labware positions, etc.)

## Where are Step Returns?

![](<../../.gitbook/assets/0 (31).png>)
