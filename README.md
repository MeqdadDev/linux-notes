# Linux Notes
Notes and Resources for Linux OS.

## Linux History
<history will be added>

## Popular Commands

-------------------------------

### `uptime`

* __`uptime`__ - Tell how long the system has been running.

__Usage Case:__

```bash
uptime
```

_Output:_

```bash
22:23:24 up  9:21,  1 user,  load average: 0.85, 1.10, 1.27
```

-------------------------------

### `free`

* __`free`__ - Display amount of free and used memory in the system.

__Usage Case:__

```bash
free
```

_Output:_

```bash
               total        used        free      shared  buff/cache   available
Mem:         7965944     2380788     3041184      378216     2543972     4908056
Swap:        2097148     1104344      992804
```

-------------------------------

### `date`

* __`date`__ - print or set the system date and time.

__Usage Case:__

```bash
date
```

_Output:_

```bash
Fri 26 Jan 2024 22:32:48 IST
```

* __`date +%x`__ - print locale's date representation (e.g., 12/31/99)

```bash
date +%x
```

_Output:_

```bash
26/01/2024
```

-------------------------------

### `head`

* __`head`__ - output the first part of files. (10 lines)

__Usage Case:__

```bash
head test.txt
```

_Output:_

```bash
Line 1
Line 2
Line 3
Line 4
Line 5
Line 6
Line 7
Line 8
Line 9
Line 10
```

* __`head <file_name> -n 5`__ - output the first 5 lines of file.

```bash
head test.txt -n 5
```

_Output:_

```bash
Line 1
Line 2
Line 3
Line 4
Line 5
```

-------------------------------

### `tail`

* __`tail`__ - output the last part of files. (10 lines)

__Usage Case:__

```bash
tail test.txt
```

_Output:_

```bash
Line 10
Line 11
Line 12
Line 13
Line 14
Line 15
Line 16
Line 17
Line 18
Line 19
Line 20
```

* __`tail <file_name> -n 5`__ - output the last 5 lines of file.

```bash
tail test.txt -n 5
```

_Output:_

```bash
Line 1
Line 2
Line 3
Line 4
Line 5
```

-------------------------------

### `history`

* __`history`__ - display a list of previously executed commands in a terminal session. It shows a numbered list of commands along with their execution sequence. This command is particularly useful for reviewing and reusing commands from your command-line history.

__Usage Case:__

```bash
history
```

_Output:_

```bash
....
....
....
 1152  sudo apt-get update
 1153  sudo apt-get upgrade
 1154  dmesg
 1155  sudo dmesg
 1156  cd Desktop/
 1157  cd Tmp/
 1158  ls
 1159  mkdir Meqdad
 1160  ls
 1161  cd Meqdad/
 1162  ls
 1163  sudo code .
 1164  ls
 1165  touch hi.txt
 1166  python3
 1167  python --version
....
....
....
```

* __`!<command_id>`__ - Rerun a specific command from history by using an exclamation mark (!) followed by the line number.

Running `ls` command from history (line 1164):

```bash
!1164
```

_Output:_

```bash
LICENSE  README.md  hi.txt
```

-------------------------------

### `touch`

* __`touch`__ - Create new empty files or update the timestamp of existing files. When used to create a new file, it's followed by the name of the file you want to create.

__Usage Case:__

```bash
touch example.txt
```

-------------------------------

### `man`

* __`man`__ - Stands for "manual". It's used to display the manual pages for other commands installed on your system. These manual pages provide detailed information about commands, their options, syntax, and often include examples and explanations.

```bash
man <command_name>
```

__Usage Case:__

```bash
man ls
```
