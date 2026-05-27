# SSH Lab Session Log

## Objective

Establish a successful SSH connection from an Ubuntu laptop to a Mac mini over the local network.

---

## Initial Challenges

### Incorrect IP Address

An incorrect IP address was initially used during SSH attempts.

This caused connection timeouts and failed authentication attempts.

Important networking lesson learned:

```text
10.0.0.1 is commonly the router or gateway.
```

The actual Mac mini IP address needed to be identified before the SSH connection could succeed.

---

## Connectivity Testing

The `ping` command was used to confirm network reachability between the Ubuntu laptop and the Mac mini.

Successful replies confirmed:

- local network connectivity
- correct target IP
- working TCP/IP communication

---

## SSH Service Verification

Remote Login on macOS was enabled to allow inbound SSH connections.

Once enabled correctly, the Mac mini accepted SSH connections from the Ubuntu laptop.

---

## Successful SSH Connection

A successful SSH session was established using:

```bash
ssh <user>@<redacted-ip>
```

The Ubuntu laptop became the SSH client.

The Mac mini acted as the SSH server.

---

## Remote Verification

The following commands confirmed successful remote access:

```bash
hostname
whoami
uptime
pwd
ls
```

These commands verified that the shell session was running on the remote Mac mini instead of the local Ubuntu laptop.

---

## Remote File Management

Directories and files were created remotely during the session.

Example commands:

```bash
mkdir homelab
touch remote-test.txt
```

This demonstrated basic remote administration capabilities.

---

## Lessons Learned

- SSH uses client/server communication.
- Network troubleshooting often starts with IP verification.
- `ping` is useful for confirming network reachability.
- Remote Login on macOS enables SSH access.
- SSH allows secure remote terminal administration.
- Real troubleshooting involves patience and iterative testing.
