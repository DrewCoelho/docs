# Distributed Files Overview

**Created At:** 9/14/2018 1:06:13 PM  
**Updated At:** 10/31/2018 8:14:11 AM  
**Original Doc:** [distributed-files-overview](https://docs.jbase.com/44203-distributed-files/distributed-files-overview)  
**Original ID:** 339399  
**Internal:** No  

**Tags:**
<badge text='distributed files' vertical='middle' />

## Description 

A Distributed file is a collection of existing files used primarily for the purpose of organizing data into functional groups. Each file within the collection is called a [part file](./../part-file).  A distributed file can contain up to 254 part files. The method for determining in which part file a record belongs is called the [partition algorithm](./../partition-algorithm).

As a simple example, suppose your database consists of records which span 42 regions and you elect to distribute your data so that each part file contains all records for a specific region. With distributed files you would be able to process any one of the region part files independently of the others, or you would be able to process all 42 region part files collectively (i.e. as one database containing the records from all 42 regions).



## Note: 


> Distributed files can also be used when the size of a file exceeds the size limit for the operating system (typically 2 gigabytes). This effectively permits file sizes to reach 254 times the maximum file size your operating system allows.

