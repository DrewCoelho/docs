# TIMESTAMP

**Created At:** 9/29/2017 2:12:53 PM  
**Updated At:** 1/5/2018 6:26:25 PM  
**Original Doc:** [278969-timestamp](https://docs.jbase.com/36868-jbase-basic/278969-timestamp)  
**Original ID:** 278969  
**Internal:** No  

## Description

This function returns a Universal Coordinated Time (UTC) timestamp value as decimal seconds i.e. Seconds with tenths and hundredths specified after the decimal point. It takes the general form:

```
TIMESTAMP()
```

The return value is a variable with as many decimal places as the current precision allows. However, successive calls may return the same value many times before the operating system updates the underlying timer. For example, Windows updates the low level timer every 1/50 second even though it stores the time in billionths of a second."

Go back to [jBASE BASIC](./../README.md)

Go back to [Programmers' Reference Guide](./../../reference-guides/jbc/README.md)
