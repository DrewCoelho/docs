# JRecordNotFoundException (jremote API)

**Created At:** 9/25/2017 12:09:44 PM  
**Updated At:** 12/24/2018 7:51:46 PM  
**Original Doc:** [com_jbase_jremote_jrecordnotfoundexception](https://docs.jbase.com/39248-jremote/com_jbase_jremote_jrecordnotfoundexception)  
**Original ID:** 278303  
**Internal:** No  


JavaScript is disabled on your browser.



## Class JRecordNotFoundException

All Implemented Interfaces:[Serializable](http://java.sun.com/j2se/1.5.0/docs/api/java/io/Serializable.html?is-external=true "class or interface in java.io")
* * *


```
public class JRecordNotFoundException
extends JRemoteException
```

A generic jBASE record not found exception.

Generally it is a good idea to check if a record exists before reading as throwing exceptions is more expensive.

### Constructor Summary


| Constructor and Description<br> |
| --- |
| `JRecordNotFoundException()` <br> |






### Method Summary

- Methods inherited from class com.jbase.jremote.JRemoteException
    - `getError`
- Methods inherited from class java.lang.Throwable
    - `addSuppressed, fillInStackTrace, getCause, getLocalizedMessage, getMessage, getStackTrace, getSuppressed, initCause, printStackTrace, printStackTrace, printStackTrace, setStackTrace, toString`
- Methods inherited from class java.lang.Object
    - `clone, equals, finalize, getClass, hashCode, notify, notifyAll, wait, wait, wait`

### Constructor Detail



#### JRecordNotFoundException

```
public JRecordNotFoundException()
```

Back to [jREMOTE API](com_jbase_jremote_package-summary)


