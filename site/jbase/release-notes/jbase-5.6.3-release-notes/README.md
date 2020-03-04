# jBASE 5.6.3 RELEASE NOTES

**Created At:** 7/13/2017 8:18:15 AM  
**Updated At:** 3/11/2019 12:46:35 PM  
**Original Doc:** [jbase-563-release-notes](https://docs.jbase.com/release-notes/jbase-563-release-notes)  
**Original ID:** 263191  
**Internal:** No  


# Patches

- [PN5\_60581](./../5.6.2-release-notes/pn5_60581) - Allow "!" to execute Operating System (OS) commands in Procs and Paragraphs
- [PN5\_60582](./../5.6.2-release-notes/pn5_60582) - New environment variable to configure the jShell command stack history and/or specify a username based stack
- [PN5\_60583](./../5.6.2-release-notes/pn5_60583) - Allow attribute 1 in F-pointers and PQ/PQN/PA/PR items to be caseless
- [PN5\_60584](./../5.6.2-release-notes/pn5_60584) - jQL: Allow [Ann] style default dictionaries for d3 emulation
- [PN5\_60586](./../5.6.2-release-notes/pn5_60586) - jQL: Process malformed A-correlatives with missing semi-colons
- [PN5\_60587](./../5.6.2-release-notes/pn5_60587) - jQL: Prevent hidden columns from corrupting totals of other columns
- [PN5\_60589](./../5.6.2-release-notes/pn5_60589) - Case Independence: jQL and Secondary Index issue
- [PN5\_60591](./../5.6.2-release-notes/pn5_60591) - jQL: Issue with A/F correlative using Repeat function
- [PN5\_60592](./../5.6.2-release-notes/pn5_60592)- A jQL statement with more that 3 BREAK-ONs corrupts totals
- [PN5\_60593](./../5.6.2-release-notes/pn5_60593) - jBC: D3 style input timeout
- [PN5\_60594](./../5.6.2-release-notes/pn5_60594) - jBC: Map SYSTEM() functions for D3 compatibility
- [PN5\_60595](./../5.6.2-release-notes/pn5_60595) - Prevent the jShell dot-stacker commands from clashing with user commands
- [PN5\_60597](./../5.6.2-release-notes/pn5_60597) - Spooler enhancement to be able to assign the port number range for **jlp** print processes
- [PN5\_60598](./../5.6.2-release-notes/pn5_60598) - File cache not getting rebuilt when changing directories
- [PN5\_60599](./../5.6.2-release-notes/pn5_60599) - Add support for large records when using ACCOUNT-SAVE and ACCOUNT-RESTORE commands
- [PN5\_60600](./../5.6.2-release-notes/pn5_60600) - Remove 'root' requirement from the jInstallKey command
- [PN5\_60601](./../5.6.2-release-notes/pn5_60601)- Unable to add or update multisession or websession evaluation licenses with the jLicenseUpgrade command
- [PN5\_60602](./../5.6.2-release-notes/pn5_60602) - jInstallKey incapable of stacking multiple licenses
- [PN5\_60603](./../5.6.2-release-notes/pn5_60603) - Make jPlus the default file type when creating files
- [PN5\_60604](./../5.6.2-release-notes/pn5_60604) - Allow compiler directives to be used as variables
- [PN5\_60605](./../5.6.2-release-notes/pn5_60605) - jBASE **who** command conflict with Unix/Linux **who**
- [PN5\_60606](./../5.6.2-release-notes/pn5_60606) - Allow AND-LISTS, OR-LISTS, XOR-LISTS to accept 1 list
- [PN5\_60607](./../5.6.2-release-notes/pn5_60607) - Implement D3 style list processing commands
- [PN5\_60608](./../5.6.2-release-notes/pn5_60608) - Fix a performance issue with the LOCKED clause
- [PN5\_60609](./../5.6.2-release-notes/pn5_60609) - Correct the behavior of SYSTEM(0) for D3 emulation
- [PN5\_60613](./../5.6.2-release-notes/pn5_60613) - Case Independence: Code formatter not handling certain variables correctly
- [PN5\_60614](./../5.6.2-release-notes/pn5_60614) - Improve the case insensitive handling of subroutine calls
- [PN5\_60615](./../5.6.2-release-notes/pn5_60615) - jBC: Parenthetical expressions misinterpreted as DIMensioned arrays instead of format strings
- [PN5\_60617](./../5.6.2-release-notes/pn5_60617) - Casing issue with IF statement in combination with the LOCATE() function
- [PN5\_60618](./../5.6.2-release-notes/pn5_60618) - PortBas issue - Reserved words following a ";" ignored
- [PN5\_60619](./../5.6.2-release-notes/pn5_60619) - jbase\_agent accepts invalid port ranges, less than 1025 and greater than 65535
- [PN5\_60620](./../5.6.2-release-notes/pn5_60620) - Add option to jFormatCode to allow DIMensioned arrays to be treated like dynamic arrays
- [PN5\_60621](./../5.6.2-release-notes/pn5_60621) - jFormateCode to move semi-colon separated INCLUDEs to a dedicated lines
- [PN5\_60622](./../5.6.2-release-notes/pn5_60622) - jFormatCode to parse out expressions that are used in the LOCATE statement and LOCATE() function
- [PN5\_60623](./../5.6.2-release-notes/pn5_60623) - Enhancement to make "N" a synonym of "PA" in Paragraphs
- [PN5\_60624](./../5.6.2-release-notes/pn5_60624) - jQL: Date and Time conversion codes are not case insensitive
- [PN5\_60625](./../5.6.2-release-notes/pn5_60625) - Active select-list not retained after invoking SPOOLER() function
- [PN5\_60626](./../5.6.2-release-notes/pn5_60626) - Lift 2gb limit on index files
- [PN5\_60627](./../5.6.2-release-notes/pn5_60627) - Allow the jsh prompt to be configured via an environment variable
- [PN5\_60628](./../5.6.2-release-notes/pn5_60628) - jQL: Incorrect output from mismatched multi-values using the Repeat function
- [PN5\_60629](./../5.6.2-release-notes/pn5_60629) - ICONV doesn't strip leading zeros when the number to be converted is a string
- [PN5\_60630](./../5.6.2-release-notes/pn5_60630) - Minor issues with the new **JPP2** pre-compiler
- [PN5\_60631](./../5.6.2-release-notes/pn5_60631) - Case Independence: Correct a number of functions that failed if an argument was not a string
- [PN5\_60632](./../5.6.2-release-notes/pn5_60632) - Reduce default spooler sleep time
- [PN5\_60633](./../5.6.2-release-notes/pn5_60633) - A program could go into a CPU loop on Linux/Unix system if a **/** (forward slash) was present in the file name
- [PN5\_60634](./../5.6.2-release-notes/pn5_60634) - Distributed files give a "DISTRIB: Reentrant call to Jedi Distributed file driver" message.
- [PN5\_60635](./../5.6.2-release-notes/pn5_60635) - jQL not processing sub-values in calculations
- [PN5\_60636](./../5.6.2-release-notes/pn5_60636) - jBC: Record locking not case insensitive
- [PN5\_60637](./../5.6.2-release-notes/pn5_60637) - Locks would remain after a file is closed
- [PN5\_60638](./../5.6.2-release-notes/pn5_60638)- The **jrf** command leaves temporary index file in directory
- [PN5\_60640](./../5.6.2-release-notes/pn5_60640) - jQL not processing multi-values
- [PN5\_60642](./../5.6.2-release-notes/pn5_60642) - Don't stack the command that initiates the dot-stacker
- [PN5\_60643](./../5.6.2-release-notes/pn5_60643) - jQL: Incorrect BREAK-ON totals and formatting at major break levels
- [PN5\_60644](./../5.6.2-release-notes/pn5_60644) - Add a new file type **JBC** to the **CREATE-FILE** command
- [PN5\_60645](./../5.6.2-release-notes/pn5_60645) - New command **viewindex** to view a jBASE Secondary Index
- [PN5\_60646](./../5.6.2-release-notes/pn5_60646)  - jQL not correctly processing statements using both FMT and CONV
- [PN5\_60647](./../5.6.2-release-notes/pn5_60647) - SP-ASSIGN resets list pointer
- [PN5\_60648](./../pn5_60648) - Stale header data in JP files (Error number 2017)


# New Commands

- viewindex (see patch [PN5\_60545](./../5.6.2-release-notes/pn5_60545))




# New jBC Statements

- 


# New Modules

- [PN5\_60627](./../5.6.2-release-notes/pn5_60627)


# Changes to Current Behavior

- The **U** option of the **jchmod** command has been deprecated. Case insensitive files must be created with **CREATE-FILE** command, e.g. **CREATE-FILE BOOKS 11 101 CASE=FALSE**
- Default spooler sleep time reduced to 5 seconds, was 30 seconds (see patch [PN5\_60632](./../5.6.2-release-notes/pn5_60632))


# Changes to Commands

- New JBC file type added to the CREATE-FILE command (see patch [PN5\_60644](./../5.6.2-release-notes/pn5_60644))


# Changes to jBC 

- 


# Statements/Functions

- 


# Additional Notes

- [jBASE 5.6 Manual](./../jbase-5.6-manual)
- To obtain an evaluation version of jBASE, please email [multivalue@zumasys.com.](mailto:multivalue@zumasys.com.%3C/p%3E)



