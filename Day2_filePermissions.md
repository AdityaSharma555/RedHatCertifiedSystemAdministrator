
## File Permissions

### Viewing Permissions
- ls -l filename

### Changing Permissions
- chmod
    - chmod u+rwx filename
- chown
    - chown username filename
    - chown :groupname filename
- chgrp
    - chgrp groupname filename

## Special Permissions

|Sp.Perm.     | Symbol         | Applies to       | Effect                  |
|-------------|----------------|------------------|-------------------------|
| setUID      | s in rwsr-xr-x | Executable files | Runs as file owner      |
| setGID(file)| s in rwxr-sr-x | Executable files | Runs as file group      |
| setGID(dirs)| s in drwxr-sr-x| Directories      | New files inhirit group |
| sticky bit  | t in drwxrwxrwt| Directories      | Only owner deletes files|

- 4 / u+s : suid
- 2 / g+s : sgid
- 1 / o+t : sticky bit


## ACL



# Auditing

- w command
    - No of users logged in

- last command
    - info about last user logged in.

- lastb
    - to check failed logins.