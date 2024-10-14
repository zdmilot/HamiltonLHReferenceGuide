# Barcode Mask

The barcode mask applies to all instances of this labware and defines the required format of an expected barcode. It may contain the following control characters and jokers:

&#x20;

## Control characters

%         The Wild Card character is a place holder for zero to n arbitrary characters. It can be used only once in a barcode mask!

\               The Escape Character allows the use of control characters and jokers as regular characters. For example \\# means the # character and not the kit lot joker. An Escape Character cannot be the last character of a barcode mask!

$          The "No barcode allowed" character means that no barcode is allowed at this position. If this control character is used in a barcode mask, it must be the first and only character of the mask.

&#x20;

## Jokers

While reading a barcode, each barcode character that corresponds to a joker in the barcode mask is interpreted as valid.

Any special interpretation, for example the kit lot handling, has to be part of the method; there is no interpretation during barcode reading!

&#x20;

## Predefined jokers are:

\*           Place holder for exactly one arbitrary character.

\#          Place holder for exactly one kit lot character.

?          Reserved place holder for exactly one arbitrary character.

&#x20;

(Use the HSL library named HSLKitLotLib to interpret and handle kit lots in a method or enable the kit lot check in the steps which offer this feature).

&#x20;

## Barcode Mask Examples

| Barcode mask | Valid barcode                                | Comment                                                                                                                                                                                                                                                                                                                                                                           |
| ------------ | -------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| $            | \<empty>                                     | Only an empty barcode is allowed.                                                                                                                                                                                                                                                                                                                                                 |
| %            | \<any>                                       | Any barcode allowed including an empty barcode.                                                                                                                                                                                                                                                                                                                                   |
| A%           | <p>A</p><p>A12B34</p><p>AlueSR2</p>          | Any barcode beginning with A is allowed.                                                                                                                                                                                                                                                                                                                                          |
| BC%HIV       | <p>BCHIV</p><p>BC HIV</p><p>BC24juREXHIV</p> | Any barcode beginning with BC and ending with HIV is allowed.                                                                                                                                                                                                                                                                                                                     |
| BC\\#HIV#### | <p>BC#HIV0001</p><p>BC#HIV342A</p>           | <p>Any barcode beginning with BC#HIV followed by exactly four arbitrary characters is allowed. The barcode characters that match the kit lot jokers (#) in the barcode mask are interpreted as kit lot characters (0001, 342A). Note: The first # is interpreted together with its leading Escape Character (\) as the normal # character and not as kit lot joker.</p><p> </p>   |
| BCHIV\*\*\*X | <p>BCHIVabcX</p><p>BCHIV12sX</p>             | Any barcode beginning with BCHIV followed by exactly three arbitrary characters and an X is allowed.                                                                                                                                                                                                                                                                              |
| BCHIV00133   | BCHIV00133                                   | Only this barcode is allowed.                                                                                                                                                                                                                                                                                                                                                     |
| BC\\$\\\HIV  | BC$\HIV                                      | <p>Only this barcode is allowed. Note: \$ in the barcode mask requires the $ character in the barcode (an Escape Character followed by the "no barcode allowed" control character is the regular $ character). \\ in the barcode mask requires the \ character in the barcode (an Escape Character followed by a second Escape Character is the regular \ character).</p><p> </p> |
| BC%HIV%X     |                                              | Invalid barcode mask because of two Wild Card characters.                                                                                                                                                                                                                                                                                                                         |
| BCHIV\\      |                                              | Invalid barcode mask because the Escape Character must not be the last character of a barcode mask.                                                                                                                                                                                                                                                                               |
| BC$HIV       |                                              | Invalid barcode mask because the "no barcode allowed" control character must be the first and only character of a barcode mask.                                                                                                                                                                                                                                                   |
