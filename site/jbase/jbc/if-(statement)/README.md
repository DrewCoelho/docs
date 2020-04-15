# IF (statement)

<PageHeader />

**Tags:**
<badge text='if/else' vertical='middle' />
<badge text='if/then/else' vertical='middle' />
<badge text='if/then' vertical='middle' />
<badge text='if not' vertical='middle' />
<badge text='if else then' vertical='middle' />
<badge text='if then else' vertical='middle' />
<badge text='if then' vertical='middle' />
<badge text='if else' vertical='middle' />
<badge text='program control' vertical='middle' />
<badge text='program execution ' vertical='middle' />

## Description

Allows for the conditional execution of some statements. It takes the general form:

```
IF expression THEN|ELSE statement
```

Where:

- The **expression** evaluates to a value of Boolean **TRUE** or **FALSE**.
- If the **expression** is **TRUE**, the statements defined by the **THEN** clause will execute (if present).
- If the **expression** is **FALSE**, the statements defined by the **ELSE** clause, if any will execute.
- The **THEN** and **ELSE** clauses may take two different forms being single and multiple line statements.

The simplest form of either clause is of the form:

```
IF varA THEN CRT varA
```

or

```
IF varA ELSE CRT varA
```

However, the **END** keyword may be used to expand the clauses to enclose multiple lines of code as so:

```
IF varA THEN
    varA = varA * 6
    CRT varA
END ELSE
    varA = 76
    CRT varA
END
```

It is possible to combine the single and multi-line versions of either clause to make complex combinations of the command. For reasons of readability it is suggested that where both clauses are present for an **IF** statement that the same form of each clause is coded.

IF statements can be nested within either clause to any number of levels.

An example of use is as:

```
CRT "Are you sure (Y/N) ":
INPUT Answer,1
IF OCONV (Answer, "MCU")= "Y" THEN
* Call delete subroutine here
    CRT "Files have been deleted"
END ELSE
    CRT "File delete was ignored"
END
```

Go back to [jBASE BASIC](./../README.md)

Go back to [Programmers' Reference Guide](./../../reference-guides/jbc/README.md)

<PageFooter />
