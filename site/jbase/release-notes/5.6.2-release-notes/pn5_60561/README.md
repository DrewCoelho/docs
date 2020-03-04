# PN5_60561

**Created At:** 6/13/2017 11:57:56 AM  
**Updated At:** 11/26/2017 9:45:57 PM  
**Original Doc:** [pn5_60561](https://docs.jbase.com/36526-5-6-2-release-notes/pn5_60561)  
**Original ID:** 258828  
**Internal:** No  


### Description

Creating an encrypted file can give an error when a zero length record is written to the file.



### Previous Release Behavior

1) Create an encrypted file:

```
jsh home ~ -->CREATE-FILE encfile ENCRYPTED=TRUE 1 101
```

2) Write a null record:

```
jsh home ~ -->jed encfile 1
NEW File encfile , Record '1'
Command-> fi
0001

Record '1' written to file 'encfile'
.\crypto\evp\evp_enc.c(282): OpenSSL internal error, assertion failed: inl > 0
```



### Current Release Behavior

Doesn't abort when writing a null record to an encrypted file.
