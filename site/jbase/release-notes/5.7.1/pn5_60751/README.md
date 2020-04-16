# PN5_60751

<PageHeader />

## Description

Improve the case insensitivity option for the compiler.

### Previous Release Behavior

Case Insensitivity takes many forms. This change involves the compiler only, more specifically the keywords and variable names.

Previously, the way to obtain case insensitive variables and keywords was to use the (T) option for the BASIC command.

With jBASE 5.7 there were a number of new ways of achieving case insensitivity

- Use the .jabba extension to show the compiler this was jabbascript source code. jabbascript source code is by default case insensitive.
- Use the statement "$option nocase" at the start of the source code.
- Use the environment variable "export JBC\_JPP2=nocase"

### Current Release Behavior

This change introduces another option to add case insensitivity:

```
compiler_case_insensitive_variables_keywords = true
```

With this set, then by default all compilations will be done case insensitive.

Back to [5.7.1 Release Notes](./../README.md)

  
<PageFooter />
