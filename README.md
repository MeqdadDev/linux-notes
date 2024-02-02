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

-------------------------------

### `id`

* __`id`__ - To display the user and group identifiers associated with the current user or a specified username. It provides information about the user's UID (User Identifier), GID (Group Identifier), and supplementary group IDs.

```bash
id [username]
```

__Usage Case:__

```bash
id meqdad
```

_Output:_

```bash
uid=1000(meqdad) gid=1000(meqdad) groups=1000(meqdad),4(adm),20(dialout),24(cdrom),27(sudo),30(dip),46(plugdev),122(lpadmin),135(lxd),136(sambashare)
```

Running `id` command the root user:
 
```bash
id root
```

_Output:_

```bash
uid=0(root) gid=0(root) groups=0(root)
```

* __`id`__ - When you run the `id` command without specifying a username, it displays information about the current user.

Running `id` command the current user (`meqdad`):

```bash
id
```

_Output:_

```bash
uid=1000(meqdad) gid=1000(meqdad) groups=1000(meqdad),4(adm),20(dialout),24(cdrom),27(sudo),30(dip),46(plugdev),122(lpadmin),135(lxd),136(sambashare)
```

-------------------------------

### `useradd`

* __`useradd`__ - Create a new user account.

```bash
useradd [options] [User_name]
```

__Usage Case:__

```bash
sudo useradd meqdad
```

_Output:_

```bash
A new user account "meqdad" is created.
```

* __`sudo useradd -d [home_dir_path] [new_user]`__ - To give a home directory path for new users.

```bash
sudo useradd -d /home/test_user test_user
```

_Output:_

```bash
A new user account "test_user" is created and the Home directory is created.
```

-------------------------------

### `userdel`

* __`userdel`__ - Delete a user account.

```bash
userdel [options] [User_name]
```

__Usage Case:__

```bash
sudo userdel meqdad
```

_Output:_

```bash
The user account "meqdad" is deleted.
```

-------------------------------

### `groupadd`

* __`groupadd`__ - Create a new group.

```bash
groupadd [options] [group_name]
```

__Usage Case:__

```bash
sudo groupadd test_group
```

_Output:_

```bash
A new group "test_group" is created.
```

-------------------------------

### `cat /etc/passwd`

* __`cat /etc/passwd`__ - Display user account information.


__Usage Case:__

```bash
cat /etc/passwd
```

OR

```bash
vim /etc/passwd
```

_Output:_

```bash
root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
...
...
...
```

__Explanation of Output:__

Username (Login Name): daemon - This is the username or login name of the user account.

Password Placeholder: x - In modern Unix-like operating systems, the actual encrypted password is stored in the /etc/shadow file for security reasons. This placeholder (x) indicates that the password is stored in /etc/shadow.

User ID (UID): 1 - This is the user's unique numerical identifier. User IDs 0-99 are typically reserved for system users and services.

Group ID (GID): 1 - This is the primary group ID of the user. In this case, both the user ID and the group ID are 1, which is often the case for system-related accounts.

User Information: daemon - This field typically contains additional information about the user, such as the full name or description. In this example, it's the same as the username.

Home Directory: /usr/sbin - This is the path to the user's home directory. For system accounts like daemon, this might be set to a directory related to the system's operation.

Login Shell: /usr/sbin/nologin - This is the path to the user's login shell. If the user is not intended to log in interactively, a shell like /usr/sbin/nologin is used to prevent login.

-------------------------------

### `passwd [username]`

* __`passwd [username]`__ - Change or set the password for a user account.

```bash
passwd [username]
```

__Usage Case:__

```bash
passwd meqdad
```

_Output:_

```bash
Changing password for user meqdad.
New password:
Retype new password:
passwd: password updated successfully
```

-------------------------------

