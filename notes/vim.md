# VIm

- A language that helps us to edit files from terminal.

### Vim Pros

- Edit files on a remote server over ssh.
- Works without a graphical desktop environment.
- Many programming specific features.
- Very fast editing.

### Modes

- Press 'esc': Command mode.
- Press 'CTRL + ]'  to get out of insert mode.
- Press 'CTRL + C'  to get out of insert mode.
- 'i': Insert mode.
- 'o': Insert mode, and new line will be placed after the current line.
- 'O': Insert mode, and new line will be placed above the current line.
- 'A': go into insert mode at the end of the current line.
- 'v': Visual mode.
- 'V': Visual line mode (line select mode).

### Moving around

1. 

    - h - moves left one character.
    - l - moves right one character.
    - j - moves up one line.
    - k - moves down one line.

2. 

    - ```^``` or ```0```  - move to the start of the current line.
    - ```\$``` - move to the end of the current line.
    - ```gg``` - jump to the beginning of the file.
    - ```G``` - jump to the end of the file.

3. 

    - 'f + CHAR` - search forward on the current line to CHAR.
    - 't + CHAR` - search forward on the current line to the character before CHAR.
    - 'F + CHAR` - search backward on the current line to CHAR.
    - 'T + CHAR` - search backward on the current line to the character after CHAR.

4. 

    - 'J' - move the next line to the end of the current line.
    - '` + .' (backtick + dot) - jump to the last edit.


### Delete

- ```x``` - delete the character under the cursor.
- ```dd``` - delete the current line.
- ```d$``` or ```D```- delete from the cursor to the end of the current line.
- ```d0``` or ```d^```- delete from the cursor to the start of the current line.


- When we delete with ```d``` or ```x```, the deleted text gets put in the paste buffer. So we can hit 'p' and the text will get pasted.


### Undo / Redo

- ```u``` - undo
- 'CTRL + R'- Redo.


### Combining Delete + Moving Operations

- ```dG ``` - delete from the current position to the end of the file.
- ```dgg ``` - delete from the current position to the start of the file.
- ```dj ``` - delete the current line and the line below.
- ```dk ``` - delete the current line and the line above.
- ```dl ``` - delete to the left.
- ```dh ``` - delete to the right.
- ```2dd ```, ```3dd ``` etc - delete the next N lines.


### Lookup with regex

- We can look the match with regex, move to the next match with 'n' key, and move to the previous match with 'N' key.
- To look up forwards use '/'.
- To look up backwards use '?'.


### Combining Delete + Matching Operations

- ```d/PATTERN ``` - delete to the next match of PATTERN (does not include the PATTERN).
- ```d?PATTERN ``` - delete to the previous match of PATTERN (does not include the PATTERN).
- ```dn ``` - delete to the next already matched pattern.
- ```dN ``` - delete to the previous already matched pattern.



### Combine with delete operation

- 'df + CHAR' - delete forward on the current line to CHAR.
- 'dt + CHAR' - delete forward on the current line to the character before CHAR.
- 'dF + CHAR' - delete backward on the current line to CHAR.
- 'dT + CHAR' - delete backward on the current line to the character after CHAR.


### Visual select

1. Press 'CTRL + Vv' to go in the visual select mode.
2. Select the text.
3. Once we selected the block, these are the options:

- ```y ``` - 'yank' the text into the paste buffer (copy).
- ```x ``` or ```d``` - delete the selected text.
- ```>> ``` - indent the text right by shiftwidth. presss '.' to indent again.
- ```<< ``` - indent the text left by shiftwidth. presss '.' to indent again.


### 'Copy' / 'Paste'

In 'v' visual mode:

- ```y``` - 'Copy'.
- ```p``` - 'Paste'.


### Indent settings examples

- Set tab to indent 2 spaces instead of 4.
    1. ```vi ~/.vimrc```
    2. ```set expandtab ```
    3. ```set tabstop=2 ```
    4. ```set sw=2 ```

- Autoindent (when we hit 'enter', the next line will be automatically indented)
    - ```set autoindent```





## Vim commands

| Command | Explanation |
|---------|-------------|
| ```:w <file name> ``` | Save everything in a new file.  |
| ```:w ``` | If we already specified  file it is not necessary to add it after ```:w ```. |
| ```:q ``` | Quit / exit. |
| ```:wq ``` | Save and quit. |
| ```:q! ``` | Quit without saving changes. |
| ```:o <file name> ``` | Load file in the Vim. |
| ```:s/<pattern>/<replacing pattern> ``` | It will search only one line and replace the first instance of specified pattern with a new pattern. |
| ```:s/<pattern>/<replacing pattern>/g ``` | It will search only one line and replace all instences of the specified pattern with a new pattern. |
| ```:%s/<pattern>/<replacing pattern>/ ``` | It will search every line and replace the first instence of the specified pattern with a new pattern. |
| ```:%s/<pattern>/<replacing pattern>/g ``` | It will search every line and replace all instences of the specified pattern with a new pattern. |
| ```:'<,'>/    /  /g ``` | Indent by 4 lines (hit space bar four times). |
| ```:r <file name> ``` | Add another file in the current file. |
| ```:r!date ``` | Add date in our file. |
| ```:'<,'>r! wc -l ``` | Run visually selected code. |
