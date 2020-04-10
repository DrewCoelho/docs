# WSETSTATUS

<PageHeader />

The WSETSTATUS subroutine allows you to modify the response code.

### **COMMAND SYNTAX**

```
CALL WSETSTATUS(CODE)
```

### **SYNTAX ELEMENTS**


| <!----> | <!----> |
| --- | --- |
| Parameter | Description |
| CODE | Set to the response code you wish to return.  Default is 200 (Success) |


EXAMPLE

```
CALL WSETSTATUS(405); * Method not allowed
```

NOTES

See [link](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes) for list of codes

  
<PageFooter />
