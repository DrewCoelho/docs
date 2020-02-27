# JCL L

**Created At:** 5/28/2018 11:12:38 AM  
**Updated At:** 6/11/2018 4:23:21 AM  
**Original Doc:** [318727-jcl-l](https://docs.jbase.com/45792-jcl/318727-jcl-l)  
**Original ID:** 318727  
**Internal:** No  

**Tags:**
<badge text='print' vertical='middle' />
<badge text='jcl' vertical='middle' />

## Description 

This  command formats printed output. It takes the general form:

```
L element{, element}...
```

where element can be any of :


| Element<br> | Description<br> |
| --- | --- |
| "text"<br> | Prints literal text. Enclose the text in quotes.<br> |
| r{;input;}<br> | Prints the result of a direct or indirect reference to a buffer or select register ( r). If required, a jQL  input conversion can be applied before output.<br> |
| r{:output:}<br> | Prints the result of a direct or indirect reference to a buffer or select register ( r). If required, a jQL  output conversion can be applied before output.<br> |
| n<br> | Skips n lines before printing. You cannot use n in a HDR print format specification.<br> |
| (c)<br> | Sets the print position to column number c. Can be a direct or indirect reference to a buffer or select register.<br> |
| +<br> | Suppresses NEWLINE being output at the end of the L command. You cannot use + in a HDR print format specification.<br> |
| C<br> | Closes the print file and forces printing. You cannot use C in a HDR print format specification.<br> |
| E<br> | Ejects to top-of-form (form feed). You cannot use E in a HDR print format specification.<br> |
| N<br> | Redirects subsequent printer output to the terminal. Normally only used for debugging. Must be the only element in an L command.<br> |
| HDR<br> | Allow you to define a page heading. HDR, must be the first element in the L command.<br> |
| L<br> | Outputs a line feed in the heading. Only used in a HDR specification.<br> |
| P<br> | Outputs the current page number in a heading. Only used in a HDR specification.<br> |
| T<br> | Outputs current time and date in a heading. Only used in a HDR specification.<br> |
| Z<br> | Resets the current page number in a heading to zero. Only used in a HDR specification.<br> |




Output from the L command creates (or adds to) a print file. The print file will remain open until a shell command is issued by using the P command. If the shell command also generates print output, this will be added to the same print file. You can close the print file and avoid any unnecessary output by choosing any shell command, which does not generate print output, or by using the L C command. Alternatively, you can hold the print file open indefinitely by using the O option of the SP-ASSIGN command.

by terminating each preceding line with a comma (,), continuation lines can be created which do not start with an L. A + specified as the last element the command will cause the output from the next L command to be appended.



## Note: 


> If a heading statement (HDR) is specified, which contains direct or indirect references, these will be evaluated (and included in the heading) as the command is processed. Subsequent changes to the source values will have no effect on the heading.




###### EXAMPLE

```
MV %1 "Quarter 4"
L HDR,"PAGE  ",P,(10),T
L 5,"Sales Report for ",%1
```

will output:

```
PAGE  1 10:25:17 10 OCT 1999
Sales Report for Quarter 4
```



Back to [JCL Commands](./../jcl-commands)
