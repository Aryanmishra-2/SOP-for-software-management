# SOP for Software Management in Ubuntu

---
## Author Information

| Created | pre Reviewer | L0 Reviewer | L1 Reviewer | L2 Reviewer |
|---------|--------------|-------------|-------------|-------------|
 Aryan mishra | Siddharth | Ram Ratan  | Gaurav Singla | Mahesh Kumar
 
 ---
## Table of Contents
- [Introduction](#introduction)
- [Update the Package Index](#update-the-package-index)
- [Upgrade Installed Packages](#upgrade-installed-packages)
- [Install Software Packages](#install-software-packages)
- [Common Flags](#common-flags)
- [Check if a Package is Installed](#check-if-a-package-is-installed)
- [Search for a Package](#search-for-a-package)
- [View Package Information](#view-package-information)
- [Remove a Package](#remove-a-package)
- [Clean Up Unused Files](#clean-up-unused-files)
- [Update Only a Specific Package](#update-only-a-specific-package)
- [List Installed Packages](#list-installed-packages)
- [Best Practices](#best-practices)


     ---
    
 ## introduction
This document provides a Standard Operating Procedure (SOP) for **installing**, **updating**, and **removing software** on **Ubuntu** systems using the `apt` package manager.It also includes commonly used commands and flags.


---

## Update the Package Index

Before any software installation or upgrade, update the local package index:

```bash
sudo apt update
```
- sudo: Runs command as superuser.

- apt: Command-line package manager.

- update: Fetches the latest list of packages.

  ---
## Upgrade Installed Packages
```bash
sudo apt upgrade -y
```
---
## Install Software Packages
```bash
sudo apt install <package-name> -y
```
### Common Flags:

- -y :  Automatic yes to all prompts

 ---
## Check if a Package is Installed
```bash
dpkg -l | grep <package-name>
```
---
 
 ## Search for a Package
 ```bash
apt search <package-name>
```
---
## View Package Information
```bash
apt show <package-name>
```
---
## Remove a Package
```bash
sudo apt remove <package-name> -y
```
---
## Clean Up Unused Files
```bash
sudo apt autoremove        # Remove unused dependencies
sudo apt autoclean         # Clean up partial package files
sudo apt clean             # Clear local package cache
```
---
## Update Only a Specific Package
```bash
sudo apt install --only-upgrade <package-name>
```
---
## List Installed Packages
```bash
dpkg -l
```
---

## Best Practices

| no   | Practice                                                                 |
|-----|--------------------------------------------------------------------------|
| 1.  | Update system regularly.                                                 |
| 2.  | Prefer official Ubuntu repositories.                                     |
| 3.  | Remove unused packages.                                                  |
| 4.  | Backup config files before purge.                                        |
| 5.  | Avoid `sudo apt upgrade -y` on production servers without testing.       |
