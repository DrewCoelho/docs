# JBCNETDIR

**Created At:** 7/17/2018 1:36:43 PM  
**Updated At:** 6/6/2019 3:14:38 PM  
**Original Doc:** [jbcnetdir](https://docs.jbase.com/41717-environment-variables/jbcnetdir)  
**Original ID:** 327518  
**Internal:** No  

**Tags:**
<badge text='jnetdir' vertical='middle' />
<badge text='network directory' vertical='middle' />
<badge text='jbcnetdir' vertical='middle' />
<badge text='jrfs' vertical='middle' />
<badge text='environment variables' vertical='middle' />

## Description

This environment variable defines the location of the jRFS configuration files. If this environment variable is not set then the configuration files in **$JBCRELEASEDIR/config** (**%JBCRELEASEDIR%\config** on Windows) are used.

## Values

Valid file path.

## Default

```
$JBCRELEASEDIR/config (UNIX)
%JBCRELEASEDIR%\config (Windows)
```

## Setting

As per normal environment variable.

## UNIX

```
export JBCNETDIR=/home/globals/jrfs
```

## Windows

```
set JBCNETDIR=C:\home\globals\jrfs
```

Go Back to [Environment Variables](./../README.md)
