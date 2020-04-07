# PH-RESUME

<PageHeader />

**Tags:**
<badge text='backgroud processes' vertical='middle' />

## Description

The jBASE **PH-RESUME** command resumes a suspended jBASE background task process. The command takes the general form:

```
PH-RESUME n
```

where **n** is the number of the port number associated with the jBASE background task process to be resumed.

## Error Messages

If no port number is specified:

```
[316] WHICH LINE?
```

If a port number that is not currently logged on is specified:

```
PROCESS NOT LOGGED ON
```

If an attempt is made to resume a jBASE background task process running as a different user name, user is not logged on as root:

```
[82] YOUR SYSTEM PRIVILEGE LEVEL IS NOT SUFFICIENT FOR THIS STATEMENT.
```

## Note

> The user must have root privileges if the jBASE background task process is running as a different user name.

### Example

```
PH-RESUME 100
```

Resumes the jBASE background task process running on port 100.

Back to [Background Processing](./../README.md)
