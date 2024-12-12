# WSL Commands: A Comprehensive Guide

## Introduction

Windows Subsystem for Linux (WSL) is a compatibility layer for running Linux binary executables natively on Windows 10 and Windows 11. This guide provides a list of essential WSL commands to help you manage and use WSL effectively.

Default Ubuntu installation comes with following tools:
Curl
Vim
Tmux
git
openSSH
GCC,make
Python3.12 with virtual environment capable

## Table of Contents

1. [Basic WSL Commands](#basic-wsl-commands)
2. [WSL 2 Commands](#wsl-2-commands)
3. [WSL Distribution Management](#wsl-distribution-management)
4. [WSL File System Access](#wsl-file-system-access)
5. [WSL Networking](#wsl-networking)
6. [WSL Environment Variables](#wsl-environment-variables)
7. [WSL Configuration](#wsl-configuration)

## Basic WSL Commands



### 1. List or Check Existing Distributions installed on WSL
```sh
wsl --list
```
### 2. Verbose mode with more info
```sh
wsl --list --verbose
```

### 3. Start a WSL Distribution
```sh
wsl -d <DistributionName>
```

### 4. Stop a WSL Distribution
```sh
wsl --terminate <DistributionName>
```

### 5. Uninstall a WSL Distribution
```sh
wsl --unregister <DistributionName>
```

## WSL 2 Commands

### 2. Set WSL 2 as Default
```sh
wsl --set-default-version 2
```

### 3. Convert a WSL 1 Distribution to WSL 2
```sh
wsl --set-version <DistributionName> 2
```

### 4. Convert a WSL 2 Distribution to WSL 1
```sh
wsl --set-version <DistributionName> 1
```

## WSL Distribution Management

### 1. Install a New Distribution
```sh
wsl --install -d <DistributionName>
```

### 2. Update a Distribution
```sh
wsl --update
```

### 3. Set a Default Distribution
```sh
wsl --set-default <DistributionName>
```

## WSL File System Access

### 1. Access Windows File System from WSL
```sh
cd /mnt/c/Users/YourUsername
```

### 2. Access WSL File System from Windows
```sh
\\wsl$\<DistributionName>
```

## WSL Networking

### 1. Check WSL IP Address
```sh
ip addr show eth0
```

### 2. Access WSL from Windows
```sh
http://localhost:<Port>
```

### 3. Access Windows from WSL
```sh
http://host.docker.internal:<Port>
```

## WSL Environment Variables

### 1. Set Environment Variables
```sh
export VARIABLE_NAME=value
```

### 2. View Environment Variables
```sh
printenv
```

## WSL Configuration

### 1. Configure WSL Settings
```sh
wsl --shutdown
```

### 2. Edit WSL Configuration File
```sh
notepad %USERPROFILE%\.wslconfig
```

### 3. Edit Distribution Configuration File
```sh
notepad %USERPROFILE%\.wslconfig
```

## Conclusion

This guide provides a comprehensive list of essential WSL commands to help you manage and use WSL effectively. For more detailed information, refer to the official Microsoft documentation.

## Additional Command

To list installed packages in WSL, you can run the following command:

```bash
wsl dpkg --get-selections
```


---

If you have any feedback or need further assistance, feel free to reach out.
