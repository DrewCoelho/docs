# EISMetaDataRepository (jremote API)

<PageHeader />

## Class EISMetaDataRepository

```
public class EISMetaDataRepository
extends Object
```

Wrapper class for EISMetaDataResponse object representing a meta data repository containing information of the underlying EIS instance.

### Constructor Summary


| Constructor and Description<br> |
| --- |
| `EISMetaDataRepository()` <br> |
| `EISMetaDataRepository(EISMetaDataResponse mdRespository)` <br> |






### Method Summary


| Modifier and Type<br> | Method and Description<br> |
| --- | --- |
| `JDynArray`<br> | `getRepositoryEntry(String key)`<br>Obtain the value of a repository entry<br> |


- Methods inherited from class java.lang.Object
    - `clone, equals, finalize, getClass, hashCode, notify, notifyAll, toString, wait, wait, wait`

### Constructor Detail

#### EISMetaDataRepository

```
public EISMetaDataRepository()
```



#### EISMetaDataRepository

```
public EISMetaDataRepository(EISMetaDataResponse mdRespository)
```





### Method Detail

#### getRepositoryEntry

```
public JDynArray getRepositoryEntry(String key)
```

Obtain the value of a repository entry
Parameters:`key` - key of the repository entryReturns:value of the repository entry

Back to [jRemote API](../../../../jremote-api/README.md)

  
<PageFooter />
