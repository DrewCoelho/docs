# PN5_60666

**Created At:** 12/26/2017 10:43:33 AM  
**Updated At:** 2/16/2018 7:06:53 PM  
**Original Doc:** [pn5_60666](https://docs.jbase.com/release-notes/pn5_60666)  
**Original ID:** 292207  
**Internal:** No  


### Description

jQL: The use of LIST would cause a memory leak



### Previous Release Behavior

Using LIST would cause a memory leak. It only had to be a fairly basic LIST statement to get the process to leak memory. After looping thousands of times, it could cause the jBASE process to fall over and die due to exhaustion of memory.



### Current Release Behavior

No memory leak!
