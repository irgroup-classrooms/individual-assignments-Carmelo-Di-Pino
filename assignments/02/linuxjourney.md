# Linux Journey Documentation

## Lesson 1: The Shell

### Question
What should be outputted to the display when you type `echo Hello World`?

### Answer
Hello World

### Command Line Output
```bash
$ echo Hello World
Hello World
```

## End of Lesson 1

## Lesson 2: Finding the Current Directory

### Question
How do I find what directory you are currently in?

### Answer
Use the command `pwd` to print the current working directory. For example, the output might be `/home/pete/Movies`, where `home` is a directory, `pete` is a subdirectory within `home`, and `Movies` is a subdirectory within `pete`.

### Command Line Output
```bash
$ pwd
/home/pete/Movies 
```

## End of Lesson 2

## Lesson 3: Change Directory (cd)

### Question
If you are in `/home/pete/Pictures` and wanted to go to `/home/pete`, what’s a good shortcut to use?

### Answer
Use the command `cd ..` to move to the parent directory.

### Command Line Output
```bash
$ cd ..
$ pwd
/home/pete
```

## End of Lesson 3

## Lesson 4: List Directories (ls)

### Question
What command would you use to see hidden files?

### Answer
Use the command `ls -a` to list all files, including hidden ones.

### Command Line Output
```bash
$ ls -a
.  ..  .hidden_file  file1  file2
```

## End of Lesson 4

## Lesson 5: Create Files (touch)

### Question
How do you create a file called `myfile`?

### Answer
Use the command `touch myfile` to create an empty file.

### Command Line Output
```bash
$ touch myfile
$ ls -l
-rw-r--r-- 1 user group 0 Oct 24 10:29 myfile

```

## End of Lesson 5

## Lesson 6: File Type (file)

### Question
What command can you use to find the file type of a file?

### Answer
Use the command `file <filename>` to determine the file type.

### Command Line Output
```bash
$ file banana.jpg
banana.jpg: JPEG image data, JFIF standard 1.01

```

## End of Lesson 6

## Lesson 7: View File Contents (cat)

### Question
What's a good way to see the contents of a file?

### Answer
Use the command `cat <filename>` to display the contents of a file.

### Command Line Output
```bash
$ cat dogfile
This is the content of the dogfile.

```

## End of Lesson 7

## Lesson 8: View File Contents (less)

### Question
How do you quit out of a less command?

### Answer
Press `q` to quit out of the less command and return to your shell.

### Command Line Output
```bash
$ less /home/pete/Documents/text1

```

## End of Lesson 8

## Lesson 9: Command History and Terminal Management (history)

### Question
What is the command to clear the terminal?

### Answer
Use the command `clear` to clear the terminal display.

### Command Line Output
```bash
$ clear

```

## End of Lesson 9

## Lesson 10: Copy Files (cp)

### Question
What flag do you need to specify to copy over a directory?

### Answer
Use the `-r` (recursive) flag to copy a directory and its contents.

### Command Line Output
```bash
$ cp -r Pumpkin/ /home/pete/Documents

```

## End of Lesson 10

## Lesson 11: Move and Rename Files (mv)

### Question
How do you rename a file called `cat` to `dog`?

### Answer
Use the command `mv cat dog` to rename the file.

### Command Line Output
```bash
$ mv cat dog

```

## End of Lesson 11

## Lesson 12: Make Directory (mkdir)

### Question
What command is used to make a directory?

### Answer
Use the command `mkdir <directory_name>` to create a new directory.

### Command Line Output
```bash
$ mkdir books paintings

```

## End of Lesson 12

## Lesson 13: Remove Files (rm)

### Question
How do you remove a file called `myfile`?

### Answer
Use the command `rm myfile` to delete the file.

### Command Line Output
```bash
$ rm myfile

```

## End of Lesson 13

## Lesson 14: Find Files (find)

### Question
What option should I specify for `find` if I want to search by name?

### Answer
Use the `-name` option to search for files by name.

### Command Line Output
```bash
$ find /home -name puppies.jpg

```

## End of Lesson 14

## Lesson 15: Help Command (help)

### Question
How do you get quick command line help for built-in bash commands?

### Answer
Use the command `help <command>` to get help for built-in bash commands.

### Command Line Output
```bash
$ help echo

```

## End of Lesson 15

## Lesson 16: Manual Pages (man)

### Question
How do you see the manuals for a command?

### Answer
Use the command `man <command>` to access the manual pages for that command.

### Command Line Output
```bash
$ man ls

```

## End of Lesson 16

## Lesson 17: Command Description (whatis)

### Question
What command can you use to see a small description of a command?

### Answer
Use the command `whatis <command>` to get a brief description of that command.

### Command Line Output
```bash
$ whatis cat

```

## End of Lesson 17

## Lesson 18: Create Aliases (alias)

### Question
What command is used to make an alias?

### Answer
Use the command `alias <alias_name>='<command>'` to create an alias.

### Command Line Output
```bash
$ alias foobar='ls -la'

```

## End of Lesson 18

## Lesson 19: Exit the Shell (exit)

### Question
How can you exit from the shell?

### Answer
Use the command `exit` or `logout` to leave the shell.

### Command Line Output
```bash
$ exit

```

## End of Lesson 19
