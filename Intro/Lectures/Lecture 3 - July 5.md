# Commands - sort and uniq

`sort file.txt`
shows contents of file.txt sorted alphabetically

`uniq --help`
help of `uniq` command

`sort file.txt | uniq`
sorts contents of file.txt and shows each entry once

`sort file.txt | uniq -c`
same as `sort file.txt | uniq`, but shows counts in front of each lines

`sort file.txt | uniq -d`
shows only the entries that are not unique

# Vim

`sudo apt-get install vim`
to install vim

Vim has 2 modes - shell and insert.
Pressing `esc` gets to shell mode, pressing `i` in shell mode gets you to insert mode. `d` is for delete.
:q - quit
:w - write
:wq - write and quit. There is also a shortcut for this command: `shift+zz`

`dd` (in shell mode) - delete the whole line
`shift+s` - empty the line (leaves the line but deletes the content of the line)
`shift+a` - append to the line, also enters to insert mode
`:set number` - show line numbers
`:1,4` - delete lines 1 through 4 (can be any numbers, this is for example)
`:/bye` - find the word "bye" in the text, press `n` to go to next found entry

# sed command
`sed` command is like `awk` and `cut`, but it also lets you to modify the contents.

`sed 's/ls/ll/g' file.txt`
replaces in `file.txt` all occurrences of `ls` with `ll`
`s` - starting line
`g` - globally

`sed 'cut/d' file.txt`
delete all occurrences of `cut`

`sed -i '/^$/d' file.txt`
deletes all the empty lines
explanation: if the beginning of line (`^`) is empty (`$`), then delete
`$` also means argument
`-i` in this command means execute the command in insert mode

`sed -i '$d' file.txt`
deletes the last line

`sed -i '1d' file.txt`
deletes the first line

`sed -i '4d' file.txt`
deletes the 4th line

`sed -i '1-4d' file.txt`
deletes lines 1-4

# sed command examples by Sergey

`sed 's/ls/ll/g' history #change ls to ll`
`sed -i 's/ls/ll/g' history #the same but change in file`
`sed 's/ls//g' history #change ls to empty`
`sed '/cat/d' history #delete match`
`sed -i '/^$/d' history #remove empty lines`
`sed '$d' history #remove last line from file`
`sed '1d' history #remove first line`
`sed '1,2d' history #remove fist 2 lines`
`sed 's/\t// /g' history # remove tabs to space`
`sed -n 7,9p history #show only lines 7-9`
`sed 7,9p history # show all lines besides 7-9`
`sed G history #put empty lines after string`
`sed '8!s/ls/ll/' history # change everything besides line 8`

# dmidecode command

`dmidecode` command shows the hardware information

# vim

[https://openvim.com/](https://openvim.com/)
[https://vim-adventures.com/](https://vim-adventures.com/) - vim game

`shift+zz` save and exit
`U` - undo
`R` - replace
`O` - new line

