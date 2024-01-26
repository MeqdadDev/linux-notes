# Linux Notes
Notes and Resources for Linux OS.

## Linux History
<history will be added>

## Popular Commands

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