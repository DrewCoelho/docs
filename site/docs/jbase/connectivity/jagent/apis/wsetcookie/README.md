# WSETCOOKIE

**Created At:** 6/27/2017 8:23:53 PM  
**Updated At:** 11/21/2017 4:26:37 AM  
**Original Doc:** [wsetcookie](https://docs.jbase.com/34473-docs/wsetcookie)  
**Original ID:** 261451  
**Internal:** No  


The WSETCOOKIE subroutine will set a cookie to be sent back to the browser.

#### **COMMAND SYNTAX**

```
CALL WSETCOOKIE(NAME,VALUE,EXP.DATE,EXP.TIME,PATH,DOMAIN,SECURE)
```

#### **SYNTAX ELEMENTS**


| <!----> | <!----> |
| --- | --- |
| NAME | Name of the cookie you want to set |
| VALUE | Value you wish to set the cookie to |
| EXPDATE | Date you wish the cookie to expire on.  Use pick internal dates. |
| EXPTIME | Time you wish the cookie to expire (used with EXPDATE).  Use pick internal times. |
| PATH | Path you wish the cookie to apply to.  Use "/" for all. |
| DOMAIN | Domain you wish the cookie to apply to.  Use "." for domain called from. |
| SECURE | If set to "Y" then this cookie will only save on HTTPS requests. |


#### EXAMPLE

```
CALL WSETCOOKIE("mycookie","value",DATE(),TIME+300,"/",".","Y")
```

#### NOTES

The WSETCOOKIE command basically builds a Set-Cookie header.  This function properly formats the Set-Cookie for you and understands pick date and time formats.  If you wish more control you can use the WSETHEADER and build your own Set-Cookie line.

Here is a good [link](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Set-Cookie "Link to Set-Cookie documentation") on how Set-Cookie works.
