[Back to overview](index.md)

---
# GenerateRandom (RNG)
---
### Description
Randomizes the value of a variable according to its type. Alternatively, creates a new variable if it doesn't exist.

### Parameters

|Name|Type|Description|Required|Default Value|
|:---:|:---:|:---:|:---:|:---:|
|Variable name|String|The name of the variable who's value should be randomized.|✓|-|
|Number 1|Number|The first number.|✓|0|
|Number 2|Number|The second number.|✗|20|

### Examples:
#### Example #1: Randomize a Number-type variable with a range from 20 - 30. If the variable doesn't exist, it'll be created.
```
1:  GenerateRandom:["MyVar"|20|30];
```

#### Example #2: Randomize a Number-type variable with a range from 0 - 280.
```
1:  Set #(MyVar) = 0;
2:  GenerateRandom:["MyVar"|280];
```

#### Example #2: Randomize a String-type variable with a length of 30 characters. If the variable doesn't exist, it'll be created.
```
1:  Set #(MyStringVar) = "Hello World";
2:  GenerateRandom:["MyStringVar"|30];
```

#### Example #3: Randomize a Boolean-type variable, giving it a 25% chance of being True.
```
1:  Set #(MyBooleanVar) = False;
2:  GenerateRandom:["MyBooleanVar"|25];
```

### Remarks:
Depending on the variable type, `Number 1` and `Number 2` have a different meaning as shown in this table:

|Type|Meaning|
|:---:|:---|
|String|`Number 2` is ignored. `Number 1` determines how many characters the randoms tring should have.|
|Number|`Number 1` is the inclusive lower bound and `Number 2` is the inclusive upper bound of the range. If `Number 1` is greater than `Number 2`, their position is switched automatically. Negative numbers will be multiplied by -1.|
|Boolean|`Number 2` is ignored. `Number 1` determines the chance in percent (100 = 100%) that the result is `true`.|
|Undefined|The instruction is ignored.|

This instruction can automatically create a variable, should it not exist. If only `Number 1` is provided, the resulting variable will be of type String. If `Number 2` was provided as well, the resulting variable will be of type Number.

> It is important that you ONLY use the variable name for `Variable name`.  
> I.e. not `#(VarName)`, only `VarName`. Otherwise, you will pass the current value of the variable you want (or undefined if the variable doesn't exist) as the value for the parameter.

---
[Back to overview](index.md)