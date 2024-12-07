# Repository Server Configurations

## Table of Contents
- [Debian 11 (Bullseye)](#debian-11-bullseye)
- [Debian 12 (Bookworm)](#debian-12-bookworm)
- [Ubuntu 20.04 (Focal)](#ubuntu-2004-focal)
- [Ubuntu 22.04 (Jammy)](#ubuntu-2204-jammy)
- [Ubuntu 24.04 (Noble)](#ubuntu-2404-noble)
- [Rocky Linux 8](#rocky-linux-8)

<details>
<summary><h2>Debian 11 (Bullseye)</h2></summary>

### Repository Definitions

| Name | Distribution | Remote Storage | Max Age |
|------|--------------|----------------|----------|
| debian-bullseye-main | bullseye | http://deb.debian.org/debian | 1440 |
| debian-bullseye-security | bullseye-security | http://security.debian.org/debian-security | 1440 |
| debian-bullseye-updates | bullseye-updates | http://deb.debian.org/debian | 1440 |
| debian-bullseye-backports | bullseye-backports | http://deb.debian.org/debian | 1440 |


```
Name: debian-bullseye-main
Distribution: bullseye
Remote storage: http://deb.debian.org/debian
Maximum component age: 1440

Name: debian-bullseye-security
Distribution: bullseye-security
Remote storage: http://security.debian.org/debian-security
Maximum component age: 1440

Name: debian-bullseye-updates
Distribution: bullseye-updates
Remote storage: http://deb.debian.org/debian
Maximum component age: 1440

Name: debian-bullseye-backports
Distribution: bullseye-backports
Remote storage: http://deb.debian.org/debian
Maximum component age: 1440
```

</details>

<details>
<summary><h2>Debian 12 (Bookworm)</h2></summary>

### Repository Definitions

| Name | Distribution | Remote Storage | Max Age |
|------|--------------|----------------|----------|
| debian-bookworm-main | bookworm | http://deb.debian.org/debian | 1440 |
| debian-bookworm-security | bookworm-security | http://security.debian.org/debian-security | 1440 |
| debian-bookworm-updates | bookworm-updates | http://deb.debian.org/debian | 1440 |
| debian-bookworm-backports | bookworm-backports | http://deb.debian.org/debian | 1440 |


```
Name: debian-bookworm-main
Distribution: bookworm
Remote storage: http://deb.debian.org/debian
Maximum component age: 1440

Name: debian-bookworm-security
Distribution: bookworm-security
Remote storage: http://security.debian.org/debian-security
Maximum component age: 1440

Name: debian-bookworm-updates
Distribution: bookworm-updates
Remote storage: http://deb.debian.org/debian
Maximum component age: 1440

Name: debian-bookworm-backports
Distribution: bookworm-backports
Remote storage: http://deb.debian.org/debian
Maximum component age: 1440
```

</details>

<details>
<summary><h2>Ubuntu 20.04 (Focal)</h2></summary>

### Repository Definitions

| Name | Distribution | Remote Storage | Max Age |
|------|--------------|----------------|----------|
| ubuntu-focal-main | focal | http://archive.ubuntu.com/ubuntu | 1440 |
| ubuntu-focal-security | focal-security | http://security.ubuntu.com/ubuntu | 1440 |
| ubuntu-focal-updates | focal-updates | http://archive.ubuntu.com/ubuntu | 1440 |
| ubuntu-focal-backports | focal-backports | http://archive.ubuntu.com/ubuntu | 1440 |


```
Name: ubuntu-focal-main
Distribution: focal
Remote storage: http://archive.ubuntu.com/ubuntu
Maximum component age: 1440

Name: ubuntu-focal-security
Distribution: focal-security
Remote storage: http://security.ubuntu.com/ubuntu
Maximum component age: 1440

Name: ubuntu-focal-updates
Distribution: focal-updates
Remote storage: http://archive.ubuntu.com/ubuntu
Maximum component age: 1440

Name: ubuntu-focal-backports
Distribution: focal-backports
Remote storage: http://archive.ubuntu.com/ubuntu
Maximum component age: 1440
```

</details>

<details>
<summary><h2>Ubuntu 22.04 (Jammy)</h2></summary>

### Repository Definitions

| Name | Distribution | Remote Storage | Max Age |
|------|--------------|----------------|----------|
| ubuntu-jammy-main | jammy | http://archive.ubuntu.com/ubuntu | 1440 |
| ubuntu-jammy-security | jammy-security | http://security.ubuntu.com/ubuntu | 1440 |
| ubuntu-jammy-updates | jammy-updates | http://archive.ubuntu.com/ubuntu | 1440 |
| ubuntu-jammy-backports | jammy-backports | http://archive.ubuntu.com/ubuntu | 1440 |


```
Name: ubuntu-jammy-main
Distribution: jammy
Remote storage: http://archive.ubuntu.com/ubuntu
Maximum component age: 1440

Name: ubuntu-jammy-security
Distribution: jammy-security
Remote storage: http://security.ubuntu.com/ubuntu
Maximum component age: 1440

Name: ubuntu-jammy-updates
Distribution: jammy-updates
Remote storage: http://archive.ubuntu.com/ubuntu
Maximum component age: 1440

Name: ubuntu-jammy-backports
Distribution: jammy-backports
Remote storage: http://archive.ubuntu.com/ubuntu
Maximum component age: 1440
```

</details>

<details>
<summary><h2>Ubuntu 24.04 (Noble)</h2></summary>

### Repository Definitions

| Name | Distribution | Remote Storage | Max Age |
|------|--------------|----------------|----------|
| ubuntu-noble-main | noble | http://archive.ubuntu.com/ubuntu | 1440 |
| ubuntu-noble-security | noble-security | http://security.ubuntu.com/ubuntu | 1440 |
| ubuntu-noble-updates | noble-updates | http://archive.ubuntu.com/ubuntu | 1440 |
| ubuntu-noble-backports | noble-backports | http://archive.ubuntu.com/ubuntu | 1440 |


```
Name: ubuntu-noble-main
Distribution: noble
Remote storage: http://archive.ubuntu.com/ubuntu
Maximum component age: 1440

Name: ubuntu-noble-security
Distribution: noble-security
Remote storage: http://security.ubuntu.com/ubuntu
Maximum component age: 1440

Name: ubuntu-noble-updates
Distribution: noble-updates
Remote storage: http://archive.ubuntu.com/ubuntu
Maximum component age: 1440

Name: ubuntu-noble-backports
Distribution: noble-backports
Remote storage: http://archive.ubuntu.com/ubuntu
Maximum component age: 1440
```

</details>

<details>
<summary><h2>Rocky Linux 8</h2></summary>

### Repository Definitions

| Name | Distribution | Remote Storage | Max Age |
|------|--------------|----------------|----------|
| rocky-8-baseos | 8 | https://download.rockylinux.org/pub/rocky/8/BaseOS/$basearch/os/ | 1440 |
| rocky-8-appstream | 8 | https://download.rockylinux.org/pub/rocky/8/AppStream/$basearch/os/ | 1440 |
| rocky-8-extras | 8 | https://download.rockylinux.org/pub/rocky/8/extras/$basearch/os/ | 1440 |
| rocky-8-powertools | 8 | https://download.rockylinux.org/pub/rocky/8/PowerTools/$basearch/os/ | 1440 |


```
Name: rocky-8-baseos
Distribution: 8
Remote storage: https://download.rockylinux.org/pub/rocky/8/BaseOS/$basearch/os/
Maximum component age: 1440

Name: rocky-8-appstream
Distribution: 8
Remote storage: https://download.rockylinux.org/pub/rocky/8/AppStream/$basearch/os/
Maximum component age: 1440

Name: rocky-8-extras
Distribution: 8
Remote storage: https://download.rockylinux.org/pub/rocky/8/extras/$basearch/os/
Maximum component age: 1440

Name: rocky-8-powertools
Distribution: 8
Remote storage: https://download.rockylinux.org/pub/rocky/8/PowerTools/$basearch/os/
Maximum component age: 1440
```

</details>