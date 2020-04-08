# SP-RESUME

<PageHeader />

## Description

This command resumes despooling from a formqueue. It takes the general form:

```
SP-RESUME formqueue
```

where **formqueue** is the formqueue from which to resume despooling.

If used without arguments, as:

```
SP-RESUME
```

the user will be prompted as:

```
FORM-QUEUE:
```

The user will then enter the formqueue to resume printing.

> ### Note
>
> Despooling will be resumed from the point at which the formqueue was either [SUSPENDED](./../sp-suspend) or [STOPPED](./../sp-stop).

Back to [Spooler.](./../jbase-spooler)
