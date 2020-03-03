# PN5_60574

**Created At:** 6/13/2017 2:19:26 PM  
**Updated At:** 11/22/2017 5:58:37 AM  
**Original Doc:** [pn5_60574](https://docs.jbase.com/36526-5-6-2-release-notes/pn5_60574)  
**Original ID:** 258859  
**Internal:** No  


### Description

jQL: Fix issue with CHAR(0) termination in record.



### Previous Release Behavior

When displaying a record with jQL, a CHAR(0) in the record would cause everything after the CHAR(0) to show as NULL. The actual data in the file is not affected.

For example,

```
001 <<char(0)>>pink floyd
002 dark side of the moon
003 1973
```

Doing...

```
LIST ALBUMS ARTIST TITLE YEAR
```

...would cause the whole record to display as NULL.



### Current Release Behavior

The whole record is accessible except for the attribute that contains the CHAR(0), which is truncated at the CHAR(0) position. IOW, this patch does not fix the issue of displaying \*A1 in the above example but will allow the rest of the record to be accessed.
