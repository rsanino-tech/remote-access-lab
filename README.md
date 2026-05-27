# SSH Remote Access Lab: Ubuntu Laptop to Mac mini

## Overview

This lab documents my first successful SSH connection from an Ubuntu laptop to a Mac mini.

The purpose of this project was to practice real remote administration using the terminal, understand how SSH works, troubleshoot connection mistakes, and build confidence working between two machines on the same local network.

This project is focused only on SSH remote access.

---

## Lab Setup

```text
Ubuntu Laptop
      ↓ SSH
Mac mini
```

The Ubuntu laptop was the SSH client.

The Mac mini was the SSH host.

---

## Objectives

- Enable SSH access on the Mac mini
- Connect from Ubuntu using SSH
- Verify network connectivity with ping
- Identify the correct IP address
- Troubleshoot a failed SSH attempt
- Confirm remote access using terminal commands
- Learn how to reduce typing mistakes with Tab autocomplete

---

## Technologies Used

| Tool | Purpose |
|---|---|
| Ubuntu Terminal | Started the SSH connection |
| macOS Remote Login | Allowed SSH access to the Mac mini |
| SSH | Secure remote terminal access |
| Ping | Tested if the Mac mini was reachable |
| Tab Autocomplete | Reduced typos and improved terminal efficiency |

---

## Steps Completed

### 1. Enabled SSH on the Mac mini

On the Mac mini, I enabled Remote Login:

```text
System Settings
→ General
→ Sharing
→ Remote Login
```

This allowed the Mac mini to accept SSH connections.

---

### 2. Found the Mac mini IP address

I located the Mac mini IP address from macOS network settings.

This IP address was needed so the Ubuntu laptop could connect to the correct machine over the local network.

---

### 3. Tested network connectivity

From the Ubuntu laptop, I tested connectivity with:

```bash
ping <mac-mini-ip-address>
```

The ping replies confirmed that the Ubuntu laptop could see the Mac mini on the network.

---

### 4. Started the SSH connection

From the Ubuntu laptop, I started the SSH connection with:

```bash
ssh username@mac-mini-ip-address
```

After entering the Mac mini password, the SSH connection was successful.

---

## Commands Practiced

```bash
ping <ip-address>
ssh username@ip-address
hostname
whoami
uptime
pwd
ls
touch remote-test.txt
```

---

## Mistake Made

During the first SSH attempt, I used the wrong IP address.

I accidentally tried to connect to the router/gateway IP instead of the Mac mini IP address.

That caused the SSH connection to fail.

---

## What I Learned From the Mistake

This mistake helped me understand that:

- The router/gateway IP is not the same as the Mac mini IP
- Each device on the network has its own IP address
- Ping is useful for confirming whether a device is reachable
- SSH requires the correct username and the correct host IP
- Troubleshooting is part of the learning process

Instead of guessing, I learned to slow down and verify one thing at a time.

---

## Tab Autocomplete Lesson

While working in the terminal, I learned that pressing `Tab` helps autocomplete commands, filenames, and folder names.

This is useful because it:

- Reduces typing mistakes
- Speeds up command-line work
- Helps avoid misspelled filenames or paths
- Makes terminal navigation more efficient

Example:

```bash
cd Doc<Tab>
```

The terminal can complete the folder name if it exists.

This is a small skill, but it makes working in Linux much smoother.

---

## Verification

After connecting through SSH, I verified that I was inside the Mac mini by running:

```bash
hostname
whoami
uptime
```

I also created a test file remotely:

```bash
touch remote-test.txt
```

Then I confirmed it existed:

```bash
ls
```

---

## Key Takeaways

This lab helped me understand:

- How SSH works at a beginner level
- How one machine can remotely access another
- The difference between a client and a host
- Why the correct IP address matters
- How to troubleshoot failed connections
- How terminal efficiency improves with Tab autocomplete

This project was my first successful hands-on SSH remote access lab.