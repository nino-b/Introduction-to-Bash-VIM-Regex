#### Manual
- '*' Each line marked with this symbol contains information about the same subject, even though it appears on different rows in the table for visual purposes
- '**' just to differentiate subjects if one of them is written right after another.
- '!->' some trick.
- '!!!' Use with caution!

### Commands

| Command | Explanation| Example| Example explanation |
|---------|------------|--------|---------------------|
| ```echo $SHELL``` |  |        |                     |
| * ```ls ``` | Expects locations we want to list |
| *```ls /``` | Lists all of the files in the root directory |
| * ```ls -1 ``` | Lists files and directories in a single column format with one entry per line. |  
| ```pwd ``` | Tells where we are in the system |  
| ```cd ``` | change directory |  
| * ```alias ``` | Run code in a custom way |
| *``` alias ls='ls -1' ``` | Every time when we use ```ls``` it should give ```ls -1``` output. |
| * ```vi ~/.bashrc ``` | We can set up aliases in this file |  
| ```. ``` | The current directory. |  
| ```.. ``` | The parent directory. |  
| ```../.. ``` | Skip up 2 directories (parents parent). |  
| ```~ ``` | Our home directory. |
| ```cd ~ ``` | Navigate to home directory. |
| ```v1 ~/<full path to the file> ``` | If we want to edit a file without having to ```cd``` into this file |  
| ** ```cat ``` | Display contents of the file |
| ** !-> ```reset``` | If we accidentally ```cat``` out JPEG or PNG files and possibly get stuck, write ```reset``` even if we can't see the writing itself! |
| **```cat <file-1> <file-2>  ``` | Concatenates those files. We can pass as any files as we want. |  
| ```CTRL+D ``` | Exit from the program |  
| ```CTRL+C ``` | Exit from the program |  
| ```cp <source file (copy from)><another source file, if we need> <file where to paste into / or directory path> ``` | copy a file (or multiple files). If we specify new file name, it will create that file and paste there. If we don't specify the file name but specify the directory name, in this directory it will create a new file which will have the name as the name of the file from where we copied the information. |  
| ```cp -r <source directory> <new directory name> ``` | Recursively copy the entire structure of a directory into another place. If we have a directory full of fils and directories and want to copy into another place. |  
| !!! ```rm -rf <directory name> ``` | recursively forcefully remove directories and their contents. Use it carefully. We might delete important files forever!!! |  
| !!! ```rm -r <file name> ``` | Remove / Delete files recursively. Use it carefully. We might delete important files forever!!! |  
| ```rm <file name> ``` | Remove / Delete file |  
| !!! ```mv <source file> <destination / new name> ``` | Rename or move files and directories |  
| * ```mkdir ``` | create a directory. |
| * ``` mkdir a/b/c/d``` | This won't work, instead use ```mkdir -p a/b/c/d``` |
| * ```mkdir -p ``` | If that directory already exists, use it, else create a directory. |  
| ```rmdir ``` | remove an empty directory. |  
| ```gunzip <filename.gz> ``` | Decompress Gzipped file. |  
| * ```* ``` | A wild card |
| *  ```cat b*p.txt ``` | ```cat``` out everything that starts with 'b', has anything in the middle, ends with the 'p' and has .txt format. |
| ```wc <file name> ``` | Computes the number of lines, words and bytes in a file. |  
| ```wc ``` | It will wait for us to write words. When we finish writing, we should press 'CTRL + D', we will return to command line and we will get ```wc``` result. |
| ```wc -l ``` | number of lines. |  
| ```wc -c ``` | number of characters. |  
| ```wc -w ``` | number of words. |
| ```head <file name> ``` | Will print out 10 lines. |
| ```head -n <number> <file name> ``` | Will print out <number> amount of lines. |
| ```head --lines=<number> <file name> ``` | Will print out <number> amount of lines. |
| ```echo <some input> ``` | will print out the ```<input>``` |
| ```echo <input> > <file name>``` | will redirect the ```<input>``` in the specified file and overwrites the file's content. We can check out the input with: ```cat <file name>```. |
| ```echo <input> >> <file name> ``` | Will append the ```<input>``` at the end of the file. Input can be anything: ```ls / >> list.txt```. |
| ```< ``` | Read files into the stdin of a program. |
| ```> ``` | Redirect the input. |
| ```>> ``` | append the input at the end of a file. |
| ```wc -c < <file name> ``` | Read a file from stdin and count number of characters. |
| ```\| ``` | Takes output (stdout) and copies it into the standard input of a second program. |
| ```ls -1 \| wc -l ``` | Number of files in the current directory. |
| ```ls -1 *.txt \| wc -l ``` | Number of .txt files in the current directory. |
| ```curl -s <github url>.keys ``` | Loads the list of all of their publc keys. |
| ``` ``` |  |
| ```curl -s <github url>.keys \| grep ^ssh-ed25519 \| head -n1 ``` |  |
| ```curl -s <github url>.keys \| grep ^ssh-ed25519 \| head -n1 \| awk '{print $2}' ``` |  |
| ``` ``` |  |
| ```sed -r 's/\s+/\n/g'| ```sed``` replaces all white space with new lines. |
| ```-i ``` | Make case insensitve. |
| ```grep <pattern> ``` | filters the output according to ```<pattern>```. |
| * ```head ``` | Prints the first part of a file. If a file is not given, ```head``` reads from STDIN. |
| * ```head -n <number> ``` | Will read first ```<number>``` (e.g. 3) lines of a file. |
| ** ```tail ``` | Reads from the bottom up. |
| ** ```tail -n <number> ``` | Will read last ```<number>``` (e.g. 3) lines of a file. |
| ```cal ``` | get calendar. |
| ```date ``` | Prints current date and time. |
| ```date + '%H' ``` | Prints hours. |
| ```date + '%M' ``` | Prints minues. |
| ```date + '%H:%M:%S ``` | prints hour:minute:second. |
|```date + '%Y-%m-%d ``` | Year-month-day |
| ```date + '%F' ``` | Shorthand for Year-month-day. |
| ```date + '%T' ``` | Shorthand for hour:minute:second |
| ```fold  ``` | Break long lines into shorter lines. |
| ```fold -sw <number> ``` | Break lines into '<number>' (e.g. 30) characters width lines. ```-s``` enables not to break words when it is time to break the line. |
| ```echo $? ``` | Read what is 'exit code'. If we run a command and it's successfull, its 'exit code' will be 0. |
| ```touch ``` | Creates files, modifies timestamps. |
| ```until ``` | Opposite of ```while```. It runs the code until the 'exit code' is non-zero. |
| ```&& ``` | Used to execute multiple commands sequentially, one after another, but only if the preceeding command succeeds. |
| ```\|\| ``` | 'Or' operator. It will run only one of commands. If first one was successful, it won't run the second command. Also called 'short circuiting'. |
| ```; ``` | 'Semicolon'. It will always execute the next command. Even if the first command does not exist, if the second one exists, second one will run. |
| ```() ``` | 'Subshell' environment. If we put chain of commands in parenthesis, it treats those commands as one program. |
| ```time cat ``` | Measures execution time of the 'cat' command. Use 'CTRL + C to exit'. |
| ```vi ``` | Opens Vim text editor. |
| ```jobs ``` | It will return list of stopped jobs. |
| * ```fg ``` | Will bring the last stopped job to the foreground. |
| * ```fg %<number> ``` | Will bring e.g. third (```fg %3```) stopped job to the foreground. |
| * ```kill %<number> ``` | Will stop e.g. second (```kill %2 ```) job. |
| * ```kill -9 %<number> ``` | Will stop e.g. second (```kill -9 %2 ```) job. ```-9``` is necessary in some cases, like stopping vim jobs (because it does not respond to ```kill %2 ```). It is most severe form of signal that can't be intercepted by the program itself. |
| ```%% ``` | The last job. |
| ```& ``` | Will put that program in the background automatically. |
| ```bg ``` | Run in the background those programs that are in the backround. |
| ```pgrep <command> ``` | Search for a process by its name. |
| ```okill <command> ``` | Will kill all jobs with ```<command>``` command. |
| ```kill <process ID> ``` | Kill process with its ID. Every process has an ID and we can use this ID to kill specifically that process. |
| ```kill -SIGKILL <process ID> ``` or ```kill -9 <process ID> ``` | Forcefully kill the process. |
| ```screen -list ``` | List screens we are running on our system. |
| ```screen -S <name> ``` | Give a name to a screen. |
| ``` ``` |  |
| ``` ``` |  |
| ```$ echo -e '\x1b[38;5;44mwow' ``` | Change text (e.g. wow) color. ```-e``` means interpret escape sequence. |



|  Solution   | Explanation |
|-------------|-------------|
| Case: 1     |             |
| * ```mv fileName.txt{_,} ``` | There is a file 'fileName.txt_'. Change the file into 'fileName.txt' |
| * ```echo mv fileName.txt{_,} ``` | It will Show what that command expands to: ```mv fileName.txt_ fileName.txt``` |
| Case: 2 |  |
| ```cat b{ee,oo}p.txt ``` | ```cat``` out every file that starts with 'b', has either 'ee' or 'oo' in the middle, ends with 'p' and is .txt format. |
| Case: 3 |  |
| ```echo {a, b} {c, d} ``` | We can chain brace exensions. In this example we are generating different options (patterns, sequences). It is not necessary to exist all options. Result: ```ac, ad, bc, bd``` |
| Case:4  |  |
| ```mkdir -p images/img{0..100..10} ``` | Generates sequence of directory names from 'img0' to 'img100' with a step of '10'. |
| Case:5  |  |
| ```echo hello \| curl -X POST -sST- localhost:5000/api/something ``` | sends the string "hello" as the request body of an HTTP POST request to localhost:5000/api/something using the curl command. The -X POST option specifies that the request should be a POST request. The -s option suppresses progress meter output, and the -S option shows errors if they occur. The -T- option tells curl to read the request body from STDIN, and the - after -T indicates that curl should read from STDIN.
 |         
| Case: 6 |  |
| ```while ls file.txt do date; sleep 1; done ``` | While file.txt exists, logs out the date every 1 second. |
| Case: 7 |  |
| ```while -f file.txt do date; sleep 1; done ``` | It will check whether 'file.txt' exists (```-f```). If it does not, it immediately returns from it, otherwise, it executes code. |
| Case:8  |  |
| ```if test - file.txt; then echo true; else echo false; fi``` | If 'file.txt' exists, it prints out 'true', else - 'false'. |
| Case:9  |  |
| ```ls /dev ``` | Lists the contents of the '/dev' directory, which is a special directory that contains device files. |
| Case:10 |  |
| !-> ```ls <directory/file name> > /dev/null ``` | Data Redirection. Throw the data away. |
| Case:11 |  |
| !-> ```ls <directory/file name> > /dev/null 2>&1 ``` | If we don't want to see the error message. It redirects STDOUT and STDERR of ls command to '/dev/null', so it discards both normal output and error messages. |
| Case:12 |  |
| !-> ```fg ``` | Brings program that was in the background, to the foreground. To send program to the background, press: 'CTRL + Z'. Not all programs will be sent to the background. Putting them in a subshell might work. This will stop that code's execution. We can do it on more than one program at a time. We can type ```jobs``` command and it will return all stopped jos. |
