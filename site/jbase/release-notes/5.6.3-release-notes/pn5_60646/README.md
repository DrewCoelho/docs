# PN5_60646

<PageHeader />

## Description

jQL not correctly processing statements using both FMT and CONV

### Current Release Behavior

Prior to this patch, a jQL statement such as:

```
LIST LISTBUG ALT1 CONV "T1,20" FMT "20L" DESC CONV "T1,30" FMT "30L" SLINE CONV "T1,4" FMT "4L" SPEC CONV "T1,4" FMT "4L"
```

would display random characters, some of them outside the range of the normal printable character set.

Back to [5.6.2 release Notes](./../README.md)
