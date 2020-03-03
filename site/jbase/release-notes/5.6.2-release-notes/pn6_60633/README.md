# PN6_60633

**Created At:** 10/3/2017 7:51:26 AM  
**Updated At:** 10/3/2017 7:52:17 AM  
**Original Doc:** [pn6_60633](https://docs.jbase.com/36526-5-6-2-release-notes/pn6_60633)  
**Original ID:** 279159  
**Internal:** Yes  

## Description

A program could go into a CPU loop on Linux/Unix system if a **/** (forward slash) was present in the file name

### Current Release Behavior

Prior to this patch, on Linux systems the code to look up file names could loop if the following conditions were met:

1. There was a **/** in the file name, e.g **abc/def**
2. If **abc** existed but **def** did not.  
