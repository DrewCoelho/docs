# PN5_60655

**Created At:** 12/24/2017 11:19:43 AM  
**Updated At:** 2/16/2018 7:05:21 PM  
**Original Doc:** [292194-pn5_60655](https://docs.jbase.com/release-notes/292194-pn5_60655)  
**Original ID:** 292194  
**Internal:** No  


### Description

OCONV() difference in Sequoia emulation



### Previous Release Behavior

In Sequoia emulation, running this code:

```
001 PROGRAM oconv_test
002 CRT OCONV(OCONV(17082:@VM:17089, "D"), "MCP")
```

would return:

```
17082]17089
```



### Current Release Behavior

The above code now returns:

```
07 OCT 2014
```
