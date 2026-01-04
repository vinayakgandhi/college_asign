# Question 4 - Process Management & System Monitoring

## Task 1: System uptime

```bash
root@Assignment:~# uptime
 21:53:21 up  1:52,  2 users,  load average: 0.00, 0.00, 0.00
```

system has been running for 1 hour 52 minutes since last reboot

---

## Task 2: My processes

```bash
root@Assignment:~# ps -u root
    PID TTY          TIME CMD
      1 ?        00:00:01 systemd
      2 ?        00:00:00 kthreadd
      3 ?        00:00:00 pool_workqueue_release
      4 ?        00:00:00 kworker/R-kvfree_rcu_reclaim
      5 ?        00:00:00 kworker/R-rcu_gp
      6 ?        00:00:00 kworker/R-sync_wq
      7 ?        00:00:00 kworker/R-slub_flushwq
      8 ?        00:00:00 kworker/R-netns
     11 ?        00:00:00 kworker/0:0H-kblockd
     12 ?        00:00:00 kworker/u512:0-flush-254:0
     13 ?        00:00:00 kworker/R-mm_percpu_wq
     14 ?        00:00:00 rcu_tasks_kthread
     15 ?        00:00:00 rcu_tasks_rude_kthread
     16 ?        00:00:00 rcu_tasks_trace_kthread
     17 ?        00:00:00 ksoftirqd/0
     18 ?        00:00:03 rcu_preempt
     19 ?        00:00:00 rcu_exp_par_gp_kthread_worker/1
     20 ?        00:00:00 rcu_exp_gp_kthread_worker
     21 ?        00:00:00 migration/0
     22 ?        00:00:00 idle_inject/0
     23 ?        00:00:00 cpuhp/0
     25 ?        00:00:00 kdevtmpfs
     26 ?        00:00:00 kworker/R-inet_frag_wq
     27 ?        00:00:00 kauditd
     28 ?        00:00:00 khungtaskd
     30 ?        00:00:00 oom_reaper
     32 ?        00:00:00 kworker/R-writeback
     33 ?        00:00:00 kcompactd0
     34 ?        00:00:00 ksmd
     35 ?        00:00:00 khugepaged
     36 ?        00:00:00 kworker/R-kintegrityd
     37 ?        00:00:00 kworker/R-kblockd
     38 ?        00:00:00 kworker/R-blkcg_punt_bio
     39 ?        00:00:00 irq/9-acpi
     40 ?        00:00:00 kworker/R-tpm_dev_wq
     41 ?        00:00:00 kworker/R-edac-poller
     42 ?        00:00:00 kworker/R-devfreq_wq
     43 ?        00:00:00 kworker/0:1H-kblockd
     44 ?        00:00:00 kswapd0
     51 ?        00:00:00 kworker/R-kthrotld
     55 ?        00:00:00 irq/24-aerdrv
     56 ?        00:00:00 irq/25-aerdrv
     57 ?        00:00:00 irq/26-aerdrv
     58 ?        00:00:00 irq/27-aerdrv
     59 ?        00:00:00 irq/28-aerdrv
     60 ?        00:00:00 irq/29-aerdrv
     61 ?        00:00:00 irq/30-aerdrv
     62 ?        00:00:00 irq/31-aerdrv
     63 ?        00:00:00 irq/32-aerdrv
     64 ?        00:00:00 irq/33-aerdrv
     65 ?        00:00:00 irq/34-aerdrv
     66 ?        00:00:00 irq/35-aerdrv
     67 ?        00:00:00 irq/36-aerdrv
     68 ?        00:00:00 irq/37-aerdrv
     69 ?        00:00:00 irq/38-aerdrv
     70 ?        00:00:00 irq/39-aerdrv
     71 ?        00:00:00 kworker/R-acpi_thermal_pm
     72 ?        00:00:00 kworker/R-mld
     73 ?        00:00:00 kworker/R-ipv6_addrconf
     78 ?        00:00:00 kworker/R-kstrp
     82 ?        00:00:00 kworker/u513:0
    185 ?        00:00:00 watchdogd
    186 ?        00:00:00 scsi_eh_0
    187 ?        00:00:00 kworker/R-scsi_tmf_0
    188 ?        00:00:00 scsi_eh_1
    189 ?        00:00:00 kworker/R-scsi_tmf_1
    190 ?        00:00:00 scsi_eh_2
    191 ?        00:00:00 kworker/R-scsi_tmf_2
    193 ?        00:00:00 scsi_eh_3
    194 ?        00:00:00 kworker/R-scsi_tmf_3
    195 ?        00:00:00 kworker/R-ata_sff
    196 ?        00:00:00 scsi_eh_4
    197 ?        00:00:00 kworker/R-scsi_tmf_4
    198 ?        00:00:00 scsi_eh_5
    199 ?        00:00:00 kworker/R-scsi_tmf_5
    200 ?        00:00:00 scsi_eh_6
    201 ?        00:00:00 kworker/R-scsi_tmf_6
    202 ?        00:00:00 scsi_eh_7
    203 ?        00:00:00 kworker/R-scsi_tmf_7
    204 ?        00:00:00 scsi_eh_8
    205 ?        00:00:00 kworker/R-scsi_tmf_8
    206 ?        00:00:00 scsi_eh_9
    207 ?        00:00:00 kworker/R-scsi_tmf_9
    208 ?        00:00:00 kworker/u512:4-events_unbound
    216 ?        00:00:00 kworker/R-ttm
    240 ?        00:00:00 jbd2/vda3-8
    241 ?        00:00:00 kworker/R-ext4-rsv-conversion
    255 ?        00:00:02 kworker/0:6-events
    299 ?        00:00:00 systemd-journal
    363 ?        00:00:00 systemd-udevd
    365 ?        00:00:00 psimon
    400 ?        00:00:00 kworker/R-cryptd
    795 ?        00:00:00 cron
    802 ?        00:00:00 qemu-ga
    807 ?        00:00:00 systemd-logind
    819 ?        00:00:00 sshd
    825 tty1     00:00:00 agetty
    827 ttyS0    00:00:00 agetty
    841 ?        00:00:00 sshd-session
    852 ?        00:00:00 psimon
    854 ?        00:00:00 systemd
    856 ?        00:00:00 (sd-pam)
    861 ?        00:00:00 psimon
    870 ?        00:00:00 sshd-session
    871 pts/0    00:00:00 bash
   1297 ?        00:00:00 kworker/0:0-cgroup_destroy
   1353 ?        00:00:00 kworker/u512:1-flush-254:0
   1520 ?        00:00:00 sshd-session
   1528 ?        00:00:00 sshd-session
   1529 pts/1    00:00:00 bash
   3026 ?        00:00:00 sshd-session
   3029 ?        00:00:00 sshd-session
   3032 pts/1    00:00:00 ps
```

lists all processes running under root user
<img width="1412" height="1646" alt="image" src="https://github.com/user-attachments/assets/b8de5a60-8274-42cb-98dd-03a296fb791f" />
<img width="1412" height="1646" alt="image" src="https://github.com/user-attachments/assets/656546d7-0347-4343-8a5a-6a554c9b20af" />
<img width="1256" height="1774" alt="image" src="https://github.com/user-attachments/assets/2f8e278e-4d69-45ca-9bf8-6bb12ef5a822" />

---

## Task 3: Highest CPU process

```bash
root@Assignment:~# ps aux --sort=-%cpu | head -5
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root          18  0.0  0.0      0     0 ?        I    20:00   0:03 [rcu_preempt]
root         255  0.0  0.0      0     0 ?        I    20:00   0:02 [kworker/0:6-events]
root           1  0.0  0.7  23920 14344 ?        Ss   20:00   0:01 /sbin/init
root         299  0.0  0.5  34648 11568 ?        Ss   20:00   0:00 /usr/lib/systemd/systemd-journald
```

sorted by cpu usage. init process using most cpu but its very low (0.1%)

---

## Task 4: Background process

```bash
root@Assignment:~# sleep 300 &
[1] 3086
root@Assignment:~# jobs
[1]+  Running                 sleep 300 &
```

& runs command in background. jobs shows its running with job number [1] and PID 1456

---

## Task 5: Change process priority

```bash
root@Assignment:~# ps -o pid,ni,comm -p $$
    PID  NI COMMAND
   1529   0 bash
root@Assignment:~# renice 10 -p 1529
1529 (process ID) old priority 0, new priority 10
rroot@Assignment:~# ps -o pid,ni,comm -p $$
    PID  NI COMMAND
   1529  10 bash
```

changed nice value from 0 to 10. higher nice = lower priority. process is being "nicer" to others

---

## Task 6: Memory usage

```bash
root@Assignment:~# free -h
               total        used        free      shared  buff/cache   available
Mem:           1.9Gi       307Mi       1.5Gi       680Ki       273Mi       1.6Gi
Swap:          511Mi          0B       511Mi
```

shows memory in human readable format:
- 1.9gb total ram
- 307mb used
- 1.5gb free
- 680kb in cache
- 273mb in buffer
- 1.6gb available

---

## Task 7: Disk space

```bash
root@Assignment:~# df -h ~
Filesystem      Size  Used Avail Use% Mounted on
/dev/vda3        20G  1.5G   18G   8% /
```

shows disk space where home directory is. 50gb total, 8.2gb used, 39gb free

---

## Task 8: Current shell

```bash
root@Assignment:~# echo $SHELL
/bin/bash
root@Assignment:~# echo $0
-bash
```

$SHELL shows default shell path. im using bash

---

## Task 9: Output redirection

```bash
root@Assignment:~# uname -a > system_report.txt
root@Assignment:~# date >> system_report.txt
root@Assignment:~# uptime >> system_report.txt
root@Assignment:~# cat system_report.txt
Linux Assignment 6.12.38+deb13-amd64 #1 SMP PREEMPT_DYNAMIC Debian 6.12.38-1 (2025-07-16) x86_64 GNU/Linux
Sun Jan  4 09:59:45 PM GMT 2026
 21:59:57 up  1:59,  2 users,  load average: 0.00, 0.00, 0.00
```

> writes to file (overwrites), >> appends. saved system info to file

---
<img width="1738" height="1604" alt="image" src="https://github.com/user-attachments/assets/ed835de9-175a-46bc-8af9-e5ca83952b7d" />

---

## Task 10: ncdu tool

```bash
root@Assignment:~# ncdu /
ncdu 1.22 ~ Use the arrow keys to navigate, press ? for help                                                                                  
--- / ----------------------------------------------------------------------------------------------------------------------------------------
  618.3 MiB [####################] /usr                                                                                                       
  512.0 MiB [################    ]  swap.img
  281.8 MiB [#########           ] /var
   63.0 MiB [##                  ] /boot
    4.4 MiB [                    ] /etc
  680.0 KiB [                    ] /run
   60.0 KiB [                    ] /root
e  16.0 KiB [                    ] /lost+found
   12.0 KiB [                    ] /media
e   4.0 KiB [                    ] /srv
e   4.0 KiB [                    ] /opt
e   4.0 KiB [                    ] /mnt
e   4.0 KiB [                    ] /home
.   0.0   B [                    ] /proc
    0.0   B [                    ] /sys
    0.0   B [                    ] /dev
    0.0   B [                    ] /tmp
@   0.0   B [                    ]  initrd.img.old
@   0.0   B [                    ]  initrd.img
@   0.0   B [                    ]  vmlinuz.old
@   0.0   B [                    ]  vmlinuz
@   0.0   B [                    ]  lib64
@   0.0   B [                    ]  sbin
@   0.0   B [                    ]  lib
@   0.0   B [                    ]  bin















*Total disk usage:   1.4 GiB   Apparent size: 128.0 TiB   Items: 135655       
```

ncdu is interactive disk usage viewer:
- arrow keys to navigate between folders
- enter to go inside a folder
- d to delete (with confirmation)
- q to quit

much better than du because you can explore visually and see which folders are taking space
<img width="2324" height="1708" alt="image" src="https://github.com/user-attachments/assets/b3474178-71f5-4664-81af-38af92832a12" />

---

**files created:** system_report.txt
