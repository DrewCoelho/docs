# Uses of Interface com.jbase.jremote.JSelectList (jremote API)

**Created At:** 9/25/2017 11:39:59 AM  
**Updated At:** 4/5/2018 8:55:35 PM  
**Original Doc:** [com_jbase_jremote_class-use_jselectlist](https://docs.jbase.com/39249-class-use/com_jbase_jremote_class-use_jselectlist)  
**Original ID:** 278059  
**Internal:** No  

<!--<br>    try {<br>        if (location.href.indexOf('is-external=true') == -1) {<br>            parent.document.title="Uses of Interface com.jbase.jremote.JSelectList (jremote   API)";<br>        }<br>    }<br>    catch(err) {<br>    }<br>//-->
JavaScript is disabled on your browser.



<!--<br>  allClassesLink = document.getElementById("allclasses\_navbar\_top");<br>  if(window==top) {<br>    allClassesLink.style.display = "block";<br>  }<br>  else {<br>    allClassesLink.style.display = "none";<br>  }<br>  //-->

## Uses of Interface
com.jbase.jremote.JSelectList

| Package<br> | Description<br> |
| --- | --- |
 Packages that use [JSelectList](./../../jselectlist-%28jremote-api%29 "interface in com.jbase.jremote")  | com.jbase.jremote<br> |  <br> |
| com.jbase.jremote.io<br> |  <br> |
| com.jbase.jremote.jca<br> |  <br> |






### Uses of [JSelectList](./../../jselectlist-%28jremote-api%29 "interface in com.jbase.jremote") in [com.jbase.jremote](./../../../../jremote-api)


| Modifier and Type<br> | Interface and Description<br> |
| --- | --- |
 Subinterfaces of [JSelectList](./../../jselectlist-%28jremote-api%29 "interface in com.jbase.jremote") in [com.jbase.jremote](./../../../../jremote-api)  | `interface `<br> | `JCursor`<br>A cursor to a jBASE file.<br> |



| Modifier and Type<br> | Method and Description<br> |
| --- | --- |
 Methods in [com.jbase.jremote](./../../../../jremote-api) that return [JSelectList](./../../jselectlist-%28jremote-api%29 "interface in com.jbase.jremote")  | `JSelectList`<br> | JConnection.`createSelectList(JDynArray jd)`<br>Create a select list object from an existing dynamic array containing a list of keys separated by attribute markers.<br> |
| `JSelectList`<br> | JExecuteResults.`getReturnList()` <br> |
| `JSelectList`<br> | JFile.`select()`<br>Returns a select list containing the record keys in this jBASE file.<br> |



| Modifier and Type<br> | Method and Description<br> |
| --- | --- |
 Methods in [com.jbase.jremote](./../../../../jremote-api) with parameters of type [JSelectList](./../../jselectlist-%28jremote-api%29 "interface in com.jbase.jremote")  | `JResultSet`<br> | JStatement.`execute(JDynArray queries, JSelectList selectList)`<br>Execute query using an existing select list as a filter.<br> |
| `JResultSet`<br> | JStatement.`execute(String query, JSelectList selectList)`<br>Execute query using an existing select list as a filter.<br> |
| `JExecuteResults`<br> | JConnection.`execute(String command, JSelectList selectList)`<br>Execute a jBASE command using an existing select list as a filter.<br> |






### Uses of [JSelectList](./../../jselectlist-%28jremote-api%29 "interface in com.jbase.jremote") in [com.jbase.jremote.io](./../../io/com.jbase.jremote.io-%28jremote---api%29)


| Modifier and Type<br> | Class and Description<br> |
| --- | --- |
 Classes in [com.jbase.jremote.io](./../../io/com.jbase.jremote.io-%28jremote---api%29) that implement [JSelectList](./../../jselectlist-%28jremote-api%29 "interface in com.jbase.jremote")  | `class `<br> | `JCursorImpl`<br>A cursor to a jBASE file.<br> |
| `class `<br> | `JSelectListImpl`<br>A select list to a jBASE file.<br> |



| Modifier and Type<br> | Method and Description<br> |
| --- | --- |
 Methods in [com.jbase.jremote.io](./../../io/com.jbase.jremote.io-%28jremote---api%29) that return [JSelectList](./../../jselectlist-%28jremote-api%29 "interface in com.jbase.jremote")  | `JSelectList`<br> | JConnectionImpl.`createSelectList(JDynArray jd)` <br> |
| `JSelectList`<br> | JFileImpl.`select()` <br> |



| Modifier and Type<br> | Method and Description<br> |
| --- | --- |
 Methods in [com.jbase.jremote.io](./../../io/com.jbase.jremote.io-%28jremote---api%29) with parameters of type [JSelectList](./../../jselectlist-%28jremote-api%29 "interface in com.jbase.jremote")  | `JResultSet`<br> | JStatementImpl.`execute(JDynArray queries, JSelectList selectList)` <br> |
| `JResultSet`<br> | JStatementImpl.`execute(String query, JSelectList selectList)` <br> |
| `JExecuteResults`<br> | JConnectionImpl.`execute(String command, JSelectList selectList)` <br> |






### Uses of [JSelectList](./../../jselectlist-%28jremote-api%29 "interface in com.jbase.jremote") in [com.jbase.jremote.jca](./../../jca/com.jbase.jremote.jca-%28jremote---api%29)


| Modifier and Type<br> | Method and Description<br> |
| --- | --- |
 Methods in [com.jbase.jremote.jca](./../../jca/com.jbase.jremote.jca-%28jremote---api%29) that return [JSelectList](./../../jselectlist-%28jremote-api%29 "interface in com.jbase.jremote")  | `JSelectList`<br> | WrappedJConnection.`createSelectList(JDynArray jd)` <br> |
| `JSelectList`<br> | WrappedJFile.`select()` <br> |



| Modifier and Type<br> | Method and Description<br> |
| --- | --- |
 Methods in [com.jbase.jremote.jca](./../../jca/com.jbase.jremote.jca-%28jremote---api%29) with parameters of type [JSelectList](./../../jselectlist-%28jremote-api%29 "interface in com.jbase.jremote")  | `JExecuteResults`<br> | WrappedJConnection.`execute(String command, JSelectList selectList)` <br> |





Back to [jREMOTE API](com_jbase_jremote_package-summary)


