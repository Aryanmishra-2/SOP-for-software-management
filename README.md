# SOP for Software Management in Ubuntu

---
## Author Information

| Created         | Created on         | Version          | Last updated by   | pre Reviewer       | L0 Reviewer     | L1 Reviewer          |    L2 Reviewer    |
|-----------------|--------------------|------------------|-------------------|--------------------|-----------------|----------------------|-------------------|
| Aryan mishra    |                    |                  |                  |        Siddharth    |  Ram Ratan      |      Gaurav Singla   |   Mahesh Kumar    |
 
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
- [Conclusion](#Conclusion)
- [References](#References)


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

---
## Conclusion

This Standard Operating Procedure (SOP) provides a structured approach for managing software on Ubuntu systems. By following these steps, users can efficiently handle package installation, updates, configuration, and removal using tools like `apt` and `snap`. Consistent software management not only improves system stability and performance but also ensures better security and resource optimization. 

## References

- Ubuntu Official Documentation – Package Management: https://help.ubuntu.com/lts/serverguide/apt.html
- APT – Advanced Package Tool (Ubuntu Wiki): https://wiki.ubuntu.com/Apt
- Debian Manpages – apt(8): https://manpages.debian.org/bullseye/apt/apt.8.en.html
- napcraft Docs – Installing Software Using Snap: https://snapcraft.io/docs/installing-snap-on-ubuntu
