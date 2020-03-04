# PN5_60791

**Created At:** 9/7/2018 9:09:23 AM  
**Updated At:** 10/24/2018 8:48:04 PM  
**Original Doc:** [pn5_60791](https://docs.jbase.com/48420-5-7-1-release-notes/pn5_60791)  
**Original ID:** 338139  
**Internal:** No  


### Description

Prevent jlogdup from running out of resources



### Previous Release Behavior

Under extreme circumstances, the Transaction Journaling restore process, jlogdup, could run out of opened files and so the restore operation would fail with the 'no files' message.

This was caused by the jlogdup process having an open file cache of 970 files. On Linux the default number of open files allowed is 1024. The two numbers are perilously close to each other. Occasionally it ran out of files.

One answer is to increase the number of opened files on Unix/AIX using 'ulimit -n 2000' .



### Current Release Behavior

When jlogdup starts, it checks the number of open files allowable and adjusts the cache size accordingly. In fact it limits the cache to 50% of the open files size.

Note: This is not an issue on Windows as the default number of open files on Windows is 16384.
