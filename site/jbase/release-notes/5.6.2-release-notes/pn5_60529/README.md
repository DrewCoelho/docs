# PN5_60529

**Created At:** 2/15/2019 9:13:35 PM  
**Updated At:** 2/15/2019 9:36:51 PM  
**Original Doc:** [pn5_60529](https://docs.jbase.com/36526-5-6-2-release-notes/pn5_60529)  
**Original ID:** 365924  
**Internal:** No  


### Description

jQL: Calculations based on totals using a correlative

Update break processor to try and mimic other PICKs, if the total is a calculation based on other attributes used in other totals we need some mechanism to flag that the values are to come from the aggregates. This issue is more or less exactly the same problem as using CALC.



### Previous Release Behavior

Calculations on break totals simply did not work when using correlatives in attribute 8 of the dictionary.



### Current Release Behavior

New behavior is to make dictionary attributes 7 and 8 identical and contain both the correlative and output format.

For example:



```
001 A
002 0
. . .
007 F;44;43;_;-;C0;#;44;43;_;-;44;C100;*;_;/;*]MR0
008 F;44;43;_;-;C0;#;44;43;_;-;44;C100;*;_;/;*]MR0
. . .
```

At runtime this will become:



```
007 MR0
008 F;44;43;_;-;C0;#;44;43;_;-;44;C100;*;_;/;*
```

While the file is being processed data will be read, however when we hit a break the data will now be taken from the totalling columns for \*A43, \*A44.

Note that both \*A43 and \*A44 must be present and TOTAL'd.
