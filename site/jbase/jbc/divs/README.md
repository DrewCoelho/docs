# DIVS

<PageHeader />

## Description

The **DIVS** function is used to create a dynamic array containing the result of the element-by-element division of two dynamic arrays. It may take the general form:

```
 DIVS(array1, array2)
```

The division of each element of **array1** is by the corresponding element of **array2**, which returns the result in the corresponding element of a new dynamic array. If elements of **array1** have no corresponding elements in **array2**, it pads **array2** with ones and returns the **array1** elements. If an element of **array2** has no corresponding element in **array1**, it returns zero. If an element of **array2** is zero, it display a run-time error message and returns 0. If either element of a corresponding pair is null, it returns null.

An example of use is as:

```
dynArray1 = 10 : @VM : 15
dynArray2 = 2 : @VM : 5

CRT DIVS(dynArray1,dynArray2)
```

The output of this program is:  5ÿ3

Go back to [jBASE BASIC](./../README.md)

Go back to [Programmers' Reference Guide](./../../reference-guides/jbc/README.md)

<PageFooter />
