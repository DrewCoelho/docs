# JBCSCREEN_WIDTH

**Created At:** 7/17/2018 12:58:29 PM  
**Updated At:** 8/22/2018 9:23:56 AM  
**Original Doc:** [327509-jbcscreen_width](https://docs.jbase.com/41717-environment-variables/327509-jbcscreen_width)  
**Original ID:** 327509  
**Internal:** No  

**Tags:**
<badge text='terminal' vertical='middle' />
<badge text='environment variables' vertical='middle' />

## Description

This environment variable specifies the page width for paged terminal output, and overrides the value specified by the [TERM](term) type.

Valid only on jBASE 3.x.



## Values

Decimal number



## Default

None.



## Setting

It should be setup before the jSHELL is invoked.

**UNIX**

```
export JBCSCREEN_WIDTH=132
```

**Windows**

```
set JBCSCREEN_WIDTH=132
```
