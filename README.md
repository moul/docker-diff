# docker-diff
:whale: Compare Docker images

## Installation

### On macOS via Homebrew

`brew install moul/moul/docker-diff`

Or `brew tap moul/moul` and then `brew install docker-diff`

## Usage

[See full examples](./examples).

---

Comparing changes between [alpine:3.2](https://hub.docker.com/r/library/alpine/) and [alpine:3.3](https://hub.docker.com/r/library/alpine/).

```console
$ ./docker-diff alpine:3.2 alpine:3.3
```

```diff
--- /tmp/alpine:3.2	2018-05-03 01:43:06.326570762 +0700
+++ /tmp/alpine:3.3	2018-05-03 01:43:08.102671272 +0700
@@ -3,8 +3,7 @@
 lrwxrwxrwx	0	/bin/ash
 lrwxrwxrwx	0	/bin/base64
 lrwxrwxrwx	0	/bin/bbconfig
----s--x--x	9944	/bin/bbsuid
--rwxr-xr-x	800936	/bin/busybox
+-rwxr-xr-x	809128	/bin/busybox
 lrwxrwxrwx	0	/bin/cat
 lrwxrwxrwx	0	/bin/catv
 lrwxrwxrwx	0	/bin/chgrp
@@ -59,7 +58,6 @@
 lrwxrwxrwx	0	/bin/printenv
 lrwxrwxrwx	0	/bin/ps
 lrwxrwxrwx	0	/bin/pwd
-lrwxrwxrwx	0	/bin/rc-status
 lrwxrwxrwx	0	/bin/reformime
 lrwxrwxrwx	0	/bin/rev
 lrwxrwxrwx	0	/bin/rm
@@ -78,7 +76,6 @@
 lrwxrwxrwx	0	/bin/true
 lrwxrwxrwx	0	/bin/umount
 lrwxrwxrwx	0	/bin/uname
--rwxr-xr-x	9872	/bin/uniso
 lrwxrwxrwx	0	/bin/usleep
 lrwxrwxrwx	0	/bin/watch
 lrwxrwxrwx	0	/bin/zcat
@@ -88,9 +85,6 @@
 drwxr-xr-x	0	/dev/shm/
 drwxr-xr-x	0	/etc/
 -rw-r--r--	4	/etc/TZ
-drwxr-xr-x	0	/etc/acpi/
-drwxr-xr-x	0	/etc/acpi/PWRF/
--rwxr-xr-x	19	/etc/acpi/PWRF/00000080
 -rw-r--r--	6	/etc/alpine-release
 drwxr-xr-x	0	/etc/apk/
 -rw-r--r--	7	/etc/apk/arch
@@ -101,94 +95,21 @@
 -rw-r--r--	451	/etc/apk/keys/alpine-devel@lists.alpinelinux.org-524d27bb.rsa.pub
 -rw-r--r--	451	/etc/apk/keys/alpine-devel@lists.alpinelinux.org-5261cecb.rsa.pub
 drwxr-xr-x	0	/etc/apk/protected_paths.d/
--rw-r--r--	47	/etc/apk/repositories
--rw-r--r--	12	/etc/apk/world
+-rw-r--r--	99	/etc/apk/repositories
+-rw-r--r--	51	/etc/apk/world
 drwxr-xr-x	0	/etc/conf.d/
--rw-r--r--	328	/etc/conf.d/bootmisc
--rw-r--r--	876	/etc/conf.d/consolefont
--rw-r--r--	55	/etc/conf.d/cron
--rw-r--r--	348	/etc/conf.d/devfs
--rw-r--r--	117	/etc/conf.d/dmesg
--rw-r--r--	1402	/etc/conf.d/fsck
--rw-r--r--	59	/etc/conf.d/hostname
--rw-r--r--	857	/etc/conf.d/hwclock
--rw-r--r--	911	/etc/conf.d/keymaps
--rw-r--r--	105	/etc/conf.d/killprocs
--rw-r--r--	14	/etc/conf.d/klogd
--rw-r--r--	121	/etc/conf.d/localmount
--rw-r--r--	124	/etc/conf.d/modloop
--rw-r--r--	898	/etc/conf.d/modules
--rw-r--r--	1335	/etc/conf.d/netmount
--rw-r--r--	106	/etc/conf.d/ntpd
--rw-r--r--	48	/etc/conf.d/rdate
--rw-r--r--	357	/etc/conf.d/staticroute
--rw-r--r--	16	/etc/conf.d/syslog
--rw-r--r--	76	/etc/conf.d/tmpfiles
--rw-r--r--	282	/etc/conf.d/urandom
--rw-r--r--	40	/etc/conf.d/watchdog
 drwxr-xr-x	0	/etc/crontabs/
--rw-r--r--	283	/etc/crontabs/root
+-rw-------	283	/etc/crontabs/root
 -rw-r--r--	89	/etc/fstab
--rw-r--r--	810	/etc/group
+-rw-r--r--	683	/etc/group
 -rwxr-xr-x	0	/etc/hostname
 -rwxr-xr-x	0	/etc/hosts
 drwxr-xr-x	0	/etc/init.d/
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
--- /tmp/ubuntu:wily	2018-05-03 01:46:23.825609637 +0700
+++ /tmp/ubuntu-debootstrap:wily	2018-05-03 01:46:28.257854572 +0700
@@ -9,12 +9,12 @@
 -rwxr-xr-x	125400	/bin/dash
 -rwxr-xr-x	64256	/bin/date
 -rwxr-xr-x	60232	/bin/dd
--rwxr-xr-x	101928	/bin/df
--rwxr-xr-x	118272	/bin/dir
+-rwxr-xr-x	101960	/bin/df
+-rwxr-xr-x	118368	/bin/dir
 -rwxr-xr-x	56448	/bin/dmesg
 lrwxrwxrwx	0	/bin/dnsdomainname
 lrwxrwxrwx	0	/bin/domainname
--rwxr-xr-x	31264	/bin/echo
+-rwxr-xr-x	31296	/bin/echo
 -rwxr-xr-x	29	/bin/egrep
 -rwxr-xr-x	27168	/bin/false
 -rwxr-xr-x	29	/bin/fgrep
@@ -24,13 +24,15 @@
 -rwxr-xr-x	5927	/bin/gzexe
 -rwxr-xr-x	98240	/bin/gzip
 -rwxr-xr-x	14736	/bin/hostname
+-rwxr-xr-x	363680	/bin/ip
 -rwxr-xr-x	470256	/bin/journalctl
 -rwxr-xr-x	23088	/bin/kill
 -rwxr-xr-x	56072	/bin/ln
 -rwxr-xr-x	49232	/bin/login
 -rwxr-xr-x	449776	/bin/loginctl
--rwxr-xr-x	118272	/bin/ls
+-rwxr-xr-x	118368	/bin/ls
 -rwxr-xr-x	73056	/bin/lsblk
+-rwxr-xr-x	474352	/bin/machinectl
 -rwxr-xr-x	80832	/bin/mkdir
 -rwxr-xr-x	64384	/bin/mknod
 -rwxr-xr-x	39616	/bin/mktemp
@@ -38,20 +40,23 @@
 -rwsr-xr-x	40088	/bin/mount
 -rwxr-xr-x	14712	/bin/mountpoint
 -rwxr-xr-x	130376	/bin/mv
--rwxr-xr-x	670304	/bin/networkctl
+-rwxr-xr-x	670296	/bin/networkctl
 lrwxrwxrwx	0	/bin/nisdomainname
 lrwxrwxrwx	0	/bin/pidof
+-rwsr-xr-x	70768	/bin/ping
+-rwsr-xr-x	61520	/bin/ping6
 -rwxr-xr-x	93232	/bin/ps
--rwxr-xr-x	31360	/bin/pwd
+-rwxr-xr-x	31392	/bin/pwd
 lrwxrwxrwx	0	/bin/rbash
[...]
```

[See full examples](./examples).

## Sub-project

* [docker-promote](https://github.com/Wealthforge-Technologies/docker-promote): promote a docker image only if it is different than than the one presently there. ([@Wealthforge-Technologies](https://github.com/Wealthforge-Technologies))

## License

MIT
