# docker-diff
:whale: Compare Docker images

## Usage

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
