# How to check what linux distribution is running


What kind of Linux are you running?
---

```bash
uname -a
```

Ask the kernel and the pseudo file system:
```bash
cat /proc/version
```

View Release files:
```bash
ls /etc/*release*
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
Boot time messages
```bash
dmesg | head
```

Example outputs:
---
```
$ uname -a
Linux vagrant 5.4.0-77-generic #86-Ubuntu SMP Thu Jun 17 02:35:03 UTC 2021 x86_64 x86_64 x86_64 GNU/Linux
```

```
$ cat /proc/version
Linux version 5.4.0-77-generic (buildd@lgw01-amd64-028) (gcc version 9.3.0 (Ubuntu 9.3.0-17ubuntu1~20.04)) #86-Ubuntu SMP Thu Jun 17 02:35:03 UTC 2021
$ 
```

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

```
$ dmesg | head
[    0.000000] Linux version 5.4.0-77-generic (buildd@lgw01-amd64-028) (gcc version 9.3.0 (Ubuntu 9.3.0-17ubuntu1~20.04)) #86-Ubuntu SMP Thu Jun 17 02:35:03 UTC 2021 (Ubuntu 5.4.0-77.86-generic 5.4.119)
[    0.000000] Command line: BOOT_IMAGE=/boot/vmlinuz-5.4.0-77-generic root=/dev/mapper/vgvagrant-root ro net.ifnames=0 biosdevname=0 quiet
[    0.000000] KERNEL supported cpus:
[    0.000000]   Intel GenuineIntel
[    0.000000]   AMD AuthenticAMD
[    0.000000]   Hygon HygonGenuine
[    0.000000]   Centaur CentaurHauls
[    0.000000]   zhaoxin   Shanghai  
[    0.000000] Disabled fast string operations
[    0.000000] x86/fpu: Supporting XSAVE feature 0x001: 'x87 floating point registers'
$ 
```

