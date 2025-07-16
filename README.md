# SOP for Software Management in Ubuntu

---
## Author Information

| Created | pre Reviewer | L0 Reviewer | L1 Reviewer | L2 Reviewer |
|---------|--------------|-------------|-------------|-------------|
 Aryan mishra | Siddharth | Ram Ratan  | Gaurav Singla | Mahesh Kumar
 
 ---
 ## Table of Contents
   - introduction
   - Objective
   - Update the Package Index
   - Upgrade Installed Packages
   - Install Software Packages
   - Common Flags
   - Check if a Package is Installed
   - Search for a Package
   - View Package Information
   - Remove a Package
   - Clean Up Unused Files
   - Update Only a Specific Package
   - List Installed Packages
   - Best Practices

     ---
    
 ## introduction
This document provides a Standard Operating Procedure (SOP) for **installing**, **updating**, and **removing software** on **Ubuntu** systems using the `apt` package manager.It also includes commonly used commands and flags.


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

## 12. Best Practices

| #   | Practice                                                                 |
|-----|--------------------------------------------------------------------------|
| 1.  | Update system regularly.                                                 |
| 2.  | Prefer official Ubuntu repositories.                                     |
| 3.  | Remove unused packages.                                                  |
| 4.  | Backup config files before purge.                                        |
| 5.  | Avoid `sudo apt upgrade -y` on production servers without testing.       |
