# How to check what linux distribution you are running


What Kind of Linux are you running?
---
View Release files:
```bash
$ ls /etc/*release*
```

View the Issue Files:
```bash
cat /etc/*issue*
```

Ubuntu specific use lsb_release utilility:
```bash
lsb_release -a
```

SystemD system:
```bash
hostnamectl
```

Example outputs:
---
```
$ls /etc/*release*
/etc/lsb-release  /etc/os-release
$ cat /etc/*release*
DISTRIB_ID=Ubuntu
DISTRIB_RELEASE=18.04
DISTRIB_CODENAME=bionic
DISTRIB_DESCRIPTION="Ubuntu 18.04.5 LTS"
NAME="Ubuntu"
VERSION="18.04.5 LTS (Bionic Beaver)"
ID=ubuntu
ID_LIKE=debian
PRETTY_NAME="Ubuntu 18.04.5 LTS"
VERSION_ID="18.04"
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
VERSION_CODENAME=bionic
UBUNTU_CODENAME=bionic
```

```
$ cat /etc/*issue*
Ubuntu 18.04.5 LTS \n \l

Ubuntu 18.04.5 LTS
$ lsb_release -a
No LSB modules are available.
Distributor ID: Ubuntu
Description:    Ubuntu 18.04.5 LTS
Release:        18.04
Codename:       bionic
$ 
```

```
$ lsb_release -a
No LSB modules are available.
Distributor ID: Ubuntu
Description:    Ubuntu 18.04.5 LTS
Release:        18.04
Codename:       bionic
$ 
```

```
$ hostnamectl
   Static hostname: ip-10-0-1-10
         Icon name: computer-vm
           Chassis: vm
        Machine ID: f89138299a734aec9037cb36dcca0fa2
           Boot ID: 426b0d203e224b9ab1d1e045d44eae3d
    Virtualization: xen
  Operating System: Ubuntu 18.04.5 LTS
            Kernel: Linux 5.4.0-1037-aws
      Architecture: x86-64
$
```




