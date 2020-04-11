# DEL

**Created At:** 8/23/2017 1:23:31 PM  
**Updated At:** 10/24/2018 11:00:12 PM  
**Original Doc:** [268474-del](https://docs.jbase.com/36868-jbase-basic/268474-del)  
**Original ID:** 268474  
**Internal:** No  

**Tags:**
<badge text='delete from dynamic array' vertical='middle' />

## Description

The **DEL** statement is used to remove a specified element of a dynamic array.

```
DEL variable<expression1{, expression2{, expression3}}>
```

Where

- **variable** can be any previously assigned variable or matrix element. The expressions must evaluate to a numeric value or a runtime error will occur.
- **expression1** specifies the field in the array to operate upon and must be present.
- **expression2** specifies the multivalue within the field to operate upon and is an optional parameter.
- **expression3** is optionally present when **expression2** has been included. It specifies which subvalue to delete within the specified multivalue.

## Note

> - Truncates non-integer values for any of the expressions to integers.
> - Ignores invalid numeric values for the expressions without warning The command operates within the scope specified, i.e. if specifying only a field then it deletes the entire field (including its multivalues and subvalues). If specifying a subvalue, then it deletes only the subvalue leaving its parent multivalue and field intact.

An example of use is as follows:

```
Numbers=""
FOR I = 1 TO 20
    Numbers<I> = I        ;*generate numbers
NEXT I

FOR I = 19 TO 1 STEP 2
    DEL Numbers<I>        ;*remove odd numbers
NEXT I
```

Go back to [jBASE BASIC](./../README.md)

Go back to [Programmers' Reference Guide](./../../reference-guides/jbc/README.md)

  
<PageFooter />
