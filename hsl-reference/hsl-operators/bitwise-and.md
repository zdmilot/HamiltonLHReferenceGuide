# Bitwise AND

## Description

Performs a bit-wise AND on two expressions.

## Syntax

result = expression1 & expression2

The & operator syntax has these parts:

| Part        | Description                 |
| ----------- | --------------------------- |
| result      | An object of type variable. |
| expression1 | Any numeric expression.     |
| expression2 | Any numeric expression.     |

## Remarks

The & operator looks at the binary representation of the values of two expressions and does a bit-wise AND operation on them. The result of this operation behaves as follows:

0101 (expression1)

1100 (expression2)

\----

0100 (result)

Any time both of the expressions have a 1 in a digit, the result has a 1 in that digit. Otherwise, the result has a 0 in that digit.

If either of the expressions does not evaluate to a number, a run-time error is generated by the & operator.

&#x20;