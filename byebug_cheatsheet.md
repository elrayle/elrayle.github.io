## Byebug Cheatsheet

This cheatsheet includes most of the byebug commands organized by related commands (e.g. breakpoint related commands are together).

To see official help...

Command              | Aliases          | Example        | Comments
-------              | -------          | -------        | --------
`help`               | `h`              | `h`            | list top level of all commands
`help cmd`           | `h cmd-alias`    | `h n`          | list the details of the `next` command (this works for all commands)

### Stepping through code

Command              | Aliases          | Example        | Comments
-------              | -------          | -------        | --------
`next`               | `n`              | `n`            | step over to next line in same block or method (or back to calling block/method if at end of current block/method)
&nbsp;               |                  | `n 3`          | step over next N lines (e.g. if on line 11, `n 3` will continue and break on line 14)
`step`               | `s`              | `s`            | step into block or method
&nbsp;               |                  | `s 3`          | step in 3 times
`continue`           | `c`              | `c`            | continue execution to next breakpoint (or end of program if no breakpoints reached)
&nbsp;               |                  | `c 43`         | continues and stops at line 43 (stopping at breakpoint if encountered first)
`continue!`          | `c!`             | `c!`           | continue execution to end of program ignoring all breakpoints

### Breakpoint Commands

Command              | Aliases          | Example        | Comments
-------              | -------          | -------        | --------
`info breakpoints`   | `i b`            | `i b`          | Lists breakpoint id, enabled?, and breakpoint line
`break`              | `b`              | `b 33`         | Set breakpoint at specified line (e.g. 33) in the current file
`disable breakpoint` | `dis b`          | `dis b 2`      | Disable breakpoint with id (e.g. 2) (disables all if no id specified)
`enable breakpoint ` | `en b`           | `en b 2`       | Enable breakpoint with id (e.g. 2) (disables all if no id specified)
`delete`             | `del`            | `del 1`        | Deletes breakpoint with id (e.g. 1) (deletes all if no id specified)
`condition`          | `cond`           | `cond 3 i > 3` | Breaks at breakpoint with id (e.g. 3) only if condition is met
&nbsp;               |                  | `cond 3`       | Removes condition from breakpoint with id (e.g. 3)

### Watch Commands

Enabled watch expressions display every time byebug stops.

Command              | Aliases          | Example        | Comments
-------              | -------          | -------        | --------
`info display    `   | `i d`            | `i d`          | Lists display id, enabled?, and expression being watched
`display`            | `disp`           | `disp arg`     | Set expression to watch (e.g. arg) everytime the debugger stops
&nbsp;               |                  | `disp`         | Lists all display expressions with values
`disable display`    | `dis d`          | `dis d 2`      | Disable display with id (e.g. 2) (maybe - disables all if no id specified)
`enable display `    | `en d`           | `en d 2`       | Enable display with id (e.g. 2) (maybe - disables all if no id specified)
`undisplay`          | `undisp`         | `undisp 1`     | Stop displaying expression with id (e.g. 1) (stops displaying all if no id specified)

### Variable values

Command              | Aliases          | Example        | Comments
-------              | -------          | -------        | --------
`var args`           | `v a`            | `v a`          | show arguments and values for current method
`var local`          | `v l`            | `v l`          | show local variable and values for current scope (e.g. scope = method or block)
`var instance`       | `v i`            | `v i`          | show instance variables and values for instance
&nbsp;               |                  | `v i obj`      | show instance variables and values for another object (e.g. obj)
`var const`          | `v c`            | `v c`          | show constants and values for current instance's class
&nbsp;               |                  | `v c klass`    | show constants and values for another module/class (e.g. klass)
`var global`         | `v g`            | `v g`          | show global variables and values
`var all`            | `v all`          | `v all`        | show local, global, and instance variables and values of self

### Tracing and Location

Command              | Aliases          | Example        | Comments
-------              | -------          | -------        | --------
`list=`              | `l=`             | `l=`           | List 5 before and 4 after the current line pending execution (resets to current stop point)
`list`               | `l`              | `l 8-20`       | List specified range of lines (e.g. lines 8-20)
&nbsp;               |                  | `l`            | List next 10 lines from current location listed. (`l` again gives next 10 after that)
`list-`              | `l-`             | `l-`           | List previous 10 lines from current location listed. (`l-` again gives previous 10 before that)
`where` or `backtrace` | `w` or `bt`    | `w`            | display backtrace (`w` and `bt` are the same command)
&nbsp;               |                  | `bt`           | display backtrace


