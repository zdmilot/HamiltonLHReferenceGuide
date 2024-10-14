# HSL Operators

HSL has a full range of operators, including arithmetic, logical, bit-wise, and assignment operators.

&#x20;

| **Symbol**      | **Operator**                                                                          | **Associativity**             |
| --------------- | ------------------------------------------------------------------------------------- | ----------------------------- |
| \|\| && \| &    | logical OR logical AND bitwise OR bitwise AND                                         | left left left left           |
| < <= == != >= > | less than less than or equal to equal not equal greater than or equal to greater than | left left left left left left |
| %               | remainder                                                                             | left                          |
| + -             | add subtract                                                                          | left left                     |
| \* /            | multiply divide                                                                       | left left                     |
| !               | not                                                                                   | right                         |
| ^               | power                                                                                 | right                         |
| -               | unary minus operator                                                                  | right                         |
| ++ --           | increment decrement                                                                   | left left                     |
| =               | assignment                                                                            | right                         |

&#x20;

#### Operator Precedence

Operators in HSL are evaluated in a particular order. This order is known as the operator precedence. Each box in the preceding table contains operators of the same priority, whereby an operator has always lower priority than the operators in the following section.

Parentheses are used to alter the order of evaluation. The expression within parentheses is fully evaluated before its value is used in the remainder of the statement.

An operator with higher precedence is evaluated before one with lower precedence. For example:

```clike
z = 78 * (96 + 3 + 45)
```

This expression contains five operators: =, \*, (), +, and +. According to precedence, they are evaluated in the following order: (), \*, +, +, =.

Evaluation of the expression within the parentheses is first: There are two addition operators, and they have the same precedence: 96 and 3 are added together and 45 is added to that total, resulting in a value of 144.

Multiplication is next: 78 and 144 are multiplied, resulting in a value of 11232.

Assignment is last: 11232 is assigned into z.
