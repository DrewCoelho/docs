# JQLEXECUTE

<PageHeader />  

**Tags:**
<badge text='record handling' vertical='middle' />
<badge text='query language' vertical='middle' />

## Description

**JQLEXECUTE** starts executing a compiled jQL statement. It takes the general form:

```
JQLEXECUTE(Statement, SelectVar)
```

Where:

- **Statement** is the valid result of a call to a [JQLCOMPILE](./../jqlcompile)
- **SelectVar** is a valid select list used to limit the statement to a predefined set of items. For example:

```
SELECT PROGRAMMERS WITH IQ_IN_PTS > 250
LIST PROGRAMMERS NAME
```

This function returns -1 in the event of a problem, such as an incorrect statement variable. It will cause the **statement** to run against the database and produce a result set for use with [JQLFETCH](./../jqlfetch).

For a practical example of use, see the **jexport.b** program in the **$JBCRELELEASEDIR**/samples/JQLBASIC directory.

Go back to [jBASE BASIC](./../README.md)

Go back to [Programmers' Reference Guide](./../../reference-guides/jbc/README.md)

<PageFooter />
