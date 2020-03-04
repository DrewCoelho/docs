# PN5_60805

**Created At:** 9/27/2018 10:34:45 AM  
**Updated At:** 10/24/2018 8:49:06 PM  
**Original Doc:** [pn5_60805](https://docs.jbase.com/48420-5-7-1-release-notes/pn5_60805)  
**Original ID:** 340897  
**Internal:** No  


### Description

jQL: Sorting by default "inbuilt" ID column ignores justification

### Previous Release Behavior

```
LIST MYFILE
```

would always display its result left justified even if you added an @ID dictionary with right justification.

```
001: D
002: 0
005: 20R
```

### Current Release Behavior

Use the formatting if there is a @ID dictionary or if there is a dictionary that matches the filename, if not keep the existing 14 left justified formatting.
