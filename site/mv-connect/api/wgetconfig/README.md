# WGETCONFIG

<PageHeader />

The WGETCONFIG will retrieve items from the WDB.RESOURCE master config item.

#### COMMAND SYNTAX

```
CALL WGETCONFIG(VALUE,NAME)
```

#### SYNTAX ELEMENTS


| <!----> | <!----> |
| --- | --- |
| Parameter | Description |
| VALUE | The returned value |
| NAME | The name of the config item |


#### EXAMPLE

```
CALL WGETVAR(KEY,"APIKEY")
* Will return 12345
```

#### NOTES

This function is used internally to get config items.  The config file is in WDB.RESOURCE CONFIG.

```
001 C
002 DEFAULT_HANDLER]DBC
003 DEFAULT_RESOURCE]MVDB.MAIN
004 APIKEY]12345
```
