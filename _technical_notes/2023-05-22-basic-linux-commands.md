---
layout: page
title: "Basic Linux Commands"
date: 2023-05-22
---

This is a short, practical guide for new lab members getting started with the Linux command line.

Official references:
- Ubuntu CLI beginner guide: <https://ubuntu.com/tutorials/command-line-for-beginners>
- Linux man pages overview: <https://man7.org/linux/man-pages/>

## 1) Navigation

```bash
pwd                  # show current directory
ls                   # list files/folders
ls -la               # list with details + hidden files
cd /path/to/folder   # change directory
cd ..                # move up one level
```

## 2) File and folder operations

```bash
touch notes.txt                  # create empty file
cp source.txt backup.txt         # copy file
cp -r project project_backup     # copy folder recursively
mv oldname.txt newname.txt       # rename file
mv file.txt /path/to/dest/       # move file
rm file.txt                      # remove file
rm -r folder/                    # remove folder recursively
mkdir results                    # create folder
```

## 3) View and search text

```bash
cat file.txt                     # print file content
less file.txt                    # scroll through file
head -n 20 file.txt              # first 20 lines
tail -n 20 file.txt              # last 20 lines
grep "pattern" file.txt          # search text in file
grep -R "pattern" folder/        # recursive search in folder
```

## 4) Permissions and ownership

```bash
ls -l                            # show permission bits
chmod u+x script.sh              # add execute for user
chmod 644 file.txt               # rw-r--r--
chown user:group file.txt        # change owner/group (if permitted)
```

## 5) Process management

```bash
ps -ef                           # list running processes
top                              # live process monitor
kill <pid>                       # stop process by PID
kill -9 <pid>                    # force kill (use cautiously)
```

## 6) Disk and system checks

```bash
uname -a                         # system/kernel info
df -h                            # disk usage by filesystem
du -sh *                         # size of files/folders in current dir
free -h                          # memory usage
```

## 7) Help and best practice

```bash
man ls                           # full manual for a command
ls --help                        # quick help
```

Best practice:
- Avoid running destructive commands as root unless necessary.
- Double-check paths before `rm -r`.
- Start with `-n` or dry-run options when available.
- Keep command history readable with comments in scripts.

For lab workflows, combine these basics with the other tutorials on SSH, SLURM, Miniforge, Snakemake, and CWL.
