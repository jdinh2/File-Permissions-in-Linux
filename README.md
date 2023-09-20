<p align="center">
<img src="https://1000logos.net/wp-content/uploads/2017/03/Symbol-Linux.jpg" alt="Linux Logo" width="400" height="200" />
</p>

# File Permissions in Linux

## Overview
The research team requires updated file permissions for specific files and directories in the 'projects' directory. Adjusting these permissions will align them with the intended authorization levels, enhancing the system's security.

## Procedure

### 1. Inspecting File and Directory Details
Using the `ls -la` command, I determined the permissions of the 'projects' directory contents, revealing files including 'drafts', '.project_x.txt', and five other project files. Each entry's first 10 characters reflect the permissions for that item.

<img src="https://i.gyazo.com/e1662545f583e4f212f5bd45ef2c84a3.png" alt="linux" />

### 2. Understanding the Permissions String
- **1st character:** Indicates file type. 'd' for directory and '-' for regular files.
- **2nd-4th characters:** Represent user's read (r), write (w), and execute (x) permissions. A '-' indicates the absence of that permission.
- **5th-7th characters:** Represent group permissions.
- **8th-10th characters:** Indicate permissions for others.

For instance, '-rw-rw-r--' denotes a file where both the user and group can read and write, but others can only read.

### 3. Modifying File Permissions
To align with the organization's directive, I removed write permissions for 'other' from `project_k.txt` using the `chmod` command.

<img src="https://i.gyazo.com/79bc3a406fc2b0d5f07f263509c00595.png" alt="linux2" />

### 4. Adjusting Hidden File Permissions
For the archived '.project_x.txt', I restricted write permissions and ensured read access for both the user and group.

<img src="https://i.gyazo.com/08942ce0a9be22e0d4230bff23e76d46.png" alt="linux3" />

### 5. Altering Directory Permissions
To limit access to the 'drafts' directory exclusively to 'researcher2', I modified the permissions, ensuring only 'researcher2' has execute permissions.

<img src="https://i.gyazo.com/192187bc491f7ac2de722860e6a1e070.png" alt="linux4" />

## Conclusion
After a detailed review using `ls -la`, I adjusted permissions on numerous files and directories in the 'projects' directory with the `chmod` command, ensuring security as per the organization's requirements.
