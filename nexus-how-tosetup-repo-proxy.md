How to set:

### Debian 11 (Bullseye)
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

### Debian 12 (Bookworm)
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

### Ubuntu 20.04 (Focal)
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

### Ubuntu 22.04 (Jammy)
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

### Ubuntu 24.04 (Noble)
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

### Rocky 8
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

Now, here are the sources.list configurations for each distribution:

### Debian 11 (Bullseye) sources.list
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

### Debian 12 (Bookworm) sources.list
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

### Ubuntu 20.04 (Focal) sources.list
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

### Ubuntu 22.04 (Jammy) sources.list
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

### Ubuntu 24.04 (Noble) sources.list
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

### Rocky 8 repo file (/etc/yum.repos.d/rocky-nexus.repo)
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