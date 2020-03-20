# JRemoteRequest (jremote API)

**Created At:** 9/25/2017 12:19:37 PM  
**Updated At:** 4/4/2018 8:39:01 PM  
**Original Doc:** [com_jbase_jremote_protocol_jremoterequest](https://docs.jbase.com/39270-protocol/com_jbase_jremote_protocol_jremoterequest)  
**Original ID:** 278391  
**Internal:** No  

<!--<br>    try {<br>        if (location.href.indexOf('is-external=true') == -1) {<br>            parent.document.title="JRemoteRequest (jremote   API)";<br>        }<br>    }<br>    catch(err) {<br>    }<br>//--><br>var methods = {"i0":10,"i1":10,"i2":10};<br>var tabs = {65535:["t0","All Methods"],2:["t2","Instance Methods"],8:["t4","Concrete Methods"]};<br>var altColor = "altColor";<br>var rowColor = "rowColor";<br>var tableTab = "tableTab";<br>var activeTableTab = "activeTableTab";
JavaScript is disabled on your browser.



## Class JRemoteRequest

All Implemented Interfaces:[JBaseSerializable](./../../io/jbaseserializable-%28jremote-api%29 "interface in com.jbase.jremote.io")Direct Known Subclasses:[AccountAuthenticationRequest](./../accountauthenticationrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [AuthenticationRequest](./../authenticationrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [BeginTransactionRequest](./../begintransactionrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [CallSubroutineRequest](./../callsubroutinerequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [ClearFileRequest](./../clearfilerequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [CloseFileRequest](./../closefilerequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [CommitTransactionRequest](./../committransactionrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [ConvRequest](./../convrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [DateTimeRequest](./../datetimerequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [DeleteRecordRequest](./../deleterecordrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [EchoRequest](./../echorequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [EISMetaDataRequest](./../eismetadatarequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [ExistsRecordRequest](./../existsrecordrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [JExecuteRequest](./../jexecuterequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [MonitoringRequest](./../monitoringrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [OpenFileRequest](./../openfilerequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [ReadCommonRequest](./../readcommonrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [ReadRecordRequest](./../readrecordrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [ReleaseRecordLockRequest](./../releaserecordlockrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [RemoteInputRequest](./../remoteinputrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [RollbackTransactionRequest](./../rollbacktransactionrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [SelectFileRequest](./../selectfilerequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [SelectListCloseRequest](./../selectlistcloserequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [SelectListCommitRequest](./../selectlistcommitrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [SelectListFetchRequest](./../selectlistfetchrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [SetPropertiesRequest](./../setpropertiesrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [StatementExecuteQueryRequest](./../statementexecutequeryrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [StatementFetchRequest](./../statementfetchrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [SwitchAccountRequest](./../switchaccountrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [WriteRecordRequest](./../writerecordrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [XACommitTransactionRequest](./../xacommittransactionrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [XAEndTransactionRequest](./../xaendtransactionrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [XAPrepareTransactionRequest](./../xapreparetransactionrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [XARollbackTransactionRequest](./../xarollbacktransactionrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol"), [XAStartTransactionRequest](./../xastarttransactionrequest-%28jremote-api%29 "class in com.jbase.jremote.protocol")
* * *


```
public abstract class JRemoteRequest
extends Object
implements JBaseSerializable
```

### Nested Class Summary

- Nested classes/interfaces inherited from interface com.jbase.jremote.io.JBaseSerializable
    - `JBaseSerializable.TYPE`






### Constructor Summary


| Constructor and Description<br> |
| --- |
| `JRemoteRequest()` <br> |






### Method Summary


| Modifier and Type<br> | Method and Description<br> |
| --- | --- |
| `int`<br> | `getVersion()` <br> |
| `void`<br> | `readObject(JBaseObjectReader reader, int version)` <br> |
| `void`<br> | `writeObject(JBaseObjectWriter writer, int version)` <br> |


- Methods inherited from class java.lang.Object
    - `clone, equals, finalize, getClass, hashCode, notify, notifyAll, toString, wait, wait, wait`
- Methods inherited from interface com.jbase.jremote.io.JBaseSerializable
    - `getType`

### Constructor Detail

#### JRemoteRequest

```
public JRemoteRequest()
```



### 


### Method Detail

#### writeObject

```
public void writeObject(JBaseObjectWriter writer,
                        int version)
                 throws IOException
```
Specified by:`writeObject` in interface `JBaseSerializable`Throws:`IOException`
#### readObject

```
public void readObject(JBaseObjectReader reader,
                       int version)
                throws IOException,
                       ClassNotFoundException
```
Specified by:`readObject` in interface `JBaseSerializable`Throws:`IOException``ClassNotFoundException`
#### getVersion

```
public int getVersion()
```
Specified by:`getVersion` in interface `JBaseSerializable`

Back to [jREMOTE API](com_jbase_jremote_package-summary)


