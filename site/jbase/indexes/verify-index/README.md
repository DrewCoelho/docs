# VERIFY-INDEX

<PageHeader />

**Tags:**
<badge text='file indexing' vertical='middle' />

## Description

This command will verify the integrity of an index definition, in so far as it looks for internal corruption. It doesn't actually verify that the index data actually correctly cross references the data file records.

It is called as:

```
verify-index -Options filename { {indexname {indexname ...}} | *}
```

where options may be:

| Option | Description |
| --- | --- |
| -a | Verifies ALL indexes in the file |
| -l | Display Leaf information |
| -o | Display Overflow frame information |
| -r | Display Record information |
| -v | Verbose mode |

- Option **-a** means all indexes will be verified and this can also be achieved by using **\*** on the command line for the index name. Without the -a option (or **\*** as index name) you must specify on the command line one or more indexes to verify.
- Option **-l** means information about each leaf of the index is displayed.
- Option **-o** causes the overflow table information to be displayed.
- Option **-r** causes all the record information to be displayed. This is the index key followed by all the record keys that share the same index value.
- Option **-v** is the verbose mode and causes extra information to be displayed.

## Note

> While this command is active a lock on an entire index is taken. Should an application try to update that index then the application will wait until the lock is released, which isn't until the verify-index command has completed for that particular index. This means scenarios such as the one below should be used only with caution as the piping of the output into "more" means the lock will be retained until the display has completed.
>
> ``` bash
> % verify-index -avrl FILENAME | more
> ```

Back to [Indexes](./../README.md)

  
<PageFooter />
