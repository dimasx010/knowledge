#  Text editor VI

Vi is a text editor that is available in all GNU/Linux and most Unix distributions. The Vi editor handles the entire text of a file in memory, and provides many other features that make it one of the most used text editors by administrators. Moreover, in certain emergency situations, this is the only editor available to us.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/a9f49b2f-7890-404f-b3f6-1e4d2a8bf3da">
</p>

## Operating modes in Vi editor

- Command: this is the mode in which you will find the editor every time it starts. This mode accepts commands in the form of letters, moves the cursor, executes text output commands, saves changes or exits the editor, among others.

- Edit or insert text: allows you to add text to the file, i.e. any character you enter will be inserted into the document (with the esc key as an exception).

- Ex or last line: used to write commands in the last line at the end of the screen. It is preceded by : and allows file manipulation.

## Vi text editor commands

Some of the Vi editor commands will be listed below:

### To start in the Vi editor:

- vi: opens the program without any file.
- vi file: edits the file if it exists, and if not, creates it.
- vi file1 file2: edits several files.
    :next or :n to go to the next file.
    prev or :N to go to the previous file.
- vi + [file number] : edit the file starting at the specified line.
- vi+/pattern file: edit the file starting at the first time the pattern is found.

### Other Vi editor commands:

- i to insert text to the left of the cursor.
- a to insert text to the right of the cursor.
- I is for inserting text at the beginning of the line.
- A is for inserting text at the end of the line.
- ESC returns to command mode.
- X is the command that deletes the character under the cursor.
- dd to delete the current line.
- dw deletes the current word.
- h or left arrow will move the cursor to the left.
- j or down arrow will move the cursor to the bottom line.
- k or up arrow will move the cursor to the line above.
- l or right arrow will move the cursor to the right.
- :w saves changes.
- q to exit the editor.

In addition, the command mode contains certain multipliers that allow you to execute a command as many times as indicated in the Vi text editor, for example:

- 5And copies five lines.
- 10dd deletes ten lines.
- 3dw deletes 3 words.
- 8j moves the cursor 8 lines down.

Regarding the cursor movement in the command mode of the Vi text editor, we have:

- Arrows: move in different directions.
- $ : move to the beginning or end of the line.
- G : last line.
- xG : moves the cursor to line x.
- xl : moves the cursor to the x character of 

As for the screen movements, we have in the Vi text editor:

- Ctrl+ f : one screen forward.
- Ctrl+ b : one screen back.
- Ctrl+ d : half screen forward.
- Ctrl+ u : half screen back.

## Referencias
- https://keepcoding.io/blog/como-funciona-el-editor-de-texto-vi/

## Courses
- https://youtu.be/XgQFzi3VkC8
- https://www.udemy.com/course/vim-aumenta-tu-velocidad-de-desarrollo/