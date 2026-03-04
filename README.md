# linux-fundamentals
linux-fundamentals/
│
├── README.md
├── basics/
│   ├── commands.md
│   ├── filesystem.md
│   └── editors.md
│
├── permissions/
│   ├── ownership.md
│   └── acl.md
│
├── storage/
│   ├── partitioning.md
│   ├── mounting.md
│   └── fsck.md
│
├── backup-compression/
│   ├── tar-zip.md
│   ├── gzip-bzip.md
│   └── rsync.md
│
├── processes/
│   ├── process-management.md
│   └── performance-monitoring.md
│
└── interview-notes.md

# Linux Fundamentals Notes 🐧

This repository contains complete Linux fundamentals notes based on hands-on system administration lectures.

## Topics Covered
- Linux basic commands
- Filesystem hierarchy
- VI / VIM / NANO editors
- Soft & Hard links
- Permissions & Ownership
- ACL & Advanced permissions
- Runlevels & boot process
- Disk partitioning & mounting
- Filesystems (ext2, ext3, ext4, xfs)
- Backup & compression tools
- Rsync incremental backup
- Process & daemon management
- Performance monitoring
- Interview questions & tasks

## Who Is This For?
- Linux beginners
- System administrators
- DevOps learners
- Interview preparation

# Basic Linux Commands

## Navigation
- `pwd` – Show current directory
- `ls` – List files
- `ls -l` – Long listing
- `ls -a` – Show hidden files
- `cd ..` – Go back one directory

## File Operations
- `touch file.txt` – Create file
- `rm file.txt` – Delete file
- `rm -rf folder` – Force delete directory (dangerous)
- `cp file /path` – Copy file
- `mv old new` – Rename / move file

## Help
- `man command`
- `command --help`

# Linux Editors

## VI / VIM
- `vi file`
- `i` → Insert mode
- `Esc :wq` → Save & exit
- `dd` → Delete line
- `yy` → Copy line
- `p` → Paste
- `%s/old/new/g` → Replace text

## NANO
- `nano file`
- Ctrl + K → Delete line
- Ctrl + U → Paste
- Ctrl + X → Exit

# File Permissions

r = 4, w = 2, x = 1

## Examples
- `chmod 777 file`
- `chmod 750 file`
- `chmod u+rwx file`
- `chown user file`
- `chgrp group file`

## Notes
- Root can override permissions
- `chattr +i file` makes file immutable

# Disk Partitioning

## Commands
- `lsblk`
- `fdisk /dev/sdb`
- `mkfs.ext4 /dev/sdb1`
- `mount /dev/sdb1 /data`
- `df -h`

## Filesystems
- ext2 – non-journaling
- ext3 – journaling
- ext4 – improved performance
- xfs – high performance, snapshots

# Rsync Backup

## Incremental Backup
rsync -avz /source/ /destination/

## Preserve Permissions
rsync -parv /src/ /dest/

## Types of Backup
- Full
- Incremental
- Differential

# Process Management

- `ps -ef`
- `top`
- `htop`
- `kill PID`
- `pkill process`
- `pstree`

## Signals
- SIGTERM (15)
- SIGKILL (9)


## Author
Muhammad Talha
