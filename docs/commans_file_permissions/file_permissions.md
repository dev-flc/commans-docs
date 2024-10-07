# C O M M A N S - F I L E - P E R M I S S I O N S


### Viewing and Changing File Permissions

```sh
ls -l <file> # List file permissions in long format

chnod u+x <file> # Add execute permission for the user (owner)

chmod g-w <file> # Remove write permission for the group

chnod o+r <file> # Add read permission for others

chnod u=rw,g=r, 0= <file> # Set user (read/write), group (read), and others (none) permissions

chnod 755 <file> # Set permissions using numeric notation (ruxr-xr-x)

chnod -R 755 <directory> # Recursively change permissions for a directory and its contents
```

### Viewing and Changing Ounership

```sh
chown <user>:<group> <file> # Change the owner and group of a file

chown <user> <file> # Change only the owner of a file

chgrp <group> <file> # Change only the group of a file

chown -R <user>:<group> <directory> # Recursively change ownership for a directory and its contents
```

### Setting Default Permissions with umask

```sh
umask # Display the current umask value

umask 622 # Set the default permission to 755 for new files and directories

umask 077 # Set the default permission to 760 for new files and directories
```

### Working with Access Control Lists (ACLs)

```sh
getfacl <file> # Display the ACL of a file

setfacl -m u:<user>:rwx <file> # Add or modify an ACL entry for a user (Px pernissions)

setfacl -m g:<group>:r-- <file> # Add or modify an ACL entry for a group (read-only permissions)

setfacl -x u:<user> <file> # Remove an ACL entry for a user

setfacl -b <file> # Remove all ACL entries from a file

setfacl -R -m u:<user>:rwx <directory> # Recursively set ACLs for a directory and its contents

setfacl -d -m u:<user>rwx <directory> # Set default ACLs for new files created within a directory 
```
### Special Permissions (Setuid, Setgid, Sticky Bit)

```sh
chmod u+s <file> # Set the setuid bit (run as the file's owner)

chmod g+s <directory> # Set the setgid bit (new files inherit the group ID)

chmod o+t <directory> # Set the sticky bit (only the owner can delete files)

ls -ld <directory> # List the special permissions (e.g., druxrusr-t)
```

### Viewing and Changing File Attributes

```sh
tsattr <file> # List file attributes (e.g., imutable, append-only)

chattr +i <file> # Set the innutable attribute (file cannot be modified)

chattr -i <file> # Remove the immutable attribute

chattr +a <file> # Set the append-only attribute (file can only be appended)

chattr -a <file> # Remove the append-only attribute
```