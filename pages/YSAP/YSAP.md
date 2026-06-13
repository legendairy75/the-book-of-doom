---
date: 6/1/26
---

## Terminal
The terminal is arguably the most importance part of working with bash and such requires a few commands to memorize
`echo [arg]` 
	echo prints the argument to stdout. If you entered:
	`echo hello`
	bash would print:
	`hello`
`pwd` 
	**prints** the current **working directory**. If you were in /usr/share/dict, *pwd* would print `/usr/share/dict`
	if you were in your home directory and your user was named bob *pwd* wpuld print `/home/bob`
`ls`
	**lists** the *content* of a directory
`touch [file]`
	mainly used to *create* a file
`rm [file]`
	**removes** a file. 
>[!warning]- `rm` will **permenently** remove a file from your computer.

`cd [dir]`
	**changes** the current **directory**

>[!note]- The current shell environment exists **within a directory** at all times

## File Manipulation
`mv [file]`
	**Moves** a file to a different directory and can rename a file
`*` is the wildcard operator meaning it denotes anything
	`rm file.*` will remove all files in the current directory that start with 'file.'
`rm -i` makes *rm* interactive allowing you to say yes or no to removing a file before hand
### Navigation
| key        | function                     |
| ---------- | ---------------------------- |
| up arrow   | goes up in history           |
| down arrow | goes down in history         |
| Ctrl + i   | exicutes the *clear* command |
`clear` **clears** the terminal window

