# Question 2 - File and Directory Management

## Task 1: Create documents folder

```bash
root@Assignment:~# mkdir ~/documents
```

created documents folder in home directory

---

## Task 2: Create plan.txt

```bash
root@Assignment:~# cd ~/documents
root@Assignment:~/documents# touch plan.txt
```

went into documents and made empty plan.txt file

---

## Task 3: Add content to file

```bash
root@Assignment:~/documents# echo "Project Plan: Web App Development
- Phase 1: Requirements gathering
- Phase 2: Design  
- Phase 3: Implementation
- Phase 4: Testing" > plan.txt
root@Assignment:~/documents# cat plan.txt
Project Plan: Web App Development
- Phase 1: Requirements gathering
- Phase 2: Design  
- Phase 3: Implementation
- Phase 4: Testing
```

wrote project notes into file using echo

---

## Task 4: Check file permissions

```bash
root@Assignment:~/documents# ls -l plan.txt
-rw-r--r-- 1 root root 124 Jan  5 01:16 plan.txt
```

shows file permissions rw-r--r-- (read/write for owner, read for others), owned by root, size 124 bytes

---

## Task 5: Copy file

```bash
root@Assignment:~/documents# cp plan.txt plan_copy.txt
root@Assignment:~/documents# ls
plan.txt  plan_copy.txt
```

copied plan.txt to make a backup

---

## Task 6: Rename directory

```bash
root@Assignment:~/documents# cd ~
root@Assignment:~# mv documents project_documents
root@Assignment:~# ls -d project_documents
project_documents
```

renamed documents folder to project_documents using mv

---

## Task 7: Create archive folder

```bash
root@Assignment:~# mkdir ~/project_documents/archive
```

made archive subfolder for old files

---

## Task 8: Move file to archive

```bash
root@Assignment:~# mv ~/project_documents/plan_copy.txt ~/project_documents/archive/
root@Assignment:~# ls ~/project_documents/archive/
plan_copy.txt
```

moved the copy into archive folder

---

## Task 9: Recursive listing

```bash
root@Assignment:~# ls -lR ~/project_documents
/root/project_documents:
total 8
drwxr-xr-x 2 root root 4096 Jan  5 01:17 archive
-rw-r--r-- 1 root root  124 Jan  5 01:16 plan.txt

/root/project_documents/archive:
total 4
-rw-r--r-- 1 root root 124 Jan  5 01:16 plan_copy.txt
```

-R shows everything recursively. can see the whole folder structure

---

## Task 10: Get absolute path

```bash
root@Assignment:~# realpath ~/project_documents/archive/plan_copy.txt
/root/project_documents/archive/plan_copy.txt
```

realpath gives full absolute path of the file

---

**files created:** plan.txt
