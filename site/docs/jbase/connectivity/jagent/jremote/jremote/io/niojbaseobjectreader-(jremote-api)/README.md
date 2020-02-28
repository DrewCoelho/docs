# NIOJBaseObjectReader (jremote API)

**Created At:** 9/25/2017 11:53:12 AM  
**Updated At:** 12/24/2018 9:03:37 PM  
**Original Doc:** [com_jbase_jremote_io_niojbaseobjectreader](https://docs.jbase.com/39250-io/com_jbase_jremote_io_niojbaseobjectreader)  
**Original ID:** 278170  
**Internal:** No  

<!--<br>    try {<br>        if (location.href.indexOf('is-external=true') == -1) {<br>            parent.document.title="NIOJBaseObjectReader (jremote   API)";<br>        }<br>    }<br>    catch(err) {<br>    }<br>//--><br>var methods = {"i0":10,"i1":10,"i2":10,"i3":10,"i4":10,"i5":10,"i6":10,"i7":10,"i8":10,"i9":10,"i10":10,"i11":10};<br>var tabs = {65535:["t0","All Methods"],2:["t2","Instance Methods"],8:["t4","Concrete Methods"]};<br>var altColor = "altColor";<br>var rowColor = "rowColor";<br>var tableTab = "tableTab";<br>var activeTableTab = "activeTableTab";
JavaScript is disabled on your browser.



## Class NIOJBaseObjectReader

All Implemented Interfaces:[JBaseObjectReader](./../jbaseobjectreader-%28jremote-api%29 "interface in com.jbase.jremote.io")
* * *


```
public class NIOJBaseObjectReader
extends AbstractJBaseObjectReader
```

jBASE object reader based on the new Java IO.

### Field Summary


| Modifier and Type<br> | Field and Description<br> |
| --- | --- |
| `static long`<br> | `READ_TIMEOUT`<br>The temporary selectors read timeout.<br> |


- Fields inherited from class com.jbase.jremote.io.AbstractJBaseObjectReader
    - `log`






### Constructor Summary


| Constructor and Description<br> |
| --- |
| `NIOJBaseObjectReader(ObjectFactory factory, SocketChannel channel)` <br> |






### Method Summary


| Modifier and Type<br> | Method and Description<br> |
| --- | --- |
| `protected void`<br> | `checkBuffer(int newDataLength)` <br> |
| `void`<br> | `close()` <br> |
| `protected int`<br> | `doRead(int numberOfBytes)`<br>Read bytes using the read a temporary Selector<br> |
| `protected byte`<br> | `getByte()` <br> |
| `protected int`<br> | `getBytes(byte[] buf)` <br> |
| `protected int`<br> | `getBytes(ByteBuffer bBuf)` <br> |
| `protected int`<br> | `getInt()` <br> |
| `ObjectFactory`<br> | `getObjectFactory()`<br>This method must be implemented by concrete ObjectReaders.<br> |
| `protected int`<br> | `inBytes(int numberOfBytesToRead)` <br> |
| `boolean`<br> | `isClosed()` <br> |
| `protected String`<br> | `readUTF()` <br> |
| `void`<br> | `setSocketChannel(SocketChannel socketChannel)` <br> |


- Methods inherited from class com.jbase.jremote.io.AbstractJBaseObjectReader
    - `bufferedRead, checkBuffer, readByteObject, readBytes, readInt, readJBaseSerializableObject, readObject, readObject, readObject, readRootObject, readString`
- Methods inherited from class java.lang.Object
    - `clone, equals, finalize, getClass, hashCode, notify, notifyAll, toString, wait, wait, wait`

### Field Detail

#### READ\_TIMEOUT

```
public static final long READ_TIMEOUT
```

The temporary selectors read timeout. 30 seconds.
See Also:[Constant Field Values](./../../constant-field-values)


### 


### Constructor Detail

#### NIOJBaseObjectReader

```
public NIOJBaseObjectReader(ObjectFactory factory,
                            SocketChannel channel)
```



### 


### Method Detail

#### getObjectFactory

```
public ObjectFactory getObjectFactory()
```

Description copied from class: `AbstractJBaseObjectReader`

This method must be implemented by concrete ObjectReaders.
Specified by:`getObjectFactory` in class `AbstractJBaseObjectReader`Returns:an instance of a class implementing JBaseSerializable
#### 


#### close

```
public void close()
           throws IOException
```
Specified by:`close` in interface `JBaseObjectReader`Specified by:`close` in class `AbstractJBaseObjectReader`Throws:`IOException`
#### 


#### getByte

```
protected byte getByte()
                throws IOException
```
Specified by:`getByte` in class `AbstractJBaseObjectReader`Throws:`IOException`
#### 


#### getInt

```
protected int getInt()
              throws IOException
```
Specified by:`getInt` in class `AbstractJBaseObjectReader`Throws:`IOException`
#### 


#### getBytes

```
protected int getBytes(byte[] buf)
                throws IOException
```
Specified by:`getBytes` in class `AbstractJBaseObjectReader`Throws:`IOException`
#### 


#### getBytes

```
protected int getBytes(ByteBuffer bBuf)
                throws IOException
```
Specified by:`getBytes` in class `AbstractJBaseObjectReader`Throws:`IOException`
#### 


#### inBytes

```
protected int inBytes(int numberOfBytesToRead)
               throws IOException
```
Specified by:`inBytes` in class `AbstractJBaseObjectReader`Throws:`IOException`
#### 


#### readUTF

```
protected String readUTF()
                  throws IOException
```
Specified by:`readUTF` in class `AbstractJBaseObjectReader`Throws:`IOException`
#### 


#### doRead

```
protected int doRead(int numberOfBytes)
              throws IOException
```

Read bytes using the read a temporary Selector
Throws:`IOException`
#### 


#### checkBuffer

```
protected void checkBuffer(int newDataLength)
```

#### 


#### isClosed

```
public boolean isClosed()
```

#### 


#### setSocketChannel

```
public void setSocketChannel(SocketChannel socketChannel)
```

Back to [jREMOTE API](com_jbase_jremote_package-summary)
