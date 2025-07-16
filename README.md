# SOP for Software Management in Ubuntu

---
**Maintained By:** Aryan mishra
 
 ---
 # intro
This document provides a Standard Operating Procedure (SOP) for **installing**, **updating**, and **removing software** on **Ubuntu** systems using the `apt` package manager.

---

## Objective

This SOP outlines the standard procedure for installing, updating, and removing software on Ubuntu systems using the APT (Advanced Package Tool) package manager. It also includes commonly used commands and flags.

---

## 1. Update the Package Index

Before any software installation or upgrade, update the local package index:

```bash
sudo apt update
```
- sudo: Runs command as superuser.

- apt: Command-line package manager.

- update: Fetches the latest list of packages.

  ---
## 2. Upgrade Installed Packages
```bash
sudo apt upgrade -y
```
---
## 3. Install Software Packages
```bash
sudo apt install <package-name> -y
```
### Common Flags:

- -y :  Automatic yes to all prompts

 ---
## 3. Check if a Package is Installed
```bash
dpkg -l | grep <package-name>
```
---
 
 ## 5. Search for a Package
 ```bash
apt search <package-name>
```
---
##  6. View Package Information
```bash
apt show <package-name>
```
---
##  7. Remove a Package
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
## 9. Update Only a Specific Package
```bash
sudo apt install --only-upgrade <package-name>
```
---
## 10. List Installed Packages
```bash
dpkg -l
```
---
## 11. Check Logs for Package Operations
```bash
cat /var/log/apt/history.log
cat /var/log/dpkg.log
```
---
## 12. Best Practices
- Update system regularly.

- Prefer official Ubuntu repositories.

- Remove unused packages.

- Backup config files before purge.

- Avoid sudo apt upgrade -y on production servers without testing.
---
