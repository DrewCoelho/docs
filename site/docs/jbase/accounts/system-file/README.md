# System File

**Created At:** 5/22/2018 9:52:58 PM  
**Updated At:** 10/31/2018 7:48:09 AM  
**Original Doc:** [317964-system-file](https://docs.jbase.com/41717-environment-variables/317964-system-file)  
**Original ID:** 317964  
**Internal:** No  


## Description 

The location of the jBASE SYSTEM file is determined by the [JEDIFILENAME\_SYSTEM](./../jedifilename_system) environment variable. The environment variable is usually setup when the user logs on. By default, jBASE uses a hash file named SYSTEM, in a subdirectory named src, in the jBASE release directory as defined by the environment variable [JBCRELEASEDIR](./../jbcreleasedir).

Use of the SYSTEM file also depends upon the setting of the environment or registry variable JEDIFILENAME\_MD, which describes the users MD/VOC file. This environment variable should be set to the users required MD file. e.g. To use an MD file in the users home directory set the environment variable, [JEDIFILENAME\_MD](./../jedifilename_md) to $HOME/MD or %HOME%\MD.

In its minimum form, a record in the SYSTEM file must contain two fields. Field 1<br>contains the character "D" to specify a local account, and field 2 contains the<br>absolute path of the account directory. For example:

```
ACCOUNTX
001 D
002 C:\users\accountx or /accounts/accountx
```



Fields 7 and 20 through 37, of the SYSTEM record, are used by the jBASE LOGTO and PASSWORD commands.<br>All other fields are reserved. The full format of a SYSTEM record is as follows<br>and will be described in subsequent sections on this page:

```
ID:  AccountName
001 Type
002 Absolute Account Path
003 Reserved
004 Reserved
005 Reserved
006 Reserved
007 Encrypted Password (optional)
008 Reserved
009 Reserved
010 Reserved
011 - 019 Reserved
020 ESYSTEM_START
021 JBCEMULATE
022 HOME
023 JBCDEV_BIN
024 JBCDEV_LIB
025 PATH
026 JBCOBJECTLIST
027 JEDIFILEPATH
028 JEDIFILENAME_MD
029 JBC_TCLRESTART
030 JBC_ENDRESTART
031 JBCRESTARTPROG
032 JBCLOGINPROG
033 Reserved
034 JBASE_I18N
035 JBCPORTNO (multi-valued range)
036 OTHER ENVIRONMENT VARIABLES (multi-valued)
037 ESYSTEM_END
```

### 


### ENCRYPTED PASSWORD (Field 7)

This optional field should only be maintained through the jBASE PASSWORD command. The PASSWORD command prompts for an Account Name which must be a valid entry in the SYSTEM file (i.e. the file defined by the [JEDIFILENAME\_SYSTEM](./../jedifilename_system) environment variable). The password must be entered twice for verification that it was entered correctly. Be aware that entry of this password is case sensitive (e.g. "MyPassword" is different than "mypassword").



### 

## Extended System File Values  

The SYSTEM File of jBASE 4 and jBASE 5 has 16 new attributes that are used to define<br>the assignment of environment variables in the LOGTO process. These values are<br>stored in attributes 21 through 36 and are encapsulated by attribute 20, "ESYSTEM\_START",<br>and attribute 37, "ESYSTEM\_END".



```
020 ESYSTEM_START
021 JBCEMULATE
022 HOME
023 JBCDEV_BIN
024 JBCDEV_LIB
025 PATH
026 JBCOBJECTLIST
027 JEDIFILEPATH
028 JEDIFILENAME_MD
029 JBC_TCLRESTART
030 JBC_ENDRESTART
031 JBCRESTARTPROG
032 JBCLOGINPROG
033 JBCLOGNAME
034 JBASE_I18N
035 JBCPORTNO (multi-valued range)
036 Other Environment Variables (multi-valued)
037 ESYSTEM_END
 
```

For attributes 21 - 35 simply specify the value.
For attribute 36 specify: env\_var1=valueX]env\_var2=valueY]...       ] = value mark

In most cases, if a value is not included then the environment variable will<br>remain the same as it was prior to the LOGTO. However, it is best to assign<br>values explicitly rather than relying on this behavior.

An example of use is as:

```

001 D
002 C:\accounts\payables
003
004
005
006
007
008
009
010
011
012
013
014
015
016
017
018
019
020 ESYSTEM_START
021 jbase
022 C:\accounts\payables
023 C:\accounts\payables\bin
024 C:\accounts\payables\lib
025 C:\accounts\payables\bin;%PATH%
026 C:\accounts\payables\lib
027 C:\accounts\payables;C:\globals
028 C:\globals\MD]D
029
030
031
032
033
034
035
036 JBCNETDIR=C:\globals\jrfs]JBCNETACCESS=C:\globals\jrfs\netaccess
037 ESYSTEM_END
```



## Note: 


> The Extended SYSTEM File values (ESYSTEM\_START+1 thru ESYSTEM\_START+15) are<br>held internally within the jBASE process. These settings are NOT passed to the<br>Operating System where 'expansion' is performed. In order to set environment<br>variables containing references passed to the Operating System for 'expansion',<br>use ESYSTEM\_START+16.
> 
> Environment variables set in ESYSTEM\_START+16 override any corresponding values set in ESYSTEM\_START+1 thru ESYSTEM\_START+15.
> 
> Certain environment variables are controlled by LOGTO (e.g. HOME) and should not be assigned in ESYSTEM\_START+16.




Back to [Environment Variables](./../../migration-station/articles/environment-variables)
