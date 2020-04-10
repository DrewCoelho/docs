# WGETPARAM

<PageHeader />

The WSETPARAM subroutine will retrieve additional URI parameters.

#### **COMMAND SYNTAX**

```
CALL WGETPARAM(VALUE,PARAM)
```

#### **SYNTAX ELEMENTS**


| <!----> | <!----> |
| --- | --- |
| VALUE | The value of the param you requested. |
| PARAM | The param number you want (first is 1) |


#### EXAMPLE

Requested URL

```
http://localhost:20002/api/employee/1234
```

```
CALL WGETPARAM(VALUE,1)
* Value should equal "1234"
```

#### NOTES

Typically on rest calls you send the Primary Key you want retrieved as the first parameter.  You would use this subroutine to retrieve that id.

  
<PageFooter />
