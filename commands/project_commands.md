# Project Commands

## Install Tools

```bash
sudo apt update
sudo apt upgrade -y
sudo apt install chkrootkit rkhunter lynis
```

## Run Security Tools

```bash
sudo chkrootkit
sudo rkhunter --check
sudo lynis audit system
```

## Execute PRE_LOAD 
```bash
cat << 'EOF' > demo_hook.c
#define _GNU_SOURCE
#include <stdio.h>
#include <string.h>
#include <dlfcn.h>
#include <sys/utsname.h>

int uname(struct utsname *buf) {
    int (*sys_uname)(struct utsname *) = dlsym(RTLD_NEXT, "uname");
    int result = sys_uname(buf);
    printf("\n[!] HOOK ACTIVE: Intercepted system query\n");

    // Updated custom name string
    strcpy(buf->sysname, "Linux-Hardening-Project");

    return result;
}
EOF

```

## Run Security Tools again

```bash
sudo chkrootkit
sudo rkhunter --check
sudo lynis audit system


## remove PRE_LOAD


##System hardening
## Firewall

```bash
sudo ufw enable
sudo ufw status
```
