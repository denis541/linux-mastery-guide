# File Operations & Basic Commands in Linux  

In Linux, almost everything is treated as a **file** – regular files, directories, devices, and even processes. Mastering basic file operations is essential for working effectively on the system.  

---

## 🔹 Navigating the File System  

| Command | Example | Description |
|---------|---------|-------------|
| `ctrl+alt+t` |      | starts the terminal|
| `pwd` | `pwd` | Prints the **current working directory**. |
| `ls` | `ls -l` | Lists files and directories. Options: `-a` (all), `-l` (long format), `-h` (human-readable sizes). |
| `cd` | `cd /home/user` | Changes directory. Use `cd ..` to go up one level, `cd ~` for home. |

<img width="1920" height="947" alt="image" src="https://github.com/user-attachments/assets/63b82db9-3fb7-4e8f-bb76-9c00291aa748" />

---

## 🔹 Creating Files & Directories  

| Command | Example | Description |
|---------|---------|-------------|
| `touch` | `touch file.txt` | Creates an empty file or updates its timestamp. |
| `mkdir` | `mkdir projects` | Creates a new directory. Use `-p` to create parent directories. |

---

## 🔹 Viewing File Contents  

| Command | Example | Description |
|---------|---------|-------------|
| `cat` | `cat notes.txt` | Displays the entire file content. |
| `less` | `less bigfile.txt` | View file page by page (useful for long files). |
| `head` | `head -n 10 file.txt` | Shows the first 10 lines of a file. |
| `tail` | `tail -f logfile.log` | Shows the last lines of a file (`-f` follows live updates). |

---

## 🔹 Copying, Moving, Renaming, and Deleting  

| Command | Example | Description |
|---------|---------|-------------|
| `cp` | `cp file.txt backup.txt` | Copies a file. Use `-r` for directories. |
| `mv` | `mv old.txt new.txt` | Moves or renames a file. |
| `rm` | `rm file.txt` | Removes a file. Use `-r` for directories, `-f` to force delete. **⚠ Dangerous** |
| `rmdir` | `rmdir emptydir` | Removes an empty directory. |

---

## 🔹 File Searching  

| Command | Example | Description |
|---------|---------|-------------|
| `find` | `find /home -name file.txt` | Finds files by name or pattern. |
| `locate` | `locate passwd` | Quickly searches for files using an indexed database. Run `updatedb` to refresh. |

---

## 🔹 File Permissions & Ownership  

| Command | Example | Description |
|---------|---------|-------------|
| `ls -l` | | Shows file permissions (e.g., `-rw-r--r--`). |
| `chmod` | `chmod 755 script.sh` | Changes file permissions. |
| `chown` | `chown user:group file.txt` | Changes file ownership. |

---

## 🔹 Useful Shortcuts  

- `.` → Current directory  
- `..` → Parent directory  
- `~` → Home directory  
- `*` → Wildcard (matches many files, e.g., `*.txt`)  

---

✨ **In short:**  
These commands form the **foundation of Linux usage**. They let you navigate, create, modify, and manage files efficiently.  

---

✅ **Pro Tip for Learners:**  
Practice by creating a `practice` directory and try:  
```bash
mkdir practice
cd practice
touch test.txt
echo "Hello World" > test.txt
cp test.txt copy.txt
mv copy.txt moved.txt
rm moved.txt

