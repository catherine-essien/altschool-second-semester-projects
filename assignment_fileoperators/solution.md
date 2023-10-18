In Bash, you can use various file operators to check the properties and conditions of files and directories. Here are fifteen file operators with explanations and examples of how they can be executed in a Bash script:

1. -e (Exists): Checks if a file or directory exists.

<br>

```bash

#! /bin/bash

if [ -e "$file.txt" ]; then
    echo "file.txt exists."
fi
```

<br>

2. -f (File): Checks if a path is a regular file.

<br>

```bash

#! /bin/bash

if [ -f "$file.txt" ]; then
    echo "file.txt is a regular file."
fi
```

<br>

3. -d (Directory): Checks if a path is a directory.

<br>

```bash

#! /bin/bash

if [ -d "$my_directory" ]; then
    echo "my_directory is a directory."
fi
```

<br>


4. -r (Read): Checks if a file is readable.

<br>

```bash

#! /bin/bash

if [ -r "$file.txt" ]; then
    echo "file.txt is readable."
fi
```

<br>

5. -w (Write): Checks if a file is writable.

<br>

```bash

#! /bin/bash

if [ -w "$file.txt" ]; then
    echo "file.txt is writable."
fi
```

<br>

6. -x (Execute): Checks if a file is executable.

<br>

```bash

#! /bin/bash

if [ -x "$script.sh" ]; then
    echo "script.sh is executable."
fi
```
<br>

7. -s (Size): Checks if a file is not empty (has a size greater than zero).

<br>

```bash

#! /bin/bash

if [ -s "$file.txt" ]; then
    echo "file.txt is not empty."
fi
```
<br>

8. -L (Symbolic Link): Checks if a file is a symbolic link.

<br>

```bash

#! /bin/bash
if [ -L "$symlink" ]; then
    echo "symlink is a symbolic link."
fi
```
<br>

9. -c (Character Special File): Checks if a file is a character special file.

<br>

```bash

#! /bin/bash

if [ -c "$/dev/tty" ]; then
    echo "/dev/tty is a character special file."
fi
```

<br>

10. -b (Block Special File): Checks if a file is a block special file.

<br>

```bash

#! /bin/bash
if [ -b "$/dev/sda" ]; then
    echo "/dev/sda is a block special file."
fi
```
<br>

11. -p (Named Pipe): Checks if a file is a named pipe (FIFO).

<br>

```bash

#! /bin/bash

if [ -p "$fifo" ]; then
    echo "fifo is a named pipe."
fi
```

<br>

12. -u (Setuid): Checks if a file has the setuid permission.

<br>

```bash

#! /bin/bash

if [ -u "$executable" ]; then
    echo "executable has the setuid permission."
fi
```

13. -g (Setgid): Checks if a file has the setgid permission.

<br>

```bash

#! /bin/bash

if [ -g "$executable" ]; then
    echo "executable has the setgid permission."
fi
```
<br>

14. -k (Sticky Bit): Checks if a file has the sticky bit set.

```bash
#! /bin/bash
if [ -k "$directory" ]; then
    echo "directory has the sticky bit set."
fi
```
<br>
15. -N (Newer): Checks if a file is newer than a reference file.


```bash

#! /bin/bash
if [ "$file.txt" -nt "backup.txt" ]; then
    echo "file.txt is newer than backup.txt."
fi
```