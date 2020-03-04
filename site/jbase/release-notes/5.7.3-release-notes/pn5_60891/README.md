# PN5_60891

**Created At:** 6/27/2019 1:28:52 PM  
**Updated At:** 6/29/2019 8:04:10 AM  
**Original Doc:** [pn5_60891](https://docs.jbase.com/61286-5-7-3-release-notes/pn5_60891)  
**Original ID:** 400141  
**Internal:** No  


### Description

Add **-D**option to the **BASIC**command to compile programs with a compiler directive



### Previous Release Behavior

The **jcompile -D**option was not recognized by the **BASIC**command.



### Current Release Behavior

The **-D** option can now be used with the **BASIC**command giving the same functionality as with the **jcompile**command.

For example, given the following program:

```
PROGRAM test_compiler_directive
#ifdef DEBUG_BUILD
    CRT 'This is a debug build'
#endif
```

If the program is compiled as:

```
BASIC bp test_compiler_directive.b
CATALOG bp test_compiler_directive
```

there would be no output.

Compiling this with the **-D** option:

```
BASIC -DDEBUG_BUILD test_compiler_directive.b
CATALOG bp test_compiler_directive
```

the output would be **This is a debug build**.
