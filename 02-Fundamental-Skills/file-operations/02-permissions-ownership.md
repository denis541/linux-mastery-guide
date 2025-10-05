# File Permissions & Ownership in Linux  

Linux is a **multi-user system**. File permissions and ownership control **who can read, write, or execute** a file or directory.  

---

## 🔹 Ownership  

Every file in Linux has:  
- **User (Owner):** The person who created the file.  
- **Group:** A collection of users who may share access.  
- **Others:** Everyone else on the system.  

You can see ownership info with:  
```bash
ls -l
```
<img width="941" height="227" alt="image" src="https://github.com/user-attachments/assets/cd43f5ed-32a3-439b-ae42-77d4e66edad7" />

**-rw-rw-r-- 1 kali kali 0 Oct  5 07:08 file1.txt
**

* kali ->Owner(user)
* kali ->Group
* the `-` in the begining -> shows this is a regular file 
* rw-rw-r-- -> Permisions
---

## 🔹Permision types 

* `r` -(read: view file / list directory)
* `w` -(write: modify file / add/remove)
* `x` -(execute: run file / enter directory)
* `-` -(no permision)
  
Permisions are grouped into three sets:

rw- (owner) rw-(group) r--(others)
---
## 🔹Changing Permissions (chmod)
### symbolic mode:

* `chmod u+x script.sh     # give execute to user`
* `chmod g-w report.txt    # remove write from group`
* `chmod o+r notes.txt     # give read to others`
* `chmod a+x tool.sh       # give execute to everyone (a = all)`

### Numeric mode 
permisions represented by numbers:

| Number | Permission | Example |
|--------|------------|---------|
| 0      | ---        | No permissions |
| 1      | --x        | Execute only |
| 2      | -w-        | Write only |
| 4      | r--        | Read only |
| 6      | rw-        | Read and Write |
| 7      | rwx        | Read + Write + Execute|

# Usage 
* `chmod 755 script.sh   # rwx for owner, rx for group/others`
* `chmod 644 file.txt    # rw for owner, r for group/others`

----

# Changing Ownership (chown & chgrp)
* `chown user file.txt         # change owner`
* `chown user:group file.txt   # change owner and group`
* `chgrp developers file.txt   # change group(developers) only for the file.txt`

----
# Special Permissions 
setgid `s` -the new files in the directory wil inherit the group
```bash
chmod g+s shared_dir
```
Sticky Bit `t` -Only owner can delete files in the directory 
* common `/tmp`
```bash
chmod +t /shared
```












