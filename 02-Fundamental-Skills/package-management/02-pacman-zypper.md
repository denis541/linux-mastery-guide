# Pacman Commands && Their functions.

Pacman is the package manager used by Arch Linux and its derivatives.  
These are the most commonly used commands and what they do.

---

## 🔍 Package Searching

| Command | Description |
|--------|-------------|
| `pacman -Ss <name>` | Search for a package in the repositories. |
| `pacman -Qs <name>` | Search for an installed package. |

---

## 📦 Installing & Removing Packages

| Command | Description |
|--------|-------------|
| `sudo pacman -S <package>` | Install a package. |
| `sudo pacman -R <package>` | Remove a package, but keep its configs. |
| `sudo pacman -Rs <package>` | Remove a package **and** dependencies not needed by others. |
| `sudo pacman -Rns <package>` | Remove a package + deps + config files. Basically a digital exorcism. |

---

## 🔄 Updating the System

| Command | Description |
|--------|-------------|
| `sudo pacman -Syu` | Sync repos and update the entire system. Your daily ritual as an Arch user. |

---

## 📁 Local Package Management

| Command | Description |
|--------|-------------|
| `pacman -Qi <package>` | Show info about an installed package. |
| `pacman -Si <package>` | Show info about a package in the repo. |
| `pacman -Ql <package>` | List all files installed by a package. |
| `pacman -Qo <file>` | Find which package owns a file. |

---

## 🧹 Cleaning & Maintenance

| Command | Description |
|--------|-------------|
| `sudo pacman -Sc` | Remove old package archive files. |
| `sudo pacman -Scc` | Remove **all** cached packages. Brings peace, removes space. |
| `pacman -Qdt` | List orphaned packages (no longer needed). |
| `sudo pacman -Rns $(pacman -Qdtq)` | Remove all orphaned packages. |

---

## 📜 Package Database

| Command | Description |
|--------|-------------|
| `pacman -Q` | List installed packages. |
| `pacman -Qs <keyword>` | Search installed packages by keyword. |
| `pacman -Qe` | List explicitly installed packages (not deps). |
| `pacman -Qm` | List manually installed **foreign** packages (e.g., AUR). |

---

## 💾 Installing Local Packages

| Command | Description |
|--------|-------------|
| `sudo pacman -U <file.pkg.tar.zst>` | Install a package from a local file. |

---

## 🛠️ Fixing Stuff

| Command | Explanation |
|---------|-------------|
| `sudo pacman -Fy` | Download file database for searching file ownership. |
| `pacman -F <file>` | Find which package provides a file. |
| `sudo pacman -Syy` | Force refresh package database (use only if needed). |

---

## 🧭 Useful Shortcuts

| Shortcut | Meaning |
|----------|---------|
| `-S` | Install/search/sync. |
| `-R` | Remove. |
| `-Q` | Query (local). |
| `-U` | Install from local file. |
| `-y` | Refresh repo databases. |
| `-u` | Upgrade packages. |
| `-v` | Show more output. |

---

