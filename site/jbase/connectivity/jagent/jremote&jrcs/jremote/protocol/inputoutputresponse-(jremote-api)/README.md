# InputOutputResponse (jremote API)

**Created At:** 9/25/2017 12:19:18 PM  
**Updated At:** 12/24/2018 6:16:33 PM  
**Original Doc:** [com_jbase_jremote_protocol_inputoutputresponse](https://docs.jbase.com/39270-protocol/com_jbase_jremote_protocol_inputoutputresponse)  
**Original ID:** 278388  
**Internal:** No  

<!--<br>    try {<br>        if (location.href.indexOf('is-external=true') == -1) {<br>            parent.document.title="InputOutputResponse (jremote   API)";<br>        }<br>    }<br>    catch(err) {<br>    }<br>//--><br>var methods = {"i0":10,"i1":10,"i2":10,"i3":10,"i4":10};<br>var tabs = {65535:["t0","All Methods"],2:["t2","Instance Methods"],8:["t4","Concrete Methods"]};<br>var altColor = "altColor";<br>var rowColor = "rowColor";<br>var tableTab = "tableTab";<br>var activeTableTab = "activeTableTab";
JavaScript is disabled on your browser.



## Class InputOutputResponse

All Implemented Interfaces:[JBaseSerializable](./../../io/jbaseserializable-%28jremote-api%29 "interface in com.jbase.jremote.io")
* * *


```
public class InputOutputResponse
extends JRemoteResponse
```

### Nested Class Summary

- Nested classes/interfaces inherited from interface com.jbase.jremote.io.JBaseSerializable
    - `JBaseSerializable.TYPE`






### Field Summary


| Modifier and Type<br> | Field and Description<br> |
| --- | --- |
| `static int`<br> | `INPUTCMD` <br> |
| `static int`<br> | `OUTPUTCMD` <br> |






### Constructor Summary


| Constructor and Description<br> |
| --- |
| `InputOutputResponse()` <br> |






### Method Summary


| Modifier and Type<br> | Method and Description<br> |
| --- | --- |
| `int`<br> | `getCommand()` <br> |
| `JDynArray`<br> | `getOutput()` <br> |
| `int`<br> | `getType()` <br> |
| `void`<br> | `readObject(JBaseObjectReader reader, int version)` <br> |
| `void`<br> | `writeObject(JBaseObjectWriter writer, int version)` <br> |


- Methods inherited from class com.jbase.jremote.protocol.JRemoteResponse
    - `getVersion`
- Methods inherited from class java.lang.Object
    - `clone, equals, finalize, getClass, hashCode, notify, notifyAll, toString, wait, wait, wait`

### Field Detail

#### OUTPUTCMD

```
public static final int OUTPUTCMD
```
See Also:[Constant Field Values](./../../constant-field-values)
#### INPUTCMD

```
public static final int INPUTCMD
```
See Also:[Constant Field Values](./../../constant-field-values)


### Constructor Detail

#### InputOutputResponse

```
public InputOutputResponse()
```



### Method Detail

#### getCommand

```
public int getCommand()
```

#### getOutput

```
public JDynArray getOutput()
```

#### writeObject

```
public void writeObject(JBaseObjectWriter writer,
                        int version)
                 throws IOException
```
Throws:`IOException`
#### readObject

```
public void readObject(JBaseObjectReader reader,
                       int version)
                throws IOException,
                       ClassNotFoundException
```
Throws:`IOException``ClassNotFoundException`
#### getType

```
public int getType()
```
Returns:type id of the objects, used during the serializationSee Also:[`JBaseSerializable.getType()`](./../../io/jbaseserializable-%28jremote-api%29#getType--)


Back to [jREMOTE API](com_jbase_jremote_package-summary)


