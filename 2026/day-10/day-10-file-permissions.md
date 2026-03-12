# Task 1: Create Files
* Command : `touch devops.txt` - Creates an empty file
* Command : `echo "this is notes.txt file" > notes.txt` - write content using echo and redirect it to notes.txt through redirection symbol

* Command : `vim script.sh` - Go to insert mode using press `i` , Then write content `echo "Hello DevOps"`, To save file use `Esc:wq and Enter`

# Task 2: Read Files
* Command : `cat notes.txt ` - See content of notes.txt
* Command : `vim script.sh` - See the content of script.sh
* Command : `head -5 /etc/passwd` - Show first five lines
* Command : `tail -5 /etc/passwd` - Show last five lines

# Task 3: Understand Permissions
* `-rw-rw-r-- 1 ubuntu ubuntu  0 Mar 12 02:16 devops.txt` : 664 is current permission
Owner can read, write: Group can also read, write : Others can only read
* `-rw-rw-r-- 1 ubuntu ubuntu 23 Mar 12 02:18 notes.txt` : 664 is current permission
Owner can read, write: Group can also read, write : Others can only read
* `-rw-rw-r-- 1 ubuntu ubuntu 13 Mar 12 02:18 script.sh` : 664 is current permission
 Owner can read, write: Group can also read, write : Others can only read

# Task 4: Modify Permissions
* Command : `chmod +x script.sh` - Using this the script.sh is executable and run by `./script.sh`
* Command : `chmod 444 devops.txt` - Using this the devops.txt can only read by owner , group , others.
* Command : `chmod 640 notes.txt` - Using this the Owner have read , write permission: Group can read : Other don't have any permission.
* Command : `mkdir project && sudo chmod 755 project/` - Using this command create a directory `project` and using `sudo chmod 755 project/` applied permission on project directory.

# Task 5: Test Permissions
1. Try writing to a read-only file - what happens?
* Error : `-bash: devops.txt: Permission denied`
2. Try executing a file without execute permission
* Error : `-bash: ./script.sh: Permission denied`

