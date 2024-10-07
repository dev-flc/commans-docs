# C O M M A N S - F I L E - M A N A G E M E N T


### Navigating Directories

```sh
pwd # Print the current working directory

cd <directory> # Change to a specific directory

cd .. # Move up one directory level

cd - # Switch to the previous directory
```

### Listing Files and Directories

```sh
ls # List files and directories in the current directory

ls -l # List files with detailed information (permissions, size, etc.)

ls -a # List all files, including hidden files (those starting with .)

ls -lh # List files with human-readable sizes (e.g., KB, MB)
```

### Managing Files

```sh
cp <source> <destination> # Copy a file or directory

mv <source> <destination> # Move or rename a file or directory

rm <file> # Delete a file

rm -r <directory> # Recursively delete a directory and its contents

rm -f <file> # Force delete a file (no prompt)

touch <file> # Create an empty file or update the timestan of an existing file
```

### Creating and Managing Directories

```sh
mkdir <directory> # Create a new directory

mkdir -p <path/to/directory> # Create nested directories (e.g., parent anc subdirectories)

rmdir <directory> # Remove an empty directory
```

### Viewing File Content

```sh
cat <file> # Display the content of a file

tac <file> # Display the content of a file in reverse order

less <file> # View the content of a file one screen at a time

head <file> # Display the first 10 lines of a file

tail <file> # Display the last 10 lines of a file

tail -f <file> # Continuously display the last lines of a file (e.g., log monitoring)

nl <file> # Display the content of a file with line numbers
```

### Finding Files and Directories

```sh
find <path> -name <filename> # Search for files by name

find <path> -type d -name <dirname> # Search for directories by name

locate <filename> # Quickly find files and directories by name (requires updatedb)

whereis <command> # Locate the binary, source, and manual page files for a command

which <command> # Locate the executable path of a command
```

### Compressing and Archiving Files

```sh
tar -czvf <archive.tar.gz> <directory-or-file> # Create a compressed tarball (gzip)

tar -xzvf <archive.tar.gz> # Extract a compressed tarball (gzip)

zip <archive.zip> <file> # Create a compressed zip archive

unzip <archive.zip> # Extract files from a zip archive
```

### Disk Usage and Quotas

```sh
du -h <directory> # Show disk usage of a directory and its contents in human-readable format

df -h # Display available disk space in human- readable format
```