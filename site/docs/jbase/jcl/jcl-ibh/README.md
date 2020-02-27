# JCL IBH

**Created At:** 5/28/2018 10:57:59 AM  
**Updated At:** 6/1/2018 5:35:11 PM  
**Original Doc:** [318689-jcl-ibh](https://docs.jbase.com/45792-jcl/318689-jcl-ibh)  
**Original ID:** 318689  
**Internal:** No  

**Tags:**
<badge text='conversions' vertical='middle' />
<badge text='pointer' vertical='middle' />
<badge text='buffer' vertical='middle' />
<badge text='jcl' vertical='middle' />

## Description 

The command places text in the active input buffer whilst retaining embedded spaces and applying any required input/output conversions. It takes the general form:

```
IBHtext
```

or

```
IBHreference;input-conversion; 
```

or

```
IBHreference:output-conversion:
```



where:

- text is the text to be placed in the active input buffer. Can be a literal (not enclosed in quotes), or a direct or indirect reference to a buffer or select register.
- reference is a direct or indirect reference to a buffer or select register.
- input-conversion is a jQL  input conversion to be applied to the string before putting it in the buffer.
- output-conversion is a jQL  output conversion to be applied to the string before putting it in the buffer.




## Note: 


> The IBH command works in the same way as the IH command except that the string is moved as a single parameter and all spaces are maintained. Depending on the position of the buffer pointer, IBH will either replace an existing parameter or add a new parameter to the end of the input buffer. The rules are as follows:


If the buffer pointer is at the beginning of an existing parameter, that parameter will be replaced with the new string.

If the buffer pointer is within an existing parameter, IBH will concatenate the new string (without inserting a field mark), starting at the current location of the buffer pointer.

If the buffer pointer is at the end of the input buffer, a new parameter will be created and the buffer pointer will be left pointing to the field mark preceding the new parameter.

In all cases, the position of the buffer pointer will remain unchanged. Conversions containing colons or semicolons will not work (for example IBH;G1;1;).



##### EXAMPLE 1


| Command<br> | PIB Before<br> | PIB After<br> |
| --- | --- | --- |
| IBHDEF GHI<br> | ABC^XXX^Z<br> | ABC^DEF GHI^Z<br> |
| <br> | ^<br> | ^<br> |


#####  EXAMPLE 2


| Command<br> | PIB Before<br> | PIB After<br> |
| --- | --- | --- |
| IBH XX<br> | AA^BB^CC^DD<br> | AA^BB^CC^DD^ XX<br> |
| <br> | ^<br> | ^<br> |




##### EXAMPLE 3

File buffer 1 contains:

```
000 Key
001 11350
```


| Command<br> | PIB Before<br> | PIB After<br> |
| --- | --- | --- |
| IBH&1.1:D2:<br> | AA^BB^CC^DD<br> | AA^BB^27 JAN 99^DD<br> |
| <br> |             ^<br> |              ^<br> |




Back to [JCL Commands](./../jcl-commands)
