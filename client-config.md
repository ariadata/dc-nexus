# Repository Client Configurations

## Table of Contents
- [Backup Commands](#backup-commands)
- [Debian 11 (Bullseye)](#debian-11-bullseye)
- [Debian 12 (Bookworm)](#debian-12-bookworm)
- [Ubuntu 20.04 (Focal)](#ubuntu-2004-focal)
- [Ubuntu 22.04 (Jammy)](#ubuntu-2204-jammy)
- [Ubuntu 24.04 (Noble)](#ubuntu-2404-noble)
- [Rocky Linux 8](#rocky-linux-8)

## Backup Commands

### For Debian/Ubuntu Systems
```bash
# Create backup directory
sudo mkdir -p /etc/apt/sources.list.backup

# Backup sources.list with timestamp
sudo cp /etc/apt/sources.list /etc/apt/sources.list.backup/sources.list.$(date +%Y%m%d_%H%M%S)

# Backup all repository configurations
sudo tar czf /etc/apt/sources.list.backup/sources_backup_$(date +%Y%m%d_%H%M%S).tar.gz /etc/apt/sources.list /etc/apt/sources.list.d/

# Optional: Create a restore point
sudo cp /etc/apt/sources.list.backup/sources.list.$(date +%Y%m%d_%H%M%S) /etc/apt/sources.list.restore
```

### For Rocky Linux
```bash
# Create backup directory
sudo mkdir -p /etc/yum.repos.d/backup

# Backup all repo files with timestamp
sudo tar czf /etc/yum.repos.d/backup/repos_backup_$(date +%Y%m%d_%H%M%S).tar.gz /etc/yum.repos.d/*.repo

# Backup specific repo file
sudo cp /etc/yum.repos.d/rocky-nexus.repo /etc/yum.repos.d/backup/rocky-nexus.repo.$(date +%Y%m%d_%H%M%S)
```

<details>
<summary><h2>Debian 11 (Bullseye)</h2></summary>

### sources.list Configuration
```
# Main
deb https://nexus.arzinja.dev/repository/debian-bullseye-main/ bullseye main
deb-src https://nexus.arzinja.dev/repository/debian-bullseye-main/ bullseye main

# Security
deb https://nexus.arzinja.dev/repository/debian-bullseye-security/ bullseye-security main
deb-src https://nexus.arzinja.dev/repository/debian-bullseye-security/ bullseye-security main

# Updates
deb https://nexus.arzinja.dev/repository/debian-bullseye-updates/ bullseye-updates main
deb-src https://nexus.arzinja.dev/repository/debian-bullseye-updates/ bullseye-updates main

# Backports
deb https://nexus.arzinja.dev/repository/debian-bullseye-backports/ bullseye-backports main
deb-src https://nexus.arzinja.dev/repository/debian-bullseye-backports/ bullseye-backports main
```
</details>

<details>
<summary><h2>Debian 12 (Bookworm)</h2></summary>

### sources.list Configuration
```
# Main
deb https://nexus.arzinja.dev/repository/debian-bookworm-main/ bookworm main
deb-src https://nexus.arzinja.dev/repository/debian-bookworm-main/ bookworm main

# Security
deb https://nexus.arzinja.dev/repository/debian-bookworm-security/ bookworm-security main
deb-src https://nexus.arzinja.dev/repository/debian-bookworm-security/ bookworm-security main

# Updates
deb https://nexus.arzinja.dev/repository/debian-bookworm-updates/ bookworm-updates main
deb-src https://nexus.arzinja.dev/repository/debian-bookworm-updates/ bookworm-updates main

# Backports
deb https://nexus.arzinja.dev/repository/debian-bookworm-backports/ bookworm-backports main
deb-src https://nexus.arzinja.dev/repository/debian-bookworm-backports/ bookworm-backports main
```
</details>

<details>
<summary><h2>Ubuntu 20.04 (Focal)</h2></summary>

### sources.list Configuration
```
# Main
deb https://nexus.arzinja.dev/repository/ubuntu-focal-main/ focal main restricted universe multiverse
deb-src https://nexus.arzinja.dev/repository/ubuntu-focal-main/ focal main restricted universe multiverse

# Security
deb https://nexus.arzinja.dev/repository/ubuntu-focal-security/ focal-security main restricted universe multiverse
deb-src https://nexus.arzinja.dev/repository/ubuntu-focal-security/ focal-security main restricted universe multiverse

# Updates
deb https://nexus.arzinja.dev/repository/ubuntu-focal-updates/ focal-updates main restricted universe multiverse
deb-src https://nexus.arzinja.dev/repository/ubuntu-focal-updates/ focal-updates main restricted universe multiverse

# Backports
deb https://nexus.arzinja.dev/repository/ubuntu-focal-backports/ focal-backports main restricted universe multiverse
deb-src https://nexus.arzinja.dev/repository/ubuntu-focal-backports/ focal-backports main restricted universe multiverse
```
</details>

<details>
<summary><h2>Ubuntu 22.04 (Jammy)</h2></summary>

### sources.list Configuration
```
# Main
deb https://nexus.arzinja.dev/repository/ubuntu-jammy-main/ jammy main restricted universe multiverse
deb-src https://nexus.arzinja.dev/repository/ubuntu-jammy-main/ jammy main restricted universe multiverse

# Security
deb https://nexus.arzinja.dev/repository/ubuntu-jammy-security/ jammy-security main restricted universe multiverse
deb-src https://nexus.arzinja.dev/repository/ubuntu-jammy-security/ jammy-security main restricted universe multiverse

# Updates
deb https://nexus.arzinja.dev/repository/ubuntu-jammy-updates/ jammy-updates main restricted universe multiverse
deb-src https://nexus.arzinja.dev/repository/ubuntu-jammy-updates/ jammy-updates main restricted universe multiverse

# Backports
deb https://nexus.arzinja.dev/repository/ubuntu-jammy-backports/ jammy-backports main restricted universe multiverse
deb-src https://nexus.arzinja.dev/repository/ubuntu-jammy-backports/ jammy-backports main restricted universe multiverse
```
</details>

<details>
<summary><h2>Ubuntu 24.04 (Noble)</h2></summary>

### sources.list Configuration
```
# Main
deb https://nexus.arzinja.dev/repository/ubuntu-noble-main/ noble main restricted universe multiverse
deb-src https://nexus.arzinja.dev/repository/ubuntu-noble-main/ noble main restricted universe multiverse

# Security
deb https://nexus.arzinja.dev/repository/ubuntu-noble-security/ noble-security main restricted universe multiverse
deb-src https://nexus.arzinja.dev/repository/ubuntu-noble-security/ noble-security main restricted universe multiverse

# Updates
deb https://nexus.arzinja.dev/repository/ubuntu-noble-updates/ noble-updates main restricted universe multiverse
deb-src https://nexus.arzinja.dev/repository/ubuntu-noble-updates/ noble-updates main restricted universe multiverse

# Backports
deb https://nexus.arzinja.dev/repository/ubuntu-noble-backports/ noble-backports main restricted universe multiverse
deb-src https://nexus.arzinja.dev/repository/ubuntu-noble-backports/ noble-backports main restricted universe multiverse
```
</details>

<details>
<summary><h2>Rocky Linux 8</h2></summary>

### Repository Configuration (/etc/yum.repos.d/rocky-nexus.repo)
```
[rocky-baseos]
name=Rocky Linux $releasever - BaseOS
baseurl=https://nexus.arzinja.dev/repository/rocky-8-baseos/
enabled=1
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-rockyofficial

[rocky-appstream]
name=Rocky Linux $releasever - AppStream
baseurl=https://nexus.arzinja.dev/repository/rocky-8-appstream/
enabled=1
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-rockyofficial

[rocky-extras]
name=Rocky Linux $releasever - Extras
baseurl=https://nexus.arzinja.dev/repository/rocky-8-extras/
enabled=1
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-rockyofficial

[rocky-powertools]
name=Rocky Linux $releasever - PowerTools
baseurl=https://nexus.arzinja.dev/repository/rocky-8-powertools/
enabled=0
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-rockyofficial
```
</details>
