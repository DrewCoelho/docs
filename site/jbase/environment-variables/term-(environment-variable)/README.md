# TERM (Environment Variable)

**Created At:** 11/3/2017 3:14:45 PM  
**Updated At:** 12/28/2018 8:51:42 AM  
**Original Doc:** [term-environment-variable](https://docs.jbase.com/41717-environment-variables/term-environment-variable)  
**Original ID:** 284152  
**Internal:** No  

**Tags:**
<badge text='terminal' vertical='middle' />
<badge text='environment variables' vertical='middle' />

## Description

On UNIX, this variable should be set to your terminal type as defined by the UNIX terminfo database. On Windows, it should be set to a value in any of the directories under %JBCRELEASEDIR%\misc\.

## Values

On UNIX, any valid terminfo database entry.

On Windows, any file name (up to the underscore) in the directories under **%JBCRELEASEDIR%\misc\**. Additional terminal definitions can be created using the [**jtic**](./../../jbase/tools/jtic)command.

## Default

On UNIX, the default depends upon your system and how it has been set up.

## Setting

It can be set at any time by the commands:

## UNIX

```
export TERM=vt220
```

## Windows

```
set TERM=vt220
```

Go Back to [Environment Variables](./../README.md)
