---
layout: page 
title: "Basic SSH Usages"
date: 2023-06-02 
---

# Using SSH to Login to the CCR Server

SSH is a secure protocol used to log in to remote servers. It provides a secure channel over an unsecured network and is widely used for remote command-line login and remote command execution.

Here's how to use SSH to log in to the CCR server:

1. Open a terminal window.

2. To connect to the CCR server, type:

```bash
ssh username@vortex.ccr.buffalo.edu
```

Replace `username` with your actual username on the CCR server.

3. The first time you connect to the CCR server, you'll see a message like this:

```bash
The authenticity of host 'vortex.ccr.buffalo.edu (xxx.xxx.xxx.xxx)' can't be established.
ECDSA key fingerprint is SHA256:********************************.
Are you sure you want to continue connecting (yes/no)?
```

Type `yes` and press Enter. This will add the CCR server to your list of known hosts.

4. You'll be prompted to enter your password. Type your password and press Enter. Note that you won't see any characters appear as you type your password. This is a security feature.

Once you're logged in, you can start using the CCR server.

# Using SCP to Transfer Files to the CCR server

SCP is a secure file transfer protocol that uses SSH for data transfer. Here's how to use SCP to transfer files to the CCR server:

1. Open a terminal window.

2. To copy a file to the CCR server, type:

```bash
scp /path/to/local/file username@vortex.ccr.buffalo.edu:/path/to/remote/directory
```

Replace `/path/to/local/file` with the path to the file on your local machine that you want to copy, and replace `/path/to/remote/directory` with the path to the directory on the CCR server where you want to copy the file to.

3. You'll be prompted to enter your password. Type your password and press Enter. The file will then be copied to the CCR server.

Remember to replace `username` with your actual username on the CCR server in both the SSH and SCP commands. 

Please note that you need appropriate permissions to copy files to the CCR server. If you encounter any permission issues, contact your system administrator.

This guide should help you get started with SSH and SCP for accessing and transferring files to the CCR server. As always, be sure to follow best practices for security, such as using strong passwords, not sharing your credentials, and logging out when you're done.

For more information, you can check out the man pages for SSH and SCP (`man ssh`, `man scp`), or visit the online manual pages for [SSH](https://man7.org/linux/man-pages/man1/ssh.1.html) and [SCP](https://man7.org/linux/man-pages/man1/scp.1.html).

# Using SSH Keys for Login

SSH keys consist of a private key and a public key. The private key stays on your local machine and should be kept secret. The public key is copied to the CCR server. the CCR server uses the public key to verify your identity by checking it against your private key.

## 1. Generate SSH Keys

First, you need to generate an SSH key pair on your local machine. 

1. Open a terminal window.

2. Type the following command and press Enter:

```bash
ssh-keygen -t rsa -b 4096
```

This command generates a 4096-bit RSA key pair.

3. You'll be prompted to enter a file in which to save the keys. You can press Enter to accept the default location (`~/.ssh/id_rsa`).

4. You'll be asked to enter a passphrase. You can either enter a passphrase or leave it empty for no passphrase. A passphrase adds an additional layer of security to prevent unauthorized users from using your key, even if they can access your files.

## 2. Copy the Public Key to the CCR Server

Next, you need to copy your public key to the CCR server. 

1. Use the following command to copy your public key to the CCR server:

```bash
ssh-copy-id username@vortex.ccr.buffalo.edu
```

Replace `username` with your actual username on the CCR server.

2. You'll be prompted to enter your password. Type your password and press Enter. Your public key will be appended to the `~/.ssh/authorized_keys` file on the CCR server.

## 3. Login to the CCR server Using SSH Keys

Now you can log in to the CCR server using SSH keys instead of a password:

1. Type the following command and press Enter:

```bash
ssh username@vortex.ccr.buffalo.edu
```

If you set a passphrase for your key, you'll be prompted to enter it. Note that this is the passphrase for the key, not the password for the CCR server.

Once you're logged in, you can start using the CCR server. 

Please note that you should protect your private key as you would a password. Don't share your private key with anyone. If you think your key has been compromised, you should generate a new one.

For more information, you can check out the [SSH Key Guide](https://www.ssh.com/ssh/key/) by SSH.COM.
