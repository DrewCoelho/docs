# PN5_60595

<PageHeader />

## Description

Runtime: Prevent the jShell dot-stacker commands from clashing with user commands

### Previous Release Behavior

The jShell dot-stacker commands would override user commands. For example, if a user had a command called **.DATE** then the jShell would interpret that as a **.D** command and perform the dot-stacker function instead of the user's command.

### Current Release Behavior

The jShell no longer overrides user commands, however if a user command  matches a pattern recognized by the dot-stacker then the user's command  will still be overridden.

Back to [5.6.2 release Notes](./../README.md)
