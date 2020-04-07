# JRemoteException (jremote API)

<PageHeader />

## Class JRemoteException

All Implemented Interfaces:SerializableDirect Known Subclasses:[JAuthenticationException](./../jauthenticationexception-%28jremote-api%29 "class in com.jbase.jremote"), [JRecordLockedException](./../jrecordlockedexception-%28jremote-api%29 "class in com.jbase.jremote"), [JRecordNotFoundException](./../jrecordnotfoundexception-%28jremote-api%29 "class in com.jbase.jremote"), [JSubroutineNotFoundException](./../jsubroutinenotfoundexception-%28jremote-api%29 "class in com.jbase.jremote")
* * *


```
public class JRemoteException
extends Exception
```

A generic exception thrown when an unexpected error occurs whilst communicating with the remote jBASE instance.

### Constructor Summary


| Constructor and Description<br> |
| --- |
| `JRemoteException()` <br> |
| `JRemoteException(ErrorResponse response)` <br> |
| `JRemoteException(String msg)` <br> |
| `JRemoteException(String msg, int error)` <br> |






### Method Summary


| Modifier and Type<br> | Method and Description<br> |
| --- | --- |
| `int`<br> | `getError()` <br> |




- Methods inherited from class java.lang.Throwable
    - `addSuppressed, fillInStackTrace, getCause, getLocalizedMessage, getMessage, getStackTrace, getSuppressed, initCause, printStackTrace, printStackTrace, printStackTrace, setStackTrace, toString`


- Methods inherited from class java.lang.Object
    - `clone, equals, finalize, getClass, hashCode, notify, notifyAll, wait, wait, wait`

### Constructor Detail

#### JRemoteException

```
public JRemoteException()
```

#### JRemoteException

```
public JRemoteException(String msg)
```

#### JRemoteException

```
public JRemoteException(String msg,
                        int error)
```

#### JRemoteException

```
public JRemoteException(ErrorResponse response)
```



### 


### Method Detail

#### getError

```
public int getError()
```



Back to [jREMOTE API](com_jbase_jremote_package-summary)


