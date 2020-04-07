# WDB.RESOURCE

<PageHeader />

## WDB.RESOURCE record layout

| Attribute  | Description  |
| --- | --- |
| 001 | resource type - this should be 'P' |
| 002 | description of the resource / service |
| 003 | name of program to execute to handle the request |
| 004 | reserved |
| 005 | set to 1 to parse CGI variables before executing handler program |
| 006 | set to 1 to enable this resource, 0 to disable |
| 007 | set to 1 to save request debug information for use with WDEBUG debugging tool, 0 to disable debug info |

[Back to jAgent APIs](./../README.md)
