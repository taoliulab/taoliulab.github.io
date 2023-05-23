---
layout: page
title: "Basic Linux Commands"
date: 2023-05-22
---

# 1. Navigating the File System

- `pwd`: **Print Working Directory.** This command displays the current directory.

- `cd`: **Change Directory.** Navigate between directories. 
  - Usage: `cd [directory_name]`. 
  - For example, `cd /home/user/Documents` will navigate to the Documents directory.

- `ls`: **List.** This command lists files and directories in the current directory.
  - Use `ls -l` for a detailed list, or `ls -a` to see hidden files.

You can learn more about navigating the Linux file system [here](https://ubuntu.com/tutorials/command-line-for-beginners#1-overview).

# 2. File Operations

- `touch`: Create a new empty file.
  - Usage: `touch [file_name]`.

- `cp`: **Copy.** Copy files or directories.
  - Usage: `cp [source_file] [destination_directory]`.

- `mv`: **Move.** Move or rename files or directories.
  - Usage: `mv [source_file] [destination_directory]`.

- `rm`: **Remove.** Delete files or directories.
  - Usage: `rm [file_name]`.

More details about file operations can be found [here](https://www.howtogeek.com/412055/37-important-linux-commands-you-should-know/).

# 3. Permissions

- `chmod`: **Change Mode.** Change the permissions of a file or directory.
  - Usage: `chmod [permissions] [file_name]`. 

Read more about permissions [here](https://linuxhandbook.com/linux-file-permissions/).

# 4. Process Management

- `ps`: **Process Status.** Show running processes.

- `top`: Display an ongoing, updated list of running processes.

- `kill`: Terminate a process.
  - Usage: `kill [process_id]`.

You can find more information about process management [here](https://www.digitalocean.com/community/tutorials/how-to-manage-processes-in-linux).

# 5. System Information

- `uname`: Display system information.

- `df`: **Disk Free.** Show disk usage.

- `free`: Show memory usage.

Check out this [link](https://www.tecmint.com/linux-commands-cheat-sheet/) for more system information commands.

Remember, to learn more about any command, you can use the `man` command, which stands for "manual". For example, `man ls` will show you the manual for the `ls` command.

Please note that many of these commands will require you to have appropriate permissions in your Linux system to run. Be cautious when using commands that modify files or processes, especially when running commands as the root user. 

This guide should help you get started with basic Linux command line operations. As you become more comfortable, you can explore more complex commands and procedures. Happy learning!

