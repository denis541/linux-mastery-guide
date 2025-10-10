# System Monitoring with `top` and `htop`
`top` is a command-line system monitoring tool that has been a staple in Unix/Linux systems for decades. It provides a real-time, dynamic view of running processes and system resource usage.

`htop` is an interactive process viewer designed as a more user-friendly and feature-rich replacement for top. It provides the same core functionality but with significant improvements in usability and visualization.

<img width="1920" height="947" alt="image" src="https://github.com/user-attachments/assets/ef5a72a9-33e9-48b0-bf67-d27c2f827740" />

# installling `htop` 
### Most distros already have it in their package repos.

Debian/Ubuntu: 
```bash
sudo apt update && sudo apt install htop
```
Fedora/RHEL/CentOS: 
```bash
sudo dnf install htop or sudo yum install htop
```
Arch: 
```bash
sudo pacman -S htop
```

If you're on macOS  use `brew install htop.`

# Commands used & functions:

`sudo apt update` — refresh package lists.

`sudo apt install htop` — install htop.

# 2. Start htop
### command:
```bash
htop
```
### Variants:

`htop -d 5` — set refresh delay to 5 tenths of a second (the unit is 1/10s).

`htop -u username` — show only processes for that user.

`htop -p 123,456` — show only specific PIDs.
# 3. Navigation & searching (useful immediately)
`Arrow keys / PageUp / PageDown` — move selection/scroll.

`F3` or `/` — search for a process name (incremental).

`F4` or `\` — filter: show only processes matching pattern. Press Esc to clear.

`Space` — tag/untag a selected process (useful to act on multiple).

`u` — untag all.
# 4. Sorting & tree view 
`F6` — pick sort column `(CPU%, MEM%, TIME+, etc.)`.

Press `Shift+i` to invert sort order.

`F5` or `t` — `tree view`: shows parent-child relationships.

<img width="1576" height="691" alt="image" src="https://github.com/user-attachments/assets/2a643b10-8bc1-4368-9aee-6dddd0fd32f3" />

### Commands used & functions:

`F6` — open sort menu.

`Shift+i` — reverse sort order.

`F5 (t)` — toggle tree view.

# 5. Kill / Nice / Renice (shutting down unresponsive tasks).
Some processes might be unresponsive to any signal thats when you use the `F9 in  htop to kill them forcefully`

Select a process `(arrow keys)`, then:

`F9` — **kill menu** (choose signal; `9 is SIGKILL`, `15 default TERM`). **Be careful.**

<img width="1920" height="947" alt="image" src="https://github.com/user-attachments/assets/94ac4f47-4447-4b01-8510-4c7d2f4157d6" />

`F7` — decrease nice (make process higher priority, needs privileges).

`F8` — increase nice (lower priority).
You can tag multiple processes with `Space` and then `F9` to kill them all at once. 

### Commands used & functions:

`F9` — kill selected processes (choose signal).

`F7 / F8` — adjust nice value (priority).

# 6. Setup & persistent config
In this place you can change the layout of the tool by adding or removing staff from htop 

`F2` — `Setup menu`. Here you can change meters (which bars show).
* columns
* colors
* enable/disble mouse
* set "Show userland threads"
* arrange the header.

<img width="1920" height="947" alt="image" src="https://github.com/user-attachments/assets/a67bb75b-77d3-4ee2-808b-9fb101f0ef1a" />

After you make changes, use `F10` to quit; settings are saved in `~/.config/htop/htoprc` so your layout persists. 

# Commands used & functions:

`F2` — open Setup.

`F10` — quit (settings save to ~/.config/htop/htoprc).


# Quick cheat-sheet: commands & keys.
## Terminal commands:

`htop` — launch the tool.

`htop -d 20` — set delay (in tenths of seconds).

`htop -u USER` — show only USER’s processes.

`htop -p PID[,PID...]` — show only specified PIDs.

`htop --version` — show version.

`man htop` — read manual.

# In-htop keys:

`F1 or ?` — help.

`F2` — setup (change columns, meters).

`F3 or /` — search.

`F4 or \` — filter.

`F5 or t` — tree view.

`F6` — sort by column.

`F7 / F8` — nice decrement/increment.

`F9` — kill.

`Space` — tag process for multi-action.

`u` — untag all.

`Arrow keys / PgUp / PgDn` — navigate.

`Esc` — cancel search/filter.
(If any key combos don’t work, try the lowercase letter alternatives sometimes shown at the footer.)












