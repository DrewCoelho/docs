# GOSUB

<PageHeader />

**Tags:**
<badge text='program profiling' vertical='middle' />

## Description

Transfer execution of the script to a specified label, but as a subroutine call. Program execution will continue with the next line after 'gosub' after the subroutine completes execution, usually with a RETURN statement.

```
gosub label
```

where **label** is the label to which execution should transfer.

An example of use may be as:

```
gosub loadprog
if exitcode ne 0 then exit exitcode
# Any other code
exit 0
#
loadprog: progname = "TESTER " : $VARNAME : " " : portno
portno = portno + 1
program loadprog
exitcode = $?
Return
```

[Back to jKeyAuto](./../README.md)

<PageFooter />
