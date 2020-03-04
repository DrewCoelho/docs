# PN5_60695

**Created At:** 2/7/2018 8:16:37 AM  
**Updated At:** 2/16/2018 7:11:44 PM  
**Original Doc:** [pn5_60695](https://docs.jbase.com/release-notes/pn5_60695)  
**Original ID:** 298031  
**Internal:** No  


### Description

Telnet: Update terminfo definitions



### Previous Release Behavior

Wyse & ADDS terminfo for Windows were incomplete and contained errors. Some VT100 / VT220 functions were missing. No terminfo for Wyse & ADDS was supplied for Unix. Terminals which use LF for cursor-down were treating LF as CR in the jShell. Terminfo backspace key definition was overridden with ^H in Windows. No way to send terminal initialization string, which can be used to fix the Wyse ambiguity between backspace and cursor-left.



### Current Release Behavior

Modified the **jsh** and **TERM** commands to work nicely with Wyse & ADDS terminals.

Wyse 50, Wyse 60, ADDS Viewpoint, ADDS 4000 terminal definitions now work correctly with jBASE, including jShell cursor movement and command stack. The **TERM** command can be used to initialize the terminal. New terminfo source can be used in Linux/Unix since most lack Wyse/ADDS definitions.
