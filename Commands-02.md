# Additional Linux Commands

## Directory and File Navigation
- `pwd` : To get the current working directory.
- `cd /home` : To change current working directory to `/home`.
- `cd ~` : To go to your current user's home directory.
- `mkdir abc` : To create the `abc` directory.

## File and Directory Operations
- `cp -r [source_dir] [destination_dir]` : To copy a file or directory. `-r` for recursive copy.
- `mv -r [source_dir] [destination_dir]` : To move a file or directory. `-r` for recursive move.
- `rm -r [folder_to_delete]` : To remove/delete a directory and its contents.
- `lsblk` : To display disk list.

## Mounting and Unmounting
- `mkdir /mnt/usb` : Create a folder for mounting a USB drive.
- `mount /dev/sdb1 /mnt/usb` : Mount `/dev/sdb1` to `/mnt/usb`.
- `umount /mnt/usb` : Unmount the USB.

## File Viewing
- `head -n 5 abc.txt` : Print the first 5 lines of `abc.txt`.
- `tail -n 5 abc.txt` : Print the last 5 lines of `abc.txt`.
- `more abc.txt` : Browse through large files.
- `less abc.txt` : Similar to `more`, but faster and more efficient.

## Sorting and Searching
- `sort ab.txt > ab_sort.txt` : Sort the contents of `ab.txt` and save them in `ab_sort.txt`.
- `uniq ab.txt > ab_uniq.txt` : Save unique values from `ab.txt` to `ab_uniq.txt`.
- `grep -irl "password" /` : Search for "password" in all directories. `-i` (ignore case), `-r` (recursive), `-l` (print filenames).
- `grep -c "password" rockyou.txt` : Count occurrences of "password" in `rockyou.txt`.

## Text Processing
- `awk '/root/' /etc/passwd` : Search for the word "root" in `/etc/passwd`.
- `awk -F ':' '/root/{print $2}' /etc/shadow` : Extract the second field (password hash) from `/etc/shadow` using `:` as a delimiter.
- `cat /etc/shadow | grep "root" | cut -d ":" -f 2` : Extract the second field using `cut`.

## Remote Access
- `rdesktop [windows_ip] -u [username] -p [password]` : Connect to a Windows remote desktop.
- `ssh username@ipaddress` : Connect to a remote machine via SSH.
- `service ssh start` : Start the SSH service.
- `service ssh stop` : Stop the SSH service.
- `systemctl enable ssh` : Enable SSH service to start on boot.
- `service ssh status` : Check the status of the SSH service.
- `ssh username@ip -p port` : Connect to SSH on a specified port.

