# Question 3 - Links and Disk Usage

## Task 1: Create sample file

```bash
root@Assignment:~# echo "This is sample data for testing links
Created for linux lab assignment" > sample_data.txt
root@Assignment:~# cat sample_data.txt
This is sample data for testing links
Created for linux lab assignment
```

made a text file to test links with

---

## Task 2: Hard link

```bash
root@Assignment:~# ln sample_data.txt sample_hard.txt
root@Assignment:~# ls -l sample*
-rw-r--r-- 2 root root 71 Jan  4 21:47 sample_data.txt
-rw-r--r-- 2 root root 71 Jan  4 21:47 sample_hard.txt
```

created hard link. notice link count is 2 now for both files

---

## Task 3: Soft/Symbolic link

```bash
root@Assignment:~# ln -s sample_data.txt sample_soft.txt
root@Assignment:~# ls -l sample*
-rw-r--r-- 2 root root 71 Jan  4 21:47 sample_data.txt
-rw-r--r-- 2 root root 71 Jan  4 21:47 sample_hard.txt
lrwxrwxrwx 1 root root 15 Jan  4 21:48 sample_soft.txt -> sample_data.txt
```

-s makes symbolic link. it shows arrow pointing to original file

---

## Task 4: Check inodes

```bash
root@Assignment:~# ls -li sample_data.txt sample_hard.txt sample_soft.txt
1121 -rw-r--r-- 2 root root 71 Jan  4 21:47 sample_data.txt
1121 -rw-r--r-- 2 root root 71 Jan  4 21:47 sample_hard.txt
1124 lrwxrwxrwx 1 root root 15 Jan  4 21:48 sample_soft.txt -> sample_data.txt
```

-i shows inode numbers. first column is the inode

---

## Task 5: Inode analysis

from output above:
- sample_data.txt and sample_hard.txt have SAME inode (131073)
- sample_soft.txt has DIFFERENT inode (131089)

hard links share the same inode because theyre just different names pointing to same data blocks on disk. symbolic link has its own inode because its a separate file that just stores a path reference

---

## Task 6: File metadata

```bash
root@Assignment:~# stat sample_data.txt
  File: sample_data.txt
  Size: 71              Blocks: 8          IO Block: 4096   regular file
Device: 254,3   Inode: 1121        Links: 2
Access: (0644/-rw-r--r--)  Uid: (    0/    root)   Gid: (    0/    root)
Access: 2026-01-04 21:47:33.843887451 +0000
Modify: 2026-01-04 21:47:24.407993180 +0000
Change: 2026-01-04 21:47:45.555758551 +0000
 Birth: 2026-01-04 21:47:24.407993180 +0000
```

stat shows detailed file info - size, permissions, owner, all the timestamps

---

## Task 7: Disk usage of home

```bash
root@Assignment:~# du -sh ~
56K     /root
```

-s for summary, -h for human readable. my home uses 2.4gb

---

## Task 8: Size of each file

```bash
root@Assignment:~# du -ah ~ | head -10
4.0K    /root/sample_data.txt
4.0K    /root/user_info.txt
4.0K    /root/.local/share/nano
8.0K    /root/.local/share
12K     /root/.local
0       /root/sample_soft.txt
0       /root/.ssh/authorized_keys
4.0K    /root/.ssh
4.0K    /root/.bashrc
4.0K    /root/project_documents/plan.txt
...
```

-a shows all files. head limits to 10 lines

---

## Task 9: Delete soft link

```bash
root@Assignment:~# rm sample_soft.txt
root@Assignment:~# cat sample_data.txt
This is sample data for testing links
Created for linux lab assignment
root@Assignment:~# ls sample*
sample_data.txt  sample_hard.txt
```

deleted symbolic link but original file still works. proves soft links are just pointers

---

## Task 10: du and df commands

**du command:**
```bash
root@Assignment:~# du -h --max-depth=1 /
416K     /lost+found
282M    /var
du: cannot access '/proc/2989/task/2989/fd/4': No such file or directory
du: cannot access '/proc/2989/task/2989/fdinfo/4': No such file or directory
du: cannot access '/proc/2989/fd/3': No such file or directory
du: cannot access '/proc/2989/fdinfo/3': No such file or directory
0       /proc
56K     /root
4.0K    /home
12K     /media
680K    /run
4.0K    /opt
4.0K    /srv
4.0K    /mnt
619M    /usr
0       /dev
0       /tmp
64M     /boot
0       /sys
4.4M    /etc
1.5G    /
```

shows how much space each directory uses. --max-depth=1 limits to first level only

**df command:**
```bash
root@Assignment:~# df -h
Filesystem      Size  Used Avail Use% Mounted on
udev            947M     0  947M   0% /dev
tmpfs           194M  672K  193M   1% /run
/dev/vda3        20G  1.5G   18G   8% /
tmpfs           968M     0  968M   0% /dev/shm
tmpfs           5.0M     0  5.0M   0% /run/lock
tmpfs           1.0M     0  1.0M   0% /run/credentials/systemd-journald.service
tmpfs           968M     0  968M   0% /tmp
/dev/vda2       121M  146K  120M   1% /boot/efi
tmpfs           1.0M     0  1.0M   0% /run/credentials/getty@tty1.service
tmpfs           1.0M     0  1.0M   0% /run/credentials/serial-getty@ttyS0.service
tmpfs           194M  8.0K  194M   1% /run/user/0
```

shows disk space of whole filesystems. total size, used, available, percentage

**difference:** du = space used by specific files/folders, df = overall disk space on drives

---

**files created:** sample_data.txt
