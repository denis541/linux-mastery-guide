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
## Permision types 
|symbol    | meaning  | applies to                             |
|--------------------------------------------------------------|
|r         | read(view file / list directory | file/directory  |

