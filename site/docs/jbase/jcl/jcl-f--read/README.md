# JCL F -READ

**Created At:** 5/28/2018 10:52:02 AM  
**Updated At:** 6/11/2018 4:25:44 AM  
**Original Doc:** [318670-jcl-f-read](https://docs.jbase.com/45792-jcl/318670-jcl-f-read)  
**Original ID:** 318670  
**Internal:** No  

**Tags:**
<badge text='read' vertical='middle' />
<badge text='jcl' vertical='middle' />

## Description 

This command reads a record from an open file into a file buffer. It takes the general form:

```
F-READ  file-buffer key error-cmd-line
```

or

```
F-R file-buffer key error-cmd-line
```

where:

- file-buffer is the number (1 to 9) of the file buffer with which the file is associated.
- key is the key of the record to be read. Can be a literal (not enclosed in quotes), or a direct or indirect reference to a buffer or select register.
- error-cmd-line is the line immediately after the F-READ  command. Only executed if the specified record cannot be read.




## Note: 


> If an associated file has not been opened, the program will terminate with an error message. If the specified record is not on file, the line immediately following the F-READ  command will be executed. If the read is successful, this line will be ignored.




##### EXAMPLE

```
001 PQN
002 F-OPEN  1 SALES
003 X ERROR: Can't find the Sales File!
004 T C, (5, 10), "Welcome to...",+
...
015 F-READ  1 ABC
016 X ERROR: Record ABC not found!
017 T "Record ABC found"
```

Attempts to read record ABC from the SALES file into file buffer 1. If record ABC is not found, the program terminates with an appropriate error message. If the record is found, the message on line 17 is displayed and execution continues.



See also [F-OPEN](./../jcl-f--open)

Back to [JCL Commands](./../jcl-commands)
