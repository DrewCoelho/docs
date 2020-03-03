# PN5_60646

**Created At:** 10/6/2017 11:04:49 AM  
**Updated At:** 11/23/2017 7:48:17 AM  
**Original Doc:** [pn5_60646](https://docs.jbase.com/36526-5-6-2-release-notes/pn5_60646)  
**Original ID:** 279798  
**Internal:** No  


### Description

jQL not correctly processing statements using both FMT and CONV



### Current Release Behavior

Prior to this patch, a jQL statement such as:

```
LIST LISTBUG ALT1 CONV "T1,20" FMT "20L" DESC CONV "T1,30" FMT "30L" SLINE CONV "T1,4" FMT "4L" SPEC CONV "T1,4" FMT "4L"
```

would display random characters, some of them outside the range of the normal printable character set.
