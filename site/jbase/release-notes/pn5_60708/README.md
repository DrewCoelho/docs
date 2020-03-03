# PN5_60708

**Created At:** 2/20/2018 1:05:21 PM  
**Updated At:** 2/20/2018 1:06:02 PM  
**Original Doc:** [pn5_60708](https://docs.jbase.com/release-notes/pn5_60708)  
**Original ID:** 299975  
**Internal:** No  


### Description

Transaction Journaling: The **jlogdup** command does not accept a select-list to control what is restored



### Previous Release Behavior

On jBASE 3.4, the TJ restore program, **jlogdup**, would accept a select list to control what it restored. In jBASE 5.x this feature was no longer available.



### Current Release Behavior

We now accept a default select list. This means you can do selective restores with **jlogdup**.

Caveat: This patch simply makes the **jlogdup** command available as a shared object, meaning it will run in the same process as the caller. **jlogdup** was never designed to do this, so it might consume, and not release, memory and other resources. However, using **jlogdup** in this manner is very seldom used, and if it is used in this way, and it consumes memory, then then simply log out and back in again.
