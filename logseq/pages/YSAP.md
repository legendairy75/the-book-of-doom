## terminal
collapsed:: true
	- `echo [arg]` #card
	  card-last-interval:: -1
	  card-repeats:: 0
	  card-ease-factor:: 2.5
	  card-next-schedule:: nil
	  card-last-reviewed:: nil
	  card-last-score:: nil
		- prints argument
	- Terminal exhists in a directory
	- `pwd` #card
	  card-last-interval:: -1
	  card-repeats:: 1
	  card-ease-factor:: 2.5
	  card-next-schedule:: 2026-04-08T05:00:00.000Z
	  card-last-reviewed:: 2026-04-07T16:33:07.877Z
	  card-last-score:: 1
		- **prints** the **working directory**
	- `ls` #card
		- **lists** the content of the directory
	- `touch [file]` #card
		- creates a new file
	- `rm [file]` #card
		- **removes** file
	- `cd  [dir]` #card
		- **changes** the **directory**
- ## file menipulation
	- `mv [file]` #card
		- **moves** a file and can rename it
	- `*` is a wiled card meaning it denotes anything
		- `rm file.*` will remove any file starting with *file.*
	- `rm -i`  makes `rm` interactive
		- will ask if you want to remove file (y/n)
	- ### navigation
		- up arrow goes up in history
		- down arrow goes down in history
		- Ctl + l exicutes the `clear` command
			- `clear` clears terminal window
	- `alias` #card
		- combines commands and flags togeather
		- `alias rm='rm -i'` will make rm run rm -i when executed
		- find an *alias* with `alias [cmd]` to see what the alias does
	- `history` prints the command history
- ## hidden files
  collapsed:: true
	- a file prefixed with a '.' is considered hiden
	- running `touch .file1` and the n running `ls` will not print *.file1*
	- to print *.file1* run `ls -a` (list including hidden files)
	- `./` is the current directory
	- `../` is the parent directory
	- `cd -` will change to the previous directory
- ## searching in files
  collapsed:: true
	- `cat [file]` will print content of a file
	- `grep [pattern] [file]` will search a file for a pattern
		- `grep dave /usr/share/dict/words`
		- quotes ' stop bash from interperating special characters
			- `grep '^dave' ...`
		- *^* matchesd the begining of a line
		- *$* matches the end of a line
	- *>* will redirect the output of a command to a file
		- it will also override the files conternt
	- *>>* will append the output of a command to a file
	- `grep -A[n] ...` prints patern and *n* lines after
	- `grep -B[n] ...` prints pattern and *n* lines before
	- `grep -C[n] ...` prints pattern and *n* lines around (context)
	- `grep -i ...` case insinsative
	- `grep -o ...` **ONlY**what you explisitly put for the pattern
	- ### Combine flags
		- instead of `grep -i -o` use ` grep -io`
	- *|* pipe
		- `cmd1|cmd2` takes the out put of cmd1 and pipes it to the input of cmd2
- ## paging files
  collapsed:: true
	- `less [ file]` like cat excepta a pager where you can scroll through the content of the file
	- up arrow to  go up a line and down arrow to go down a line
	- q to quit
	- */* will search the content
		- *n* to go to next result
		- *shift + n* to go to last result
- ## man pages
  collapsed:: true
	- `man [cmd]` is a command  to view ther manual for cmd (oppens in less)
	- `man [n] [cmd]` goes to n section of cmd
	- to get man pages of bash builtins use `help [cmd]`
	- `which [cmd]` prints the location of cmd (external)
	- `type [cmd]` prints what type comand is (alias, exicutable)
	- `type -a` prints all locations of command
	- `compgen -b` prints all bash builtin commands
- ## programs & commands
	- `file [file]` tells you what type of file *file* is
	- *PATH* is a variable list of directories
		- to check PATH run `echo $PATH`
		- Variables must have *$* prefixed to thjem for bash to know its a variable`
	- `tr [old-char] [new-char]` translates old character to new character
		- `tr : '\n'` turns all *:* input to *'\n'* input
- ## Variables
  collapsed:: true
	- *USER* is a variable for the current user
	- `whoami` is a command that effectvly does the same as `echo $USER`
	- *SHELL* is a variable for the current shell
	- *HOSTNAME* is a variable for the machines name
	- make a variable with `x=[var]`
		- `name=bob`
	- You should **usually** quote variables to prevent word splitting and globbing
		- ~~`echo $name`~~  `echo "$name"`
	- `unset [x]` unsets the variable
	- `uname` prints system information
	- `uname -a` prints all system information
	- to make a variable an exicutable `x=$(cmd)`
		- thing=$(uname -a)
- ## vim
  collapsed:: true
	- *vim* (Visualy improved Editor)
	- navigate
	- |key | function|
	  |---|---|
	  |navigate|
	  |h | left|
	  |j | down|
	  |k | up|
	  |l | right|
	  |---|---|
	  |a | append **after** cursor|
	  |i | insert **before** cursor|
	  |esc | back to normal mode|
	  |:w| write to file (save)|
	  |:q| quit editor|
	  |dd| delete line|
	  |.| repeat last command|
	  |p | paste |
	  |o | open new line below curesr|
	  |Shft + o| open line above curesr|
	- `bat` *cat* but better
- ## file permisions
  collapsed:: true
	- `ls -l` long list files, lists permissions, user, group
	- `chmod` changes permmision of file
		- `chmod +x [file]` make a file exicutable
	- add `#!/usr/bin/env bash` or `#!/bin/bash` to the beginning of a file so the system knows to use bash
	- *.sh* is not required for a bash script
- ## Scripting
	- `rm*` removes all files in a directory