# JBASEUNIQUE

<PageHeader />

**Tags:**
<badge text='workfiles' vertical='middle' />
<badge text='environment variables' vertical='middle' />

## Description

When this environment variable is set to a directory, jBASE dynamically creates the workfiles based on port number and clears the contents of them when a new user connects to that port. The 'workfiles' are created as '$JBASEUNIQUE/jBASEWORK\_portno'. No dictionary is created (or needed).

This environment variable superceeds JBCBASETMP.

## Values

Any valid directory.

## Default

Not set.

## Setting

It must be set before any jBASE process is invoked.

## UNIX

```
export JBASEUNIQUE=/home/workfiles/
```

## Windows

```
set JBASEUNIQUE=C:\temp\workfiles\
```

Back to [Environment Variables](./../README.md)
