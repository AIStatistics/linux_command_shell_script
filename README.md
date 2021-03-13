
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
## Parsing command line arguments
you can follow the 4 steps to write a [parsing arguments script](parse_command_lines.md)

## Linux commands
- **echo** -Input a line of text with env variables, and display on standard output. The ‘**-e**‘ option with echo  acts as interpretation of escaped characters that are backslashed.
-- Example 1: Using option ‘**\b**‘ – backspace with backslash interpretor  ‘**-e**‘ which removes all the spaces in between.
```
$ echo -e "Spaces \bbtween \bwords \bare \removed" 

Spacesbetweenwordsremoved
```
-- Example 2: redirect and output to a file and not standard output.
```
$ echo "Test Page" > testpage

