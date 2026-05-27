# Commands Used

## Connectivity Testing

```bash
ping <redacted-ip>
```

Used to verify that the Ubuntu laptop could reach the Mac mini across the local network.

---

## SSH Connection

```bash
ssh <redacted-user>@<redacted-ip>
```

Used to remotely connect from the Ubuntu laptop to the Mac mini.

---

## Remote Verification Commands

```bash
hostname
```

Displays the remote system hostname.

```bash
whoami
```

Displays the currently authenticated user.

```bash
uptime
```

Shows how long the remote system has been running.

```bash
pwd
```

Displays the current working directory.

```bash
ls
```

Lists files and folders in the current directory.

---

## Remote File and Directory Management

```bash
mkdir homelab
```

Creates a new directory remotely.

```bash
touch remote-test.txt
```

Creates a test file remotely.
