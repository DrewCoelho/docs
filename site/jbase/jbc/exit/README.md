# EXIT

<PageHeader />

**Tags:**
<badge text='program control' vertical='middle' />
<badge text='program execution' vertical='middle' />

## Description

The **EXIT** statement halts the execution of a program and returns a numeric exit code to the parent process.

It takes the general form:

```
EXIT(expression)
```

or

```
EXIT
```

where **expression** must evaluate to a numeric result, which should be the appropriate error code for the environment in which jBASE is being run. The error code is returned to the parent C function exit().

## Note

> - For compatibility with older versions of the language, the **EXIT** statement should be used without an expression. In this case, it is synonymous with the [BREAK](./../break) statement.
> - If the expression does not evaluate to a numeric result the program will enter the debugger and display a suitable error message.
> - The expression has been forced to be parenthesized to avoid confusion with the **EXIT** statement without an expression as much as is possible.

Assuming a file has been opened to FileDesc, an example of use is as follows:

```
    READ Record FROM FileDesc, RecordKey
    ELSE CRT "Record ":RecordKey:" is missing"
        EXIT(1)
    END
```

See also: [BREAK](./../break).

Go back to [jBASE BASIC](./../README.md)

Go back to [Programmers' Reference Guide](./../../reference-guides/jbc/README.md)

<PageFooter />
