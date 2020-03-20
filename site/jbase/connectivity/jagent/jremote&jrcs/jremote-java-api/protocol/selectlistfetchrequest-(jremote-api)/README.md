# SelectListFetchRequest (jremote API)

**Created At:** 9/25/2017 12:21:38 PM  
**Updated At:** 4/4/2018 9:00:08 PM  
**Original Doc:** [com_jbase_jremote_protocol_selectlistfetchrequest](https://docs.jbase.com/39270-protocol/com_jbase_jremote_protocol_selectlistfetchrequest)  
**Original ID:** 278410  
**Internal:** No  

<!--<br>    try {<br>        if (location.href.indexOf('is-external=true') == -1) {<br>            parent.document.title="SelectListFetchRequest (jremote   API)";<br>        }<br>    }<br>    catch(err) {<br>    }<br>//--><br>var methods = {"i0":10,"i1":10,"i2":10,"i3":10,"i4":10,"i5":10,"i6":10,"i7":10};<br>var tabs = {65535:["t0","All Methods"],2:["t2","Instance Methods"],8:["t4","Concrete Methods"]};<br>var altColor = "altColor";<br>var rowColor = "rowColor";<br>var tableTab = "tableTab";<br>var activeTableTab = "activeTableTab";
JavaScript is disabled on your browser.



## Class SelectListFetchRequest

All Implemented Interfaces:[JBaseSerializable](./../../io/jbaseserializable-%28jremote-api%29 "interface in com.jbase.jremote.io")
* * *


```
public class SelectListFetchRequest
extends JRemoteRequest
```

### Nested Class Summary

- Nested classes/interfaces inherited from interface com.jbase.jremote.io.JBaseSerializable
    - `JBaseSerializable.TYPE`






### Constructor Summary


| Constructor and Description<br> |
| --- |
| `SelectListFetchRequest()` <br> |
| `SelectListFetchRequest(int selectListId, int fetchDirection, int fetchSize, boolean fetchData, JSelectListProt modifiedSelectList)` <br> |






### Method Summary


| Modifier and Type<br> | Method and Description<br> |
| --- | --- |
| `int`<br> | `fetchDirection()` <br> |
| `boolean`<br> | `getFetchData()` <br> |
| `int`<br> | `getFetchSize()` <br> |
| `JSelectListProt`<br> | `getModifiedSelectList()` <br> |
| `int`<br> | `getSelectListId()` <br> |
| `int`<br> | `getType()` <br> |
| `void`<br> | `readObject(JBaseObjectReader reader, int version)` <br> |
| `void`<br> | `writeObject(JBaseObjectWriter writer, int version)` <br> |


- Methods inherited from class com.jbase.jremote.protocol.JRemoteRequest
    - `getVersion`
- Methods inherited from class java.lang.Object
    - `clone, equals, finalize, getClass, hashCode, notify, notifyAll, toString, wait, wait, wait`

### Constructor Detail

#### SelectListFetchRequest

```
public SelectListFetchRequest()
```

#### SelectListFetchRequest

```
public SelectListFetchRequest(int selectListId,
                              int fetchDirection,
                              int fetchSize,
                              boolean fetchData,
                              JSelectListProt modifiedSelectList)
```



### 


### Method Detail

#### getSelectListId

```
public int getSelectListId()
```

#### fetchDirection

```
public int fetchDirection()
```

#### getFetchSize

```
public int getFetchSize()
```

#### getFetchData

```
public boolean getFetchData()
```

#### getModifiedSelectList

```
public JSelectListProt getModifiedSelectList()
```

#### writeObject

```
public void writeObject(JBaseObjectWriter writer,
                        int version)
                 throws IOException
```
Specified by:`writeObject` in interface `JBaseSerializable`Overrides:`writeObject` in class `JRemoteRequest`Throws:`IOException`
#### readObject

```
public void readObject(JBaseObjectReader reader,
                       int version)
                throws IOException,
                       ClassNotFoundException
```
Specified by:`readObject` in interface `JBaseSerializable`Overrides:`readObject` in class `JRemoteRequest`Throws:`IOException``ClassNotFoundException`
#### getType

```
public int getType()
```
Returns:type id of the objects, used during the serializationSee Also:[`JBaseSerializable.getType()`](./../../io/jbaseserializable-%28jremote-api%29#getType--)



Back to [jREMOTE API](com_jbase_jremote_package-summary)
