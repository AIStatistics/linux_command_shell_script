## Tips for linux commands and shell scripts

Frequently used linux commands and shell script  **Note:**  MarkDown is done by [stackedit] ([https://stackedit.io/app#](https://stackedit.io/app#))
## Common environment variables

-   **USER**  – your current username.
-   **SHELL**  – the path to the current command shell (for example,  **/bin/bash**).
-   **PWD**  – the current working directory.
-   **HOSTNAME**  – the hostname of the computer.
-   **HOME**  – your home directory.
-   **PS1**  – the default prompt in bash.
-   **TERM**  – the current terminal type (for example,  **xterm**).
-   **DISPLAY**  – the display used by  **X**. This variable is usually set to  **:0.0**, which means the first display on the current computer.
-   **IFS** - Internal/input Field Separator. The _**$IFS**_ variable is often used with bash loops or with the `read` or `printf` builtin commands.

## Script for Parsing command line arguments
Here are the 4 steps to write a [parsing arguments script](parse_command_lines.md)

