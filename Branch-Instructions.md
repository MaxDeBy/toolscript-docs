[Back to overview](index.md)

---
# Branch Instructions
---
Branch instructions are the loops and conditionals of AACS. They look completely different to other instructions syntax-wise. They do not follow normal conventions outlined in other documentation. The unique syntax for branch instructions is defined in this article.

## If

The **If** instruction requires an expression which returns a boolean value. If the boolean value is `true`, then the instructions within the if statement will be executed. **Else If** and **Else** statements can also be defined in addition to the **If** statement in case the initial expression returns `false`, or a value that isn't a boolean.

Syntax:
```
1:  If [Expression]
2:  (
3:    [AACS HERE]
4:  );
5:  Else If [Expression]
6:  (
7:    [AACS HERE]
8:  );
9:  Else
10: (
11:   [AACS HERE]
12: );
```
>You can learn more about expressions in the documentation about [Variables](Variables.md). **Else** and **Else If** instructions are ignored if the previous instruction is not an **If** or an **Else If**.

## While

The While instruction takes an expression just like the **If** instruction. It will then continue to execute its containing instructions as long as the expression returns `true`. The loop ceases execution if the expression returns `false` or something that isn't a boolean.

Syntax:
```
1:  Loop While [Expression]
2:  (
3:    [AACS HERE]
4:  );
```

## For

The For instruction does not take an expression. It requires two parts instead.

Syntax:
```
1:  Loop For [VALUE]: #([COUNTER])
2:  (
3:    [AACS HERE]
4:  );
```
**[VALUE]** can be either a number or a variable which returns a number. If the value or a variable is not a number, the for loop will be skipped like a regular invalid instruction. Otherwise, the **For** instruction will loop as many times as the **[VALUE]** equals to.

**#([COUNTER])** is a variable which will store the current iteration n-1. This means that iteration's counter equals 0 during the first iteration, the second iteration equals 1, the third equals 2, and so on.

>All branch instructions support nesting, meaning that you can put other branches, or even containers, inside the brackets of a branch instruction.

---
[Back to overview](index.md)