# JEDIFILENAME_SYSTEM

<PageHeader />

## Description

If you are using Q-pointers in a defined MD/VOC file then you may well need to create a SYSTEM file to define the home directories of other accounts. By default Q-pointers are resolved by using the **$JBCRELEASEDIR/src/SYSTEM** file. This can be changed by setting the JEDIFILENAME\_SYSTEM variable to an alternative hash file or directory.

While it is not required, it is strongly advised that this value be set to the **complete** path of the system file and not a relative path (as an example, **/home/islandjim/SYSTEM]D** should be used instead of **./SYSTEM]D**).

## Values

Valid file path.

## Default

None.

## Setting

As per normal environment variable, so it can be set at any time by the commands:

### UNIX

```
export JEDIFILENAME_SYSTEM=/home/globals/SYSTEM]D
```

### Windows

```
SET JEDIFILENAME_SYSTEM=D:\home\globals\SYSTEM]D
```

Go Back to [Environment Variables](./../README.md)

<PageFooter />
