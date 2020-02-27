# JRM JMV JDIR

**Created At:** 8/30/2018 2:13:28 PM  
**Updated At:** 10/25/2018 8:55:23 AM  
**Original Doc:** [jrm-jmv-jdir](https://docs.jbase.com/48399-tools/jrm-jmv-jdir)  
**Original ID:** 336923  
**Internal:** No  


## Description 

Many commands are built-in to the Windows command shell and so can be executed like other executables. The following commands have been provided to use in either [jsh](./../../jshell) or cmd shell. As they are executables to use in place of **cmd.exe** functionality, the commands are provided only on Windows.




| Command<br> | Description<br> |
| --- | --- |
| jrm file | jrm -r directory<br> | remove file or directory, recursively<br> |
| jmv oldfile newfile<br> | move oldfile to newfile<br> |
| jdir {directory|file}<br> | list directory<br> |


* * *



## Note: 


> If [transaction journaling](./../../../administration/transaction-replication/introduction-to-transaction-journaling) is active, the actions performed by jrm and jmv are **not** logged.



