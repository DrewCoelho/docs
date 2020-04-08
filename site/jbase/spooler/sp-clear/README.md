# SP-CLEAR

<PageHeader />

## Description

This command clears a formqueue of queued print jobs. It takes the general form:

```
SP-CLEAR formqueue
```

where **formqueue** is the formqueue to be cleared.

All print jobs queued to the specified formqueue will be deleted. Any print job currently despooling from the specified formqueue will be killed and then deleted.

If used without the argument, the user will be prompted as:

```
FORM-QUEUE:
```

The user will then specify which formqueue is to be cleared.

> ### Note
>
> Root or the user that generated the print job can only clear print jobs assigned with the P option. Any user can clear print jobs assigned with the U option. Print jobs, which have an OPEN or EDIT status cannot be cleared.

Back to [Spooler](./../jbase-spooler).
