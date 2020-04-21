# JEDIFILEPATH

<PageHeader />

**Tags:**
<badge text='jdirectories' vertical='middle' />
<badge text='environment variables' vertical='middle' />

## Description

This environment variable provides a list of directories in which to search for jBASE data files. If a MD or VOC file is configured, i.e.  [**JEDIFILENAME\_MD**](./../jedifilename_md), and contains  Q-pointers or F-pointers these take precedence over the directories in [**JEDIFILEPATH**](./.)**.**

## Values

Colon separated file paths (UNIX)  
Semicolon separated file paths (Windows)

## Default

The current directory

## Setting

As per normal environment variable, so it can be set at any time. The use of relative file paths (such as '.') should be avoided as it can result in unintended file access

## UNIX

```
export JEDIFILEPATH=/appvol/WB1:/appvol/WB2:/appvol/WB3
```

## Windows

```
set JEDIFILEPATH=C:\apps\WB1;C:\apps\WB2;C:\apps\WB3
```

Go Back to [Environment Variables](./../README.md)

<PageFooter />
