# UNIQUEKEY

<PageHeader />

## Description

The function returns a unique 16-byte character key, that it generates at each call to the function.  It takes the general form:

```
UNIQUEKEY()
```

The key contains characters from the set A-Z a-z 0-9 ^ and \_.

Based on the current UTC time and the process number, the key is unique on a single computer system providing that the system clock is not turned back.

If the system administrator adjusts the system clock backwards, then there is a slight possibility of generating duplicate keys during the period until the clock has caught back up to time that the adjustment was made.

Any process that continues to execute throughout this period will continue to produce unique keys.

A process that starts up during this period and is given the process ID of a process that terminated during the period, may possibly generate a duplicate key until the period ends.

## Note

 > Change **5\_20431** changed the '+' and '/' to '^' and '\_' respectively.

Go back to [jBASE BASIC](./../README.md)

Go back to [Programmers' Reference Guide](./../../reference-guides/jbc/README.md)

  
<PageFooter />
