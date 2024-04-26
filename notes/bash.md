<b></b>

## UNIX

The UNIX operating system is a collection of programs, each with special role:
1. Kernel: a program that manages resources.
2. Shell: a program that runs other programs.
3. Utilities: little system tools (some are provided by system, some of them are written by us).


#### Kernel

- Kernel's job is scheduling.
    - E.g. if two programs are running at the same time and there is only one CPU, Kernel makes sure that program-1 runs e.g. 1000 instructions, then program-2 runs 1000 instructions. 
- It provides standardized interface for different hardware (like keyboard and a mouse).
- It manages how programs can allocate and free memory. 
    - E.g. two different programs won't read each other's memory.


Programs request resources by making a <b>syscall</b> (a standard called Posix).



#### Shell

- A computer program that can execute other programs from a text based interface.
- In a text-based interface, we interact with a program completely from the command-line with text commands and text output.


#### Utilities

Any distribution of UNIX will come with many other programs that perform narrow single-purpose tasks (like: make a new directory (```mkdir```)).


#### UNIX Pros

- Portable to many kinds of hardware.
- Consistent conventions.
- Vast software ecosystem.
- Text interface.


#### Places we can find UNIX command-line

- Wi-Fi routers.
- DSL and cable modems
- Raspberry pi, beaglebone, nvidia jetson.
- Android phones.
- Linux laptop / desktop.
- Mac OSX computer.
- Web servers.


#### Text interface

To remotely access a UNIX system, we can use the same command-line tools and interface that we use locally. We can remotely access devices without a display.

With text interface (like a shell), to interact with the system we need some way of getting data into and out of it. E.g. network connection, serial port link, bluetooth, web socket.


#### UNIX philosophy

- Each program should do one thing well.
- The output of a program can become the input of another one.

We should be able to combine these single purpose programs to build bigger programs.


### Command Line

- ```echo $SHELL```
    - ```echo``` a command.
    - ```$SHELL``` an argument.
- <b>Flag / Switch</b>: a special type of argument that starts with a dash or two dashes. It is used to customize command behavior.
- 'Tab' completion: if we start typing the name of the file and hit 'Tab', it will automatically finish typing the file name. It needs as much characters as is necessary to uniquely identify the file. 
    - !-> If it can't identify the file we can !-> hit tab twice and it will list out all the files with that characters in their name.

#### Paths

- '.' or '..' or '~': Paths that start with '.' or '..' or '~' are relative paths.
- '/': Paths that start with '/' are absolute paths.
