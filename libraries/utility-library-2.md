# Utility Library 2

The HSL utility library 2 is an extension library to the core HSL utility library.

The “Util2:”, “Util2: Debug” and “Util2: Error” Prefixes have all been removed for a better overview.

<table><thead><tr><th width="250">Command</th><th width="76">Icon</th><th>Action Performed</th></tr></thead><tbody><tr><td>CheckValueType</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Checks a variable to be of a given type.</td></tr><tr><td>CheckValueRange</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Checks a variable to be in a given (open) range.</td></tr><tr><td>CheckValueRangeMinMax</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Checks a variable to be in a given (closed) range.</td></tr><tr><td>CheckValueTypeAndRange</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Checks a variable to be of a given type and to be in a given (open) range.</td></tr><tr><td>CheckValueTypeAndRange MinMax</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Checks a variable to be of a given type and to be in a given (closed) range.</td></tr><tr><td>VarArrCheckIndex</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Generates a runtime error with detailed description if the index is invalid for the given variable array.</td></tr><tr><td>SeqArrCheckIndex</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Generates a runtime error with detailed description if the index is invalid for the given sequence array.</td></tr><tr><td>VarArrGetAt</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Returns a copy of the array element at the given index and raises a runtime error with a detailed description if the specified index is invalid for the given variable array.</td></tr><tr><td>SeqArrGetAt</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Returns a copy of the array element at the given index and raises a runtime error with a detailed description if the specified index is invalid for the given sequence array.</td></tr><tr><td>ToString</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Returns a string that represents the value of a given variable.</td></tr><tr><td>RoundVolume</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Rounds the given volume to one decimal place.</td></tr><tr><td>RoundVolumeUp</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Rounds the given volume up to one decimal place.</td></tr><tr><td>RoundVolumeDown</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Rounds the given volume down to one decimal place.</td></tr><tr><td>GetLabwarePosXYZ</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Obtains the position of the given labware item from the Deck Layout using deck coordinates.</td></tr><tr><td>RaiseRuntimeError</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Raises a runtime error.</td></tr><tr><td>RaiseRuntimeErrorInclPrevErrDe sc</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Raises a runtime error with an error description that includes the description of the previous error.</td></tr><tr><td>RaiseLast</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Re-throws the current runtime error.</td></tr><tr><td>MakeHxResult</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Returns an HxResult value given a major ID, a minor ID and an error code.</td></tr><tr><td>TraceSequence</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Traces the name, the indexes and all labware and position IDs of the given sequence.</td></tr><tr><td>TraceSequenceAndData_1</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Traces the given sequence and additional sequence data.</td></tr><tr><td>TraceSequenceAndData_2</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Traces the given sequence and additional sequence data.</td></tr><tr><td>TraceSequencesAndData_1</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Traces the given sequences and additional sequence data.</td></tr><tr><td>TraceSequencesAndData_2</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Traces the given sequences and additional sequence data.</td></tr><tr><td>TraceArray</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Traces the elements of the given array.</td></tr><tr><td>TraceArray_2</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Traces the elements of the given arrays.</td></tr><tr><td>TraceArray_3</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Traces the elements of the given arrays.</td></tr><tr><td>TraceArray_4</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Traces the elements of the given arrays.</td></tr><tr><td>SetTraceArraySettings</td><td><img src="../../.gitbook/assets/image (723).png" alt="" data-size="original"></td><td>Sets the current settings to trace multiple arrays.</td></tr></tbody></table>

\