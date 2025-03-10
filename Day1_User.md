## Basic Commands -

**lsblk** - Lists the block devices in the system. (NVME, SATA, etc.) \
**sleep** - delay / pauses the execution of commands/scripts \
**> output redirection** - Redirects the output stream and overwrites \
**>> output redirection** - Redirects the output stream and appends \
**2> error redirection** - Redirects the error stream but overwrites \
**2> error redirection** - Redirects the error stream but appends \
**&>** - Output + error. \
**;** - command separator and multiple execution. \
**less command** - Scroll up and down \
**more command** - Scroll down only and exit automatically on 100% scroll \
**tail -n** n=number of lines \
**head -n** \
**&&** - Executes 2nd command only if 1st command is successfully executed. \
**||** - Executes 2nd command only if 1st command is failed. \
**find** - To find any file/directory in linux file system \
example - find / -name "jitendra"
-> / - it is the directory in which you want to find
- find / -size 100M
- find / -type f -name "newbee"
- find / -type d -name "newbee"
- find / -type f -name *.txt 

**du -h** \
**ls -h** \
**grep** - To search words/patterns in files
- grep -i "word" file : -i for ignore case
- grep "^root" /etc/passwd : Lists all lines which START with 'root'
- grep "root$" /etc/passwd : Lists all lines which END with 'root'

**echo** - prints a string \
**NAME=techno** - creates temporary variable NAME \
**env** - Lists all permanent variables \
**useradd** - create user \
**id** - show uid, gid, groups \
**passwd** - change password of user \
**su - user** - To login as user. It changes the environment variable as well. It also loads users profile files - .bash_profile, .profile \
**su user** - Keeps the current environment.


## User Administration
User administrator works on AAA
- 1.Authentication
- 2.Authorization
- 3.Auditing

3 types of users 
- Super user : root user. \
Uid = 0 \
shell = /bin/bash

- System user : created for running processes. eg - Apache, ftp \
uid = 1-999
shell = /sbin/nologin

- local user : uid = 1000-60000 \
shell = /bin/bash (default, can be changed)

Various Files in User Administration
- 1. /etc/groups 
    - Information about all the groups.
- 2. /etc/passwd
    - User information
    - 7 entries for 1 user.
    - username : password pointer (x) : udi : gid : comment : Home_directory : shell
- 3. /etc/shadow
    - Password
    - age of password
- 4. /etc/gshadow


Commands :
- 1. useradd
- 2. userdel (only deletes user, not home directory) : 
    - userdel -r : deletes user and home directory and mail pool. Does not delete files outside of home directory.
- 3. groupadd
- 4. groupdel
- 5. gpasswd
- 6. chgrp - permanently change group
- 7. usermod - change user config.
    - usermod -u 1011 username : change uid
    - usermod -g groupname username : change primary group
    - usermod -G groupname username : change secondary group
    - usermod -aG groupname username : append secondary group
    - usermod -s /sbin/nologin batman : change shell
- newgrp - temporarily change primary group



-------------------------

Assignments -
- usermod options
- files in user administration
- superuser privileges







## Topics Covered

> Input/Output Rediection \
> Symbols for multiple command execution - Shell operators -> ';' , '&&' , '||' (Chaining operators) \
> /dev/null - Dustbin of linux \
> Variables in Linux \
