# SSH Remote Access Lab

This project documents my first successful SSH connection from an Ubuntu laptop to a Mac mini.

The goal was simple:

Learn how remote administration actually works instead of just reading about it.

What started as a basic SSH setup turned into a real troubleshooting session involving:

- incorrect IP addresses
- connection timeouts
- network testing
- service verification
- command-line troubleshooting
- successful remote administration

This was my first time experiencing what it actually feels like to troubleshoot infrastructure problems step by step.

---

# Project Goal

I wanted to:

- remotely access my Mac mini from my Ubuntu laptop
- understand how SSH works
- learn basic networking concepts hands-on
- practice terminal usage
- build confidence using Linux and networking tools

Instead of watching another tutorial, I wanted to actually do it.

---

# Lab Setup

| Device | Purpose |
|---|---|
| Ubuntu Laptop | SSH Client |
| Mac mini | SSH Server |

Connection flow:

```text
Ubuntu Laptop  →  SSH  →  Mac mini
```

---

# What I Did

## Step 1: Enabled Remote Login on the Mac mini

The Mac mini needed to accept SSH connections.

I enabled:

```text
System Settings → General → Sharing → Remote Login
```

This allowed the Mac mini to function as an SSH server.

---

## Step 2: Found the Mac mini IP Address

I located the local IP address of the Mac mini using:

- macOS network settings
- terminal commands

This IP address would later be used for the SSH connection.

---

## Step 3: First SSH Attempt Failed

I attempted to connect from Ubuntu using:

```bash
ssh user@ip-address
```

The connection failed.

At first I thought SSH itself was broken.

It wasn’t.

I had used the wrong IP address.

---

# The Mistake

One of the biggest beginner mistakes I made was accidentally trying to connect to the router instead of the Mac mini.

I confused:

```text
10.0.0.1
```

with the actual Mac mini IP address.

This caused:

- connection timeouts
- confusion
- failed SSH attempts

At first it felt frustrating.

But this ended up becoming the most important part of the project because I learned how troubleshooting actually works.

---

# How I Troubleshot It

Instead of randomly guessing, I started verifying things one step at a time.

## Tested Connectivity with Ping

I used:

```bash
ping <target-ip>
```

to verify whether the Ubuntu laptop could even see the target device.

Once I received replies, I knew:

- the machines could communicate
- the network itself was functioning
- the issue was somewhere else

---

## Verified SSH Configuration

I confirmed:

- Remote Login was enabled
- the Mac mini was reachable
- the correct username was being used

---

## Corrected the IP Address

After realizing I had the wrong IP address, I retried the SSH connection using the correct Mac mini IP.

That changed everything.

---

# Successful SSH Connection

Once the correct IP was used, the SSH session worked successfully.

This was the command:

```bash
ssh user@correct-ip
```

After connecting, I verified the remote session using:

```bash
hostname
whoami
uptime
pwd
ls
```

This confirmed:

- I was connected to the Mac mini
- the Ubuntu laptop was acting as the SSH client
- the Mac mini was acting as the SSH server

---

# Remote Administration Practice

Once connected, I started interacting with the remote system.

I created files and directories remotely:

```bash
mkdir homelab
```

```bash
touch remote-test.txt
```

This was the moment the project really clicked for me.

I realized:

```text
I was controlling another machine remotely through the terminal.
```

That completely changed how networking and Linux felt to me.

---

# Technologies Used

- Ubuntu Linux
- macOS
- SSH
- Terminal
- TCP/IP Networking
- ICMP / ping

---

# Commands Practiced

```bash
ping
ssh
hostname
whoami
uptime
pwd
ls
mkdir
touch
```

---

# What I Learned

This project taught me:

- SSH is client/server based
- troubleshooting matters more than memorization
- incorrect IP addresses are a common real-world issue
- ping helps verify connectivity
- remote administration feels very different from local terminal usage
- networking becomes easier to understand when practiced hands-on

Most importantly:

I learned that making mistakes is part of infrastructure work.

The important part is learning how to isolate the problem and recover from it.

---

# Next Steps

Next I want to:

- add Tailscale for remote access outside my home
- learn tmux for persistent sessions
- remotely manage Ollama from Ubuntu
- expand the homelab environment
- continue building networking projects hands-on
