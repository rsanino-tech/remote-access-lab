# SSH Remote Access Lab

Practicing remote administration between an Ubuntu laptop and a macOS Mac mini using SSH.

This lab documents a beginner-friendly remote access workflow using real terminal commands, basic network troubleshooting, and careful protection of sensitive information.

---

## Lab Objective

The goal of this lab was to connect from a Linux laptop to a Mac mini over the local network using SSH.

This helped practice:

- SSH remote administration
- client/server communication
- IP-based connectivity testing
- terminal-based troubleshooting
- remote command execution
- safe documentation habits

---

## Lab Environment

| Device | Role | Operating System |
|---|---|---|
| Ubuntu laptop | SSH client | Ubuntu Linux |
| Mac mini | SSH server / remote host | macOS |

```text
Ubuntu Laptop  →  SSH  →  Mac mini
```

Sensitive details such as usernames, internal IP addresses, hostnames, and SSH fingerprints should be redacted before screenshots are published.

---

## Technologies Used

- SSH
- Ubuntu Linux terminal
- macOS terminal
- ICMP / ping
- TCP/IP networking
- macOS Remote Login

---

## Commands Practiced

```bash
ping <redacted-ip>
ssh <redacted-user>@<redacted-ip>
hostname
whoami
uptime
pwd
ls
mkdir
touch
```

---

## Lab Workflow

### 1. Enabled Remote Login on macOS

Remote Login was enabled on the Mac mini so it could accept SSH connections from another system on the same local network.

### 2. Identified the Mac mini IP Address

The local IP address was found from macOS network settings and used as the SSH destination.

### 3. Tested Network Reachability

The Ubuntu laptop used `ping` to confirm that the Mac mini was reachable on the local network.

### 4. Connected with SSH

The Ubuntu laptop initiated an SSH session to the Mac mini using the format:

```bash
ssh <user>@<host-ip>
```

### 5. Verified Remote Access

Commands such as `hostname`, `whoami`, `uptime`, `pwd`, and `ls` were used to confirm that the terminal session was running on the remote Mac mini instead of the local Ubuntu laptop.

---

## Screenshots

Screenshots will be added after sensitive information is redacted.

Recommended screenshot names:

```text
screenshots/
├── 01-ping-connectivity.png
├── 02-ssh-login-redacted.png
├── 03-remote-host-verification.png
├── 04-remote-command-output.png
└── 05-remote-directory-creation.png
```

---

## What Should Be Redacted

Before publishing screenshots, hide:

- personal usernames
- internal IP addresses
- full device names
- SSH fingerprints
- home directory paths
- public IP addresses
- tokens, passwords, or key material

Example redaction format:

```text
10.0.0.25 → 10.x.x.x
personal-username → user
Mac-mini.local → remote-host
```

---

## What I Learned

- The Mac mini acted as the SSH server.
- The Ubuntu laptop acted as the SSH client.
- A successful ping confirmed network reachability.
- SSH allowed terminal-based control of the remote machine.
- Remote commands verified that the session was running on the Mac mini.
- Real troubleshooting requires checking IP address, username, service status, and connection behavior.

---

## Security Notes

This lab was performed only on devices and networks I own or am authorized to access.

SSH should not be exposed directly to the public internet without proper hardening. For remote access from outside the home network, a private VPN-style solution such as Tailscale is preferred over router port forwarding.

---

## Next Steps

- Add redacted screenshots
- Add a command reference
- Add a troubleshooting log
- Test persistent remote sessions using `tmux`
- Add Tailscale for secure remote access from outside the home network
