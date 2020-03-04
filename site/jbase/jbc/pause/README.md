# PAUSE

**Created At:** 9/22/2017 12:04:38 PM  
**Updated At:** 11/27/2018 9:42:29 AM  
**Original Doc:** [277627-pause](https://docs.jbase.com/36868-jbase-basic/277627-pause)  
**Original ID:** 277627  
**Internal:** No  

**Tags:**
<badge text='program execution' vertical='middle' />

## Description

The **PAUSE** statement allows processing to be suspended until an external event triggered by a [WAKE](./../wake) statement from another process or a timeout occurs. This takes the general form:

```
PAUSE {expression}
```

Where **expression** may evaluate to a timeout value, which is the maximum number of seconds to suspend the process. If expression is omitted then the **PAUSE** statement will cause the process to suspend until woken by the [WAKE](./../wake) statement.

If a timeout value is specified and the suspended process is not woken by a [WAKE](./../wake) statement then the process will continue once the timeout period has expired.

If executing a [WAKE](./../wake) statement for the process before the process executes the **PAUSE** statement then the **PAUSE** will be ignored and processing will continue until a subsequent **PAUSE** statement.

Go back to [jBASE BASIC](./../README.md)
