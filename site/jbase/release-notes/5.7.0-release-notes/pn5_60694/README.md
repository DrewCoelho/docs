# PN5_60694

**Created At:** 1/8/2018 10:29:32 AM  
**Updated At:** 2/16/2018 7:10:41 PM  
**Original Doc:** [pn5_60694](https://docs.jbase.com/release-notes/pn5_60694)  
**Original ID:** 293727  
**Internal:** No  


### Description

Spooler: The **SETPTR** banner does not persist after being set by a previous **SETPTR**



### Previous Release Behavior

When a banner was specified in a **SETPTR** command then it did not persist to subsequent **SETPTR** commands, e.g.

```
jsh home ~ -->SETPTR ,132,62,0,0,3,AT FILE,BANNER wibble
Unit Number   :0
Page Width    :132
Page Depth    :62
Top Margin    :0
Bottom Margin :0
Print mode    : 3 - Output to HOLD file ( wibble )

Default spool banner : "wibble"
Destination printer  : $JBCRELEASEDIR%stmp%s%q_%j.txt
Initial Job State    : HOLD

jsh home ~ -->SETPTR ,80,25,0,0,3
Unit Number   :0
Page Width    :80
Page Depth    :25
Top Margin    :0
Bottom Margin :0
Print mode    : 3 - Output to HOLD file ( P#0000 )

Default spool banner : "P#0000"
Destination printer  : $JBCRELEASEDIR%stmp%s%q_%j.txt
Initial Job State    : HOLD
```

In the above example, the banner was reset to the default **P#0000**.

The banner should have been kept as **wibble**, which is the default behavior on platforms that support the **SETPTR** command.



### Current Release Behavior

Any time a banner is used with **SETPTR** then it uses that banner. However, if the previous **SETPTR** specified a banner and a one is NOT specified with the current **SETPTR** then we pick up the existing banner unless the **SETPTR** command used the **AT printer** option.

The **SP-ASSIGN** command unconditially resets the BANNER to its default of **P#0000**.

e.g.

```
jsh home ~ -->SETPTR ,132,62,0,0,3,AT FILE,BANNER wibble
Unit Number   :0
Page Width    :132
Page Depth    :62
Top Margin    :0
Bottom Margin :0
Print mode    : 3 - Output to HOLD file ( wibble )

Default spool banner : "wibble"
Destination printer  : /home/danielk/temp/file.txt
Initial Job State    : HOLD

jsh home ~ -->SETPTR ,80,25,0,0,3
Unit Number   :0
Page Width    :80
Page Depth    :25
Top Margin    :0
Bottom Margin :0
Print mode    : 3 - Output to HOLD file ( wibble )

Default spool banner : "wibble"
Destination printer  : /home/danielk/temp/file.txt
Initial Job State    : HOLD

jsh home ~ -->SP-ASSIGN
jsh home ~ -->SETPTR ?
Unit Number   :0
Page Width    :132
Page Depth    :64
Top Margin    :3
Bottom Margin :3
Print mode    : 1 - Spooled Output

Default spool banner : "P#0000"
Destination printer  : /dev/lp0
Initial Job State    : PRINT
```
