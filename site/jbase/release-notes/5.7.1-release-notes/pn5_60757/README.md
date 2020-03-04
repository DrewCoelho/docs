# PN5_60757

**Created At:** 8/27/2018 10:25:18 AM  
**Updated At:** 10/24/2018 8:38:58 PM  
**Original Doc:** [336199-pn5_60757](https://docs.jbase.com/48420-5-7-1-release-notes/336199-pn5_60757)  
**Original ID:** 336199  
**Internal:** No  


### Description

**PRINTER CLOSE** prevents the **FOOTING** text from being printed on the last page of a print job



### Previous Release Behavior

When this program is run, the **PRINTER CLOSE** prevents the **FOOTING** text from printing:

```
0001 EXECUTE "SP-ASSIGN HS"
0002 PRINTER ON
0003 HEADING "Heading"
0004 FOOTING "Footing"
0005 FOR x = 1 TO 2
0006     PRINT "Line ":x
0007 NEXT x
0008 PRINTER OFF
0009 PRINTER CLOSE
```

The **FOOTING** will print on every page except the last page.



### Current Release Behavior

All pages print the FOOTING.
