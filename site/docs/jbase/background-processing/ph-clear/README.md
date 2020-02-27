# PH-CLEAR 

**Created At:** 6/14/2018 2:08:08 PM  
**Updated At:** 7/19/2018 12:12:16 PM  
**Original Doc:** [ph-clear](https://docs.jbase.com/46465-background-processing/ph-clear)  
**Original ID:** 321817  
**Internal:** No  


## Description 

The jBASE PH-CLEAR command clears the jBTP log and history file. The command may be as:

```
PH-CLEAR {taskid | port} {(Options}
```

where:

- taskid specifies that only the entries for the taskid are to be cleared.
- port specifies that the entries for the port number are to be cleared.


and options may be:

- I  Clear entries interactively. i.e. prompt before deleting entry.




## Note: 


> This command can only be executed by the super user/Administrators. If a taskid, port number or interactive option is NOT specified all entries in the log file will be deleted.




### EXAMPLE

```
PH-CLEAR 100
```

Deletes log and history records for port number 100.



Back to [jBTP](./../jbtp)
