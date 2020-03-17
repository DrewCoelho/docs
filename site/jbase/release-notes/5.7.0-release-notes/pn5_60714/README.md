# PN5_60714

**Created At:** 2/7/2018 1:51:37 PM  
**Updated At:** 2/7/2018 1:52:34 PM  
**Original Doc:** [pn5_60714](https://docs.jbase.com/release-notes/pn5_60714)  
**Original ID:** 298058  
**Internal:** No  


### Description

jBC code with END followed by a comment would not compile



### Previous Release Behavior

jBC code with the last line an 'END' followed by a comment would not compile. Note, this is when 'END' denotes end of program rather an END to a matching IF.

Each of these 2 lines, as the last line of a program, failed to compile (spaces replace with \_ for clarity):

```
END;_*
END_;_*
```



### Current Release Behavior

The above examples compile successfully.
