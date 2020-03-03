# LD_LIBRARY_PATH

**Created At:** 11/3/2017 3:08:37 PM  
**Updated At:** 8/8/2018 7:54:20 AM  
**Original Doc:** [ld_library_path](https://docs.jbase.com/41717-environment-variables/ld_library_path)  
**Original ID:** 284148  
**Internal:** No  

**Tags:**
<badge text='environment variables' vertical='middle' />

## Description

This variable is only valid on Linux and Solaris and must be set to the jBASE lib directory ($JBCRELEASEDIR/lib).



## Values

Colon separated library file paths.



## Default

None.



## Setting

Normal environment variable, so it can be set at any time by the commands:

```
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$JBCRELEASEDIR/lib
```
