#**CLI(Command Line Interface)**

The computer understands the language of 0s and 1s which becomes difficult for us to read and write hence to overcome this problem we use an operating system known as the Shell command. This shell command is used to convert the human written language to binary so that the computer can understand the commands.


###**More about Shells**

Linux shells are an essential part of the Linux operating system. They are command-line interpreters that allow users to interact with the operating system in many ways such as interpreting a user’s command and script files along with telling the OS what to do with them. There are many different types of shells available for Linux, but some of the most popular ones include bash, zsh, and ksh.

Some of the characteristics of the Linux shell include:

-Background processing: Sets up lengthy tasks to run in the background.

-Command aliasing: Gives an alias name to a command or phrase.

-Command history: Records the commands you enter in a history.

-Input and output redirection: Redirects input and output to and from files.

-Shell variable substitution: Stores data in user-defined variables.

-0Shell commands: cd, ls, echo, pwd, touch etc.

-Functions

-Control flow: if…then…else, case and shell loops etc.



###**Getting Started with the CLI**

A Command-Line Interface (CLI) is a text-based method for interacting with a computer’s operating system or software. It allows users to issue commands to perform tasks by typing specific instructions into a terminal or command prompt. Unlike Graphical User Interfaces (GUIs), which rely on visual elements like icons and windows, CLI operates purely through text commands.

####**Popular CLI Environments:**

-**Bash**

    **Description**: The Bourne Again Shell (Bash) is a Unix shell commonly found on Unix-based systems like Linux and macOS. It's known for its versatility, powerful scripting capabilities, and extensive support in the Unix/Linux ecosystem.
    **Key Features**:
        Supports scripting with extensive control structures, functions, and variables.
        Offers powerful file and text manipulation tools (e.g., awk, sed).
        Built-in commands and utilities for system administration and automation.
        Rich ecosystem of third-party tools and libraries.


-**PowerShell**

    **Description**: Developed by Microsoft, PowerShell is the standard shell and scripting language in Windows environments. It's deeply integrated with the .NET framework and designed for system administration, automation, and object-oriented programming.
    **Key Features**:
        Object-oriented scripting language with strong integration with .NET classes and libraries.
        Commandlets (cmdlets) for performing common administrative tasks.
        Pipeline support for chaining commands and passing objects between them.
        Extensive support for managing Windows components, services, and configurations.


-**Command Prompt**

    **Description**: Also known as cmd.exe, Command Prompt is the default command-line interpreter in Windows operating systems. It provides basic command-line functionalities for system management, file operations, and scripting.
    **Key Features**:
        Basic commands for file manipulation, directory navigation, and system administration.
        Limited scripting capabilities compared to PowerShell.
        Batch scripting using .bat files for automating repetitive tasks.
        Commonly used for running system utilities and troubleshooting tasks.



###** Directory Structure and File Hierarchy of UNIX**


-Root Directory (/):

The top-level directory in the UNIX file system hierarchy.

All other directories and files are located under this root directory.

Example: /bin, /etc, /home, /usr, etc.

-Standard Directories:

/bin: Essential user binaries (commands), such as ls, cp, mv.

/boot: Files required for booting the system.

/dev: Device files.

/etc: System configuration files.

/home: Home directories for users.

/lib and /lib64: Essential shared libraries and kernel modules.

/media: Mount points for removable media (USB drives, optical discs).

/mnt: Temporary mount point for mounting filesystems.

/opt: Optional software packages.

/proc: Virtual file system that provides information about processes and kernel parameters.

/root: Home directory for the root user.

/sbin: System binaries (utilities for system administration).

/srv: Data for services provided by the system.

/tmp: Temporary files.

/usr: Secondary hierarchy for read-only user data and programs.

/var: Variable data, such as logs, spool files, etc.


###**How do I find out my current shell name?**

To find out your current shell in a Unix-like operating system (such as Linux), you can use the following commands:

echo $SHELL:


`echo $SHELL`

This command prints the path to the current shell executable.

ps $${PID}:


`ps $$`

This command lists information about the process ID of the current shell. The $$ represents the PID of the current shell instance.

ps -p $$:


`ps -p $$`

this lists information about the process ID of the current shell.

PID: Process ID of the current shell instance.
TTY: Terminal device associated with the shell.
TIME: CPU time used by the shell.
CMD: Name of the shell executable (bash in this case).


###**CLI Command**

####**Bread and Butter Commands**

man - Display the manual page for a command:

`man ls`

This command opens the manual page for ls, providing detailed information on its usage and options.

cd - Change directory:

`cd /path/to/directory`

    . : Represents the current directory.
    .. : Represents the parent directory.
    ~ : Represents the user's home directory.
    - : Represents the previous working directory.

mkdir - Create a new directory:

`mkdir new_directory`

Creates a directory named new_directory in the current working directory.

mv - Move or rename files/directories:

`mv file.txt new_location/`

Moves file.txt to new_location/ or renames file.txt to new_name.txt.

cp - Copy files/directories with recursive flag:

`cp -r source_directory/ destination/`

Copies source_directory/ and its contents recursively to destination/.

ls - List directory contents with different flags:

`ls -l`
`ls -a`
`ls -lh`

    -l : Long format listing.
    -a : Include hidden files.
    -h : Human-readable sizes.

pwd - Print working directory:

`pwd`

Displays the current working directory path.

rm - Remove files/directories:

`rm file.txt`
`rm -r directory/`

    file.txt : Deletes file.txt.
    -r : Recursively deletes directory/ and its contents.

chmod - Change file permissions:

`chmod 755 script.sh`

Sets executable permissions (755) for script.sh.

chown - Change file owner and group:

`chown user:group file.txt`

Changes ownership of file.txt to user and group.

sudo - Execute a command as superuser:

`sudo apt-get update`

Updates package list using apt-get with superuser privileges.

apt - Package manager for Debian-based systems:

`apt install package_name`

Installs package_name using apt.

touch - Create an empty file or update timestamp:

`touch new_file.txt`

Creates new_file.txt if it doesn't exist or updates its timestamp.

cat - Concatenate and display file contents:

`cat file.txt`

Displays contents of file.txt.

less - View file contents interactively (scrolling):

`less large_file.log`

Allows scrolling through large_file.log interactively.

more - View file contents page by page:

`more readme.txt`

Displays readme.txt one screenful at a time.

tail - Output the last part of files:

`tail -n 10 file.log`

Displays the last 10 lines of file.log.

rsync - Remote file and directory synchronization:

`rsync -avz source/ user@remote_host:destination/`

Synchronizes source/ directory to user@remote_host:destination/ using rsync.

grep - Search for patterns in files:

`grep "pattern" file.txt`

find - Search for files in a directory hierarchy:

`find . -name "*.txt"`

Finds all .txt files in the current directory (.) and subdirectories.

sort - Sort lines of text files:

`sort file.txt`

Sorts lines of file.txt.

date - Display or set the system date and time:

`date`

Displays the current system date and time.

tree - List contents of directories in a tree-like format:

`tree directory/`

Lists contents of directory/ in a tree structure (requires installation).

wc - Print newline, word, and byte counts for each file:

`wc file.txt`

Displays newline, word, and byte counts for file.txt.


###**OS/Process Related Commands**

ps - Display information about active processes:

`ps aux`

Lists all processes (-e) with full format (-f).

top - Display Linux tasks:

`top`

Interactive command showing system summary information and running tasks.

df - Display disk space usage:

`df -h`

Shows disk space usage in human-readable format (-h).

uname - Print system information:

`uname -a`

Displays all system information (-a).

free - Display amount of free and used memory:

`free -h`

Shows memory usage in human-readable format (-h).

lspci - List PCI devices:

`lspci`

Lists all PCI devices connected to the system.

kill - Terminate processes:

`kill -9 PID`

Sends signal SIGKILL (-9) to process PID to terminate it.
Network Related Commands

ping - Test network connectivity:

`ping google.com`

Pings google.com to test network connectivity.

ifconfig - Configure network interfaces:

`ifconfig eth0`

Displays configuration of eth0 network interface.

ssh - Open SSH session:

`ssh user@hostname`

Connects to hostname as user using SSH.
Bash Related Commands

xargs - Build and execute command lines from standard input:

`echo "file1 file2" | xargs rm`

Deletes file1 and file2 using xargs.

printenv - Print environment variables:

`printenv PATH`

Displays value of PATH environment variable.

nano - Simple text editor:

`nano file.txt`

Opens file.txt for editing using nano.

awk - Pattern scanning and processing language:

`awk '{print $1}' file.txt`

Prints the first field of each line in file.txt using awk.

sed - Stream editor:

`sed 's/old/new/' file.txt`

Replaces old with new in file.txt using sed.

Pipe operator | - Redirects output of one command as input to another:

`ls -l | grep ".txt"`

Lists .txt files using ls and filters (grep) for .txt files.

These commands cover a wide range of functionalities essential for everyday tasks and system administration in a Unix-like environment. 
