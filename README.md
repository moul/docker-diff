# docker-diff
:whale: Compare Docker images

## Installation

### On macOS via Homebrew

`brew install joenyland/docker/docker-diff`

Or `brew tap joenyland/docker` and then `brew install docker-diff`

## Usage

[See full examples](./examples).

---

Comparing changes between [alpine:3.2](https://hub.docker.com/r/library/alpine/) and [alpine:3.3](https://hub.docker.com/r/library/alpine/).

```console
$ ./docker-diff alpine:3.2 alpine:3.3
```

```diff
7,8c7
< ---s--x--x 9944       bin/bbsuid
< -rwxr-xr-x 800936     bin/busybox
---
> -rwxr-xr-x 809128     bin/busybox
63d61
< lrwxrwxrwx 0          bin/rc-status
82d79
< -rwxr-xr-x 9872       bin/uniso
92,94d88
< drwxr-xr-x 0          etc/acpi/
< drwxr-xr-x 0          etc/acpi/PWRF/
< -rwxr-xr-x 19         etc/acpi/PWRF/00000080
105,106c99,100
< -rw-r--r-- 45         etc/apk/repositories
< -rw-r--r-- 12         etc/apk/world
---
> -rw-r--r-- 95         etc/apk/repositories
> -rw-r--r-- 51         etc/apk/world
108,129d101
< -rw-r--r-- 328        etc/conf.d/bootmisc
< -rw-r--r-- 876        etc/conf.d/consolefont
< -rw-r--r-- 55         etc/conf.d/cron
< -rw-r--r-- 348        etc/conf.d/devfs
< -rw-r--r-- 117        etc/conf.d/dmesg
< -rw-r--r-- 1402       etc/conf.d/fsck
< -rw-r--r-- 59         etc/conf.d/hostname
< -rw-r--r-- 857        etc/conf.d/hwclock
< -rw-r--r-- 911        etc/conf.d/keymaps
< -rw-r--r-- 105        etc/conf.d/killprocs
< -rw-r--r-- 14         etc/conf.d/klogd
< -rw-r--r-- 121        etc/conf.d/localmount
< -rw-r--r-- 124        etc/conf.d/modloop
< -rw-r--r-- 898        etc/conf.d/modules
< -rw-r--r-- 1335       etc/conf.d/netmount
< -rw-r--r-- 106        etc/conf.d/ntpd
< -rw-r--r-- 48         etc/conf.d/rdate
< -rw-r--r-- 357        etc/conf.d/staticroute
< -rw-r--r-- 16         etc/conf.d/syslog
< -rw-r--r-- 76         etc/conf.d/tmpfiles
< -rw-r--r-- 282        etc/conf.d/urandom
< -rw-r--r-- 40         etc/conf.d/watchdog
131c103
< -rw-r--r-- 283        etc/crontabs/root
---
> -rw------- 283        etc/crontabs/root
133c105
< -rw-r--r-- 810        etc/group
---
> -rw-r--r-- 683        etc/group
137,185c109
[...]
```

---

Comparing changes between [ubuntu:wily](https://hub.docker.com/r/library/ubuntu/) and [ubuntu-debootstrap:wily](https://hub.docker.com/r/library/ubuntu-debootstrap/).

```console
$ ./docker-diff ubuntu:wily ubuntu-debootstrap:wily
Unable to find image 'ubuntu:wily' locally
wily: Pulling from library/ubuntu
cde2d46a079b: Pulling fs layer
e189717d7053: Pulling fs layer
7147b2632305: Pulling fs layer
d8a164f81acc: Pulling fs layer
7147b2632305: Verifying Checksum
7147b2632305: Download complete
e189717d7053: Verifying Checksum
e189717d7053: Download complete
d8a164f81acc: Verifying Checksum
d8a164f81acc: Download complete
cde2d46a079b: Verifying Checksum
cde2d46a079b: Download complete
cde2d46a079b: Pull complete
e189717d7053: Pull complete
7147b2632305: Pull complete
d8a164f81acc: Pull complete
Digest: sha256:f399d4101e8e41196b9bc58a96e63d17e3d5fcef702df2bda05e166dc3b5ac3c
Status: Downloaded newer image for ubuntu:wily
Unable to find image 'ubuntu-debootstrap:wily' locally
wily: Pulling from library/ubuntu-debootstrap
15b60992a765: Pulling fs layer
56590e6e34d5: Pulling fs layer
56590e6e34d5: Verifying Checksum
56590e6e34d5: Download complete
15b60992a765: Verifying Checksum
15b60992a765: Download complete
15b60992a765: Pull complete
56590e6e34d5: Pull complete
Digest: sha256:0d464ac0c99ecb124f5cc078b2f3db5e33699d030d90c27164af38a721a2b7f2
Status: Downloaded newer image for ubuntu-debootstrap:wily
...
```

```diff
13,14c13,14
< -rwxr-xr-x 101928     bin/df
< -rwxr-xr-x 118272     bin/dir
---
> -rwxr-xr-x 101960     bin/df
> -rwxr-xr-x 118368     bin/dir
18c18
< -rwxr-xr-x 31264      bin/echo
---
> -rwxr-xr-x 31296      bin/echo
27a28
> -rwxr-xr-x 363680     bin/ip
33c34
< -rwxr-xr-x 118272     bin/ls
---
> -rwxr-xr-x 118368     bin/ls
34a36
> -rwxr-xr-x 474352     bin/machinectl
42c44
< -rwxr-xr-x 670304     bin/networkctl
---
> -rwxr-xr-x 670296     bin/networkctl
44a47,48
> -rwsr-xr-x 70768      bin/ping
> -rwsr-xr-x 61520      bin/ping6
46c50
< -rwxr-xr-x 31360      bin/pwd
---
> -rwxr-xr-x 31392      bin/pwd
50c54
[...]
```

[See full examples](./examples).

## Sub-project

* [docker-promote](https://github.com/Wealthforge-Technologies/docker-promote): promote a docker image only if it is different than than the one presently there. ([@Wealthforge-Technologies](https://github.com/Wealthforge-Technologies))

## License

MIT
