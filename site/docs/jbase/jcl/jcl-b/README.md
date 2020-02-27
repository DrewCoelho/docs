# jCL B

**Created At:** 5/28/2018 10:19:31 AM  
**Updated At:** 6/1/2018 5:38:12 PM  
**Original Doc:** [318616-jcl-b](https://docs.jbase.com/45792-jcl/318616-jcl-b)  
**Original ID:** 318616  
**Internal:** No  

**Tags:**
<badge text='jcl' vertical='middle' />

## Description

The command moves the active input buffer pointer back to the previous parameter. It takes the general form:

```
B
```

## Note

> The input buffer pointer is moved backwards to the preceding field mark or to the beginning of the input buffer. If the pointer is on the first character of a parameter (or a field marker), the pointer will be moved back to the field mark of the previous parameter.

### Example 1

```
| Command |  PIB Before   |   PIB After   |
| ------- |  ----------   |   ---------   |
| B       | ABC^DEF^GHIJK | ABC^DEF^GHIJK |
|         |            ^  |        ^      |
```

### Example 2

```
| Command |  PIB Before   |    PIB After  |
| ------- |  ----------   |    ---------  |
| B       | ABC^DEF^GHIJK | ABC^DEF^GHIJK |
|         |         ^     |    ^          |
```

Back to [jCL.](./../README.md)
