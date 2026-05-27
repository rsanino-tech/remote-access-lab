# Networking Concepts Learned

## SSH

SSH (Secure Shell) is a secure remote administration protocol used to access another computer over a network.

SSH encrypts communication between the client and the server.

Default SSH port:

```text
22
```

---

## Client and Server Roles

In this lab:

| System | Role |
|---|---|
| Ubuntu laptop | SSH Client |
| Mac mini | SSH Server |

The client initiates the connection.

The server accepts the connection.

---

## IP Addressing

Devices on the same network communicate using IP addresses.

Example private ranges include:

```text
10.x.x.x
192.168.x.x
172.16.x.x
```

A common beginner mistake is confusing a router gateway address with the actual target device.

In many home networks, the gateway address is often:

```text
10.0.0.1
```

---

## Ping and ICMP

The `ping` command uses ICMP (Internet Control Message Protocol) to test whether another device is reachable on the network.

Example:

```bash
ping <redacted-ip>
```

Successful replies confirm:

- network connectivity
- reachable destination
- working IP communication

---

## Remote Login on macOS

macOS includes a built-in SSH server.

Enabling Remote Login from macOS Sharing settings allows inbound SSH connections.

---

## Remote Administration

After a successful SSH login, terminal commands run on the remote machine rather than the local machine.

Verification commands:

```bash
hostname
whoami
uptime
```

These commands help confirm the identity and status of the remote system.

---

## Infrastructure Thinking

This lab introduced several important infrastructure concepts:

- remote administration
- client/server architecture
- troubleshooting workflows
- network reachability
- service enablement
- authentication
- operational awareness

Hands-on troubleshooting is one of the fastest ways to learn networking and Linux administration.
