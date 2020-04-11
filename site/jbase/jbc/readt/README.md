# READT

**Created At:** 9/27/2017 2:49:33 PM  
**Updated At:** 11/27/2018 10:04:21 AM  
**Original Doc:** [278662-readt](https://docs.jbase.com/36868-jbase-basic/278662-readt)  
**Original ID:** 278662  
**Internal:** No  

**Tags:**
<badge text='tape devices' vertical='middle' />

## Description

The **READT** statement is used to read a range of tape devices 0-9. It takes the general form:

```
READT variable {FROM expression} THEN|ELSE statements
```

Where:

- **variable** is the variable that will receive any data read from the tape device.
- **expression** should evaluate to an integer value in the range 0-9 and specifies from which tape channel to read data. If the **FROM** clause is not specified the **READT** will assume channel 0.
- If the **READT** fails then the statements associated with any **ELSE** clause will be executed. [SYSTEM(0)](./../system-functions) will return the reason for the failure as follows:

| Code |  Description |
| --- | --- |
| 1 | There is no media attached to the channel |
| 2 | An end of file mark was found. |

## Note

> - A "tape" does not only refer to magnetic tape devices, but also any device that has been described to jBASE.
> - Writing device descriptors for jBASE is beyond the scope of this document.
> - If no tape device has been assigned to the specified channel the jBASE debugger is entered with an appropriate message.
> - Each instance of the **READT** statement will read the next record available on the device. The record size is not limited to a single tape block and the entire record will be returned whatever block size has been allocated by the T-ATT command.

An example of use is as:

```
LOOP
    READT TapeRec FROM 5 ELSE
    Reason = SYSTEM(0)
    IF Reason = 2 THEN BREAK ;* done
        CRT "Error" ; STOP
    END
REPEAT
```

Go back to [jBASE BASIC](./../README.md)

Go back to [Programmers' Reference Guide](./../../reference-guides/jbc/README.md)

  
<PageFooter />
