# PN5_60720

<PageHeader />

### Description

Unable to access encrypted Dynamic Files with Q- and F-pointers



### Previous Release Behavior

Q- and F-pointers could not open an encrypted Dynamic file when an algorithm and key were specified, e.g.

```
create-file jdfile encrypted=true algorithm=blowfish key=123456

ED MD QPOINTER
001 Q
002 home
003 jdfile

jsh ~ -->LIST QPOINTER
Unknown decrypt algorithm in KEY
No file name could be found for your query
```



### Current Release Behavior

Q- and F-pointers can now access encrypted Dynamic Files.

  
<PageFooter />
