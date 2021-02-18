# Variables
Variables, like all instructions, have a set syntax. They have the following format: #([VARNAME]).  
[VARNAME] can be any alphanumerical string (a-z, A-Z, 0-9).

Variables can have 4 different types: **String**, **Boolean**, **Number**,and **Undefined**. Keep in mind, variables are not strong typed. This means that the type can change at any time. The type is set implicit depending on the value it receives.

## Quick Overview:

* **String**
>A string is simple text. Encapsulating the value in quotes ("") will turn the variable into a string-type variable.  
A string has the second highest priority.


* **Number** 
>Numbers are integers when used in for loops, and floating point values at all other times. This means that numbers have the range of a double value with decimals allowed when not used in a for loop, and have the range of a 32-bit integer with decimals not allowed when in a for loop.  
A number has the third highest priority.

* **Boolean**
>A boolean has two values: True and False (not case sensitive). Booleans are used for the If and While branch instructions. An expression must always return a boolean when used in a branch instruction, or else the branch instruction will be ignored. Branches can be studied in their appropriate article.  
Booleans have the lowest (fourth highest) priority.

* **Undefined**
>If a variable has no value defined, its type will be undefined. This can happen in two ways: if you access a variable that was never defined, in which case it will be initialized with no value, or if you explicitly set the value to undefined by using the **Null** keyword.  
This type has the highest priority.

## Combining Variables 
As mentioned earlier, the different variable types have priorities. These priorities come into play when combining variables with different types. Combining includes the operations: addition, subtraction, multiplication, division, greater than, less than, equal, and not equal. Combinations marked with an X will always result in an empty value and an Undefined variable type. Some operations do not make mathematical sense or are even possible, and will result in an Undefined variable type. Others are mapped to special operations.

### Addition (+)

||String|Number|Boolean|Undefined|
|:-:|:-:|:-:|:-:|:-:|
|String|String|String|String|String|
|Number|String|Number|Number|X|
|Boolean|String|Number|Boolean|X|
|Undefined|String|X|X|X|

#### Effects
>>
String→String: Both strings will be put together.  
String→Number: The number will be considered as a string and both values are put together. The second's value will be appended to the first value.  
String→Boolean: The boolean will be considered as a string and both values are put together. The second's values will be appended to the first value  
String→Undefined: The string "null" will be put at the beginning or end of the string value.  
Number→Number: Both numbers will be added.  
Number→Boolean: The boolean will be turned into a number and added. True = 1, False = 0.  
Boolean→Boolean: Both booleans will perform an AND operation, returning true if both equal true, and false otherwise.

### Subtraction (-)

||String|Number|Boolean|Undefined|
|:-:|:-:|:-:|:-:|:-:|
|String|String|String|String|String|
|Number|String|Number|Number|X|
|Boolean|String|Number|Boolean|X|
|Undefined|String|X|X|X|

#### Effects
>>
String→String: Every occurence of the second value will be removed from the first value.  
String→Number: The number will be considered as a string and every occurence of the second value will be removed from the first value.  
String→Boolean: The boolean will be considered as a string and every occurence of the second value will be removed from the first value.  
String→Undefined: All occurences of the string "null" will be removed from the first value.  
Number→Number: Both numbers will be subtracted.  
Number→Boolean: The boolean will be turned into a number and subtracted from the number value. True = 1, False = 0.  
Boolean/Boolean: Both booleans will perform an OR operation, returning true if either value is true, and false otherwise.


### Multiplication (\*)

||String|Number|Boolean|Undefined|
|:-:|:-:|:-:|:-:|:-:|
|String|Boolean|Boolean|Boolean|Boolean|
|Number|Boolean|Number|X|X|
|Boolean|Boolean|X|Boolean|X|
|Undefined|Boolean|X|X|X|

#### Effects
>>
String→String: Returns true if the first value starts with the second value.  
String→Number: The number will be considered a string. Returns true if the first value starts with the second value.  
String→Boolean: The boolean will be considered as a string. Returns true if the first value starts with the second value.  
String→Undefined: The undefined value will be considered as the string "null". Returns true if the first value starts with the second value.  
Number→Number: The two numbers are multiplied together.  
Boolean→Boolean: Both booleans will perform an XOR operation, returning true only if the two values are not equal to each other.

### Division (/)

||String|Number|Boolean|Undefined|
|:-:|:-:|:-:|:-:|:-:|
|String|Boolean|Boolean|Boolean|Boolean|
|Number|Boolean|Number|X|X|
|Boolean|Boolean|X|X|X|
|Undefined|Boolean|X|X|X|

#### Effects
>>
String→String: Returns true if the first value ends with the second value.  
String→Number: The number will be considered a string. Returns true if the first value ends with the second value.  
String→Boolean: The boolean will be considered as a string. Returns true if the first value ends with the second value.  
String→Undefined: The undefined value will be considered as the string "null". Returns true if the first value ends with the second value.  
Number→Number: The two numbers are divided.

### Greater Than/Less Than (<|>)

||String|Number|Boolean|Undefined|
|:-:|:-:|:-:|:-:|:-:|
|String|Boolean|Boolean|Boolean|Boolean|
|Number|Boolean|Boolean|Boolean|X|
|Boolean|Boolean|Boolean|X|X|
|Undefined|Boolean|X|X|X|

#### Effects
>>
String→String: Compares the length of the two strings.  
String→Number: The number will be considered a string. Compares the length of the two strings.  
String→Boolean: The boolean will be considered as a string. Compares the length of the two strings.  
String→Undefined: The undefined value will be considered as the string "null". Compares the length of the two strings.  
Number→Number: Compares if the first value is greater or smaller than the second number.  
Boolean→Boolean: Checks if the first boolean is greater than 0.

### Equal/Not Equal (=|!=)

||String|Number|Boolean|Undefined|
|:-:|:-:|:-:|:-:|:-:|
|String|Boolean|Boolean|Boolean|Boolean|
|Number|Boolean|Boolean|Boolean|X|
|Boolean|Boolean|Boolean|Boolean|X|
|Undefined|Boolean|X|X|Boolean|

#### Effects
>>
String→String: Checks if the two strings are equal.  
String→Number: The number will be considered a string. Checks if the two strings are equal.  
String→Boolean: The boolean will be considered as a string. Checks if the two strings are equal.  
String→Undefined: The undefined value will be considered as the string "null". Checks if the two strings are equal.  
Number→Number: Checks if the two numbers are equal.  
Number→Boolean: The boolean will be considered a number. Checks to see if the two numbers are equal.  
Boolean→Boolean: Checks if the first boolean is greater than 0.  
Undefined→Undefined: Checks if an undefined value is equal to an undefined value.

## Expressions & Additional Information
It is important to know that strings will always consider the second value as a string as well. This means that the string "40" **DOES** equal the number 40, for example.  
But "80" is not greater than 40.

**Expressions:**  
The combinations mentioned above come into play when using expressions.  
An expression is nothing but a chain of variable commands. An expression is either a single value/variable or multiple variables  
with an operator between them. You can chain as many variables and operators together as need be.

A variable can be set with the following instruction
```
Set #([VARNAME]) = [EXPRESSION];
```
Where [EXPRESSION] can be something like
```
#(MyVar) + 4 * 3 / 2 - #(Var2)
```

Keep in mind that mathematics are very unlikely to be used in AACT and thus, the brackets ( and ) are not supported.

Like the branch instructions, this will be executed like a regular instruction, but it does not follow the regular syntax.  
Be mindful of typos while creating expressions, as this can result in undefined values being returned unexpectedly.