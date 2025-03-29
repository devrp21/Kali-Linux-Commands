
# Linux Commands Reference Guide

This document provides a comprehensive list of essential Linux commands, categorized for ease of use. These commands are useful for file management, user management, permissions, and more.

---

## 📂 **Directory and File Listing**
| Command | Description |
|---------|-------------|
| `ls` | List the contents of the current directory. |
| `ls -la` | List all files, including hidden ones (`-a`), in a detailed format. |
| `ls > abc.txt` | Save the output of the `ls` command to a file named `abc.txt`. |
| `cat abc.txt` | Display the contents of `abc.txt`. |
| `cat abc.txt | sort | grep ab` | Print the contents of `abc.txt`, sort them, and filter lines containing the string `ab`. |

---

## 🖥️ **Terminal Management**
| Command | Description |
|---------|-------------|
| `tmux` | Start a tmux session to manage multiple terminal windows. Use `Ctrl + B` to rename windows. |
| `exit` | Close the current shell session. |
| `clear` | Clear the terminal screen. |

---

## 👤 **User Management**
| Command | Description |
|---------|-------------|
| `useradd -m kali -G sudo -s /bin/bash` | Add a user `kali` to the `sudo` group with `/bin/bash` shell and create a home directory. |
| `passwd kali` | Set a password for the user `kali`. |
| `su kali` | Switch to user `kali`. |
| `sudo -l` | Display the commands the current user can run with `sudo` privileges. |
| `id` | Display user ID (UID) and group ID (GID) information. |
| `w` or `who` | Show currently logged-in users. |
| `userdel kali` | Delete the user `kali`. |
| `last` | Show the list of last logged-in users. |

---

## 👥 **Group Management**
| Command | Description |
|---------|-------------|
| `groupadd hackers` | Create a new group called `hackers`. |
| `usermod -aG hackers kali` | Add user `kali` to the `hackers` group. |
| `cat /etc/group` | Display all groups available in the system. |

---

## 📄 **File and Directory Operations**
| Command | Description |
|---------|-------------|
| `touch abc.txt` | Create an empty file named `abc.txt`. |
| `file abc.txt` | Display the file type of `abc.txt`. |
| `cp abc.txt /home/kali` | Copy `abc.txt` to `/home/kali`. |
| `mv abc.txt /home/kali` | Move `abc.txt` to `/home/kali`. |
| `mv abc.txt ab.txt` | Rename `abc.txt` to `ab.txt`. |
| `rm abc.txt` | Remove the file `abc.txt`. |
| `echo 'echo test' > test.sh` | Create a file `test.sh` with the content `echo test`. |
| `chmod 774 test.sh` | Set file permissions to `rwx` for the owner and group, and `r--` for others. |
| `chmod +x test.sh` | Make `test.sh` executable. |

---

## 🔍 **Search and Locate Files**
| Command | Description |
|---------|-------------|
| `updatedb` | Update the database used by `locate`. |
| `locate abc.txt` | Find the location of `abc.txt`. |
| `locate *.sh -n 3` | Find the first 3 files with the `.sh` extension. |
| `find /root -name "file.txt"` | Find `file.txt` in the `/root` directory. |
| `find / -size +1G 2> /dev/null` | Find files larger than 1 GB and ignore errors. |
| `which python` | Show the path of the `python` binary. |
| `$PATH` | Show the directories searched for executables. |

---

## 🗜️ **File Compression and Archiving**
| Command | Description |
|---------|-------------|
| `tar cf compress.tar files` | Create a `.tar` archive named `compress.tar` from `files`. |
| `tar xf compress.tar` | Extract the contents of `compress.tar`. |
| `tar cfz compress.tar.gz files` | Create a `.tar.gz` archive from `files`. |
| `tar xfz compress.tar.gz` | Extract the contents of `compress.tar.gz`. |
| `gzip file.txt > compressed.txt.gz` | Create a `.gz` compressed file. |
| `gzip -d compress.txt.gz` | Decompress a `.gz` file. |
| `tar cfj compressed.tar.bz2 files` | Create a `.tar.bz2` compressed archive from `files`. |
| `tar xfj compressed.tar.bz2` | Extract the contents of `compressed.tar.bz2`. |
| `zip compress.zip files` | Create a `.zip` file from `files`. |
| `unzip compress.zip` | Extract the contents of `compress.zip`. |

---

## ➡️ **Redirection and Pipes**
| Command | Description |
|---------|-------------|
| `command > file` | Redirect output to a file (overwrite). |
| `command >> file` | Redirect output to a file (append). |
| `command 2> /dev/null` | Redirect errors to `/dev/null` (suppress errors). |
| `command1 | command2` | Pipe the output of `command1` to `command2`. |

---

## 🏆 **Best Practices**
- Always use `sudo` when modifying system files or installing packages.
- Use `man <command>` to see detailed documentation on any command.
- Combine `grep`, `sort`, and `awk` for powerful data filtering and processing.

---

© 2025 Linux Commands Guide. All Rights Reserved.
