Here is a [vim cheatsheet] (https://www.worldtimzone.com/res/vi.html) 
## Cursor movement

-   h - move left
-   j - move down
-   k - move up
-   l - move right
-   w - jump by start of words (punctuation considered words)
-   W - jump by words (spaces separate words)
-   e - jump to end of words (punctuation considered words)
-   E - jump to end of words (no punctuation)
-   b - jump backward by words (punctuation considered words)
-   B - jump backward by words (no punctuation)
-   0 - (zero) start of line
-   ^ - first non-blank character of line
-   $ - end of line
-   G - Go To command (prefix with number - 5G goes to line 5)
**Note:** Prefix a cursor movement command with a number to repeat it. For example, 4j moves down 4 lines.
 ## Insert Mode - Inserting/Appending text

-   i - start insert mode at cursor
-   I - insert at the beginning of the line
-   a - append after the cursor
-   A - append at the end of the line
-   o - open (append) blank line below current line (no need to press return)
-   O - open blank line above current line
-   ea - append at end of word
-   Esc - exit insert mode
-  u - undo
## Cut and Paste

-   yy - yank (copy) a line
-   2yy - yank 2 lines
-   yw - yank word
-   y$ - yank to end of line
-   p - put (paste) the clipboard after cursor
-   P - put (paste) before cursor
-   dd - delete (cut) a line
-   dw - delete (cut) the current word
-   x - delete (cut) current character
## Search/Replace

-   /_pattern_  - search for pattern
-   ?_pattern_  - search backward for pattern
-   n - repeat search in same direction
-   N - repeat search in opposite direction
-   :%s/_old_/_new_/g - replace all  _old_  with  _new_  throughout file
-   :%s/_old_/_new_/gc - replace all  _old_  with  _new_  throughout file with confirmations
## Exiting

-   :w - write (save) the file, but don't exit
-   :wq - write (save) and quit
-   :q - quit (fails if anything has changed)
-   :q! - quit and throw away changes
