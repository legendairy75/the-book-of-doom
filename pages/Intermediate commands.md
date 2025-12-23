- Common comands that are a but advances
- ## grep  #card
	- prints the line from a file or input stream that matches an expression
	- `grep Hello file.1`
		- *-i* for case insinsative matching
		- *-v* for inverted matching
	- grep also understands #wildCard
- ## less #card
	- command to see contence of file if file is big, alowing you to scroll through
	- if you cant use *less* try *more*
- ## pwd #card
	- prents working directory
- ## diff #card
	- shows difference between 2 text files
	- `diff file1 file2`
- ## file
	- command that allows the system to try and guess the file type
- ## find & locate #note
	- if you know theres a file in a directory but cant find it use *find*
	- *locate* does the same thing as find exept it looks at a document that is periodicaly updated and may not have the file yourt looking fore
	- |find|locate|
	  :LOGBOOK:
	  CLOCK: [2025-12-22 Mon 22:20:59]
	  :END:
	  |---|---|
	  |use when locate doesnt work|use first for speed|
- ## head & tail
	- *head* prints the first 10 lines of a file
	- *tail* prints the last 10 lines of a file
- ## sort
	- sorts lines in a file alphanumericaly
- ## Changing password
- you can change your password with the `passwd` command
- ## env & shell vaariables
- the shell can store temperary variables valled *shell variables* containing strings
- ### Shell variables
	- usfull for keeping track of values inscripts
	- assign a variable with `STUFF=blah`
		- #+BEGIN_WARNING
		  Donot add space before or after the '='
		  #+END_WARNING
- ### Env variable
	- like a shel variable but  alows other programs to access it
	- all processes on Unix systems have env variable storage
	- assign an env variable with `export STUFF`
- ## Path
- A special envierment variable that contains the *command path* (*path*) which are a list of directories  the shell searches when you are trying to locate a command
- to tell the shell to look in a dirrectory before the PATH
	- `PATH=dir:$PATH`
- to tell the shell to look in a directory last
	- `PATH=$PATH:dir`
- ## Special characters
- |character|name|use|
  |---|---|---|
  |*|star, asterisk|Regular expression, glob char|
  |.|dot|Current directory, file|
  |!|bang|Negateion, command history|
  |\||Pipe|command pipe|
- ## Command line editing
- |key|action|
- ## Text editors
- ### nano
	- basic terminal editor
- ### vim (vi)
	- advanced terminal editor
- ### emacs
	- gui test editor
- ### vscode
	- easier gui text editor
- ## Get help
- Linux comes with a  wealth of documentation, for commands you can try the manual pages `man ls`
- you can also search for a man page with keywords using `-k` flag
	- you will need to load the index  for keywords to work `sudo mandb`
- ### sections
- |section|desc|
- `man 5 passwd` gose to sectioin 5 of the passwd man page
- modern linux systems also hav *info* command
	- like *man* info has the informantion you may need and often more than man
- you can also try the --help (-h) flag after a command, this will give you a description and maybey flag info `ls --help`
- theres also tldr, a shorter version of --help