## Cat
- cat #card
  card-last-score:: 1
  card-repeats:: 1
  card-next-schedule:: 2025-12-23T06:00:00.000Z
  card-last-interval:: -1
  card-ease-factor:: 2.5
  card-last-reviewed:: 2025-12-22T19:17:01.986Z
  collapsed:: true
	- lets you view the contense of one or more files
	- `cat file1 file2 ...`
- Cat can laso make and edit a file with `cat > file1` or add to a file with `cat >> file1`
  id:: 69498726-8df6-4b16-b7c6-753a469f84dc
  collapsed:: true
	- becarful wit h *cat > file1* as it will erase everything in the file before adding new content
- ## Standard input & output (stdin, stdout)
- Streams used for reading and writing data. processing read data from inputstreams and write data fro moutput streams
  collapsed:: true
	- the sorce of an input stream can be a file, device, terminal, or an output stream from another process
- if you enter *cat* byitself you wont see anything becaus there is no output stream
- ## other commands
- **ls** #card
  collapsed:: true
	- lists files and directorys in curent directory
	- -l adds long list alowing you to see extra data
	- -a shows all files including *dotfiles*
- **cp** #card
  collapsed:: true
	- coppies files from one directory to another
- **mv** #card
  collapsed:: true
	- moves files from one directory to anothe
- **touch** #card
  collapsed:: true
	- creates a file if it doesnt already exist, if thet file does exist than it updates the time stamp
- **rm** #card
  collapsed:: true
	- removes a file (Not a directory)
	- #+BEGIN_WARNING
	  *rm* will perminently remove file (not place it in the trash bin)
	  #+END_WARNING
- **echo** #card
  collapsed:: true
	- prints arguments to stdout
	- `echo hello world`
	- `echo $HOME`
- ### navication
- **cd** #card
  collapsed:: true
	- changes the curent directory
- **mkdir** #card
  collapsed:: true
	- makes a directory
- **rmdir** #card
  collapsed:: true
	- removes a directory
	- the dirrectory must be clear for this comand to work
	- use `rm -rf` to remove a dorectory and its contense but be carful
- #### Shell globals #wildCard
- The shell can match patterns to files and directories through *globaling8 denoted by the character \*
	- `echo *` prents everything in the curent directory (just like *ls*)
	- `echo file.*` prints everything in curent directory that starts with "file."
	- `echo *.1` prints everything in the current directory that ends in ".1"
	- `echo "*"` will prent a star, treating it as a string instead of an operator
-