# libutils

**Created At:** 8/30/2018 2:25:23 PM  
**Updated At:** 5/17/2019 9:49:58 PM  
**Original Doc:** [libutils](https://docs.jbase.com/48399-tools/libutils)  
**Original ID:** 336950  
**Internal:** No  

**Tags:**
<badge text='terminal independence' vertical='middle' />

The libutils shared library is provided to enable users to code terminal independent code to handle keyboard input. For example:

```
* Include key definitions
INCLUDE jCmdKeys.h
* Initialize command key strings
CALL CommandInit
TimeOut = 150 ;* Set timeout value deciseconds
ECHO OFF
LOOP
    * Get Next Command Value
    CALL CommandNext(RetNo, RetString, TimeOut)
    * RetNo should match numbers in include/header file
    BEGIN CASE
        CASE RetNo = cmd_cursor_up
           CRT "CURSOR UP"
        CASE RetNo = cmd_cursor_down
           CRT "CURSOR DOWN"
        CASE RetNo = cmd_cursor_left
           CRT "CURSOR LEFT"
        CASE RetNo = cmd_cursor_right
           CRT "CURSOR RIGHT"
        CASE RetNo = cmd_alpha_numeric
           CRT "ALPHANUMERIC"
        CASE RetNo = cmd_timeout
           CRT "TIMEOUT"
           BREAK
    END CASE
    * Output the actual string returned
    CRT "RetString :":OCONV(RetString,"MCP.")
REPEAT
```




