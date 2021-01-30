# SP-LOOK

<PageHeader />

## Description

The command displays current spooler assignments. It takes the general form:

```
SP-LOOK
```

The output may be as:

```
SPOOLER ASSIGNMENTS            PAGE   1

PORT     REPORT#    QUEUE NAME              JOB#  OPTIONS  COPIES

1        DEFAULT    SCREEN                     0            1
```

where :

- PORT is the current port that issued the [SP-ASSIGN](./../sp-assign)
- REPORT# is the print report channel numbers:
  - DEFAULT - Print report channel zero, the default assignment
  - 1-127 - Print report channels assigned by the [SP-ASSIGN](./../sp-assign) command
- QUEUE NAME is the formqueue name assigned by [SP-ASSIGN](./../sp-assign) command
- JOB# is the currently open print job numbers
- OPTIONS are any options assigned by the [SP-ASSIGN](./../sp-assign) command
- COPIES is the number of copies specified via the [SP-ASSIGN](./../sp-assign) command

Back to [Spooler.](./../jbase-spooler)

<PageFooter />
