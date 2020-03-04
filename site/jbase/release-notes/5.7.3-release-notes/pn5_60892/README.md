# PN5_60892

**Created At:** 6/27/2019 12:48:18 PM  
**Updated At:** 6/29/2019 8:04:10 AM  
**Original Doc:** [pn5_60892](https://docs.jbase.com/61286-5-7-3-release-notes/pn5_60892)  
**Original ID:** 400131  
**Internal:** No  


### Description

New environment variable to ignore **EDICT** flags and **jDP\_Options**

### Previous Release Behavior

Using **SQLSELECT** or **JODBC** to retrieve a column which had a conversion in the dictionary item could display the data incorrectly due to the existence of certain **EDICT**flags or the **jDP\_Options** item in the dictionary.

### Current Release 

A new environment variable, **JSQL\_IGNORE\_JDPFLAGS**, causes the **EDICT**flags and the **jDP\_Options**item to be ignored. Set the environment variable as follows:

```
set JSQL_IGNORE_JDPFLAGS=1     [Windows]
export JSQL_IGNORE_JDPFLAGS=1  [Unix]
```
