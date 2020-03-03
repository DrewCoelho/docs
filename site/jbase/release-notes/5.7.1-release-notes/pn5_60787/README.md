# PN5_60787

**Created At:** 8/29/2018 10:35:55 AM  
**Updated At:** 10/24/2018 8:47:55 PM  
**Original Doc:** [pn5_60787](https://docs.jbase.com/48420-5-7-1-release-notes/pn5_60787)  
**Original ID:** 336541  
**Internal:** No  


### Description

Util: Paragraphs with "N" in attribute 1 do not get called with **LOGTO**



### Previous Release Behavior

Using "N" instead of "PA" in attribute 1 of a Paragraph, a login Paragraph did not get called with **LOGTO**or "jsh -"



### Current Release Behavior

"N" is now recognized as a valid synonym for Paragraphs when used as a login process.
