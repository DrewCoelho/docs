# PN5_60680

**Created At:** 12/27/2017 9:07:25 AM  
**Updated At:** 2/16/2018 7:08:04 PM  
**Original Doc:** [pn5_60680](https://docs.jbase.com/release-notes/pn5_60680)  
**Original ID:** 292255  
**Internal:** No  


### Description

jQL: Multiple BREAK-ON "'P'" clauses produce multiple page breaks



### Previous Release Behavior

```
LIST MD 'LIST' BREAK-ON *A0 "'P'" BREAK-ON *A0 "'P'" 
```

would produce 2 page breaks, one for each BREAK-ON. This is correct as 'P' is used twice; however this is not the same behavior with other PICKs.



### Current Release Behavior

For compatibility with other Multi-Value implentations, there is now a new configuration option:

```
dont_page_on_all_breaks
```

When **dont\_page\_on\_all\_breaks = true** then additional page ejects are suppressed.

This option is not added to any emulation by default in the **Config\_EMULATE** file, it is documented in **Config\_EMULATE.txt** and should only be used if all else fails.
