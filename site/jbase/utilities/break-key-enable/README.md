# BREAK-KEY-ENABLE

**Created At:** 8/16/2018 2:47:42 PM  
**Updated At:** 10/24/2018 9:29:39 AM  
**Original Doc:** [break-key-enable](https://docs.jbase.com/46963-utilities/break-key-enable)  
**Original ID:** 334580  
**Internal:** No  

## Description

The jBASE **BREAK-KEY-ENABLE** command enables the break key when executing jBASE programs. The break key can be enabled on the current port or a port number specified as an argument.

It takes the general form:

```
BREAK-KEY-ENABLE {port number}
BREAK-KEY-ENABLE -?|-h
```

If **port number** is not specified then the break key is enabled on the current port number.

For example, if the break key has been disabled on port 6 then this command will re-enable it:

```
BREAK-KEY-ENABLE 6
```

Back to [Utilities](./../utilities)