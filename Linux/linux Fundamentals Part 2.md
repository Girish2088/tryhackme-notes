# Room Name: Linux Fundamentals Part 2

## Overview

- Remote access using SSH
- File and directory management
- Understanding manual/help commands
- Linux file permissions and their numeric representation
- Basic Linux directory structure

### Remote Access
- `ssh username@IP`
  - Used to connect to a remote machine securely
  - Example:
    ```
    ssh user@10.49.128.171
    ```
###  Listing & Help Commands
- `ls -a` → Shows hidden files
- `ls --help` → Displays help options for `ls`
- `man ls` → Opens manual page for detailed explanation

### File Management
- `touch filename` → Creates a new file  
- `rm filename` → Deletes a file  
- `cp source destination` → Copies a file  
- `mv oldname newname` → Renames or moves a file  
- `file filename` → Identifies file type  

###  User Management
- `su user2` → Switch user (keeps current environment)
- `su -l user2` → Switch user with new environment

###  File Permissions
Permissions are represented using numbers:

- `r (read) = 4`
- `w (write) = 2`
- `x (execute) = 1`

Examples:
- `7 = rwx (full permission)`
- `6 = rw-`
- `5 = r-x`

Example:
- Owner → Full permissions (7)
- Group → Read only (4)
- Others → Read & execute (5)

###  Important Directories
- `/etc` → System configuration files  
- `/var` → Logs and variable data  
- `/root` → Root (admin) home directory  
- `/tmp` → Temporary files  

