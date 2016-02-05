# docker-diff
:whale: Compare Docker images

## Usage

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
< -rwxr-xr-x 203        etc/init.d/acpid                                                                                    
< -rwxr-xr-x 379        etc/init.d/binfmt                                                                                   
< -rwxr-xr-x 5353       etc/init.d/bootmisc                                                                                 
< -rwxr-xr-x 1421       etc/init.d/consolefont                                                                              
< -rwxr-xr-x 165        etc/init.d/cron                                                                                     
< -rwxr-xr-x 3128       etc/init.d/devfs                                                                                    
< -rwxr-xr-x 326        etc/init.d/dmesg                                                                                    
< -rwxr-xr-x 172        etc/init.d/dnsd                                                                                     
< -rwxr-xr-x 2693       etc/init.d/fsck                                                                                     
< lrwxrwxrwx 0          etc/init.d/functions.sh                                                                             
< -rwxr-xr-x 256        etc/init.d/hostname                                                                                 
< -rwxr-xr-x 152        etc/init.d/httpd                                                                                    
< -rwxr-xr-x 2591       etc/init.d/hwclock                                                                                  
< -rwxr-xr-x 720        etc/init.d/hwdrivers                                                                                
< -rwxr-xr-x 184        etc/init.d/inetd                                                                                    
< -rwxr-xr-x 272        etc/init.d/keymaps                                                                                  
< -rwxr-xr-x 405        etc/init.d/killprocs                                                                                
< -rwxr-xr-x 202        etc/init.d/klogd                                                                                    
< -rwxr-xr-x 2210       etc/init.d/local                                                                                    
< -rwxr-xr-x 2956       etc/init.d/localmount                                                                               
< -rwxr-xr-x 785        etc/init.d/loopback                                                                                 
< -rwxr-xr-x 740        etc/init.d/mdev                                                                                     
< -rwxr-xr-x 1953       etc/init.d/mdev-mount                                                                               
< -rwxr-xr-x 4087       etc/init.d/modloop                                                                                  
< -rwxr-xr-x 505        etc/init.d/modules                                                                                  
< -rwxr-xr-x 1082       etc/init.d/mount-ro                                                                                 
< -rwxr-xr-x 1114       etc/init.d/mtab                                                                                     
< -rwxr-xr-x 1209       etc/init.d/netmount                                                                                 
< -rwxr-xr-x 1276       etc/init.d/networking                                                                               
< -rwxr-xr-x 207        etc/init.d/ntpd                                                                                     
< -rwxr-xr-x 715        etc/init.d/numlock                                                                                  
< -rwxr-xr-x 229        etc/init.d/osclock                                                                                  
< -rwxr-xr-x 675        etc/init.d/procfs                                                                                   
< -rwxr-xr-x 253        etc/init.d/rdate                                                                                    
< -rwxr-xr-x 986        etc/init.d/root                                                                                     
< -rwxr-xr-x 1161       etc/init.d/savecache                                                                                
< -rwxr-xr-x 1622       etc/init.d/staticroute                                                                              
< -rwxr-xr-x 867        etc/init.d/swap                                                                                     
< -rwxr-xr-x 804        etc/init.d/swapfiles                                                                                
< -rwxr-xr-x 544        etc/init.d/swclock                                                                                  
< -rwxr-xr-x 623        etc/init.d/sysctl                                                                                   
< -rwxr-xr-x 3883       etc/init.d/sysfs                                                                                    
< -rwxr-xr-x 196        etc/init.d/syslog                                                                                   
< -rwxr-xr-x 1049       etc/init.d/termencoding                                                                             
< -rwxr-xr-x 362        etc/init.d/tmpfiles.dev                                                                             
< -rwxr-xr-x 338        etc/init.d/tmpfiles.setup                                                                           
< -rwxr-xr-x 949        etc/init.d/urandom                                                                                  
< -rwxr-xr-x 291        etc/init.d/watchdog                                                                                 
< -rw-r--r-- 530        etc/inittab                                                                                         
---
> -rw-r--r-- 554        etc/inittab                                                                                         
187,190d110
< drwxr-xr-x 0          etc/lbu/                                                                                            
< -rwxr-xr-x 494        etc/lbu/lbu.conf                                                                                    
< drwxr-xr-x 0          etc/local.d/                                                                                        
< -rw-r--r-- 652        etc/local.d/README                                                                                  
192c112,113
< -rw-r--r-- 2764       etc/mdev.conf                                                                                       
---
> drwxr-xr-x 0          etc/logrotate.d/                                                                                    
> -rw-r--r-- 115        etc/logrotate.d/acpid                                                                               
210c131
< -rw-r--r-- 1555       etc/passwd                                                                                          
---
> -rw-r--r-- 1269       etc/passwd                                                                                          
221d141
< -rw-r--r-- 8627       etc/rc.conf                                                                                         
223,227c143
< drwxr-xr-x 0          etc/runlevels/                                                                                      
< drwxr-xr-x 0          etc/runlevels/boot/                                                                                 
< drwxr-xr-x 0          etc/runlevels/default/                                                                              
< drwxr-xr-x 0          etc/runlevels/shutdown/                                                                             
< drwxr-xr-x 0          etc/runlevels/sysinit/                                                                              
---
> -rw-r--r-- 65         etc/securetty                                                                                       
229,230c145
< -rw-r----- 553        etc/shadow                                                                                          
< -rw-r----- 552        etc/shadowe                                                                                         
---
> -rw-r----- 454        etc/shadow                                                                                          
235c150
< -rw-r--r-- 655        etc/sysctl.d/README                                                                                 
---
> -rw-r--r-- 4138       etc/udhcpd.conf                                                                                     
240c155
< -rw-r--r-- 20211      lib/apk/db/installed                                                                                
---
> -rw-r--r-- 8216       lib/apk/db/installed                                                                                
242c157
< -rw-r--r-- 13312      lib/apk/db/scripts.tar                                                                              
---
> -rw-r--r-- 9216       lib/apk/db/scripts.tar                                                                              
245,246c160
< -rwxr-xr-x 559824     lib/ld-musl-x86_64.so.1                                                                             
< -rwxr-xr-x 5795       lib/libalpine.sh                                                                                    
---
> -rwxr-xr-x 559664     lib/ld-musl-x86_64.so.1                                                                             
248,251c162,163
< -r-xr-xr-x 2215288    lib/libcrypto.so.1.0.0                                                                              
< -r--r--r-- 22320      lib/libeinfo.so.1                                                                                   
< -r--r--r-- 46896      lib/librc.so.1                                                                                      
< -r-xr-xr-x 430520     lib/libssl.so.1.0.0                                                                                 
---
> -r-xr-xr-x 2196888    lib/libcrypto.so.1.0.0                                                                              
> -r-xr-xr-x 430264     lib/libssl.so.1.0.0                                                                                 
253c165
< -rwxr-xr-x 87968      lib/libz.so.1.2.8                                                                                   
---
> -rwxr-xr-x 87976      lib/libz.so.1.2.8                                                                                   
255,329d166
< -rwxr-xr-x 356        lib/mdev/dvbdev                                                                                     
< -rwxr-xr-x 440        lib/mdev/ide_links                                                                                  
< -rwxr-xr-x 508        lib/mdev/usbdev                                                                                     
< -rwxr-xr-x 984        lib/mdev/usbdisk_link                                                                               
< -rwxr-xr-x 260        lib/mdev/xvd_links                                                                                  
< drwxr-xr-x 0          lib/rc/                                                                                             
< drwxr-xr-x 0          lib/rc/bin/                                                                                         
< lrwxrwxrwx 0          lib/rc/bin/checkpath                                                                                
< lrwxrwxrwx 0          lib/rc/bin/ebegin                                                                                   
< lrwxrwxrwx 0          lib/rc/bin/eend                                                                                     
< lrwxrwxrwx 0          lib/rc/bin/eerror                                                                                   
< lrwxrwxrwx 0          lib/rc/bin/eerrorn                                                                                  
< lrwxrwxrwx 0          lib/rc/bin/eindent                                                                                  
< lrwxrwxrwx 0          lib/rc/bin/einfo                                                                                    
< lrwxrwxrwx 0          lib/rc/bin/einfon                                                                                   
< lrwxrwxrwx 0          lib/rc/bin/eoutdent                                                                                 
< lrwxrwxrwx 0          lib/rc/bin/esyslog                                                                                  
< lrwxrwxrwx 0          lib/rc/bin/eval_ecolors                                                                             
< lrwxrwxrwx 0          lib/rc/bin/ewaitfile                                                                                
< lrwxrwxrwx 0          lib/rc/bin/ewarn                                                                                    
< lrwxrwxrwx 0          lib/rc/bin/ewarnn                                                                                   
< lrwxrwxrwx 0          lib/rc/bin/ewend                                                                                    
< lrwxrwxrwx 0          lib/rc/bin/fstabinfo                                                                                
< lrwxrwxrwx 0          lib/rc/bin/get_options                                                                              
< lrwxrwxrwx 0          lib/rc/bin/is_newer_than                                                                            
< lrwxrwxrwx 0          lib/rc/bin/is_older_than                                                                            
< lrwxrwxrwx 0          lib/rc/bin/mountinfo                                                                                
< -rwxr-xr-x 991        lib/rc/bin/on_ac_power                                                                              
< lrwxrwxrwx 0          lib/rc/bin/rc-depend                                                                                
< lrwxrwxrwx 0          lib/rc/bin/save_options                                                                             
< lrwxrwxrwx 0          lib/rc/bin/service_crashed                                                                          
< lrwxrwxrwx 0          lib/rc/bin/service_get_value                                                                        
< lrwxrwxrwx 0          lib/rc/bin/service_hotplugged                                                                       
< lrwxrwxrwx 0          lib/rc/bin/service_inactive                                                                         
< lrwxrwxrwx 0          lib/rc/bin/service_set_value                                                                        
< lrwxrwxrwx 0          lib/rc/bin/service_started                                                                          
< lrwxrwxrwx 0          lib/rc/bin/service_started_daemon                                                                   
< lrwxrwxrwx 0          lib/rc/bin/service_starting                                                                         
< lrwxrwxrwx 0          lib/rc/bin/service_stopped                                                                          
< lrwxrwxrwx 0          lib/rc/bin/service_stopping                                                                         
< lrwxrwxrwx 0          lib/rc/bin/service_wasinactive                                                                      
< lrwxrwxrwx 0          lib/rc/bin/shell_var                                                                                
< lrwxrwxrwx 0          lib/rc/bin/vebegin                                                                                  
< lrwxrwxrwx 0          lib/rc/bin/veend                                                                                    
< lrwxrwxrwx 0          lib/rc/bin/veindent                                                                                 
< lrwxrwxrwx 0          lib/rc/bin/veinfo                                                                                   
< lrwxrwxrwx 0          lib/rc/bin/veoutdent                                                                                
< lrwxrwxrwx 0          lib/rc/bin/vewarn                                                                                   
< lrwxrwxrwx 0          lib/rc/bin/vewend                                                                                   
< drwxr-xr-x 0          lib/rc/sbin/                                                                                        
< lrwxrwxrwx 0          lib/rc/sbin/mark_service_failed                                                                     
< lrwxrwxrwx 0          lib/rc/sbin/mark_service_hotplugged                                                                 
< lrwxrwxrwx 0          lib/rc/sbin/mark_service_inactive                                                                   
< lrwxrwxrwx 0          lib/rc/sbin/mark_service_started                                                                    
< lrwxrwxrwx 0          lib/rc/sbin/mark_service_starting                                                                   
< lrwxrwxrwx 0          lib/rc/sbin/mark_service_stopped                                                                    
< lrwxrwxrwx 0          lib/rc/sbin/mark_service_stopping                                                                   
< lrwxrwxrwx 0          lib/rc/sbin/mark_service_wasinactive                                                                
< lrwxrwxrwx 0          lib/rc/sbin/rc-abort                                                                                
< lrwxrwxrwx 0          lib/rc/sbin/swclock                                                                                 
< drwxr-xr-x 0          lib/rc/sh/                                                                                          
< -rwxr-xr-x 2266       lib/rc/sh/binfmt.sh                                                                                 
< -rwxr-xr-x 240        lib/rc/sh/cgroup-release-agent.sh                                                                   
< -r--r--r-- 2711       lib/rc/sh/functions.sh                                                                              
< -rwxr-xr-x 1894       lib/rc/sh/gendepends.sh                                                                             
< -rwxr-xr-x 1433       lib/rc/sh/init-early.sh                                                                             
< -rwxr-xr-x 2356       lib/rc/sh/init.sh                                                                                   
< -rwxr-xr-x 615        lib/rc/sh/migrate-to-run.sh                                                                         
< -rwxr-xr-x 8261       lib/rc/sh/openrc-run.sh                                                                             
< -rwxr-xr-x 3376       lib/rc/sh/rc-cgroup.sh                                                                              
< -r--r--r-- 2285       lib/rc/sh/rc-functions.sh                                                                           
< -r--r--r-- 1893       lib/rc/sh/rc-mount.sh                                                                               
< -rwxr-xr-x 9974       lib/rc/sh/tmpfiles.sh                                                                               
< drwxr-xr-x 0          lib/rc/tmp/                                                                                         
< -rw-r--r-- 15         lib/rc/version                                                                                      
342c179
< -rwxr-xr-x 202752     sbin/apk                                                                                            
---
> -rwxr-xr-x 202176     sbin/apk                                                                                            
369,374d205
< -rwxr-xr-x 17266      sbin/lbu                                                                                            
< lrwxrwxrwx 0          sbin/lbu_commit                                                                                     
< lrwxrwxrwx 0          sbin/lbu_exclude                                                                                    
< lrwxrwxrwx 0          sbin/lbu_include                                                                                    
< lrwxrwxrwx 0          sbin/lbu_status                                                                                     
< lrwxrwxrwx 0          sbin/lbu_update                                                                                     
389,390d219
< -rwxr-xr-x 117224     sbin/openrc                                                                                         
< lrwxrwxrwx 0          sbin/openrc-run                                                                                     
393,395d221
< lrwxrwxrwx 0          sbin/rc                                                                                             
< lrwxrwxrwx 0          sbin/rc-service                                                                                     
< lrwxrwxrwx 0          sbin/rc-update                                                                                      
399,400d224
< lrwxrwxrwx 0          sbin/runscript                                                                                      
< lrwxrwxrwx 0          sbin/service                                                                                        
402,420d225
< -rwxr-xr-x 2155       sbin/setup-acf                                                                                      
< -rwxr-xr-x 4595       sbin/setup-alpine                                                                                   
< -rwxr-xr-x 3204       sbin/setup-apkcache                                                                                 
< -rwxr-xr-x 4886       sbin/setup-apkrepos                                                                                 
< -rwxr-xr-x 10302      sbin/setup-bootable                                                                                 
< -rwxr-xr-x 24961      sbin/setup-disk                                                                                     
< -rwxr-xr-x 1239       sbin/setup-dns                                                                                      
< -rwxr-xr-x 814        sbin/setup-gparted-desktop                                                                          
< -rwxr-xr-x 1330       sbin/setup-hostname                                                                                 
< -rwxr-xr-x 10917      sbin/setup-interfaces                                                                               
< -rwxr-xr-x 2338       sbin/setup-keymap                                                                                   
< -rwxr-xr-x 3301       sbin/setup-lbu                                                                                      
< -rwxr-xr-x 976        sbin/setup-mta                                                                                      
< -rwxr-xr-x 889        sbin/setup-ntp                                                                                      
< -rwxr-xr-x 1181       sbin/setup-proxy                                                                                    
< -rwxr-xr-x 868        sbin/setup-sshd                                                                                     
< -rwxr-xr-x 2349       sbin/setup-timezone                                                                                 
< -rwxr-xr-x 462        sbin/setup-xen-dom0                                                                                 
< -rwxr-xr-x 732        sbin/setup-xorg-base                                                                                
422d226
< lrwxrwxrwx 0          sbin/start-stop-daemon                                                                              
430,431d233
< -rwxr-xr-x 2117       sbin/update-conf                                                                                    
< -rwxr-xr-x 5194       sbin/update-kernel                                                                                  
460a263
> lrwxrwxrwx 0          usr/bin/dumpleases                                                                                  
472,473c275,276
< -rwxr-xr-x 30640      usr/bin/getconf                                                                                     
< -rwxr-xr-x 36224      usr/bin/getent                                                                                      
---
> -rwxr-xr-x 31480      usr/bin/getconf                                                                                     
> -rwxr-xr-x 36544      usr/bin/getent                                                                                      
479c282
< -rwxr-xr-x 19976      usr/bin/iconv                                                                                       
---
> -rwxr-xr-x 20360      usr/bin/iconv                                                                                       
485d287
< lrwxrwxrwx 0          usr/bin/last                                                                                        
519c321
< -rwxr-xr-x 75512      usr/bin/scanelf                                                                                     
---
> -rwxr-xr-x 71416      usr/bin/scanelf                                                                                     
533d334
< lrwxrwxrwx 0          usr/bin/su                                                                                          
546a348
> lrwxrwxrwx 0          usr/bin/truncate                                                                                    
559d360
< lrwxrwxrwx 0          usr/bin/users                                                                                       
565d365
< lrwxrwxrwx 0          usr/bin/wall                                                                                        
569d368
< lrwxrwxrwx 0          usr/bin/who                                                                                         
577,579c376,378
< -r-xr-xr-x 18632      usr/lib/engines/lib4758cca.so                                                                       
< -r-xr-xr-x 18968      usr/lib/engines/libaep.so                                                                           
< -r-xr-xr-x 14760      usr/lib/engines/libatalla.so                                                                        
---
> -r-xr-xr-x 18600      usr/lib/engines/lib4758cca.so                                                                       
> -r-xr-xr-x 18840      usr/lib/engines/libaep.so                                                                           
> -r-xr-xr-x 14600      usr/lib/engines/libatalla.so                                                                        
581,582c380,381
< -r-xr-xr-x 23224      usr/lib/engines/libchil.so                                                                          
< -r-xr-xr-x 18984      usr/lib/engines/libcswift.so                                                                        
---
> -r-xr-xr-x 23096      usr/lib/engines/libchil.so                                                                          
> -r-xr-xr-x 18824      usr/lib/engines/libcswift.so                                                                        
584,585c383,384
< -r-xr-xr-x 87304      usr/lib/engines/libgost.so                                                                          
< -r-xr-xr-x 14680      usr/lib/engines/libnuron.so                                                                         
---
> -r-xr-xr-x 87208      usr/lib/engines/libgost.so                                                                          
> -r-xr-xr-x 14552      usr/lib/engines/libnuron.so                                                                         
587,588c386,387
< -r-xr-xr-x 23088      usr/lib/engines/libsureware.so                                                                      
< -r-xr-xr-x 18968      usr/lib/engines/libubsec.so                                                                         
---
> -r-xr-xr-x 22928      usr/lib/engines/libsureware.so                                                                      
> -r-xr-xr-x 18808      usr/lib/engines/libubsec.so                                                                         
614a414
> lrwxrwxrwx 0          usr/sbin/loadfont                                                                                   
627a428
> lrwxrwxrwx 0          usr/sbin/setfont                                                                                    
628a430
> lrwxrwxrwx 0          usr/sbin/udhcpd                                                                                     
630,631d431
< drwxr-xr-x 0          usr/share/udhcpc/                                                                                   
< -rwxr-xr-x 2422       usr/share/udhcpc/default.script                                                                     
635a436
> drwxr-xr-x 0          var/empty/                                                                                          
638a440
> drwxr-xr-x 0          var/lib/udhcpd/                                                                                     
```

---

Comparing changes between [alpine:3.2](https://hub.docker.com/r/library/alpine/) and [alpine:3.3](https://hub.docker.com/r/library/alpine/).

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
< -rwxr-xr-x 43616      bin/rmdir                                                                                           
---
> -rwxr-xr-x 43648      bin/rmdir                                                                                           
55a60
> -rwxr-xr-x 111656     bin/ss                                                                                              
67c72
< -rwxr-xr-x 129608     bin/systemd-tmpfiles                                                                                
---
> -rwxr-xr-x 129624     bin/systemd-tmpfiles                                                                                
74c79
< -rwxr-xr-x 436832     bin/udevadm                                                                                         
---
> -rwxr-xr-x 436848     bin/udevadm                                                                                         
78c83
< -rwxr-xr-x 118272     bin/vdir                                                                                            
---
> -rwxr-xr-x 118368     bin/vdir                                                                                            
94,99d98
< crw-rw---- 0          dev/agpgart                                                                                         
< crw-rw---- 0          dev/audio                                                                                           
< crw-rw---- 0          dev/audio1                                                                                          
< crw-rw---- 0          dev/audio2                                                                                          
< crw-rw---- 0          dev/audio3                                                                                          
< crw-rw---- 0          dev/audioctl                                                                                        
101,134d99
< lrwxrwxrwx 0          dev/core                                                                                            
< crw-rw---- 0          dev/dsp                                                                                             
< crw-rw---- 0          dev/dsp1                                                                                            
< crw-rw---- 0          dev/dsp2                                                                                            
< crw-rw---- 0          dev/dsp3                                                                                            
< lrwxrwxrwx 0          dev/fd                                                                                              
< crw-rw-rw- 0          dev/full                                                                                            
< crw-r----- 0          dev/kmem                                                                                            
< brw-rw---- 0          dev/loop0                                                                                           
< brw-rw---- 0          dev/loop1                                                                                           
< brw-rw---- 0          dev/loop2                                                                                           
< brw-rw---- 0          dev/loop3                                                                                           
< brw-rw---- 0          dev/loop4                                                                                           
< brw-rw---- 0          dev/loop5                                                                                           
< brw-rw---- 0          dev/loop6                                                                                           
< brw-rw---- 0          dev/loop7                                                                                           
< crw-r----- 0          dev/mem                                                                                             
< crw-rw---- 0          dev/midi0                                                                                           
< crw-rw---- 0          dev/midi00                                                                                          
< crw-rw---- 0          dev/midi01                                                                                          
< crw-rw---- 0          dev/midi02                                                                                          
< crw-rw---- 0          dev/midi03                                                                                          
< crw-rw---- 0          dev/midi1                                                                                           
< crw-rw---- 0          dev/midi2                                                                                           
< crw-rw---- 0          dev/midi3                                                                                           
< crw-rw---- 0          dev/mixer                                                                                           
< crw-rw---- 0          dev/mixer1                                                                                          
< crw-rw---- 0          dev/mixer2                                                                                          
< crw-rw---- 0          dev/mixer3                                                                                          
< crw-rw---- 0          dev/mpu401data                                                                                      
< crw-rw---- 0          dev/mpu401stat                                                                                      
< crw-rw-rw- 0          dev/null                                                                                            
< crw-r----- 0          dev/port                                                                                            
< crw-rw-rw- 0          dev/ptmx                                                                                            
136,181c101
< lrwxrwxrwx 0          dev/ram                                                                                             
< brw-rw---- 0          dev/ram0                                                                                            
< brw-rw---- 0          dev/ram1                                                                                            
< brw-rw---- 0          dev/ram10                                                                                           
< brw-rw---- 0          dev/ram11                                                                                           
< brw-rw---- 0          dev/ram12                                                                                           
< brw-rw---- 0          dev/ram13                                                                                           
< brw-rw---- 0          dev/ram14                                                                                           
< brw-rw---- 0          dev/ram15                                                                                           
< brw-rw---- 0          dev/ram16                                                                                           
< brw-rw---- 0          dev/ram2                                                                                            
< brw-rw---- 0          dev/ram3                                                                                            
< brw-rw---- 0          dev/ram4                                                                                            
< brw-rw---- 0          dev/ram5                                                                                            
< brw-rw---- 0          dev/ram6                                                                                            
< brw-rw---- 0          dev/ram7                                                                                            
< brw-rw---- 0          dev/ram8                                                                                            
< brw-rw---- 0          dev/ram9                                                                                            
< crw-rw-rw- 0          dev/random                                                                                          
< crw-rw---- 0          dev/rmidi0                                                                                          
< crw-rw---- 0          dev/rmidi1                                                                                          
< crw-rw---- 0          dev/rmidi2                                                                                          
< crw-rw---- 0          dev/rmidi3                                                                                          
< crw-rw---- 0          dev/sequencer                                                                                       
< drwxrwxrwt 0          dev/shm/                                                                                            
< crw-rw---- 0          dev/smpte0                                                                                          
< crw-rw---- 0          dev/smpte1                                                                                          
< crw-rw---- 0          dev/smpte2                                                                                          
< crw-rw---- 0          dev/smpte3                                                                                          
< crw-rw---- 0          dev/sndstat                                                                                         
< lrwxrwxrwx 0          dev/stderr                                                                                          
< lrwxrwxrwx 0          dev/stdin                                                                                           
< lrwxrwxrwx 0          dev/stdout                                                                                          
< crw-rw-rw- 0          dev/tty                                                                                             
< crw------- 0          dev/tty0                                                                                            
< crw------- 0          dev/tty1                                                                                            
< crw------- 0          dev/tty2                                                                                            
< crw------- 0          dev/tty3                                                                                            
< crw------- 0          dev/tty4                                                                                            
< crw------- 0          dev/tty5                                                                                            
< crw------- 0          dev/tty6                                                                                            
< crw------- 0          dev/tty7                                                                                            
< crw------- 0          dev/tty8                                                                                            
< crw------- 0          dev/tty9                                                                                            
< crw-rw-rw- 0          dev/urandom                                                                                         
< crw-rw-rw- 0          dev/zero                                                                                            
---
> drwxr-xr-x 0          dev/shm/                                                                                            
206d125
< -rw-r--r-- 581        etc/apt/apt.conf.d/01autoremove-kernels                                                             
209,211c128,131
< -rw-r--r-- 318        etc/apt/apt.conf.d/docker-clean                                                                     
< -rw-r--r-- 70         etc/apt/apt.conf.d/docker-gzip-indexes                                                              
< -rw-r--r-- 27         etc/apt/apt.conf.d/docker-no-languages                                                              
---
> -rw-r--r-- 754        etc/apt/apt.conf.d/docker-autoremove-suggests                                                       
> -rw-r--r-- 1161       etc/apt/apt.conf.d/docker-clean                                                                     
> -rw-r--r-- 506        etc/apt/apt.conf.d/docker-gzip-indexes                                                              
> -rw-r--r-- 269        etc/apt/apt.conf.d/docker-no-languages                                                              
213c133
< -rw-r--r-- 1863       etc/apt/sources.list                                                                                
---
> -rw-r--r-- 185        etc/apt/sources.list                                                                                
216a137
> -rw-r--r-- 9525       etc/apt/trusted.gpg~                                                                                
233c154,155
< -rw-r--r-- 12309      etc/dbus-1/system.d/org.freedesktop.login1.conf                                                     
---
> -rw-r--r-- 12118      etc/dbus-1/system.d/org.freedesktop.login1.conf                                                     
> -rw-r--r-- 8529       etc/dbus-1/system.d/org.freedesktop.machine1.conf                                                   
250c172
< -rw-r--r-- 16         etc/dpkg/dpkg.cfg.d/docker-apt-speedup                                                              
---
> -rw-r--r-- 259        etc/dpkg/dpkg.cfg.d/docker-apt-speedup                                                              
258,259c180,183
< -rw-r--r-- 577        etc/group                                                                                           
< -rw-r----- 487        etc/gshadow                                                                                         
---
> -rw-r--r-- 607        etc/group                                                                                           
> -rw------- 582        etc/group-                                                                                          
> -rw-r----- 514        etc/gshadow                                                                                         
> -rw------- 492        etc/gshadow-                                                                                        
271a196,197
> -rw-r--r-- 645        etc/init/udev-fallback-graphics.conf                                                                
> -rw-r--r-- 651        etc/init/udev-finish.conf                                                                           
276c202
< -rw-r--r-- 752        etc/init.d/.depend.boot                                                                             
---
> -rw-r--r-- 782        etc/init.d/.depend.boot                                                                             
295c221
< -rwxr-xr-x 1581       etc/init.d/ondemand                                                                                 
---
> -rwxr-xr-x 1346       etc/init.d/ondemand                                                                                 
304a231
> -rwxr-xr-x 461        etc/init.d/udev-finish                                                                              
314,315c241,251
< -rw-r--r-- 20         etc/issue                                                                                           
< -rw-r--r-- 13         etc/issue.net                                                                                       
---
> drwxr-xr-x 0          etc/iproute2/                                                                                       
> -rw-r--r-- 75         etc/iproute2/ematch_map                                                                             
> -rw-r--r-- 31         etc/iproute2/group                                                                                  
> -rw-r--r-- 264        etc/iproute2/nl_protos                                                                              
> -rw-r--r-- 331        etc/iproute2/rt_dsfield                                                                             
> -rw-r--r-- 326        etc/iproute2/rt_protos                                                                              
> -rw-r--r-- 112        etc/iproute2/rt_realms                                                                              
> -rw-r--r-- 92         etc/iproute2/rt_scopes                                                                              
> -rw-r--r-- 87         etc/iproute2/rt_tables                                                                              
> -rw-r--r-- 49         etc/issue                                                                                           
> -rw-r--r-- 42         etc/issue.net                                                                                       
332,333c268,269
< -rw-r--r-- 97         etc/lsb-release                                                                                     
< -r--r--r-- 0          etc/machine-id                                                                                      
---
> -rw-r--r-- 126        etc/lsb-release                                                                                     
> -r--r--r-- 33         etc/machine-id                                                                                      
339a276
> drwxr-xr-x 0          etc/network/                                                                                        
343c280
< -rw-r--r-- 240        etc/os-release                                                                                      
---
> -rw-r--r-- 269        etc/os-release                                                                                      
362a300
> -rw------- 1177       etc/passwd-                                                                                         
364a303
> -rw-r--r-- 2932       etc/protocols                                                                                       
410a350
> lrwxrwxrwx 0          etc/rcS.d/S03udev-finish                                                                            
423a364
> -rw-r--r-- 887        etc/rpc                                                                                             
438a380
> -rw-r--r-- 19605      etc/services                                                                                        
439a382
> -rw------- 626        etc/shadow-                                                                                         
502a446
> -rwxr-xr-x 85         lib/systemd/debian-fixup                                                                            
503a448
> -rw-r--r-- 247        lib/systemd/network/01-mac-for-usb.link                                                             
506d450
< -rw-r--r-- 247        lib/systemd/network/90-mac-for-usb.link                                                             
520a465
> lrwxrwxrwx 0          lib/systemd/system/busnames.target.wants/org.freedesktop.machine1.busname                           
538a484
> lrwxrwxrwx 0          lib/systemd/system/dbus-org.freedesktop.machine1.service                                            
542c488
< -rw-r--r-- 273        lib/systemd/system/debian-fixup.service                                                             
---
> -rw-r--r-- 271        lib/systemd/system/debian-fixup.service                                                             
559d504
< -rw-r--r-- 565        lib/systemd/system/halt-local.service                                                               
566c511
< -rw-r--r-- 428        lib/systemd/system/ifup@.service                                                                    
---
> -rw-r--r-- 450        lib/systemd/system/ifup@.service                                                                    
582a528
> lrwxrwxrwx 0          lib/systemd/system/local-fs.target.wants/var-lib-machines.mount                                     
584a531
> -rw-r--r-- 531        lib/systemd/system/machines.target                                                                  
596a544
> lrwxrwxrwx 0          lib/systemd/system/multi-user.target.wants/rc-local.service                                         
610a559
> -rw-r--r-- 549        lib/systemd/system/org.freedesktop.machine1.busname                                                 
638,639d586
< drwxr-xr-x 0          lib/systemd/system/resolvconf.service.wants/                                                        
< lrwxrwxrwx 0          lib/systemd/system/resolvconf.service.wants/systemd-networkd-resolvconf-update.path                 
705a653
> lrwxrwxrwx 0          lib/systemd/system/sysinit.target.wants/udev-finish.service                                         
716c664
< -rw-r--r-- 804        lib/systemd/system/systemd-bus-proxyd.service                                                       
---
> -rw-r--r-- 647        lib/systemd/system/systemd-bus-proxyd.service                                                       
738a687
> -rw-r--r-- 948        lib/systemd/system/systemd-machined.service                                                         
740,741d688
< -rw-r--r-- 152        lib/systemd/system/systemd-networkd-resolvconf-update.path                                          
< -rw-r--r-- 514        lib/systemd/system/systemd-networkd-resolvconf-update.service                                       
744a692
> -rw-r--r-- 1134       lib/systemd/system/systemd-nspawn@.service                                                          
775a724
> -rw-r--r-- 217        lib/systemd/system/udev-finish.service                                                              
783a733
> -rw-r--r-- 475        lib/systemd/system/var-lib-machines.mount                                                           
786c736
< -rwxr-xr-x 68208      lib/systemd/system-generators/systemd-cryptsetup-generator                                          
---
> -rwxr-xr-x 72304      lib/systemd/system-generators/systemd-cryptsetup-generator                                          
788,789c738,740
< -rwxr-xr-x 39440      lib/systemd/system-generators/systemd-debug-generator                                               
< -rwxr-xr-x 80400      lib/systemd/system-generators/systemd-fstab-generator                                               
---
> -rwxr-xr-x 39432      lib/systemd/system-generators/systemd-debug-generator                                               
> -rwxr-xr-x 35328      lib/systemd/system-generators/systemd-default-display-manager-generator                             
> -rwxr-xr-x 76312      lib/systemd/system-generators/systemd-fstab-generator                                               
791c742
< -rwxr-xr-x 121440     lib/systemd/system-generators/systemd-gpt-auto-generator                                            
---
> -rwxr-xr-x 117344     lib/systemd/system-generators/systemd-gpt-auto-generator                                            
794d744
< -rwxr-xr-x 35344      lib/systemd/system-generators/systemd-rc-local-generator                                            
801c751
< -rwxr-xr-x 1511488    lib/systemd/systemd                                                                                 
---
> -rwxr-xr-x 1507416    lib/systemd/systemd                                                                                 
807c757
< -rwxr-xr-x 359632     lib/systemd/systemd-bus-proxyd                                                                      
---
> -rwxr-xr-x 355536     lib/systemd/systemd-bus-proxyd                                                                      
814c764
< -rwxr-xr-x 277712     lib/systemd/systemd-initctl                                                                         
---
> -rwxr-xr-x 273616     lib/systemd/systemd-initctl                                                                         
817c767
< -rwxr-xr-x 626584     lib/systemd/systemd-logind                                                                          
---
> -rwxr-xr-x 622488     lib/systemd/systemd-logind                                                                          
818a769
> -rwxr-xr-x 479120     lib/systemd/systemd-machined                                                                        
820c771
< -rwxr-xr-x 752888     lib/systemd/systemd-networkd                                                                        
---
> -rwxr-xr-x 744696     lib/systemd/systemd-networkd                                                                        
826,827c777,778
< -rwxr-xr-x 314576     lib/systemd/systemd-resolve-host                                                                    
< -rwxr-xr-x 520080     lib/systemd/systemd-resolved                                                                        
---
> -rwxr-xr-x 310480     lib/systemd/systemd-resolve-host                                                                    
> -rwxr-xr-x 503688     lib/systemd/systemd-resolved                                                                        
900c851
< -r--r--r-- 6656240    lib/udev/hwdb.bin                                                                                   
---
> -r--r--r-- 6844761    lib/udev/hwdb.bin                                                                                   
902c853
< -rw-r--r-- 1292931    lib/udev/hwdb.d/20-OUI.hwdb                                                                         
---
> -rw-r--r-- 1456152    lib/udev/hwdb.d/20-OUI.hwdb                                                                         
904c855
< -rw-r--r-- 39591      lib/udev/hwdb.d/20-bluetooth-vendor-product.hwdb                                                    
---
> -rw-r--r-- 36947      lib/udev/hwdb.d/20-bluetooth-vendor-product.hwdb                                                    
911,915c862,866
< -rw-r--r-- 1113001    lib/udev/hwdb.d/20-usb-vendor-model.hwdb                                                            
< -rw-r--r-- 3702       lib/udev/hwdb.d/60-evdev.hwdb                                                                       
< -rw-r--r-- 52820      lib/udev/hwdb.d/60-keyboard.hwdb                                                                    
< -rw-r--r-- 12592      lib/udev/hwdb.d/70-mouse.hwdb                                                                       
< -rw-r--r-- 4281       lib/udev/hwdb.d/70-pointingstick.hwdb                                                               
---
> -rw-r--r-- 1112302    lib/udev/hwdb.d/20-usb-vendor-model.hwdb                                                            
> -rw-r--r-- 3403       lib/udev/hwdb.d/60-evdev.hwdb                                                                       
> -rw-r--r-- 52651      lib/udev/hwdb.d/60-keyboard.hwdb                                                                    
> -rw-r--r-- 11386      lib/udev/hwdb.d/70-mouse.hwdb                                                                       
> -rw-r--r-- 4213       lib/udev/hwdb.d/70-pointingstick.hwdb                                                               
920c871
< -rw-r--r-- 613        lib/udev/rules.d/40-vm-hotadd.rules                                                                 
---
> -rw-r--r-- 534        lib/udev/rules.d/40-hyperv-hotadd.rules                                                             
932c883
< -rw-r--r-- 4903       lib/udev/rules.d/60-persistent-storage.rules                                                        
---
> -rw-r--r-- 4898       lib/udev/rules.d/60-persistent-storage.rules                                                        
938c889
< -rw-r--r-- 834        lib/udev/rules.d/70-power-switch.rules                                                              
---
> -rw-r--r-- 706        lib/udev/rules.d/70-power-switch.rules                                                              
953a905
> -rwxr-xr-x 230        lib/udev/udev-finish                                                                                
987c939
< -rw-r--r-- 158848     lib/x86_64-linux-gnu/libcryptsetup.so.4.6.0                                                         
---
> -rw-r--r-- 158944     lib/x86_64-linux-gnu/libcryptsetup.so.4.6.0                                                         
1005c957
< -rw-r--r-- 92824      lib/x86_64-linux-gnu/libkmod.so.2.2.11                                                              
---
> -rw-r--r-- 92824      lib/x86_64-linux-gnu/libkmod.so.2.2.8                                                               
1051c1003
< -rw-r--r-- 252104     lib/x86_64-linux-gnu/libseccomp.so.2.2.3                                                            
---
> -rw-r--r-- 182464     lib/x86_64-linux-gnu/libseccomp.so.2.2.1                                                            
1061c1013
< -rw-r--r-- 524024     lib/x86_64-linux-gnu/libsystemd.so.0.10.2                                                           
---
> -rw-r--r-- 524024     lib/x86_64-linux-gnu/libsystemd.so.0.10.1                                                           
1075c1027
< -rw-r--r-- 104824     lib/x86_64-linux-gnu/libz.so.1.2.8                                                                  
---
> -rw-r--r-- 108920     lib/x86_64-linux-gnu/libz.so.1.2.8                                                                  
1141a1094
> -rwxr-xr-x 60072      sbin/bridge                                                                                         
1172c1125
< -rwxr-xr-x 17         sbin/initctl                                                                                        
---
> -rwxr-xr-x 253        sbin/initctl                                                                                        
1173a1127
> lrwxrwxrwx 0          sbin/ip                                                                                             
1175c1129
< -rwxr-xr-x 19000      sbin/killall5                                                                                       
---
> -rwxr-xr-x 23096      sbin/killall5                                                                                       
1199a1154,1155
> -rwxr-xr-x 37392      sbin/rtacct                                                                                         
> -rwxr-xr-x 43536      sbin/rtmon                                                                                          
1212a1169
> -rwxr-xr-x 325544     sbin/tc                                                                                             
1224c1181
< -rwxr-xr-x 39520      usr/bin/[                                                                                           
---
> -rwxr-xr-x 39552      usr/bin/[                                                                                           
1239c1196
< -rwxr-xr-x 367856     usr/bin/busctl                                                                                      
---
> -rwxr-xr-x 363760     usr/bin/busctl                                                                                      
1244c1201
< -rwxr-xr-x 60224      usr/bin/chcon                                                                                       
---
> -rwxr-xr-x 64320      usr/bin/chcon                                                                                       
1248c1205
< -rwxr-xr-x 31296      usr/bin/cksum                                                                                       
---
> -rwxr-xr-x 31328      usr/bin/cksum                                                                                       
1253a1211
> lrwxrwxrwx 0          usr/bin/ctstat                                                                                      
1265,1266c1223,1224
< -rwxr-xr-x 39528      usr/bin/dircolors                                                                                   
< -rwxr-xr-x 27200      usr/bin/dirname                                                                                     
---
> -rwxr-xr-x 39560      usr/bin/dircolors                                                                                   
> -rwxr-xr-x 31296      usr/bin/dirname                                                                                     
1275,1276c1233,1234
< -rwxr-xr-x 117792     usr/bin/du                                                                                          
< -rwxr-xr-x 31296      usr/bin/env                                                                                         
---
> -rwxr-xr-x 113664     usr/bin/du                                                                                          
> -rwxr-xr-x 31328      usr/bin/env                                                                                         
1280c1238
< -rwxr-xr-x 76480      usr/bin/factor                                                                                      
---
> -rwxr-xr-x 76512      usr/bin/factor                                                                                      
1285,1286c1243,1244
< -rwxr-xr-x 39520      usr/bin/fmt                                                                                         
< -rwxr-xr-x 31328      usr/bin/fold                                                                                        
---
> -rwxr-xr-x 39552      usr/bin/fmt                                                                                         
> -rwxr-xr-x 31360      usr/bin/fold                                                                                        
1299c1257
< -rwxr-xr-x 290000     usr/bin/hostnamectl                                                                                 
---
> -rwxr-xr-x 285904     usr/bin/hostnamectl                                                                                 
1305c1263
< -rwxr-xr-x 138736     usr/bin/install                                                                                     
---
> -rwxr-xr-x 142832     usr/bin/install                                                                                     
1319a1278
> -rwxr-xr-x 14928      usr/bin/lnstat                                                                                      
1344a1304
> -rwxr-xr-x 18816      usr/bin/nstat                                                                                       
1352,1353c1312,1313
< -rwxr-xr-x 31296      usr/bin/pathchk                                                                                     
< -rwxr-xr-x 1742800    usr/bin/perl                                                                                        
---
> -rwxr-xr-x 31328      usr/bin/pathchk                                                                                     
> -rwxr-xr-x 1739120    usr/bin/perl                                                                                        
1367c1327
< -rwxr-xr-x 60136      usr/bin/realpath                                                                                    
---
> -rwxr-xr-x 60168      usr/bin/realpath                                                                                    
1373a1334,1336
> -rwxr-xr-x 173        usr/bin/routef                                                                                      
> -rwxr-xr-x 1262       usr/bin/routel                                                                                      
> lrwxrwxrwx 0          usr/bin/rtstat                                                                                      
1389,1390c1352,1353
< -rwxr-xr-x 47784      usr/bin/sha224sum                                                                                   
< -rwxr-xr-x 47784      usr/bin/sha256sum                                                                                   
---
> -rwxr-xr-x 51880      usr/bin/sha224sum                                                                                   
> -rwxr-xr-x 51880      usr/bin/sha256sum                                                                                   
1398,1403c1361,1366
< -rwxr-xr-x 105856     usr/bin/sort                                                                                        
< -rwxr-xr-x 68912      usr/bin/split                                                                                       
< -rwxr-xr-x 76704      usr/bin/stat                                                                                        
< -rwxr-xr-x 64224      usr/bin/stdbuf                                                                                      
< -rwxr-xr-x 39560      usr/bin/sum                                                                                         
< -rwxr-xr-x 1429488    usr/bin/systemd-analyze                                                                             
---
> -rwxr-xr-x 105920     usr/bin/sort                                                                                        
> -rwxr-xr-x 68976      usr/bin/split                                                                                       
> -rwxr-xr-x 76672      usr/bin/stat                                                                                        
> -rwxr-xr-x 64256      usr/bin/stdbuf                                                                                      
> -rwxr-xr-x 39592      usr/bin/sum                                                                                         
> -rwxr-xr-x 1425376    usr/bin/systemd-analyze                                                                             
1408a1372
> -rwxr-xr-x 527616     usr/bin/systemd-nspawn                                                                              
1413c1377
< -rwxr-xr-x 35456      usr/bin/tac                                                                                         
---
> -rwxr-xr-x 35488      usr/bin/tac                                                                                         
1417c1381
< -rwxr-xr-x 35424      usr/bin/test                                                                                        
---
> -rwxr-xr-x 35456      usr/bin/test                                                                                        
1420c1384
< -rwxr-xr-x 52496      usr/bin/timeout                                                                                     
---
> -rwxr-xr-x 52528      usr/bin/timeout                                                                                     
1429c1393
< -rwxr-xr-x 35424      usr/bin/tsort                                                                                       
---
> -rwxr-xr-x 39520      usr/bin/tsort                                                                                       
1433c1397
< -rwxr-xr-x 43680      usr/bin/uniq                                                                                        
---
> -rwxr-xr-x 39584      usr/bin/uniq                                                                                        
1438c1402
< -rwxr-xr-x 31328      usr/bin/users                                                                                       
---
> -rwxr-xr-x 31360      usr/bin/users                                                                                       
1555c1519
< -rw-r--r-- 619        usr/lib/systemd/user/systemd-bus-proxyd.service                                                     
---
> -rw-r--r-- 473        usr/lib/systemd/user/systemd-bus-proxyd.service                                                     
1561a1526,1533
> drwxr-xr-x 0          usr/lib/tc/                                                                                         
> -rw-r--r-- 23077      usr/lib/tc/experimental.dist                                                                        
> lrwxrwxrwx 0          usr/lib/tc/m_ipt.so                                                                                 
> -rw-r--r-- 10536      usr/lib/tc/m_xt.so                                                                                  
> -rw-r--r-- 23573      usr/lib/tc/normal.dist                                                                              
> -rw-r--r-- 23729      usr/lib/tc/pareto.dist                                                                              
> -rw-r--r-- 23447      usr/lib/tc/paretonormal.dist                                                                        
> -rw-r--r-- 10400      usr/lib/tc/q_atm.so                                                                                 
1567a1540
> -rw-r--r-- 981        usr/lib/tmpfiles.d/systemd-nspawn.conf                                                              
1831c1804
< -rw-r--r-- 1329968    usr/lib/x86_64-linux-gnu/libapt-pkg.so.4.16.0                                                       
---
> -rw-r--r-- 1325872    usr/lib/x86_64-linux-gnu/libapt-pkg.so.4.16.0                                                       
1834c1807
< -rw-r--r-- 1756624    usr/lib/x86_64-linux-gnu/libdb-5.3.so                                                               
---
> -rw-r--r-- 1760752    usr/lib/x86_64-linux-gnu/libdb-5.3.so                                                               
1851c1824
< -rw-r--r-- 214912     usr/lib/x86_64-linux-gnu/libsemanage.so.1                                                           
---
> -rw-r--r-- 215168     usr/lib/x86_64-linux-gnu/libsemanage.so.1                                                           
1853c1826
< -rw-r--r-- 1566568    usr/lib/x86_64-linux-gnu/libstdc++.so.6.0.21                                                        
---
> -rw-r--r-- 1562472    usr/lib/x86_64-linux-gnu/libstdc++.so.6.0.21                                                        
1862c1835
< -rw-r--r-- 3336       usr/lib/x86_64-linux-gnu/perl/5.20.2/Config.pm                                                      
---
> -rw-r--r-- 3337       usr/lib/x86_64-linux-gnu/perl/5.20.2/Config.pm                                                      
1864c1837
< -rw-r--r-- 48246      usr/lib/x86_64-linux-gnu/perl/5.20.2/Config_heavy.pl                                                
---
> -rw-r--r-- 48143      usr/lib/x86_64-linux-gnu/perl/5.20.2/Config_heavy.pl                                                
1917c1890
< -rw-r--r-- 384304     usr/lib/x86_64-linux-gnu/perl/5.20.2/auto/re/re.so                                                  
---
> -rw-r--r-- 392496     usr/lib/x86_64-linux-gnu/perl/5.20.2/auto/re/re.so                                                  
1934a1908
> -rwxr-xr-x 43704      usr/sbin/arpd                                                                                       
1937c1911
< -rwxr-xr-x 35520      usr/sbin/chroot                                                                                     
---
> -rwxr-xr-x 35552      usr/sbin/chroot                                                                                     
1966c1940
< -rwxr-xr-x 19         usr/sbin/policy-rc.d                                                                                
---
> -rwxr-xr-x 255        usr/sbin/policy-rc.d                                                                                
2053a2028
> -rw-r--r-- 3194       usr/share/bash-completion/completions/machinectl                                                    
2084c2059
< -rw-r--r-- 11836      usr/share/bash-completion/completions/systemctl                                                     
---
> -rw-r--r-- 11887      usr/share/bash-completion/completions/systemctl                                                     
2090a2066
> -rw-r--r-- 5876       usr/share/bash-completion/completions/systemd-nspawn                                                
2133a2110
> -rw-r--r-- 417        usr/share/dbus-1/system-services/org.freedesktop.machine1.service                                   
2181c2158
< -rw-r--r-- 812        usr/share/doc/base-files/changelog.gz                                                               
---
> -rw-r--r-- 1079       usr/share/doc/base-files/changelog.gz                                                               
2199c2176
< -rw-r--r-- 981        usr/share/doc/bash/changelog.Debian.gz                                                              
---
> -rw-r--r-- 1174       usr/share/doc/bash/changelog.Debian.gz                                                              
2209c2186
< -rw-r--r-- 60316      usr/share/doc/coreutils/NEWS.gz                                                                     
---
> -rw-r--r-- 60280      usr/share/doc/coreutils/NEWS.gz                                                                     
2214c2191
< -rw-r--r-- 1804       usr/share/doc/coreutils/changelog.Debian.gz                                                         
---
> -rw-r--r-- 1599       usr/share/doc/coreutils/changelog.Debian.gz                                                         
2241c2218
< -rw-r--r-- 10101      usr/share/doc/dpkg/changelog.Debian.gz                                                              
---
> -rw-r--r-- 10446      usr/share/doc/dpkg/changelog.Debian.gz                                                              
2260c2237
< -rw-r--r-- 5233       usr/share/doc/gcc-5-base/README.Debian.amd64.gz                                                     
---
> -rw-r--r-- 5369       usr/share/doc/gcc-5-base/README.Debian.amd64.gz                                                     
2262c2239
< -rw-r--r-- 1327       usr/share/doc/gcc-5-base/changelog.Debian.gz                                                        
---
> -rw-r--r-- 1437       usr/share/doc/gcc-5-base/changelog.Debian.gz                                                        
2300a2278,2283
> drwxr-xr-x 0          usr/share/doc/inetutils-ping/                                                                       
> -rw-r--r-- 732        usr/share/doc/inetutils-ping/AUTHORS                                                                
> -rw-r--r-- 6325       usr/share/doc/inetutils-ping/NEWS.gz                                                                
> -rw-r--r-- 1911       usr/share/doc/inetutils-ping/THANKS                                                                 
> -rw-r--r-- 2698       usr/share/doc/inetutils-ping/changelog.Debian.gz                                                    
> -rw-r--r-- 6192       usr/share/doc/inetutils-ping/copyright                                                              
2313a2297,2300
> drwxr-xr-x 0          usr/share/doc/iproute2/                                                                             
> -rw-r--r-- 267        usr/share/doc/iproute2/README.Debian                                                                
> -rw-r--r-- 995        usr/share/doc/iproute2/changelog.Debian.gz                                                          
> -rw-r--r-- 2813       usr/share/doc/iproute2/copyright                                                                    
2318c2305
< -rw-r--r-- 2603       usr/share/doc/libapparmor1/changelog.Debian.gz                                                      
---
> -rw-r--r-- 2618       usr/share/doc/libapparmor1/changelog.Debian.gz                                                      
2322c2309
< -rw-r--r-- 1720       usr/share/doc/libapt-pkg4.16/changelog.gz                                                           
---
> -rw-r--r-- 1460       usr/share/doc/libapt-pkg4.16/changelog.gz                                                           
2364c2351
< -rw-r--r-- 2693       usr/share/doc/libcryptsetup4/changelog.Debian.gz                                                    
---
> -rw-r--r-- 3441       usr/share/doc/libcryptsetup4/changelog.Debian.gz                                                    
2368c2355
< -rw-r--r-- 1139       usr/share/doc/libdb5.3/changelog.Debian.gz                                                          
---
> -rw-r--r-- 1554       usr/share/doc/libdb5.3/changelog.Debian.gz                                                          
2392c2379
< -rw-r--r-- 1204       usr/share/doc/libkmod2/changelog.Debian.gz                                                          
---
> -rw-r--r-- 1226       usr/share/doc/libkmod2/changelog.Debian.gz                                                          
2432c2419
< -rw-r--r-- 1416       usr/share/doc/libpcre3/changelog.Debian.gz                                                          
---
> -rw-r--r-- 1458       usr/share/doc/libpcre3/changelog.Debian.gz                                                          
2447c2434
< -rw-r--r-- 1406       usr/share/doc/libseccomp2/changelog.Debian.gz                                                       
---
> -rw-r--r-- 1578       usr/share/doc/libseccomp2/changelog.Debian.gz                                                       
2450c2437
< -rw-r--r-- 1827       usr/share/doc/libselinux1/changelog.Debian.gz                                                       
---
> -rw-r--r-- 1823       usr/share/doc/libselinux1/changelog.Debian.gz                                                       
2453c2440
< -rw-r--r-- 1548       usr/share/doc/libsemanage-common/changelog.Debian.gz                                                
---
> -rw-r--r-- 1534       usr/share/doc/libsemanage-common/changelog.Debian.gz                                                
2456c2443
< -rw-r--r-- 1544       usr/share/doc/libsemanage1/changelog.Debian.gz                                                      
---
> -rw-r--r-- 1530       usr/share/doc/libsemanage1/changelog.Debian.gz                                                      
2476c2463
< -rw-r--r-- 4782       usr/share/doc/libsystemd0/changelog.Debian.gz                                                       
---
> -rw-r--r-- 6290       usr/share/doc/libsystemd0/changelog.Debian.gz                                                       
2483c2470
< -rw-r--r-- 4781       usr/share/doc/libudev1/changelog.Debian.gz                                                          
---
> -rw-r--r-- 6290       usr/share/doc/libudev1/changelog.Debian.gz                                                          
2497c2484
< -rw-r--r-- 930        usr/share/doc/locales/changelog.Debian.gz                                                           
---
> -rw-r--r-- 960        usr/share/doc/locales/changelog.Debian.gz                                                           
2547a2535,2537
> drwxr-xr-x 0          usr/share/doc/netbase/                                                                              
> -rw-r--r-- 1652       usr/share/doc/netbase/changelog.gz                                                                  
> -rw-r--r-- 535        usr/share/doc/netbase/copyright                                                                     
2562c2552
< -rw-r--r-- 52917      usr/share/doc/perl/changelog.Debian.gz                                                              
---
> -rw-r--r-- 52733      usr/share/doc/perl/changelog.Debian.gz                                                              
2595c2585
< -rw-r--r-- 5488       usr/share/doc/systemd/CODING_STYLE.gz                                                               
---
> -rw-r--r-- 5335       usr/share/doc/systemd/CODING_STYLE.gz                                                               
2599,2600c2589
< -rw-r--r-- 221        usr/share/doc/systemd/NEWS.Debian.gz                                                                
< -rw-r--r-- 80165      usr/share/doc/systemd/NEWS.gz                                                                       
---
> -rw-r--r-- 79765      usr/share/doc/systemd/NEWS.gz                                                                       
2602,2603c2591,2592
< -rw-r--r-- 1895       usr/share/doc/systemd/README.Debian.gz                                                              
< -rw-r--r-- 4222       usr/share/doc/systemd/README.gz                                                                     
---
> -rw-r--r-- 2057       usr/share/doc/systemd/README.Debian                                                                 
> -rw-r--r-- 4339       usr/share/doc/systemd/README.gz                                                                     
2607c2596
< -rw-r--r-- 4778       usr/share/doc/systemd-sysv/changelog.Debian.gz                                                      
---
> -rw-r--r-- 6289       usr/share/doc/systemd-sysv/changelog.Debian.gz                                                      
2619c2608
< -rw-r--r-- 3233       usr/share/doc/sysvinit-utils/changelog.Debian.gz                                                    
---
> -rw-r--r-- 3798       usr/share/doc/sysvinit-utils/changelog.Debian.gz                                                    
2631c2620
< -rw-r--r-- 973        usr/share/doc/tzdata/changelog.Debian.gz                                                            
---
> -rw-r--r-- 924        usr/share/doc/tzdata/changelog.Debian.gz                                                            
2700c2689
< -rw-r--r-- 997        usr/share/doc/zlib1g/changelog.Debian.gz                                                            
---
> -rw-r--r-- 1034       usr/share/doc/zlib1g/changelog.Debian.gz                                                            
2716c2705
< -rw-r--r-- 54564      usr/share/gcc-5/python/libstdcxx/v6/printers.py                                                     
---
> -rw-r--r-- 52694      usr/share/gcc-5/python/libstdcxx/v6/printers.py                                                     
2727c2716
< -rw-r--r-- 7766       usr/share/i18n/SUPPORTED                                                                            
---
> -rw-r--r-- 7754       usr/share/i18n/SUPPORTED                                                                            
3152d3140
< -rw-r--r-- 5939       usr/share/i18n/locales/ln_CD                                                                        
3154c3142
< -rw-r--r-- 5781       usr/share/i18n/locales/lt_LT                                                                        
---
> -rw-r--r-- 5776       usr/share/i18n/locales/lt_LT                                                                        
3277c3265
< -rw-r--r-- 211015     usr/share/info/coreutils.info.gz                                                                    
---
> -rw-r--r-- 210957     usr/share/info/coreutils.info.gz                                                                    
3289c3277
< -rwxr-xr-x 1725       usr/share/initramfs-tools/hooks/udev                                                                
---
> -rwxr-xr-x 1386       usr/share/initramfs-tools/hooks/udev                                                                
3315a3304
> -rw-r--r-- 109        usr/share/lintian/overrides/inetutils-ping                                                          
3436c3425
< -rw-r--r-- 45381      usr/share/locale/it/LC_MESSAGES/apt.mo                                                              
---
> -rw-r--r-- 44273      usr/share/locale/it/LC_MESSAGES/apt.mo                                                              
3439c3428
< -rw-r--r-- 28248      usr/share/locale/it/LC_MESSAGES/libapt-pkg4.16.mo                                                   
---
> -rw-r--r-- 28194      usr/share/locale/it/LC_MESSAGES/libapt-pkg4.16.mo                                                   
3518c3507
< -rw-r--r-- 59731      usr/share/locale/ru/LC_MESSAGES/apt.mo                                                              
---
> -rw-r--r-- 49446      usr/share/locale/ru/LC_MESSAGES/apt.mo                                                              
3520c3509
< -rw-r--r-- 36087      usr/share/locale/ru/LC_MESSAGES/libapt-pkg4.16.mo                                                   
---
> -rw-r--r-- 34813      usr/share/locale/ru/LC_MESSAGES/libapt-pkg4.16.mo                                                   
3548c3537
< -rw-r--r-- 45061      usr/share/locale/tr/LC_MESSAGES/apt.mo                                                              
---
> -rw-r--r-- 45064      usr/share/locale/tr/LC_MESSAGES/apt.mo                                                              
3565c3554
< -rw-r--r-- 42133      usr/share/locale/zh_CN/LC_MESSAGES/apt.mo                                                           
---
> -rw-r--r-- 42159      usr/share/locale/zh_CN/LC_MESSAGES/apt.mo                                                           
3568c3557
< -rw-r--r-- 26500      usr/share/locale/zh_CN/LC_MESSAGES/libapt-pkg4.16.mo                                                
---
> -rw-r--r-- 26497      usr/share/locale/zh_CN/LC_MESSAGES/libapt-pkg4.16.mo                                                
3644c3633
< -rw-r--r-- 17242      usr/share/man/de/man5/apt.conf.5.gz                                                                 
---
> -rw-r--r-- 17243      usr/share/man/de/man5/apt.conf.5.gz                                                                 
3659c3648
< -rw-r--r-- 2880       usr/share/man/de/man8/apt-cdrom.8.gz                                                                
---
> -rw-r--r-- 2881       usr/share/man/de/man8/apt-cdrom.8.gz                                                                
3661c3650
< -rw-r--r-- 9519       usr/share/man/de/man8/apt-get.8.gz                                                                  
---
> -rw-r--r-- 9520       usr/share/man/de/man8/apt-get.8.gz                                                                  
3664c3653
< -rw-r--r-- 3736       usr/share/man/de/man8/apt-secure.8.gz                                                               
---
> -rw-r--r-- 3737       usr/share/man/de/man8/apt-secure.8.gz                                                               
3706c3695
< -rw-r--r-- 16117      usr/share/man/es/man5/apt.conf.5.gz                                                                 
---
> -rw-r--r-- 16119      usr/share/man/es/man5/apt.conf.5.gz                                                                 
3715c3704
< -rw-r--r-- 6072       usr/share/man/es/man8/apt-cache.8.gz                                                                
---
> -rw-r--r-- 6073       usr/share/man/es/man8/apt-cache.8.gz                                                                
3717,3721c3706,3710
< -rw-r--r-- 2581       usr/share/man/es/man8/apt-config.8.gz                                                               
< -rw-r--r-- 9286       usr/share/man/es/man8/apt-get.8.gz                                                                  
< -rw-r--r-- 2264       usr/share/man/es/man8/apt-key.8.gz                                                                  
< -rw-r--r-- 2349       usr/share/man/es/man8/apt-mark.8.gz                                                                 
< -rw-r--r-- 3549       usr/share/man/es/man8/apt-secure.8.gz                                                               
---
> -rw-r--r-- 2580       usr/share/man/es/man8/apt-config.8.gz                                                               
> -rw-r--r-- 9287       usr/share/man/es/man8/apt-get.8.gz                                                                  
> -rw-r--r-- 2265       usr/share/man/es/man8/apt-key.8.gz                                                                  
> -rw-r--r-- 2350       usr/share/man/es/man8/apt-mark.8.gz                                                                 
> -rw-r--r-- 3550       usr/share/man/es/man8/apt-secure.8.gz                                                               
3762c3751
< -rw-r--r-- 17082      usr/share/man/fr/man5/apt.conf.5.gz                                                                 
---
> -rw-r--r-- 17084      usr/share/man/fr/man5/apt.conf.5.gz                                                                 
3771c3760
< -rw-r--r-- 5221       usr/share/man/fr/man5/sources.list.5.gz                                                             
---
> -rw-r--r-- 5222       usr/share/man/fr/man5/sources.list.5.gz                                                             
3776c3765
< -rw-r--r-- 6200       usr/share/man/fr/man8/apt-cache.8.gz                                                                
---
> -rw-r--r-- 6201       usr/share/man/fr/man8/apt-cache.8.gz                                                                
3780c3769
< -rw-r--r-- 2294       usr/share/man/fr/man8/apt-key.8.gz                                                                  
---
> -rw-r--r-- 2293       usr/share/man/fr/man8/apt-key.8.gz                                                                  
3783c3772
< -rw-r--r-- 3171       usr/share/man/fr/man8/apt.8.gz                                                                      
---
> -rw-r--r-- 3172       usr/share/man/fr/man8/apt.8.gz                                                                      
3857c3846
< -rw-r--r-- 16120      usr/share/man/it/man5/apt.conf.5.gz                                                                 
---
> -rw-r--r-- 16221      usr/share/man/it/man5/apt.conf.5.gz                                                                 
3866c3855
< -rw-r--r-- 4921       usr/share/man/it/man5/sources.list.5.gz                                                             
---
> -rw-r--r-- 4922       usr/share/man/it/man5/sources.list.5.gz                                                             
3871,3872c3860,3861
< -rw-r--r-- 5993       usr/share/man/it/man8/apt-cache.8.gz                                                                
< -rw-r--r-- 2796       usr/share/man/it/man8/apt-cdrom.8.gz                                                                
---
> -rw-r--r-- 5994       usr/share/man/it/man8/apt-cache.8.gz                                                                
> -rw-r--r-- 2797       usr/share/man/it/man8/apt-cdrom.8.gz                                                                
3874c3863
< -rw-r--r-- 8965       usr/share/man/it/man8/apt-get.8.gz                                                                  
---
> -rw-r--r-- 8999       usr/share/man/it/man8/apt-get.8.gz                                                                  
3877,3878c3866
< -rw-r--r-- 3516       usr/share/man/it/man8/apt-secure.8.gz                                                               
< -rw-r--r-- 3102       usr/share/man/it/man8/apt.8.gz                                                                      
---
> -rw-r--r-- 3517       usr/share/man/it/man8/apt-secure.8.gz                                                               
3927c3915
< -rw-r--r-- 16511      usr/share/man/ja/man5/apt.conf.5.gz                                                                 
---
> -rw-r--r-- 16512      usr/share/man/ja/man5/apt.conf.5.gz                                                                 
3943,3944c3931,3932
< -rw-r--r-- 3757       usr/share/man/ja/man8/apt-secure.8.gz                                                               
< -rw-r--r-- 3296       usr/share/man/ja/man8/apt.8.gz                                                                      
---
> -rw-r--r-- 3758       usr/share/man/ja/man8/apt-secure.8.gz                                                               
> -rw-r--r-- 3297       usr/share/man/ja/man8/apt.8.gz                                                                      
3983c3971
< -rw-r--r-- 680        usr/share/man/man1/arch.1.gz                                                                        
---
> -rw-r--r-- 682        usr/share/man/man1/arch.1.gz                                                                        
3993c3981
< -rw-r--r-- 1000       usr/share/man/man1/cat.1.gz                                                                         
---
> -rw-r--r-- 999        usr/share/man/man1/cat.1.gz                                                                         
3999,4001c3987,3989
< -rw-r--r-- 1270       usr/share/man/man1/chgrp.1.gz                                                                       
< -rw-r--r-- 2657       usr/share/man/man1/chmod.1.gz                                                                       
< -rw-r--r-- 1784       usr/share/man/man1/chown.1.gz                                                                       
---
> -rw-r--r-- 1269       usr/share/man/man1/chgrp.1.gz                                                                       
> -rw-r--r-- 2655       usr/share/man/man1/chmod.1.gz                                                                       
> -rw-r--r-- 1783       usr/share/man/man1/chown.1.gz                                                                       
4004c3992
< -rw-r--r-- 669        usr/share/man/man1/cksum.1.gz                                                                       
---
> -rw-r--r-- 668        usr/share/man/man1/cksum.1.gz                                                                       
4008,4011c3996,3999
< -rw-r--r-- 1027       usr/share/man/man1/comm.1.gz                                                                        
< -rw-r--r-- 2297       usr/share/man/man1/cp.1.gz                                                                          
< -rw-r--r-- 1193       usr/share/man/man1/csplit.1.gz                                                                      
< -rw-r--r-- 1201       usr/share/man/man1/cut.1.gz                                                                         
---
> -rw-r--r-- 1026       usr/share/man/man1/comm.1.gz                                                                        
> -rw-r--r-- 2296       usr/share/man/man1/cp.1.gz                                                                          
> -rw-r--r-- 1192       usr/share/man/man1/csplit.1.gz                                                                      
> -rw-r--r-- 1200       usr/share/man/man1/cut.1.gz                                                                         
4013c4001
< -rw-r--r-- 2592       usr/share/man/man1/date.1.gz                                                                        
---
> -rw-r--r-- 2591       usr/share/man/man1/date.1.gz                                                                        
4025,4026c4013,4014
< -rw-r--r-- 3069       usr/share/man/man1/dir.1.gz                                                                         
< -rw-r--r-- 869        usr/share/man/man1/dircolors.1.gz                                                                   
---
> -rw-r--r-- 3068       usr/share/man/man1/dir.1.gz                                                                         
> -rw-r--r-- 870        usr/share/man/man1/dircolors.1.gz                                                                   
4039c4027
< -rw-r--r-- 2221       usr/share/man/man1/du.1.gz                                                                          
---
> -rw-r--r-- 2222       usr/share/man/man1/du.1.gz                                                                          
4042,4043c4030,4031
< -rw-r--r-- 879        usr/share/man/man1/env.1.gz                                                                         
< -rw-r--r-- 853        usr/share/man/man1/expand.1.gz                                                                      
---
> -rw-r--r-- 877        usr/share/man/man1/env.1.gz                                                                         
> -rw-r--r-- 852        usr/share/man/man1/expand.1.gz                                                                      
4045,4046c4033,4034
< -rw-r--r-- 1317       usr/share/man/man1/expr.1.gz                                                                        
< -rw-r--r-- 725        usr/share/man/man1/factor.1.gz                                                                      
---
> -rw-r--r-- 1315       usr/share/man/man1/expr.1.gz                                                                        
> -rw-r--r-- 724        usr/share/man/man1/factor.1.gz                                                                      
4053c4041
< -rw-r--r-- 816        usr/share/man/man1/fold.1.gz                                                                        
---
> -rw-r--r-- 815        usr/share/man/man1/fold.1.gz                                                                        
4068,4069c4056,4057
< -rw-r--r-- 1012       usr/share/man/man1/head.1.gz                                                                        
< -rw-r--r-- 677        usr/share/man/man1/hostid.1.gz                                                                      
---
> -rw-r--r-- 1011       usr/share/man/man1/head.1.gz                                                                        
> -rw-r--r-- 676        usr/share/man/man1/hostid.1.gz                                                                      
4072c4060
< -rw-r--r-- 955        usr/share/man/man1/id.1.gz                                                                          
---
> -rw-r--r-- 954        usr/share/man/man1/id.1.gz                                                                          
4076c4064
< -rw-r--r-- 1825       usr/share/man/man1/install.1.gz                                                                     
---
> -rw-r--r-- 1824       usr/share/man/man1/install.1.gz                                                                     
4082c4070
< -rw-r--r-- 1540       usr/share/man/man1/join.1.gz                                                                        
---
> -rw-r--r-- 1539       usr/share/man/man1/join.1.gz                                                                        
4088c4076
< -rw-r--r-- 675        usr/share/man/man1/link.1.gz                                                                        
---
> -rw-r--r-- 674        usr/share/man/man1/link.1.gz                                                                        
4091c4079
< -rw-r--r-- 1720       usr/share/man/man1/ln.1.gz                                                                          
---
> -rw-r--r-- 1718       usr/share/man/man1/ln.1.gz                                                                          
4100a4089
> -rw-r--r-- 7872       usr/share/man/man1/machinectl.1.gz                                                                  
4103c4092
< -rw-r--r-- 1205       usr/share/man/man1/md5sum.1.gz                                                                      
---
> -rw-r--r-- 1204       usr/share/man/man1/md5sum.1.gz                                                                      
4112c4101
< -rw-r--r-- 1421       usr/share/man/man1/mv.1.gz                                                                          
---
> -rw-r--r-- 1419       usr/share/man/man1/mv.1.gz                                                                          
4119c4108
< -rw-r--r-- 958        usr/share/man/man1/nice.1.gz                                                                        
---
> -rw-r--r-- 957        usr/share/man/man1/nice.1.gz                                                                        
4121c4110
< -rw-r--r-- 1294       usr/share/man/man1/nl.1.gz                                                                          
---
> -rw-r--r-- 1293       usr/share/man/man1/nl.1.gz                                                                          
4123c4112
< -rw-r--r-- 728        usr/share/man/man1/nproc.1.gz                                                                       
---
> -rw-r--r-- 727        usr/share/man/man1/nproc.1.gz                                                                       
4126c4115
< -rw-r--r-- 2010       usr/share/man/man1/od.1.gz                                                                          
---
> -rw-r--r-- 2009       usr/share/man/man1/od.1.gz                                                                          
4130,4131c4119,4120
< -rw-r--r-- 852        usr/share/man/man1/paste.1.gz                                                                       
< -rw-r--r-- 774        usr/share/man/man1/pathchk.1.gz                                                                     
---
> -rw-r--r-- 851        usr/share/man/man1/paste.1.gz                                                                       
> -rw-r--r-- 773        usr/share/man/man1/pathchk.1.gz                                                                     
4136c4125,4127
< -rw-r--r-- 887        usr/share/man/man1/pinky.1.gz                                                                       
---
> -rw-r--r-- 4400       usr/share/man/man1/ping.1.gz                                                                        
> -rw-r--r-- 767        usr/share/man/man1/ping6.1.gz                                                                       
> -rw-r--r-- 886        usr/share/man/man1/pinky.1.gz                                                                       
4139,4141c4130,4132
< -rw-r--r-- 2030       usr/share/man/man1/pr.1.gz                                                                          
< -rw-r--r-- 861        usr/share/man/man1/printenv.1.gz                                                                    
< -rw-r--r-- 1196       usr/share/man/man1/printf.1.gz                                                                      
---
> -rw-r--r-- 2029       usr/share/man/man1/pr.1.gz                                                                          
> -rw-r--r-- 860        usr/share/man/man1/printenv.1.gz                                                                    
> -rw-r--r-- 1195       usr/share/man/man1/printf.1.gz                                                                      
4144,4145c4135,4136
< -rw-r--r-- 1310       usr/share/man/man1/ptx.1.gz                                                                         
< -rw-r--r-- 866        usr/share/man/man1/pwd.1.gz                                                                         
---
> -rw-r--r-- 1309       usr/share/man/man1/ptx.1.gz                                                                         
> -rw-r--r-- 865        usr/share/man/man1/pwd.1.gz                                                                         
4148c4139
< -rw-r--r-- 955        usr/share/man/man1/readlink.1.gz                                                                    
---
> -rw-r--r-- 954        usr/share/man/man1/readlink.1.gz                                                                    
4157c4148
< -rw-r--r-- 1090       usr/share/man/man1/runcon.1.gz                                                                      
---
> -rw-r--r-- 1089       usr/share/man/man1/runcon.1.gz                                                                      
4167c4158
< -rw-r--r-- 1108       usr/share/man/man1/seq.1.gz                                                                         
---
> -rw-r--r-- 1106       usr/share/man/man1/seq.1.gz                                                                         
4173,4174c4164,4165
< -rw-r--r-- 1107       usr/share/man/man1/sha1sum.1.gz                                                                     
< -rw-r--r-- 1105       usr/share/man/man1/sha224sum.1.gz                                                                   
---
> -rw-r--r-- 1106       usr/share/man/man1/sha1sum.1.gz                                                                     
> -rw-r--r-- 1106       usr/share/man/man1/sha224sum.1.gz                                                                   
4178,4179c4169,4170
< -rw-r--r-- 1963       usr/share/man/man1/shred.1.gz                                                                       
< -rw-r--r-- 961        usr/share/man/man1/shuf.1.gz                                                                        
---
> -rw-r--r-- 1962       usr/share/man/man1/shred.1.gz                                                                       
> -rw-r--r-- 960        usr/share/man/man1/shuf.1.gz                                                                        
4182c4173
< -rw-r--r-- 851        usr/share/man/man1/sleep.1.gz                                                                       
---
> -rw-r--r-- 849        usr/share/man/man1/sleep.1.gz                                                                       
4185,4188c4176,4179
< -rw-r--r-- 1398       usr/share/man/man1/split.1.gz                                                                       
< -rw-r--r-- 1603       usr/share/man/man1/stat.1.gz                                                                        
< -rw-r--r-- 1214       usr/share/man/man1/stdbuf.1.gz                                                                      
< -rw-r--r-- 3216       usr/share/man/man1/stty.1.gz                                                                        
---
> -rw-r--r-- 1397       usr/share/man/man1/split.1.gz                                                                       
> -rw-r--r-- 1604       usr/share/man/man1/stat.1.gz                                                                        
> -rw-r--r-- 1213       usr/share/man/man1/stdbuf.1.gz                                                                      
> -rw-r--r-- 3215       usr/share/man/man1/stty.1.gz                                                                        
4190c4181
< -rw-r--r-- 766        usr/share/man/man1/sum.1.gz                                                                         
---
> -rw-r--r-- 769        usr/share/man/man1/sum.1.gz                                                                         
4192,4193c4183,4184
< -rw-r--r-- 13078      usr/share/man/man1/systemctl.1.gz                                                                   
< -rw-r--r-- 3694       usr/share/man/man1/systemd-analyze.1.gz                                                             
---
> -rw-r--r-- 12962      usr/share/man/man1/systemctl.1.gz                                                                   
> -rw-r--r-- 3695       usr/share/man/man1/systemd-analyze.1.gz                                                             
4195,4196c4186,4187
< -rw-r--r-- 2964       usr/share/man/man1/systemd-bootchart.1.gz                                                           
< -rw-r--r-- 1542       usr/share/man/man1/systemd-cat.1.gz                                                                 
---
> -rw-r--r-- 2963       usr/share/man/man1/systemd-bootchart.1.gz                                                           
> -rw-r--r-- 1543       usr/share/man/man1/systemd-cat.1.gz                                                                 
4198c4189
< -rw-r--r-- 1917       usr/share/man/man1/systemd-cgtop.1.gz                                                               
---
> -rw-r--r-- 1916       usr/share/man/man1/systemd-cgtop.1.gz                                                               
4205a4197
> -rw-r--r-- 8407       usr/share/man/man1/systemd-nspawn.1.gz                                                              
4207c4199
< -rw-r--r-- 3373       usr/share/man/man1/systemd-run.1.gz                                                                 
---
> -rw-r--r-- 3346       usr/share/man/man1/systemd-run.1.gz                                                                 
4209c4201
< -rw-r--r-- 8677       usr/share/man/man1/systemd.1.gz                                                                     
---
> -rw-r--r-- 8671       usr/share/man/man1/systemd.1.gz                                                                     
4211,4212c4203,4204
< -rw-r--r-- 865        usr/share/man/man1/tac.1.gz                                                                         
< -rw-r--r-- 1682       usr/share/man/man1/tail.1.gz                                                                        
---
> -rw-r--r-- 864        usr/share/man/man1/tac.1.gz                                                                         
> -rw-r--r-- 1684       usr/share/man/man1/tail.1.gz                                                                        
4219c4211
< -rw-r--r-- 1604       usr/share/man/man1/test.1.gz                                                                        
---
> -rw-r--r-- 1602       usr/share/man/man1/test.1.gz                                                                        
4221,4222c4213,4214
< -rw-r--r-- 2714       usr/share/man/man1/timedatectl.1.gz                                                                 
< -rw-r--r-- 1338       usr/share/man/man1/timeout.1.gz                                                                     
---
> -rw-r--r-- 2492       usr/share/man/man1/timedatectl.1.gz                                                                 
> -rw-r--r-- 1337       usr/share/man/man1/timeout.1.gz                                                                     
4226c4218
< -rw-r--r-- 1462       usr/share/man/man1/touch.1.gz                                                                       
---
> -rw-r--r-- 1460       usr/share/man/man1/touch.1.gz                                                                       
4228c4220
< -rw-r--r-- 1478       usr/share/man/man1/tr.1.gz                                                                          
---
> -rw-r--r-- 1477       usr/share/man/man1/tr.1.gz                                                                          
4230c4222
< -rw-r--r-- 1140       usr/share/man/man1/truncate.1.gz                                                                    
---
> -rw-r--r-- 1139       usr/share/man/man1/truncate.1.gz                                                                    
4238,4239c4230,4231
< -rw-r--r-- 1329       usr/share/man/man1/uniq.1.gz                                                                        
< -rw-r--r-- 665        usr/share/man/man1/unlink.1.gz                                                                      
---
> -rw-r--r-- 1327       usr/share/man/man1/uniq.1.gz                                                                        
> -rw-r--r-- 664        usr/share/man/man1/unlink.1.gz                                                                      
4243c4235
< -rw-r--r-- 745        usr/share/man/man1/users.1.gz                                                                       
---
> -rw-r--r-- 744        usr/share/man/man1/users.1.gz                                                                       
4250c4242
< -rw-r--r-- 1014       usr/share/man/man1/wc.1.gz                                                                          
---
> -rw-r--r-- 1013       usr/share/man/man1/wc.1.gz                                                                          
4256c4248
< -rw-r--r-- 680        usr/share/man/man1/yes.1.gz                                                                         
---
> -rw-r--r-- 679        usr/share/man/man1/yes.1.gz                                                                         
4269a4262
> -rw-r--r-- 1677       usr/share/man/man3/libnetlink.3.gz                                                                  
4275c4268
< -rw-r--r-- 14642      usr/share/man/man5/apt.conf.5.gz                                                                    
---
> -rw-r--r-- 14643      usr/share/man/man5/apt.conf.5.gz                                                                    
4277,4278c4270,4271
< -rw-r--r-- 1366       usr/share/man/man5/binfmt.d.5.gz                                                                    
< -rw-r--r-- 1968       usr/share/man/man5/bootchart.conf.5.gz                                                              
---
> -rw-r--r-- 1367       usr/share/man/man5/binfmt.d.5.gz                                                                    
> -rw-r--r-- 1969       usr/share/man/man5/bootchart.conf.5.gz                                                              
4292c4285
< -rw-r--r-- 951        usr/share/man/man5/hostname.5.gz                                                                    
---
> -rw-r--r-- 952        usr/share/man/man5/hostname.5.gz                                                                    
4295c4288
< -rw-r--r-- 4857       usr/share/man/man5/journald.conf.5.gz                                                               
---
> -rw-r--r-- 4858       usr/share/man/man5/journald.conf.5.gz                                                               
4300,4301c4293,4294
< -rw-r--r-- 1298       usr/share/man/man5/locale.conf.5.gz                                                                 
< -rw-r--r-- 904        usr/share/man/man5/localtime.5.gz                                                                   
---
> -rw-r--r-- 1300       usr/share/man/man5/locale.conf.5.gz                                                                 
> -rw-r--r-- 905        usr/share/man/man5/localtime.5.gz                                                                   
4303c4296
< -rw-r--r-- 3593       usr/share/man/man5/logind.conf.5.gz                                                                 
---
> -rw-r--r-- 3594       usr/share/man/man5/logind.conf.5.gz                                                                 
4305,4306c4298,4299
< -rw-r--r-- 1603       usr/share/man/man5/machine-id.5.gz                                                                  
< -rw-r--r-- 1809       usr/share/man/man5/machine-info.5.gz                                                                
---
> -rw-r--r-- 1604       usr/share/man/man5/machine-id.5.gz                                                                  
> -rw-r--r-- 1811       usr/share/man/man5/machine-info.5.gz                                                                
4308c4301
< -rw-r--r-- 1365       usr/share/man/man5/modules-load.d.5.gz                                                              
---
> -rw-r--r-- 1366       usr/share/man/man5/modules-load.d.5.gz                                                              
4310c4303
< -rw-r--r-- 3878       usr/share/man/man5/os-release.5.gz                                                                  
---
> -rw-r--r-- 3879       usr/share/man/man5/os-release.5.gz                                                                  
4329c4322
< -rw-r--r-- 3979       usr/share/man/man5/systemd-system.conf.5.gz                                                         
---
> -rw-r--r-- 3980       usr/share/man/man5/systemd-system.conf.5.gz                                                         
4333,4335c4326,4328
< -rw-r--r-- 11211      usr/share/man/man5/systemd.exec.5.gz                                                                
< -rw-r--r-- 1639       usr/share/man/man5/systemd.kill.5.gz                                                                
< -rw-r--r-- 3021       usr/share/man/man5/systemd.link.5.gz                                                                
---
> -rw-r--r-- 10937      usr/share/man/man5/systemd.exec.5.gz                                                                
> -rw-r--r-- 1640       usr/share/man/man5/systemd.kill.5.gz                                                                
> -rw-r--r-- 3020       usr/share/man/man5/systemd.link.5.gz                                                                
4337,4338c4330,4331
< -rw-r--r-- 6458       usr/share/man/man5/systemd.netdev.5.gz                                                              
< -rw-r--r-- 5380       usr/share/man/man5/systemd.network.5.gz                                                             
---
> -rw-r--r-- 6411       usr/share/man/man5/systemd.netdev.5.gz                                                              
> -rw-r--r-- 5362       usr/share/man/man5/systemd.network.5.gz                                                             
4342,4343c4335,4336
< -rw-r--r-- 1054       usr/share/man/man5/systemd.scope.5.gz                                                               
< -rw-r--r-- 12498      usr/share/man/man5/systemd.service.5.gz                                                             
---
> -rw-r--r-- 1055       usr/share/man/man5/systemd.scope.5.gz                                                               
> -rw-r--r-- 12300      usr/share/man/man5/systemd.service.5.gz                                                             
4347c4340
< -rw-r--r-- 2158       usr/share/man/man5/systemd.swap.5.gz                                                                
---
> -rw-r--r-- 2159       usr/share/man/man5/systemd.swap.5.gz                                                                
4355c4348
< -rw-r--r-- 1444       usr/share/man/man5/timesyncd.conf.5.gz                                                              
---
> -rw-r--r-- 1445       usr/share/man/man5/timesyncd.conf.5.gz                                                              
4357c4350
< -rw-r--r-- 4967       usr/share/man/man5/tmpfiles.d.5.gz                                                                  
---
> -rw-r--r-- 4970       usr/share/man/man5/tmpfiles.d.5.gz                                                                  
4370c4363
< -rw-r--r-- 2047       usr/share/man/man7/kernel-command-line.7.gz                                                         
---
> -rw-r--r-- 2048       usr/share/man/man7/kernel-command-line.7.gz                                                         
4372c4365
< -rw-r--r-- 17450      usr/share/man/man7/systemd.directives.7.gz                                                          
---
> -rw-r--r-- 17381      usr/share/man/man7/systemd.directives.7.gz                                                          
4374,4376c4367,4369
< -rw-r--r-- 7319       usr/share/man/man7/systemd.index.7.gz                                                               
< -rw-r--r-- 3553       usr/share/man/man7/systemd.journal-fields.7.gz                                                      
< -rw-r--r-- 5835       usr/share/man/man7/systemd.special.7.gz                                                             
---
> -rw-r--r-- 7305       usr/share/man/man7/systemd.index.7.gz                                                               
> -rw-r--r-- 3554       usr/share/man/man7/systemd.journal-fields.7.gz                                                      
> -rw-r--r-- 5616       usr/share/man/man7/systemd.special.7.gz                                                             
4377a4371
> -rw-r--r-- 9934       usr/share/man/man7/tc-hfsc.7.gz                                                                     
4387,4389c4381,4383
< -rw-r--r-- 5351       usr/share/man/man8/apt-cache.8.gz                                                                   
< -rw-r--r-- 2350       usr/share/man/man8/apt-cdrom.8.gz                                                                   
< -rw-r--r-- 2071       usr/share/man/man8/apt-config.8.gz                                                                  
---
> -rw-r--r-- 5352       usr/share/man/man8/apt-cache.8.gz                                                                   
> -rw-r--r-- 2351       usr/share/man/man8/apt-cdrom.8.gz                                                                   
> -rw-r--r-- 2072       usr/share/man/man8/apt-config.8.gz                                                                  
4393,4394c4387,4389
< -rw-r--r-- 3094       usr/share/man/man8/apt-secure.8.gz                                                                  
< -rw-r--r-- 2607       usr/share/man/man8/apt.8.gz                                                                         
---
> -rw-r--r-- 3095       usr/share/man/man8/apt-secure.8.gz                                                                  
> -rw-r--r-- 2608       usr/share/man/man8/apt.8.gz                                                                         
> -rw-r--r-- 1981       usr/share/man/man8/arpd.8.gz                                                                        
4398a4394
> -rw-r--r-- 4354       usr/share/man/man8/bridge.8.gz                                                                      
4406a4403
> lrwxrwxrwx 0          usr/share/man/man8/ctstat.8.gz                                                                      
4446c4443
< -rw-r--r-- 846        usr/share/man/man8/halt.8.gz                                                                        
---
> -rw-r--r-- 847        usr/share/man/man8/halt.8.gz                                                                        
4451a4449,4468
> -rw-r--r-- 2291       usr/share/man/man8/ip-address.8.gz                                                                  
> -rw-r--r-- 777        usr/share/man/man8/ip-addrlabel.8.gz                                                                
> -rw-r--r-- 736        usr/share/man/man8/ip-fou.8.gz                                                                      
> lrwxrwxrwx 0          usr/share/man/man8/ip-gue.8.gz                                                                      
> -rw-r--r-- 4065       usr/share/man/man8/ip-l2tp.8.gz                                                                     
> -rw-r--r-- 6008       usr/share/man/man8/ip-link.8.gz                                                                     
> -rw-r--r-- 557        usr/share/man/man8/ip-maddress.8.gz                                                                 
> -rw-r--r-- 1100       usr/share/man/man8/ip-monitor.8.gz                                                                  
> -rw-r--r-- 661        usr/share/man/man8/ip-mroute.8.gz                                                                   
> -rw-r--r-- 1732       usr/share/man/man8/ip-neighbour.8.gz                                                                
> -rw-r--r-- 463        usr/share/man/man8/ip-netconf.8.gz                                                                  
> -rw-r--r-- 2122       usr/share/man/man8/ip-netns.8.gz                                                                    
> -rw-r--r-- 799        usr/share/man/man8/ip-ntable.8.gz                                                                   
> -rw-r--r-- 6563       usr/share/man/man8/ip-route.8.gz                                                                    
> -rw-r--r-- 2761       usr/share/man/man8/ip-rule.8.gz                                                                     
> -rw-r--r-- 1496       usr/share/man/man8/ip-tcp_metrics.8.gz                                                              
> -rw-r--r-- 820        usr/share/man/man8/ip-token.8.gz                                                                    
> -rw-r--r-- 1980       usr/share/man/man8/ip-tunnel.8.gz                                                                   
> -rw-r--r-- 3453       usr/share/man/man8/ip-xfrm.8.gz                                                                     
> -rw-r--r-- 2457       usr/share/man/man8/ip.8.gz                                                                          
4456c4473
< lrwxrwxrwx 0          usr/share/man/man8/libnss_resolve.so.2.8.gz                                                         
---
> -rw-r--r-- 1000       usr/share/man/man8/lnstat.8.gz                                                                      
4477c4494
< -rw-r--r-- 994        usr/share/man/man8/nss-resolve.8.gz                                                                 
---
> lrwxrwxrwx 0          usr/share/man/man8/nstat.8.gz                                                                       
4539a4557,4559
> lrwxrwxrwx 0          usr/share/man/man8/routef.8.gz                                                                      
> -rw-r--r-- 583        usr/share/man/man8/routel.8.gz                                                                      
> -rw-r--r-- 621        usr/share/man/man8/rtacct.8.gz                                                                      
4540a4561,4562
> -rw-r--r-- 979        usr/share/man/man8/rtmon.8.gz                                                                       
> lrwxrwxrwx 0          usr/share/man/man8/rtstat.8.gz                                                                      
4549a4572
> -rw-r--r-- 2356       usr/share/man/man8/ss.8.gz                                                                          
4557c4580
< -rw-r--r-- 1321       usr/share/man/man8/systemd-activate.8.gz                                                            
---
> -rw-r--r-- 1322       usr/share/man/man8/systemd-activate.8.gz                                                            
4572c4595
< -rw-r--r-- 884        usr/share/man/man8/systemd-debug-generator.8.gz                                                     
---
> -rw-r--r-- 885        usr/share/man/man8/systemd-debug-generator.8.gz                                                     
4575c4598
< -rw-r--r-- 1281       usr/share/man/man8/systemd-fsck@.service.8.gz                                                       
---
> -rw-r--r-- 1282       usr/share/man/man8/systemd-fsck@.service.8.gz                                                       
4592c4615
< -rw-r--r-- 563        usr/share/man/man8/systemd-initctl.service.8.gz                                                     
---
> -rw-r--r-- 564        usr/share/man/man8/systemd-initctl.service.8.gz                                                     
4596c4619
< -rw-r--r-- 2237       usr/share/man/man8/systemd-journald.service.8.gz                                                    
---
> -rw-r--r-- 2236       usr/share/man/man8/systemd-journald.service.8.gz                                                    
4603c4626,4628
< -rw-r--r-- 969        usr/share/man/man8/systemd-machine-id-commit.service.8.gz                                           
---
> -rw-r--r-- 970        usr/share/man/man8/systemd-machine-id-commit.service.8.gz                                           
> lrwxrwxrwx 0          usr/share/man/man8/systemd-machined.8.gz                                                            
> -rw-r--r-- 774        usr/share/man/man8/systemd-machined.service.8.gz                                                    
4605c4630
< -rw-r--r-- 704        usr/share/man/man8/systemd-modules-load.service.8.gz                                                
---
> -rw-r--r-- 703        usr/share/man/man8/systemd-modules-load.service.8.gz                                                
4619c4644
< -rw-r--r-- 1519       usr/share/man/man8/systemd-resolved.service.8.gz                                                    
---
> -rw-r--r-- 753        usr/share/man/man8/systemd-resolved.service.8.gz                                                    
4635c4660
< -rw-r--r-- 898        usr/share/man/man8/systemd-timesyncd.service.8.gz                                                   
---
> -rw-r--r-- 846        usr/share/man/man8/systemd-timesyncd.service.8.gz                                                   
4649c4674,4697
< -rw-r--r-- 600        usr/share/man/man8/systemd-user-sessions.service.8.gz                                               
---
> -rw-r--r-- 601        usr/share/man/man8/systemd-user-sessions.service.8.gz                                               
> -rw-r--r-- 1079       usr/share/man/man8/tc-bfifo.8.gz                                                                    
> -rw-r--r-- 9705       usr/share/man/man8/tc-bpf.8.gz                                                                      
> -rw-r--r-- 5672       usr/share/man/man8/tc-cbq-details.8.gz                                                              
> -rw-r--r-- 4839       usr/share/man/man8/tc-cbq.8.gz                                                                      
> -rw-r--r-- 909        usr/share/man/man8/tc-choke.8.gz                                                                    
> -rw-r--r-- 1806       usr/share/man/man8/tc-codel.8.gz                                                                    
> -rw-r--r-- 1380       usr/share/man/man8/tc-drr.8.gz                                                                      
> -rw-r--r-- 1441       usr/share/man/man8/tc-ematch.8.gz                                                                   
> -rw-r--r-- 1527       usr/share/man/man8/tc-fq_codel.8.gz                                                                 
> -rw-r--r-- 1017       usr/share/man/man8/tc-hfsc.8.gz                                                                     
> -rw-r--r-- 2172       usr/share/man/man8/tc-htb.8.gz                                                                      
> -rw-r--r-- 1614       usr/share/man/man8/tc-mqprio.8.gz                                                                   
> -rw-r--r-- 3051       usr/share/man/man8/tc-netem.8.gz                                                                    
> lrwxrwxrwx 0          usr/share/man/man8/tc-pfifo.8.gz                                                                    
> -rw-r--r-- 874        usr/share/man/man8/tc-pfifo_fast.8.gz                                                               
> -rw-r--r-- 1750       usr/share/man/man8/tc-pie.8.gz                                                                      
> -rw-r--r-- 2557       usr/share/man/man8/tc-prio.8.gz                                                                     
> -rw-r--r-- 2271       usr/share/man/man8/tc-red.8.gz                                                                      
> -rw-r--r-- 2890       usr/share/man/man8/tc-sfb.8.gz                                                                      
> -rw-r--r-- 3242       usr/share/man/man8/tc-sfq.8.gz                                                                      
> -rw-r--r-- 2989       usr/share/man/man8/tc-stab.8.gz                                                                     
> -rw-r--r-- 2474       usr/share/man/man8/tc-tbf.8.gz                                                                      
> -rw-r--r-- 5634       usr/share/man/man8/tc.8.gz                                                                          
4695c4743
< -rw-r--r-- 6537       usr/share/man/pl/man8/apt-cache.8.gz                                                                
---
> -rw-r--r-- 6538       usr/share/man/pl/man8/apt-cache.8.gz                                                                
4697c4745
< -rw-r--r-- 2606       usr/share/man/pl/man8/apt-config.8.gz                                                               
---
> -rw-r--r-- 2607       usr/share/man/pl/man8/apt-config.8.gz                                                               
4701c4749
< -rw-r--r-- 3754       usr/share/man/pl/man8/apt-secure.8.gz                                                               
---
> -rw-r--r-- 3755       usr/share/man/pl/man8/apt-secure.8.gz                                                               
4731,4738c4779,4786
< -rw-r--r-- 5946       usr/share/man/pt/man8/apt-cache.8.gz                                                                
< -rw-r--r-- 2786       usr/share/man/pt/man8/apt-cdrom.8.gz                                                                
< -rw-r--r-- 2447       usr/share/man/pt/man8/apt-config.8.gz                                                               
< -rw-r--r-- 9058       usr/share/man/pt/man8/apt-get.8.gz                                                                  
< -rw-r--r-- 2220       usr/share/man/pt/man8/apt-key.8.gz                                                                  
< -rw-r--r-- 2305       usr/share/man/pt/man8/apt-mark.8.gz                                                                 
< -rw-r--r-- 3520       usr/share/man/pt/man8/apt-secure.8.gz                                                               
< -rw-r--r-- 3085       usr/share/man/pt/man8/apt.8.gz                                                                      
---
> -rw-r--r-- 5947       usr/share/man/pt/man8/apt-cache.8.gz                                                                
> -rw-r--r-- 2787       usr/share/man/pt/man8/apt-cdrom.8.gz                                                                
> -rw-r--r-- 2448       usr/share/man/pt/man8/apt-config.8.gz                                                               
> -rw-r--r-- 9059       usr/share/man/pt/man8/apt-get.8.gz                                                                  
> -rw-r--r-- 2221       usr/share/man/pt/man8/apt-key.8.gz                                                                  
> -rw-r--r-- 2306       usr/share/man/pt/man8/apt-mark.8.gz                                                                 
> -rw-r--r-- 3521       usr/share/man/pt/man8/apt-secure.8.gz                                                               
> -rw-r--r-- 3086       usr/share/man/pt/man8/apt.8.gz                                                                      
5580c5628,5629
< -rw-r--r-- 122414     usr/share/polkit-1/actions/org.freedesktop.login1.policy                                            
---
> -rw-r--r-- 121697     usr/share/polkit-1/actions/org.freedesktop.login1.policy                                            
> -rw-r--r-- 9237       usr/share/polkit-1/actions/org.freedesktop.machine1.policy                                          
5711d5759
< -rw-r--r-- 2249       usr/share/zoneinfo/America/Fort_Nelson                                                              
6141c6189
< -rw-r--r-- 1073       usr/share/zoneinfo/Pacific/Fiji                                                                     
---
> -rw-r--r-- 1074       usr/share/zoneinfo/Pacific/Fiji                                                                     
6157c6205
< -rw-r--r-- 289        usr/share/zoneinfo/Pacific/Norfolk                                                                  
---
> -rw-r--r-- 208        usr/share/zoneinfo/Pacific/Norfolk                                                                  
6333d6380
< lrwxrwxrwx 0          usr/share/zoneinfo/posix/America/Fort_Nelson                                                        
6953d6999
< -rw-r--r-- 2769       usr/share/zoneinfo/right/America/Fort_Nelson                                                        
7383c7429
< -rw-r--r-- 1593       usr/share/zoneinfo/right/Pacific/Fiji                                                               
---
> -rw-r--r-- 1594       usr/share/zoneinfo/right/Pacific/Fiji                                                               
7399c7445
< -rw-r--r-- 809        usr/share/zoneinfo/right/Pacific/Norfolk                                                            
---
> -rw-r--r-- 728        usr/share/zoneinfo/right/Pacific/Norfolk                                                            
7457,7458c7503,7504
< -rw-r--r-- 20181      usr/share/zoneinfo/zone.tab                                                                         
< -rw-r--r-- 18734      usr/share/zoneinfo/zone1970.tab                                                                     
---
> -rw-r--r-- 20091      usr/share/zoneinfo/zone.tab                                                                         
> -rw-r--r-- 18644      usr/share/zoneinfo/zone1970.tab                                                                     
7462c7508
< -rw-r--r-- 3073       usr/share/zsh/vendor-completions/_busctl                                                            
---
> -rw-r--r-- 2185       usr/share/zsh/vendor-completions/_busctl                                                            
7466a7513
> -rw-r--r-- 3788       usr/share/zsh/vendor-completions/_machinectl                                                        
7467a7515
> -rw-r--r-- 318        usr/share/zsh/vendor-completions/_sd_machines                                                       
7474a7523
> -rw-r--r-- 4406       usr/share/zsh/vendor-completions/_systemd-nspawn                                                    
7487,7488d7535
< -rw-r--r-- 5637173    var/cache/apt/pkgcache.bin                                                                          
< -rw-r--r-- 5637124    var/cache/apt/srcpkgcache.bin                                                                       
7490a7538
> -rw-r--r-- 4153       var/cache/debconf/config.dat-old                                                                    
7492c7540,7541
< -rw-r--r-- 541116     var/cache/debconf/templates.dat                                                                     
---
> -rw-r--r-- 576605     var/cache/debconf/templates.dat                                                                     
> -rw-r--r-- 559858     var/cache/debconf/templates.dat-old                                                                 
7497d7545
< -rw-r--r-- 0          var/lib/apt/extended_states                                                                         
7501,7511d7548
< -rw-r--r-- 64433      var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_wily-updates_InRelease                            
< -rw-r--r-- 724184     var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_wily-updates_main_binary-amd64_Packages           
< -rw-r--r-- 451680     var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_wily-updates_main_i18n_Translation-en             
< -rw-r--r-- 208704     var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_wily-updates_restricted_binary-amd64_Packages     
< -rw-r--r-- 25292      var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_wily-updates_restricted_i18n_Translation-en       
< -rw-r--r-- 217861     var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_wily_InRelease                                    
< -rw-r--r-- 8565184    var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_wily_main_binary-amd64_Packages                   
< -rw-r--r-- 4440137    var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_wily_main_i18n_Translation-en                     
< -rw-r--r-- 218752     var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_wily_restricted_binary-amd64_Packages             
< -rw-r--r-- 30581      var/lib/apt/lists/archive.ubuntu.com_ubuntu_dists_wily_restricted_i18n_Translation-en               
< -rw-r----- 0          var/lib/apt/lists/lock                                                                              
7513,7517d7549
< -rw-r--r-- 64435      var/lib/apt/lists/security.ubuntu.com_ubuntu_dists_wily-security_InRelease                          
< -rw-r--r-- 531369     var/lib/apt/lists/security.ubuntu.com_ubuntu_dists_wily-security_main_binary-amd64_Packages         
< -rw-r--r-- 350683     var/lib/apt/lists/security.ubuntu.com_ubuntu_dists_wily-security_main_i18n_Translation-en           
< -rw-r--r-- 174352     var/lib/apt/lists/security.ubuntu.com_ubuntu_dists_wily-security_restricted_binary-amd64_Packages   
< -rw-r--r-- 23010      var/lib/apt/lists/security.ubuntu.com_ubuntu_dists_wily-security_restricted_i18n_Translation-en     
7528c7560
< -rw-r--r-- 95547      var/lib/dpkg/available                                                                              
---
> -rw-r--r-- 95161      var/lib/dpkg/available                                                                              
7541,7542c7573,7574
< -rw-r--r-- 9886       var/lib/dpkg/info/apt.list                                                                          
< -rw-r--r-- 11144      var/lib/dpkg/info/apt.md5sums                                                                       
---
> -rw-r--r-- 9854       var/lib/dpkg/info/apt.list                                                                          
> -rw-r--r-- 11079      var/lib/dpkg/info/apt.md5sums                                                                       
7634a7667,7668
> -rw-r--r-- 481        var/lib/dpkg/info/inetutils-ping.list                                                               
> -rw-r--r-- 659        var/lib/dpkg/info/inetutils-ping.md5sums                                                            
7646a7681,7683
> -rw-r--r-- 190        var/lib/dpkg/info/iproute2.conffiles                                                                
> -rw-r--r-- 2737       var/lib/dpkg/info/iproute2.list                                                                     
> -rw-r--r-- 4399       var/lib/dpkg/info/iproute2.md5sums                                                                  
7663c7700
< -rw-r--r-- 124515     var/lib/dpkg/info/libapt-pkg4.16:amd64.symbols                                                      
---
> -rw-r--r-- 128845     var/lib/dpkg/info/libapt-pkg4.16:amd64.symbols                                                      
7767,7768c7804,7805
< -rw-r--r-- 238        var/lib/dpkg/info/libkmod2:amd64.list                                                               
< -rw-r--r-- 217        var/lib/dpkg/info/libkmod2:amd64.md5sums                                                            
---
> -rw-r--r-- 237        var/lib/dpkg/info/libkmod2:amd64.list                                                               
> -rw-r--r-- 216        var/lib/dpkg/info/libkmod2:amd64.md5sums                                                            
7926,7927c7963,7964
< -rw-r--r-- 19157      var/lib/dpkg/info/locales.list                                                                      
< -rw-r--r-- 37136      var/lib/dpkg/info/locales.md5sums                                                                   
---
> -rw-r--r-- 19127      var/lib/dpkg/info/locales.list                                                                      
> -rw-r--r-- 37073      var/lib/dpkg/info/locales.md5sums                                                                   
7960a7998,8002
> -rw-r--r-- 38         var/lib/dpkg/info/netbase.conffiles                                                                 
> -rw-r--r-- 182        var/lib/dpkg/info/netbase.list                                                                      
> -rw-r--r-- 135        var/lib/dpkg/info/netbase.md5sums                                                                   
> -rwxr-xr-x 1563       var/lib/dpkg/info/netbase.postinst                                                                  
> -rwxr-xr-x 756        var/lib/dpkg/info/netbase.postrm                                                                    
7988,7994c8030,8036
< -rw-r--r-- 607        var/lib/dpkg/info/systemd.conffiles                                                                 
< -rw-r--r-- 29171      var/lib/dpkg/info/systemd.list                                                                      
< -rw-r--r-- 32036      var/lib/dpkg/info/systemd.md5sums                                                                   
< -rwxr-xr-x 7097       var/lib/dpkg/info/systemd.postinst                                                                  
< -rwxr-xr-x 1889       var/lib/dpkg/info/systemd.postrm                                                                    
< -rwxr-xr-x 2216       var/lib/dpkg/info/systemd.preinst                                                                   
< -rwxr-xr-x 1214       var/lib/dpkg/info/systemd.prerm                                                                     
---
> -rw-r--r-- 658        var/lib/dpkg/info/systemd.conffiles                                                                 
> -rw-r--r-- 30121      var/lib/dpkg/info/systemd.list                                                                      
> -rw-r--r-- 33392      var/lib/dpkg/info/systemd.md5sums                                                                   
> -rwxr-xr-x 6672       var/lib/dpkg/info/systemd.postinst                                                                  
> -rwxr-xr-x 1706       var/lib/dpkg/info/systemd.postrm                                                                    
> -rwxr-xr-x 2033       var/lib/dpkg/info/systemd.preinst                                                                   
> -rwxr-xr-x 1031       var/lib/dpkg/info/systemd.prerm                                                                     
8015,8016c8057,8058
< -rw-r--r-- 72805      var/lib/dpkg/info/tzdata.list                                                                       
< -rw-r--r-- 54275      var/lib/dpkg/info/tzdata.md5sums                                                                    
---
> -rw-r--r-- 72673      var/lib/dpkg/info/tzdata.list                                                                       
> -rw-r--r-- 54123      var/lib/dpkg/info/tzdata.md5sums                                                                    
8019c8061
< -rw-r--r-- 102185     var/lib/dpkg/info/tzdata.templates                                                                  
---
> -rw-r--r-- 137674     var/lib/dpkg/info/tzdata.templates                                                                  
8023,8029c8065,8071
< -rw-r--r-- 165        var/lib/dpkg/info/udev.conffiles                                                                    
< -rw-r--r-- 4465       var/lib/dpkg/info/udev.list                                                                         
< -rw-r--r-- 5565       var/lib/dpkg/info/udev.md5sums                                                                      
< -rwxr-xr-x 3418       var/lib/dpkg/info/udev.postinst                                                                     
< -rwxr-xr-x 1962       var/lib/dpkg/info/udev.postrm                                                                       
< -rwxr-xr-x 1375       var/lib/dpkg/info/udev.preinst                                                                      
< -rwxr-xr-x 1553       var/lib/dpkg/info/udev.prerm                                                                        
---
> -rw-r--r-- 254        var/lib/dpkg/info/udev.conffiles                                                                    
> -rw-r--r-- 4551       var/lib/dpkg/info/udev.list                                                                         
> -rw-r--r-- 5468       var/lib/dpkg/info/udev.md5sums                                                                      
> -rwxr-xr-x 3101       var/lib/dpkg/info/udev.postinst                                                                     
> -rwxr-xr-x 1847       var/lib/dpkg/info/udev.postrm                                                                       
> -rwxr-xr-x 1236       var/lib/dpkg/info/udev.preinst                                                                      
> -rwxr-xr-x 1092       var/lib/dpkg/info/udev.prerm                                                                        
8047c8089,8090
< -rw-r--r-- 100845     var/lib/dpkg/status                                                                                 
---
> -rw-r--r-- 100787     var/lib/dpkg/status                                                                                 
> -rw-r--r-- 100418     var/lib/dpkg/status-old                                                                             
8076,8077c8119
< -rw-r--r-- 212        var/log/apt/history.log                                                                             
< -rw-r--r-- 44502      var/log/bootstrap.log                                                                               
---
> -rw-r--r-- 46050      var/log/bootstrap.log                                                                               
8080c8122
< -rw-r--r-- 71220      var/log/dpkg.log                                                                                    
---
> -rw-r--r-- 71634      var/log/dpkg.log                                                                                    

```
