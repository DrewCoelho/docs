# PN5_60777

**Created At:** 8/28/2018 9:08:09 AM  
**Updated At:** 10/24/2018 8:46:00 PM  
**Original Doc:** [pn5_60777](https://docs.jbase.com/48420-5-7-1-release-notes/pn5_60777)  
**Original ID:** 336404  
**Internal:** No  


### Description

New security paradigm for jBASE files and utilities.



### Previous Release Behavior

The previous release had a per-file security basis which meant each secure file had a corresponding ]K file.

Some of the jBASE utilities were not working correctly with this security model.



### Current Release Behavior

jBASE now employs a system wide security mode as described [here](./../../../jbase/jbase-encryption---database-security).
