

example output of provisioning:

```

C:\Users\Admin\awx>vagrant up
Bringing machine 'default' up with 'virtualbox' provider...
==> default: Importing base box 'oraclelinux/8'...
==> default: Matching MAC address for NAT networking...
==> default: Checking if box 'oraclelinux/8' version '8.9.511' is up to date...
==> default: Setting the name of the VM: awx_default_1703612905355_22121
==> default: Clearing any previously set network interfaces...
==> default: Preparing network interfaces based on configuration...
    default: Adapter 1: nat
    default: Adapter 2: hostonly
==> default: You are trying to forward to privileged ports (ports <= 1024). Most
==> default: operating systems restrict this to only privileged process (typically
==> default: processes running as an administrative user). This is a warning in case
==> default: the port forwarding doesn't work. If any problems occur, please try a
==> default: port higher than 1024.
==> default: Forwarding ports...
    default: 80 (guest) => 80 (host) (adapter 1)
    default: 443 (guest) => 443 (host) (adapter 1)
    default: 22 (guest) => 2222 (host) (adapter 1)
==> default: Running 'pre-boot' VM customizations...
==> default: Booting VM...
==> default: Waiting for machine to boot. This may take a few minutes...
    default: SSH address: 127.0.0.1:2222
    default: SSH username: vagrant
    default: SSH auth method: private key
    default:
    default: Vagrant insecure key detected. Vagrant will automatically replace
    default: this with a newly generated keypair for better security.
    default:
    default: Inserting generated public key within guest...
    default: Removing insecure key from the guest if it's present...
    default: Key inserted! Disconnecting and reconnecting using new SSH key...
==> default: Machine booted and ready!
==> default: Checking for guest additions in VM...
==> default: Configuring and enabling network interfaces...
==> default: Mounting shared folders...
    default: /vagrant => C:/Users/Admin/awx
==> default: Running provisioner: shell...
    default: Running: inline script
    default:               total        used        free      shared  buff/cache   available
    default: Mem:          7.7Gi       137Mi       7.5Gi        16Mi       124Mi       7.4Gi
    default: Swap:            0B          0B          0B
==> default: Running provisioner: shell...
    default: Running: inline script
    default: Oracle Linux 8 BaseOS Latest (x86_64)           3.0 MB/s |  67 MB     00:22
    default: Oracle Linux 8 Application Stream (x86_64)      2.8 MB/s |  53 MB     00:18
    default: Latest Unbreakable Enterprise Kernel Release 7  2.8 MB/s |  26 MB     00:09
    default: Last metadata expiration check: 0:00:20 ago on Tue 26 Dec 2023 05:52:20 PM UTC.
    default: Dependencies resolved.
    default: ========================================================================================
    default:  Package                        Arch    Version                 Repository          Size
    default: ========================================================================================
    default: Installing:
    default:  kernel-uek-core                x86_64  5.15.0-201.135.6.el8uek ol8_UEKR7           59 M
    default:  kernel-uek-devel               x86_64  5.15.0-201.135.6.el8uek ol8_UEKR7           20 M
    default: Upgrading:
    default:  avahi-libs                     x86_64  0.7-21.el8_9.1          ol8_baseos_latest   61 k
    default:  bcache-tools                   x86_64  1.0.8-3.101.0.2.el8     ol8_baseos_latest   37 k
    default:  device-mapper                  x86_64  8:1.02.181-13.0.2.el8_9 ol8_baseos_latest  378 k
    default:  device-mapper-event            x86_64  8:1.02.181-13.0.2.el8_9 ol8_baseos_latest  271 k
    default:  device-mapper-event-libs       x86_64  8:1.02.181-13.0.2.el8_9 ol8_baseos_latest  270 k
    default:  device-mapper-libs             x86_64  8:1.02.181-13.0.2.el8_9 ol8_baseos_latest  410 k
    default:  kernel-headers                 x86_64  4.18.0-513.9.1.el8_9    ol8_baseos_latest   11 M
    default:  kernel-tools                   x86_64  4.18.0-513.9.1.el8_9    ol8_baseos_latest   10 M
    default:  kernel-tools-libs              x86_64  4.18.0-513.9.1.el8_9    ol8_baseos_latest   10 M
    default:  krb5-libs                      x86_64  1.18.2-26.0.1.el8_9     ol8_baseos_latest  841 k
    default:  lvm2                           x86_64  8:2.03.14-13.0.2.el8_9  ol8_baseos_latest  1.7 M
    default:  lvm2-libs                      x86_64  8:2.03.14-13.0.2.el8_9  ol8_baseos_latest  1.2 M
    default:  openssl                        x86_64  1:1.1.1k-12.el8_9       ol8_baseos_latest  710 k
    default:  openssl-libs                   x86_64  1:1.1.1k-12.el8_9       ol8_baseos_latest  1.5 M
    default:  systemd                        x86_64  239-78.0.3.el8          ol8_baseos_latest  3.7 M
    default:  systemd-libs                   x86_64  239-78.0.3.el8          ol8_baseos_latest  1.1 M
    default:  systemd-pam                    x86_64  239-78.0.3.el8          ol8_baseos_latest  513 k
    default:  systemd-udev                   x86_64  239-78.0.3.el8          ol8_baseos_latest  1.6 M
    default: Installing dependencies:
    default:  device-mapper-multipath        x86_64  0.8.4-39.el8            ol8_baseos_latest  209 k
    default:  device-mapper-multipath-libs   x86_64  0.8.4-39.el8            ol8_baseos_latest  334 k
    default:  userspace-rcu                  x86_64  0.10.1-4.el8            ol8_baseos_latest  101 k
    default:
    default: Transaction Summary
    default: ========================================================================================
    default: Install   5 Packages
    default: Upgrade  18 Packages
    default:
    default: Total download size: 126 M
    default: Downloading Packages:
    default: (1/23): userspace-rcu-0.10.1-4.el8.x86_64.rpm   377 kB/s | 101 kB     00:00
    default: (2/23): device-mapper-multipath-0.8.4-39.el8.x8 566 kB/s | 209 kB     00:00
    default: (3/23): device-mapper-multipath-libs-0.8.4-39.e 578 kB/s | 334 kB     00:00
    default: (4/23): avahi-libs-0.7-21.el8_9.1.x86_64.rpm    654 kB/s |  61 kB     00:00
    default: (5/23): bcache-tools-1.0.8-3.101.0.2.el8.x86_64 531 kB/s |  37 kB     00:00
    default: (6/23): device-mapper-1.02.181-13.0.2.el8_9.x86 947 kB/s | 378 kB     00:00
    default: (7/23): device-mapper-event-1.02.181-13.0.2.el8 777 kB/s | 271 kB     00:00
    default: (8/23): device-mapper-event-libs-1.02.181-13.0. 933 kB/s | 270 kB     00:00
    default: (9/23): device-mapper-libs-1.02.181-13.0.2.el8_ 976 kB/s | 410 kB     00:00
    default: (10/23): kernel-headers-4.18.0-513.9.1.el8_9.x8 1.0 MB/s |  11 MB     00:11
    default: (11/23): kernel-uek-devel-5.15.0-201.135.6.el8u 1.0 MB/s |  20 MB     00:20
    default: (12/23): kernel-tools-4.18.0-513.9.1.el8_9.x86_ 1.0 MB/s |  10 MB     00:09
    default: (13/23): krb5-libs-1.18.2-26.0.1.el8_9.x86_64.r 1.4 MB/s | 841 kB     00:00
    default: (14/23): lvm2-2.03.14-13.0.2.el8_9.x86_64.rpm   1.2 MB/s | 1.7 MB     00:01
    default: (15/23): lvm2-libs-2.03.14-13.0.2.el8_9.x86_64. 1.1 MB/s | 1.2 MB     00:01
    default: (16/23): openssl-1.1.1k-12.el8_9.x86_64.rpm     1.1 MB/s | 710 kB     00:00
    default: (17/23): openssl-libs-1.1.1k-12.el8_9.x86_64.rp 1.1 MB/s | 1.5 MB     00:01
    default: (18/23): kernel-tools-libs-4.18.0-513.9.1.el8_9 966 kB/s |  10 MB     00:10
    default: (19/23): systemd-239-78.0.3.el8.x86_64.rpm      1.1 MB/s | 3.7 MB     00:03
    default: (20/23): systemd-pam-239-78.0.3.el8.x86_64.rpm  1.1 MB/s | 513 kB     00:00
    default: (21/23): systemd-libs-239-78.0.3.el8.x86_64.rpm 926 kB/s | 1.1 MB     00:01
    default: (22/23): systemd-udev-239-78.0.3.el8.x86_64.rpm 1.6 MB/s | 1.6 MB     00:00
    default: (23/23): kernel-uek-core-5.15.0-201.135.6.el8ue 1.4 MB/s |  59 MB     00:43
    default: --------------------------------------------------------------------------------
    default: Total                                           2.9 MB/s | 126 MB     00:43
    default: Running transaction check
    default: Transaction check succeeded.
    default: Running transaction test
    default: Transaction test succeeded.
    default: Running transaction
    default:   Preparing        :                                                        1/1
    default:   Running scriptlet: systemd-libs-239-78.0.3.el8.x86_64                     1/1
    default:   Upgrading        : systemd-libs-239-78.0.3.el8.x86_64                    1/41
    default:   Running scriptlet: systemd-libs-239-78.0.3.el8.x86_64                    1/41
    default:   Upgrading        : openssl-libs-1:1.1.1k-12.el8_9.x86_64                 2/41
    default:   Running scriptlet: openssl-libs-1:1.1.1k-12.el8_9.x86_64                 2/41
    default:   Installing       : userspace-rcu-0.10.1-4.el8.x86_64                     3/41
    default:   Running scriptlet: userspace-rcu-0.10.1-4.el8.x86_64                     3/41
    default:   Upgrading        : systemd-pam-239-78.0.3.el8.x86_64                     4/41
    default:   Installing       : device-mapper-multipath-libs-0.8.4-39.el8.x86_64      5/41
    default:   Running scriptlet: device-mapper-multipath-libs-0.8.4-39.el8.x86_64      5/41
    default:   Upgrading        : device-mapper-event-libs-8:1.02.181-13.0.2.el8_9.x    6/41
    default:   Upgrading        : device-mapper-libs-8:1.02.181-13.0.2.el8_9.x86_64     7/41
    default:   Upgrading        : device-mapper-8:1.02.181-13.0.2.el8_9.x86_64          8/41
    default:   Upgrading        : lvm2-libs-8:2.03.14-13.0.2.el8_9.x86_64               9/41
    default:   Running scriptlet: systemd-239-78.0.3.el8.x86_64                        10/41
    default:   Upgrading        : systemd-239-78.0.3.el8.x86_64                        10/41
    default:   Running scriptlet: systemd-239-78.0.3.el8.x86_64                        10/41
    default:   Upgrading        : device-mapper-event-8:1.02.181-13.0.2.el8_9.x86_64   11/41
    default:   Running scriptlet: device-mapper-event-8:1.02.181-13.0.2.el8_9.x86_64   11/41
    default:   Installing       : device-mapper-multipath-0.8.4-39.el8.x86_64          12/41
    default:   Running scriptlet: device-mapper-multipath-0.8.4-39.el8.x86_64          12/41
    default:   Upgrading        : lvm2-8:2.03.14-13.0.2.el8_9.x86_64                   13/41
    default:   Running scriptlet: lvm2-8:2.03.14-13.0.2.el8_9.x86_64                   13/41
    default:   Upgrading        : systemd-udev-239-78.0.3.el8.x86_64                   14/41
    default:   Running scriptlet: systemd-udev-239-78.0.3.el8.x86_64                   14/41
    default:   Upgrading        : kernel-tools-libs-4.18.0-513.9.1.el8_9.x86_64        15/41
    default:   Running scriptlet: kernel-tools-libs-4.18.0-513.9.1.el8_9.x86_64        15/41
    default:   Upgrading        : kernel-tools-4.18.0-513.9.1.el8_9.x86_64             16/41
    default:   Running scriptlet: kernel-tools-4.18.0-513.9.1.el8_9.x86_64             16/41
    default:   Running scriptlet: kernel-uek-core-5.15.0-201.135.6.el8uek.x86_64       17/41
    default:   Installing       : kernel-uek-core-5.15.0-201.135.6.el8uek.x86_64       17/41
    default:   Running scriptlet: kernel-uek-core-5.15.0-201.135.6.el8uek.x86_64       17/41
    default:   Upgrading        : bcache-tools-1.0.8-3.101.0.2.el8.x86_64              18/41
    default:   Upgrading        : krb5-libs-1.18.2-26.0.1.el8_9.x86_64                 19/41
    default:   Upgrading        : openssl-1:1.1.1k-12.el8_9.x86_64                     20/41
    default:   Upgrading        : kernel-headers-4.18.0-513.9.1.el8_9.x86_64           21/41
    default:   Upgrading        : avahi-libs-0.7-21.el8_9.1.x86_64                     22/41
    default:   Installing       : kernel-uek-devel-5.15.0-201.135.6.el8uek.x86_64      23/41
    default:   Running scriptlet: kernel-uek-devel-5.15.0-201.135.6.el8uek.x86_64      23/41
    default:   Running scriptlet: lvm2-8:2.03.14-13.0.1.el8_9.x86_64                   24/41
    default:   Cleanup          : lvm2-8:2.03.14-13.0.1.el8_9.x86_64                   24/41
    default:   Running scriptlet: lvm2-8:2.03.14-13.0.1.el8_9.x86_64                   24/41
    default:   Cleanup          : lvm2-libs-8:2.03.14-13.0.1.el8_9.x86_64              25/41
    default:   Running scriptlet: device-mapper-event-8:1.02.181-13.0.1.el8_9.x86_64   26/41
    default:   Cleanup          : device-mapper-event-8:1.02.181-13.0.1.el8_9.x86_64   26/41
    default:   Cleanup          : openssl-1:1.1.1k-9.el8_7.x86_64                      27/41
    default:   Cleanup          : krb5-libs-1.18.2-26.el8_9.x86_64                     28/41
    default:   Cleanup          : device-mapper-event-libs-8:1.02.181-13.0.1.el8_9.x   29/41
    default:   Cleanup          : device-mapper-libs-8:1.02.181-13.0.1.el8_9.x86_64    30/41
    default:   Cleanup          : device-mapper-8:1.02.181-13.0.1.el8_9.x86_64         31/41
    default:   Running scriptlet: kernel-tools-4.18.0-513.5.1.el8_9.x86_64             32/41
    default:   Cleanup          : kernel-tools-4.18.0-513.5.1.el8_9.x86_64             32/41
    default:   Running scriptlet: kernel-tools-4.18.0-513.5.1.el8_9.x86_64             32/41
    default:   Cleanup          : bcache-tools-1.0.8-3.101.0.1.el8.x86_64              33/41
    default:   Cleanup          : kernel-headers-4.18.0-513.5.1.el8_9.x86_64           34/41
    default:   Cleanup          : systemd-udev-239-78.0.1.el8.x86_64                   35/41
    default:   Running scriptlet: systemd-udev-239-78.0.1.el8.x86_64                   35/41
    default:   Running scriptlet: systemd-239-78.0.1.el8.x86_64                        36/41
    default:   Cleanup          : systemd-239-78.0.1.el8.x86_64                        36/41
    default:   Cleanup          : openssl-libs-1:1.1.1k-9.el8_7.x86_64                 37/41
    default:   Running scriptlet: openssl-libs-1:1.1.1k-9.el8_7.x86_64                 37/41
    default:   Cleanup          : systemd-libs-239-78.0.1.el8.x86_64                   38/41
    default:   Cleanup          : systemd-pam-239-78.0.1.el8.x86_64                    39/41
    default:   Cleanup          : kernel-tools-libs-4.18.0-513.5.1.el8_9.x86_64        40/41
    default:   Running scriptlet: kernel-tools-libs-4.18.0-513.5.1.el8_9.x86_64        40/41
    default:   Cleanup          : avahi-libs-0.7-21.el8.x86_64                         41/41
    default:   Running scriptlet: systemd-239-78.0.3.el8.x86_64                        41/41
    default:   Running scriptlet: kernel-uek-core-5.15.0-201.135.6.el8uek.x86_64       41/41
    default:   Running scriptlet: avahi-libs-0.7-21.el8.x86_64                         41/41
    default:   Running scriptlet: systemd-239-78.0.3.el8.x86_64                        41/41
    default:   Running scriptlet: systemd-udev-239-78.0.3.el8.x86_64                   41/41
    default:   Verifying        : device-mapper-multipath-0.8.4-39.el8.x86_64           1/41
    default:   Verifying        : device-mapper-multipath-libs-0.8.4-39.el8.x86_64      2/41
    default:   Verifying        : userspace-rcu-0.10.1-4.el8.x86_64                     3/41
    default:   Verifying        : kernel-uek-core-5.15.0-201.135.6.el8uek.x86_64        4/41
    default:   Verifying        : kernel-uek-devel-5.15.0-201.135.6.el8uek.x86_64       5/41
    default:   Verifying        : avahi-libs-0.7-21.el8_9.1.x86_64                      6/41
    default:   Verifying        : avahi-libs-0.7-21.el8.x86_64                          7/41
    default:   Verifying        : bcache-tools-1.0.8-3.101.0.2.el8.x86_64               8/41
    default:   Verifying        : bcache-tools-1.0.8-3.101.0.1.el8.x86_64               9/41
    default:   Verifying        : device-mapper-8:1.02.181-13.0.2.el8_9.x86_64         10/41
    default:   Verifying        : device-mapper-8:1.02.181-13.0.1.el8_9.x86_64         11/41
    default:   Verifying        : device-mapper-event-8:1.02.181-13.0.2.el8_9.x86_64   12/41
    default:   Verifying        : device-mapper-event-8:1.02.181-13.0.1.el8_9.x86_64   13/41
    default:   Verifying        : device-mapper-event-libs-8:1.02.181-13.0.2.el8_9.x   14/41
    default:   Verifying        : device-mapper-event-libs-8:1.02.181-13.0.1.el8_9.x   15/41
    default:   Verifying        : device-mapper-libs-8:1.02.181-13.0.2.el8_9.x86_64    16/41
    default:   Verifying        : device-mapper-libs-8:1.02.181-13.0.1.el8_9.x86_64    17/41
    default:   Verifying        : kernel-headers-4.18.0-513.9.1.el8_9.x86_64           18/41
    default:   Verifying        : kernel-headers-4.18.0-513.5.1.el8_9.x86_64           19/41
    default:   Verifying        : kernel-tools-4.18.0-513.9.1.el8_9.x86_64             20/41
    default:   Verifying        : kernel-tools-4.18.0-513.5.1.el8_9.x86_64             21/41
    default:   Verifying        : kernel-tools-libs-4.18.0-513.9.1.el8_9.x86_64        22/41
    default:   Verifying        : kernel-tools-libs-4.18.0-513.5.1.el8_9.x86_64        23/41
    default:   Verifying        : krb5-libs-1.18.2-26.0.1.el8_9.x86_64                 24/41
    default:   Verifying        : krb5-libs-1.18.2-26.el8_9.x86_64                     25/41
    default:   Verifying        : lvm2-8:2.03.14-13.0.2.el8_9.x86_64                   26/41
    default:   Verifying        : lvm2-8:2.03.14-13.0.1.el8_9.x86_64                   27/41
    default:   Verifying        : lvm2-libs-8:2.03.14-13.0.2.el8_9.x86_64              28/41
    default:   Verifying        : lvm2-libs-8:2.03.14-13.0.1.el8_9.x86_64              29/41
    default:   Verifying        : openssl-1:1.1.1k-12.el8_9.x86_64                     30/41
    default:   Verifying        : openssl-1:1.1.1k-9.el8_7.x86_64                      31/41
    default:   Verifying        : openssl-libs-1:1.1.1k-12.el8_9.x86_64                32/41
    default:   Verifying        : openssl-libs-1:1.1.1k-9.el8_7.x86_64                 33/41
    default:   Verifying        : systemd-239-78.0.3.el8.x86_64                        34/41
    default:   Verifying        : systemd-239-78.0.1.el8.x86_64                        35/41
    default:   Verifying        : systemd-libs-239-78.0.3.el8.x86_64                   36/41
    default:   Verifying        : systemd-libs-239-78.0.1.el8.x86_64                   37/41
    default:   Verifying        : systemd-pam-239-78.0.3.el8.x86_64                    38/41
    default:   Verifying        : systemd-pam-239-78.0.1.el8.x86_64                    39/41
    default:   Verifying        : systemd-udev-239-78.0.3.el8.x86_64                   40/41
    default:   Verifying        : systemd-udev-239-78.0.1.el8.x86_64                   41/41
    default:
    default: Upgraded:
    default:   avahi-libs-0.7-21.el8_9.1.x86_64
    default:   bcache-tools-1.0.8-3.101.0.2.el8.x86_64
    default:   device-mapper-8:1.02.181-13.0.2.el8_9.x86_64
    default:   device-mapper-event-8:1.02.181-13.0.2.el8_9.x86_64
    default:   device-mapper-event-libs-8:1.02.181-13.0.2.el8_9.x86_64
    default:   device-mapper-libs-8:1.02.181-13.0.2.el8_9.x86_64
    default:   kernel-headers-4.18.0-513.9.1.el8_9.x86_64
    default:   kernel-tools-4.18.0-513.9.1.el8_9.x86_64
    default:   kernel-tools-libs-4.18.0-513.9.1.el8_9.x86_64
    default:   krb5-libs-1.18.2-26.0.1.el8_9.x86_64
    default:   lvm2-8:2.03.14-13.0.2.el8_9.x86_64
    default:   lvm2-libs-8:2.03.14-13.0.2.el8_9.x86_64
    default:   openssl-1:1.1.1k-12.el8_9.x86_64
    default:   openssl-libs-1:1.1.1k-12.el8_9.x86_64
    default:   systemd-239-78.0.3.el8.x86_64
    default:   systemd-libs-239-78.0.3.el8.x86_64
    default:   systemd-pam-239-78.0.3.el8.x86_64
    default:   systemd-udev-239-78.0.3.el8.x86_64
    default: Installed:
    default:   device-mapper-multipath-0.8.4-39.el8.x86_64
    default:   device-mapper-multipath-libs-0.8.4-39.el8.x86_64
    default:   kernel-uek-core-5.15.0-201.135.6.el8uek.x86_64
    default:   kernel-uek-devel-5.15.0-201.135.6.el8uek.x86_64
    default:   userspace-rcu-0.10.1-4.el8.x86_64
    default:
    default: Complete!
    default: Last metadata expiration check: 0:05:13 ago on Tue 26 Dec 2023 05:52:20 PM UTC.
    default: Dependencies resolved.
    default: ================================================================================
    default:  Package                  Arch    Version              Repository          Size
    default: ================================================================================
    default: Installing:
    default:  oracle-epel-release-el8  x86_64  1.0-5.el8            ol8_baseos_latest   15 k
    default: Installing dependencies:
    default:  yum-utils                noarch  4.0.21-23.0.1.el8    ol8_baseos_latest   75 k
    default:
    default: Transaction Summary
    default: ================================================================================
    default: Install  2 Packages
    default:
    default: Total download size: 90 k
    default: Installed size: 41 k
    default: Downloading Packages:
    default: (1/2): oracle-epel-release-el8-1.0-5.el8.x86_64  97 kB/s |  15 kB     00:00
    default: (2/2): yum-utils-4.0.21-23.0.1.el8.noarch.rpm   369 kB/s |  75 kB     00:00
    default: --------------------------------------------------------------------------------
    default: Total                                           426 kB/s |  90 kB     00:00
    default: Running transaction check
    default: Transaction check succeeded.
    default: Running transaction test
    default: Transaction test succeeded.
    default: Running transaction
    default:   Preparing        :                                                        1/1
    default:   Installing       : yum-utils-4.0.21-23.0.1.el8.noarch                     1/2
    default:   Installing       : oracle-epel-release-el8-1.0-5.el8.x86_64               2/2
    default:   Running scriptlet: oracle-epel-release-el8-1.0-5.el8.x86_64               2/2
    default:   Verifying        : oracle-epel-release-el8-1.0-5.el8.x86_64               1/2
    default:   Verifying        : yum-utils-4.0.21-23.0.1.el8.noarch                     2/2
    default:
    default: Installed:
    default:   oracle-epel-release-el8-1.0-5.el8.x86_64  yum-utils-4.0.21-23.0.1.el8.noarch
    default:
    default: Complete!
    default: Oracle Linux 8 EPEL Packages for Development (x 2.9 MB/s |  58 MB     00:19
    default: Oracle Linux 8 EPEL Modular Packages for Develo 562 kB/s | 322 kB     00:00
    default: Dependencies resolved.
    default: Nothing to do.
    default: Complete!
    default: Last metadata expiration check: 0:00:28 ago on Tue 26 Dec 2023 05:59:03 PM UTC.
    default: Package curl-7.61.1-33.el8.x86_64 is already installed.
    default: Dependencies resolved.
    default: ================================================================================
    default:  Package                      Arch   Version           Repository          Size
    default: ================================================================================
    default: Installing:
    default:  PackageKit-command-not-found x86_64 1.1.12-7.0.1.el8  ol8_appstream       26 k
    default:  bash-completion              noarch 1:2.7-5.el8       ol8_baseos_latest  274 k
    default:  git                          x86_64 2.39.3-1.el8_8    ol8_appstream      104 k
    default:  htop                         x86_64 3.2.1-1.el8       ol8_developer_EPEL 171 k
    default:  iftop                        x86_64 1.0-0.21.pre4.el8 ol8_developer_EPEL  60 k
    default:  iptraf-ng                    x86_64 1.2.1-2.el8       ol8_baseos_latest  258 k
    default:  mc                           x86_64 1:4.8.19-9.el8    ol8_appstream      1.9 M
    default:  screen                       x86_64 4.6.2-12.el8      ol8_developer_EPEL 582 k
    default:  tcpdump                      x86_64 14:4.9.3-3.el8    ol8_appstream      453 k
    default: Installing dependencies:
    default:  PackageKit                   x86_64 1.1.12-7.0.1.el8  ol8_appstream      598 k
    default:  PackageKit-glib              x86_64 1.1.12-7.0.1.el8  ol8_appstream      139 k
    default:  dejavu-fonts-common          noarch 2.35-7.el8        ol8_baseos_latest   74 k
    default:  emacs-filesystem             noarch 1:26.1-11.el8     ol8_baseos_latest   70 k
    default:  fontpackages-filesystem      noarch 1.44-22.el8       ol8_baseos_latest   16 k
    default:  gdk-pixbuf2                  x86_64 2.36.12-5.el8     ol8_baseos_latest  467 k
    default:  git-core                     x86_64 2.39.3-1.el8_8    ol8_appstream       11 M
    default:  git-core-doc                 noarch 2.39.3-1.el8_8    ol8_appstream      3.0 M
    default:  glib-networking              x86_64 2.56.1-1.1.el8    ol8_baseos_latest  155 k
    default:  gpm-libs                     x86_64 1.20.7-17.el8     ol8_appstream       39 k
    default:  gsettings-desktop-schemas    x86_64 3.32.0-6.el8      ol8_baseos_latest  633 k
    default:  json-glib                    x86_64 1.4.4-1.el8       ol8_baseos_latest  144 k
    default:  libappstream-glib            x86_64 0.7.14-3.el8      ol8_baseos_latest  338 k
    default:  libmodman                    x86_64 2.0.1-17.el8      ol8_baseos_latest   36 k
    default:  libproxy                     x86_64 0.4.15-5.2.el8    ol8_baseos_latest   75 k
    default:  libsoup                      x86_64 2.62.3-4.el8      ol8_baseos_latest  425 k
    default:  libstemmer                   x86_64 0-10.585svn.el8   ol8_baseos_latest   73 k
    default:  perl-Error                   noarch 1:0.17025-2.el8   ol8_appstream       46 k
    default:  perl-Git                     noarch 2.39.3-1.el8_8    ol8_appstream       79 k
    default:  perl-TermReadKey             x86_64 2.37-7.el8        ol8_appstream       40 k
    default:  polkit-libs                  x86_64 0.115-15.0.1.el8  ol8_baseos_latest   77 k
    default:  slang                        x86_64 2.3.2-3.el8       ol8_baseos_latest  368 k
    default: Installing weak dependencies:
    default:  abattis-cantarell-fonts      noarch 0.0.25-6.el8      ol8_appstream      155 k
    default:  dejavu-sans-mono-fonts       noarch 2.35-7.el8        ol8_baseos_latest  447 k
    default:
    default: Transaction Summary
    default: ================================================================================
    default: Install  33 Packages
    default:
    default: Total download size: 22 M
    default: Installed size: 72 M
    default: Downloading Packages:
    default: (1/33): iftop-1.0-0.21.pre4.el8.x86_64.rpm      187 kB/s |  60 kB     00:00
    default: (2/33): htop-3.2.1-1.el8.x86_64.rpm             516 kB/s | 171 kB     00:00
    default: (3/33): dejavu-fonts-common-2.35-7.el8.noarch.r 802 kB/s |  74 kB     00:00
    default: (4/33): bash-completion-2.7-5.el8.noarch.rpm    1.1 MB/s | 274 kB     00:00
    default: (5/33): emacs-filesystem-26.1-11.el8.noarch.rpm 721 kB/s |  70 kB     00:00
    default: (6/33): fontpackages-filesystem-1.44-22.el8.noa 269 kB/s |  16 kB     00:00
    default: (7/33): screen-4.6.2-12.el8.x86_64.rpm          765 kB/s | 582 kB     00:00
    default: (8/33): dejavu-sans-mono-fonts-2.35-7.el8.noarc 1.3 MB/s | 447 kB     00:00
    default: (9/33): glib-networking-2.56.1-1.1.el8.x86_64.r 1.3 MB/s | 155 kB     00:00
    default: (10/33): iptraf-ng-1.2.1-2.el8.x86_64.rpm       990 kB/s | 258 kB     00:00
    default: (11/33): gdk-pixbuf2-2.36.12-5.el8.x86_64.rpm   932 kB/s | 467 kB     00:00
    default: (12/33): json-glib-1.4.4-1.el8.x86_64.rpm       1.1 MB/s | 144 kB     00:00
    default: (13/33): libmodman-2.0.1-17.el8.x86_64.rpm      836 kB/s |  36 kB     00:00
    default: (14/33): gsettings-desktop-schemas-3.32.0-6.el8 1.0 MB/s | 633 kB     00:00
    default: (15/33): libproxy-0.4.15-5.2.el8.x86_64.rpm     888 kB/s |  75 kB     00:00
    default: (16/33): libstemmer-0-10.585svn.el8.x86_64.rpm  1.0 MB/s |  73 kB     00:00
    default: (17/33): libappstream-glib-0.7.14-3.el8.x86_64. 1.1 MB/s | 338 kB     00:00
    default: (18/33): polkit-libs-0.115-15.0.1.el8.x86_64.rp 1.0 MB/s |  77 kB     00:00
    default: (19/33): libsoup-2.62.3-4.el8.x86_64.rpm        970 kB/s | 425 kB     00:00
    default: (20/33): PackageKit-command-not-found-1.1.12-7. 353 kB/s |  26 kB     00:00
    default: (21/33): slang-2.3.2-3.el8.x86_64.rpm           911 kB/s | 368 kB     00:00
    default: (22/33): PackageKit-1.1.12-7.0.1.el8.x86_64.rpm 1.3 MB/s | 598 kB     00:00
    default: (23/33): PackageKit-glib-1.1.12-7.0.1.el8.x86_6 777 kB/s | 139 kB     00:00
    default: (24/33): git-2.39.3-1.el8_8.x86_64.rpm          1.1 MB/s | 104 kB     00:00
    default: (25/33): abattis-cantarell-fonts-0.0.25-6.el8.n 802 kB/s | 155 kB     00:00
    default: (26/33): gpm-libs-1.20.7-17.el8.x86_64.rpm      761 kB/s |  39 kB     00:00
    default: (27/33): mc-4.8.19-9.el8.x86_64.rpm             1.0 MB/s | 1.9 MB     00:01
    default: (28/33): perl-Error-0.17025-2.el8.noarch.rpm    735 kB/s |  46 kB     00:00
    default: (29/33): perl-Git-2.39.3-1.el8_8.noarch.rpm     804 kB/s |  79 kB     00:00
    default: (30/33): perl-TermReadKey-2.37-7.el8.x86_64.rpm 480 kB/s |  40 kB     00:00
    default: (31/33): git-core-doc-2.39.3-1.el8_8.noarch.rpm 1.2 MB/s | 3.0 MB     00:02
    default: (32/33): tcpdump-4.9.3-3.el8.x86_64.rpm         956 kB/s | 453 kB     00:00
    default: (33/33): git-core-2.39.3-1.el8_8.x86_64.rpm     2.0 MB/s |  11 MB     00:05
    default: --------------------------------------------------------------------------------
    default: Total                                           3.0 MB/s |  22 MB     00:07
    default: Running transaction check
    default: Transaction check succeeded.
    default: Running transaction test
    default: Transaction test succeeded.
    default: Running transaction
    default:   Preparing        :                                                        1/1
    default:   Installing       : git-core-2.39.3-1.el8_8.x86_64                        1/33
    default:   Installing       : PackageKit-glib-1.1.12-7.0.1.el8.x86_64               2/33
    default:   Installing       : gdk-pixbuf2-2.36.12-5.el8.x86_64                      3/33
    default:   Running scriptlet: gdk-pixbuf2-2.36.12-5.el8.x86_64                      3/33
    default:   Installing       : fontpackages-filesystem-1.44-22.el8.noarch            4/33
    default:   Installing       : dejavu-fonts-common-2.35-7.el8.noarch                 5/33
    default:   Installing       : dejavu-sans-mono-fonts-2.35-7.el8.noarch              6/33
    default:   Installing       : abattis-cantarell-fonts-0.0.25-6.el8.noarch           7/33
    default:   Installing       : gsettings-desktop-schemas-3.32.0-6.el8.x86_64         8/33
    default:   Installing       : git-core-doc-2.39.3-1.el8_8.noarch                    9/33
    default:   Installing       : perl-TermReadKey-2.37-7.el8.x86_64                   10/33
    default:   Installing       : perl-Error-1:0.17025-2.el8.noarch                    11/33
    default:   Installing       : gpm-libs-1.20.7-17.el8.x86_64                        12/33
    default:   Running scriptlet: gpm-libs-1.20.7-17.el8.x86_64                        12/33
    default:   Installing       : slang-2.3.2-3.el8.x86_64                             13/33
    default:   Installing       : polkit-libs-0.115-15.0.1.el8.x86_64                  14/33
    default:   Running scriptlet: polkit-libs-0.115-15.0.1.el8.x86_64                  14/33
    default:   Installing       : libstemmer-0-10.585svn.el8.x86_64                    15/33
    default:   Running scriptlet: libstemmer-0-10.585svn.el8.x86_64                    15/33
    default:   Installing       : libmodman-2.0.1-17.el8.x86_64                        16/33
    default:   Running scriptlet: libmodman-2.0.1-17.el8.x86_64                        16/33
    default:   Installing       : libproxy-0.4.15-5.2.el8.x86_64                       17/33
    default:   Running scriptlet: libproxy-0.4.15-5.2.el8.x86_64                       17/33
    default:   Installing       : glib-networking-2.56.1-1.1.el8.x86_64                18/33
    default:   Installing       : libsoup-2.62.3-4.el8.x86_64                          19/33
    default:   Installing       : json-glib-1.4.4-1.el8.x86_64                         20/33
    default:   Installing       : libappstream-glib-0.7.14-3.el8.x86_64                21/33
    default:   Installing       : PackageKit-1.1.12-7.0.1.el8.x86_64                   22/33
    default:   Running scriptlet: PackageKit-1.1.12-7.0.1.el8.x86_64                   22/33
    default:   Installing       : emacs-filesystem-1:26.1-11.el8.noarch                23/33
    default:   Installing       : perl-Git-2.39.3-1.el8_8.noarch                       24/33
    default:   Installing       : git-2.39.3-1.el8_8.x86_64                            25/33
    default:   Installing       : PackageKit-command-not-found-1.1.12-7.0.1.el8.x86_   26/33
    default:   Installing       : mc-1:4.8.19-9.el8.x86_64                             27/33
    default:   Running scriptlet: tcpdump-14:4.9.3-3.el8.x86_64                        28/33
    default:   Installing       : tcpdump-14:4.9.3-3.el8.x86_64                        28/33
    default:   Installing       : iptraf-ng-1.2.1-2.el8.x86_64                         29/33
    default:   Installing       : bash-completion-1:2.7-5.el8.noarch                   30/33
    default:   Running scriptlet: screen-4.6.2-12.el8.x86_64                           31/33
    default:   Installing       : screen-4.6.2-12.el8.x86_64                           31/33
    default:   Installing       : iftop-1.0-0.21.pre4.el8.x86_64                       32/33
    default:   Installing       : htop-3.2.1-1.el8.x86_64                              33/33
    default:   Running scriptlet: htop-3.2.1-1.el8.x86_64                              33/33
    default:   Verifying        : htop-3.2.1-1.el8.x86_64                               1/33
    default:   Verifying        : iftop-1.0-0.21.pre4.el8.x86_64                        2/33
    default:   Verifying        : screen-4.6.2-12.el8.x86_64                            3/33
    default:   Verifying        : bash-completion-1:2.7-5.el8.noarch                    4/33
    default:   Verifying        : dejavu-fonts-common-2.35-7.el8.noarch                 5/33
    default:   Verifying        : dejavu-sans-mono-fonts-2.35-7.el8.noarch              6/33
    default:   Verifying        : emacs-filesystem-1:26.1-11.el8.noarch                 7/33
    default:   Verifying        : fontpackages-filesystem-1.44-22.el8.noarch            8/33
    default:   Verifying        : gdk-pixbuf2-2.36.12-5.el8.x86_64                      9/33
    default:   Verifying        : glib-networking-2.56.1-1.1.el8.x86_64                10/33
    default:   Verifying        : gsettings-desktop-schemas-3.32.0-6.el8.x86_64        11/33
    default:   Verifying        : iptraf-ng-1.2.1-2.el8.x86_64                         12/33
    default:   Verifying        : json-glib-1.4.4-1.el8.x86_64                         13/33
    default:   Verifying        : libappstream-glib-0.7.14-3.el8.x86_64                14/33
    default:   Verifying        : libmodman-2.0.1-17.el8.x86_64                        15/33
    default:   Verifying        : libproxy-0.4.15-5.2.el8.x86_64                       16/33
    default:   Verifying        : libsoup-2.62.3-4.el8.x86_64                          17/33
    default:   Verifying        : libstemmer-0-10.585svn.el8.x86_64                    18/33
    default:   Verifying        : polkit-libs-0.115-15.0.1.el8.x86_64                  19/33
    default:   Verifying        : slang-2.3.2-3.el8.x86_64                             20/33
    default:   Verifying        : PackageKit-1.1.12-7.0.1.el8.x86_64                   21/33
    default:   Verifying        : PackageKit-command-not-found-1.1.12-7.0.1.el8.x86_   22/33
    default:   Verifying        : PackageKit-glib-1.1.12-7.0.1.el8.x86_64              23/33
    default:   Verifying        : abattis-cantarell-fonts-0.0.25-6.el8.noarch          24/33
    default:   Verifying        : git-2.39.3-1.el8_8.x86_64                            25/33
    default:   Verifying        : git-core-2.39.3-1.el8_8.x86_64                       26/33
    default:   Verifying        : git-core-doc-2.39.3-1.el8_8.noarch                   27/33
    default:   Verifying        : gpm-libs-1.20.7-17.el8.x86_64                        28/33
    default:   Verifying        : mc-1:4.8.19-9.el8.x86_64                             29/33
    default:   Verifying        : perl-Error-1:0.17025-2.el8.noarch                    30/33
    default:   Verifying        : perl-Git-2.39.3-1.el8_8.noarch                       31/33
    default:   Verifying        : perl-TermReadKey-2.37-7.el8.x86_64                   32/33
    default:   Verifying        : tcpdump-14:4.9.3-3.el8.x86_64                        33/33
    default:
    default: Installed:
    default:   PackageKit-1.1.12-7.0.1.el8.x86_64
    default:   PackageKit-command-not-found-1.1.12-7.0.1.el8.x86_64
    default:   PackageKit-glib-1.1.12-7.0.1.el8.x86_64
    default:   abattis-cantarell-fonts-0.0.25-6.el8.noarch
    default:   bash-completion-1:2.7-5.el8.noarch
    default:   dejavu-fonts-common-2.35-7.el8.noarch
    default:   dejavu-sans-mono-fonts-2.35-7.el8.noarch
    default:   emacs-filesystem-1:26.1-11.el8.noarch
    default:   fontpackages-filesystem-1.44-22.el8.noarch
    default:   gdk-pixbuf2-2.36.12-5.el8.x86_64
    default:   git-2.39.3-1.el8_8.x86_64
    default:   git-core-2.39.3-1.el8_8.x86_64
    default:   git-core-doc-2.39.3-1.el8_8.noarch
    default:   glib-networking-2.56.1-1.1.el8.x86_64
    default:   gpm-libs-1.20.7-17.el8.x86_64
    default:   gsettings-desktop-schemas-3.32.0-6.el8.x86_64
    default:   htop-3.2.1-1.el8.x86_64
    default:   iftop-1.0-0.21.pre4.el8.x86_64
    default:   iptraf-ng-1.2.1-2.el8.x86_64
    default:   json-glib-1.4.4-1.el8.x86_64
    default:   libappstream-glib-0.7.14-3.el8.x86_64
    default:   libmodman-2.0.1-17.el8.x86_64
    default:   libproxy-0.4.15-5.2.el8.x86_64
    default:   libsoup-2.62.3-4.el8.x86_64
    default:   libstemmer-0-10.585svn.el8.x86_64
    default:   mc-1:4.8.19-9.el8.x86_64
    default:   perl-Error-1:0.17025-2.el8.noarch
    default:   perl-Git-2.39.3-1.el8_8.noarch
    default:   perl-TermReadKey-2.37-7.el8.x86_64
    default:   polkit-libs-0.115-15.0.1.el8.x86_64
    default:   screen-4.6.2-12.el8.x86_64
    default:   slang-2.3.2-3.el8.x86_64
    default:   tcpdump-14:4.9.3-3.el8.x86_64
    default:
    default: Complete!
    default: Last metadata expiration check: 0:01:08 ago on Tue 26 Dec 2023 05:59:03 PM UTC.
    default: Dependencies resolved.
    default: =======================================================================================
    default:  Package          Arch    Version                              Repository          Size
    default: =======================================================================================
    default: Installing:
    default:  fuse-overlayfs   x86_64  1.12-1.module+el8.9.0+90102+5a5b2dad ol8_appstream       69 k
    default: Installing dependencies:
    default:  fuse-common      x86_64  3.3.0-17.0.1.el8                     ol8_baseos_latest   21 k
    default:  fuse3            x86_64  3.3.0-17.0.1.el8                     ol8_baseos_latest   54 k
    default:  fuse3-libs       x86_64  3.3.0-17.0.1.el8                     ol8_baseos_latest   95 k
    default: Enabling module streams:
    default:  container-tools          ol8
    default:
    default: Transaction Summary
    default: =======================================================================================
    default: Install  4 Packages
    default:
    default: Total download size: 239 k
    default: Installed size: 507 k
    default: Downloading Packages:
    default: (1/4): fuse-common-3.3.0-17.0.1.el8.x86_64.rpm   94 kB/s |  21 kB     00:00
    default: (2/4): fuse3-3.3.0-17.0.1.el8.x86_64.rpm        207 kB/s |  54 kB     00:00
    default: (3/4): fuse-overlayfs-1.12-1.module+el8.9.0+901 973 kB/s |  69 kB     00:00
    default: (4/4): fuse3-libs-3.3.0-17.0.1.el8.x86_64.rpm   311 kB/s |  95 kB     00:00
    default: --------------------------------------------------------------------------------
    default: Total                                           723 kB/s | 239 kB     00:00
    default: Running transaction check
    default: Transaction check succeeded.
    default: Running transaction test
    default: Transaction test succeeded.
    default: Running transaction
    default:   Preparing        :                                                        1/1
    default:   Installing       : fuse3-libs-3.3.0-17.0.1.el8.x86_64                     1/4
    default:   Running scriptlet: fuse3-libs-3.3.0-17.0.1.el8.x86_64                     1/4
    default:   Installing       : fuse-common-3.3.0-17.0.1.el8.x86_64                    2/4
    default:   Installing       : fuse3-3.3.0-17.0.1.el8.x86_64                          3/4
    default:   Installing       : fuse-overlayfs-1.12-1.module+el8.9.0+90102+5a5b2dad.   4/4
    default:   Running scriptlet: fuse-overlayfs-1.12-1.module+el8.9.0+90102+5a5b2dad.   4/4
    default:   Verifying        : fuse-common-3.3.0-17.0.1.el8.x86_64                    1/4
    default:   Verifying        : fuse3-3.3.0-17.0.1.el8.x86_64                          2/4
    default:   Verifying        : fuse3-libs-3.3.0-17.0.1.el8.x86_64                     3/4
    default:   Verifying        : fuse-overlayfs-1.12-1.module+el8.9.0+90102+5a5b2dad.   4/4
    default:
    default: Installed:
    default:   fuse-common-3.3.0-17.0.1.el8.x86_64
    default:   fuse-overlayfs-1.12-1.module+el8.9.0+90102+5a5b2dad.x86_64
    default:   fuse3-3.3.0-17.0.1.el8.x86_64
    default:   fuse3-libs-3.3.0-17.0.1.el8.x86_64
    default:
    default: Complete!
    default: NAME                UUID                                  TYPE      DEVICE
    default: System eth0         5fb06bd0-0bb0-7ffb-45f1-d6edd65f3e03  ethernet  eth0
    default: System eth1         9c92fad9-6ecb-3e6c-eb4d-8a47c6f50c04  ethernet  eth1
    default: Wired connection 1  e5725b4b-23ba-3061-9d1f-df024e12b476  ethernet  --
    default: Connection successfully activated (D-Bus active path: /org/freedesktop/NetworkManager/ActiveConnection/3)
    default: # Generated by NetworkManager
    default: search Home
    default: nameserver 10.0.2.3
    default: # Generated by NetworkManager
    default: nameserver 8.8.8.8
    default: nameserver 1.1.1.1
    default: Adding repo from: https://download.docker.com/linux/centos/docker-ce.repo
    default: Docker CE Stable - x86_64                       135 kB/s |  52 kB     00:00
    default: Dependencies resolved.
    default: Nothing to do.
    default: Complete!
    default: Last metadata expiration check: 0:00:18 ago on Tue 26 Dec 2023 08:00:36 PM EET.
    default: Dependencies resolved.
    default: =======================================================================================================
    default:  Package                     Arch    Version                                   Repository          Size
    default: =======================================================================================================
    default: Installing:
    default:  containerd.io               x86_64  1.6.26-3.1.el8                            docker-ce-stable    35 M
    default:  docker-buildx-plugin        x86_64  0.11.2-1.el8                              docker-ce-stable    13 M
    default:  docker-ce                   x86_64  3:24.0.7-1.el8                            docker-ce-stable    24 M
    default:  docker-ce-cli               x86_64  1:24.0.7-1.el8                            docker-ce-stable   7.2 M
    default:  docker-compose-plugin       x86_64  2.21.0-1.el8                              docker-ce-stable    13 M
    default: Installing dependencies:
    default:  container-selinux           noarch  2:2.221.0-1.module+el8.9.0+90102+5a5b2dad ol8_appstream       68 k
    default:  libcgroup                   x86_64  0.41-19.el8                               ol8_baseos_latest   70 k
    default:  libslirp                    x86_64  4.4.0-1.module+el8.9.0+90102+5a5b2dad     ol8_appstream       69 k
    default:  slirp4netns                 x86_64  1.2.1-1.module+el8.9.0+90102+5a5b2dad     ol8_appstream       55 k
    default: Installing weak dependencies:
    default:  docker-ce-rootless-extras   x86_64  24.0.7-1.el8                              docker-ce-stable   4.9 M
    default:
    default: Transaction Summary
    default: =======================================================================================================
    default: Install  10 Packages
    default:
    default: Total download size: 97 M
    default: Installed size: 369 M
    default: Downloading Packages:
    default: (1/10): docker-buildx-plugin-0.11.2-1.el8.x86_6 1.0 MB/s |  13 MB     00:13
    default: (2/10): docker-ce-cli-24.0.7-1.el8.x86_64.rpm   1.0 MB/s | 7.2 MB     00:06
    default: (3/10): docker-ce-24.0.7-1.el8.x86_64.rpm       1.0 MB/s |  24 MB     00:23
    default: (4/10): docker-ce-rootless-extras-24.0.7-1.el8. 1.1 MB/s | 4.9 MB     00:04
    default: (5/10): libcgroup-0.41-19.el8.x86_64.rpm        136 kB/s |  70 kB     00:00
    default: (6/10): container-selinux-2.221.0-1.module+el8. 256 kB/s |  68 kB     00:00
    default: (7/10): libslirp-4.4.0-1.module+el8.9.0+90102+5 662 kB/s |  69 kB     00:00
    default: (8/10): slirp4netns-1.2.1-1.module+el8.9.0+9010 746 kB/s |  55 kB     00:00
    default: (9/10): containerd.io-1.6.26-3.1.el8.x86_64.rpm 1.1 MB/s |  35 MB     00:30
    default: (10/10): docker-compose-plugin-2.21.0-1.el8.x86 1.7 MB/s |  13 MB     00:07
    default: --------------------------------------------------------------------------------
    default: Total                                           3.1 MB/s |  97 MB     00:31
    default: Docker CE Stable - x86_64                       7.5 kB/s | 1.6 kB     00:00
    default: Importing GPG key 0x621E9F35:
    default:  Userid     : "Docker Release (CE rpm) <docker@docker.com>"
    default:  Fingerprint: 060A 61C5 1B55 8A7F 742B 77AA C52F EB6B 621E 9F35
    default:  From       : https://download.docker.com/linux/centos/gpg
    default: Key imported successfully
    default: Running transaction check
    default: Transaction check succeeded.
    default: Running transaction test
    default: Transaction test succeeded.
    default: Running transaction
    default:   Preparing        :                                                        1/1
    default:   Running scriptlet: container-selinux-2:2.221.0-1.module+el8.9.0+90102    1/10
    default:   Installing       : container-selinux-2:2.221.0-1.module+el8.9.0+90102    1/10
    default:   Running scriptlet: container-selinux-2:2.221.0-1.module+el8.9.0+90102    1/10
    default:   Installing       : docker-compose-plugin-2.21.0-1.el8.x86_64             2/10
    default:   Running scriptlet: docker-compose-plugin-2.21.0-1.el8.x86_64             2/10
    default:   Installing       : containerd.io-1.6.26-3.1.el8.x86_64                   3/10
    default:   Running scriptlet: containerd.io-1.6.26-3.1.el8.x86_64                   3/10
    default:   Installing       : libslirp-4.4.0-1.module+el8.9.0+90102+5a5b2dad.x86    4/10
    default:   Installing       : slirp4netns-1.2.1-1.module+el8.9.0+90102+5a5b2dad.    5/10
    default:   Running scriptlet: libcgroup-0.41-19.el8.x86_64                          6/10
    default:   Installing       : libcgroup-0.41-19.el8.x86_64                          6/10
    default:   Running scriptlet: libcgroup-0.41-19.el8.x86_64                          6/10
    default:   Installing       : docker-buildx-plugin-0.11.2-1.el8.x86_64              7/10
    default:   Running scriptlet: docker-buildx-plugin-0.11.2-1.el8.x86_64              7/10
    default:   Installing       : docker-ce-cli-1:24.0.7-1.el8.x86_64                   8/10
    default:   Running scriptlet: docker-ce-cli-1:24.0.7-1.el8.x86_64                   8/10
    default:   Installing       : docker-ce-rootless-extras-24.0.7-1.el8.x86_64         9/10
    default:   Running scriptlet: docker-ce-rootless-extras-24.0.7-1.el8.x86_64         9/10
    default:   Installing       : docker-ce-3:24.0.7-1.el8.x86_64                      10/10
    default:   Running scriptlet: docker-ce-3:24.0.7-1.el8.x86_64                      10/10
    default:   Running scriptlet: container-selinux-2:2.221.0-1.module+el8.9.0+90102   10/10
    default:   Running scriptlet: docker-ce-3:24.0.7-1.el8.x86_64                      10/10
    default:   Verifying        : containerd.io-1.6.26-3.1.el8.x86_64                   1/10
    default:   Verifying        : docker-buildx-plugin-0.11.2-1.el8.x86_64              2/10
    default:   Verifying        : docker-ce-3:24.0.7-1.el8.x86_64                       3/10
    default:   Verifying        : docker-ce-cli-1:24.0.7-1.el8.x86_64                   4/10
    default:   Verifying        : docker-ce-rootless-extras-24.0.7-1.el8.x86_64         5/10
    default:   Verifying        : docker-compose-plugin-2.21.0-1.el8.x86_64             6/10
    default:   Verifying        : libcgroup-0.41-19.el8.x86_64                          7/10
    default:   Verifying        : container-selinux-2:2.221.0-1.module+el8.9.0+90102    8/10
    default:   Verifying        : libslirp-4.4.0-1.module+el8.9.0+90102+5a5b2dad.x86    9/10
    default:   Verifying        : slirp4netns-1.2.1-1.module+el8.9.0+90102+5a5b2dad.   10/10
    default:
    default: Installed:
    default:   container-selinux-2:2.221.0-1.module+el8.9.0+90102+5a5b2dad.noarch
    default:   containerd.io-1.6.26-3.1.el8.x86_64
    default:   docker-buildx-plugin-0.11.2-1.el8.x86_64
    default:   docker-ce-3:24.0.7-1.el8.x86_64
    default:   docker-ce-cli-1:24.0.7-1.el8.x86_64
    default:   docker-ce-rootless-extras-24.0.7-1.el8.x86_64
    default:   docker-compose-plugin-2.21.0-1.el8.x86_64
    default:   libcgroup-0.41-19.el8.x86_64
    default:   libslirp-4.4.0-1.module+el8.9.0+90102+5a5b2dad.x86_64
    default:   slirp4netns-1.2.1-1.module+el8.9.0+90102+5a5b2dad.x86_64
    default:
    default: Complete!
    default: vagrant : vagrant wheel docker
    default: uid=1000(vagrant) gid=1000(vagrant) groups=1000(vagrant),10(wheel) context=unconfined_u:unconfined_r:unconfined_t:s0-s0:c0.c1023
    default: Created symlink /etc/systemd/system/multi-user.target.wants/docker.service → /usr/lib/systemd/system/docker.service.
    default: Created symlink /etc/systemd/system/multi-user.target.wants/containerd.service → /usr/lib/systemd/system/containerd.service.
==> default: Running provisioner: shell...
    default: Running: inline script
    default: rebooting!
==> default: Waiting for machine to reboot...
==> default: Running provisioner: shell...
    default: Running: inline script
    default: script2
    default: ● docker.service - Docker Application Container Engine
    default:    Loaded: loaded (/usr/lib/systemd/system/docker.service; enabled; vendor preset: disabled)
    default:    Active: active (running) since Tue 2023-12-26 20:06:37 EET; 8s ago
    default:      Docs: https://docs.docker.com
    default:  Main PID: 1006 (dockerd)
    default:     Tasks: 10
    default:    Memory: 104.0M
    default:    CGroup: /system.slice/docker.service
    default:            └─1006 /usr/bin/dockerd -H fd:// --containerd=/run/containerd/containerd.sock
    default:
    default: Dec 26 20:06:36 localhost.localdomain dockerd[1006]: time="2023-12-26T20:06:36.544004248+02:00" level=info msg="Starting up"
    default: Dec 26 20:06:36 localhost.localdomain dockerd[1006]: time="2023-12-26T20:06:36.661550319+02:00" level=info msg="[graphdriver] using prior storage driver: overlay2"
    default: Dec 26 20:06:36 localhost.localdomain dockerd[1006]: time="2023-12-26T20:06:36.664281912+02:00" level=info msg="Loading containers: start."
    default: Dec 26 20:06:37 localhost.localdomain dockerd[1006]: time="2023-12-26T20:06:37.512812460+02:00" level=info msg="Default bridge (docker0) is assigned with an IP address 172.17.0.0/16. Daemon option --bip can be used to set a preferred IP address"
    default: Dec 26 20:06:37 localhost.localdomain dockerd[1006]: time="2023-12-26T20:06:37.678591721+02:00" level=info msg="Loading containers: done."
    default: Dec 26 20:06:37 localhost.localdomain dockerd[1006]: time="2023-12-26T20:06:37.772990807+02:00" level=warning msg="Not using native diff for overlay2, this may cause degraded performance for building images: kernel has CONFIG_OVERLAY_FS_REDIRECT_DIR enabled" storage-driver=overlay2
    default: Dec 26 20:06:37 localhost.localdomain dockerd[1006]: time="2023-12-26T20:06:37.773697722+02:00" level=info msg="Docker daemon" commit=311b9ff graphdriver=overlay2 version=24.0.7
    default: Dec 26 20:06:37 localhost.localdomain dockerd[1006]: time="2023-12-26T20:06:37.774177410+02:00" level=info msg="Daemon has completed initialization"
    default: Dec 26 20:06:37 localhost.localdomain dockerd[1006]: time="2023-12-26T20:06:37.869259794+02:00" level=info msg="API listen on /run/docker.sock"
    default: Dec 26 20:06:37 localhost.localdomain systemd[1]: Started Docker Application Container Engine.
    default: Docker version 24.0.7, build afdd53b
    default: Unable to find image 'hello-world:latest' locally
    default: latest: Pulling from library/hello-world
    default: c1ec31eb5944: Pulling fs layer
    default: c1ec31eb5944: Download complete
    default: c1ec31eb5944: Pull complete
    default: Digest: sha256:ac69084025c660510933cca701f615283cdbb3aa0963188770b54c31c8962493
    default: Status: Downloaded newer image for hello-world:latest
    default:
    default: Hello from Docker!
    default: This message shows that your installation appears to be working correctly.
    default:
    default: To generate this message, Docker took the following steps:
    default:  1. The Docker client contacted the Docker daemon.
    default:  2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    default:     (amd64)
    default:  3. The Docker daemon created a new container from that image which runs the
    default:     executable that produces the output you are currently reading.
    default:  4. The Docker daemon streamed that output to the Docker client, which sent it
    default:     to your terminal.
    default:
    default: To try something more ambitious, you can run an Ubuntu container with:
    default:  $ docker run -it ubuntu bash
    default:
    default: Share images, automate workflows, and more with a free Docker ID:
    default:  https://hub.docker.com/
    default:
    default: For more examples and ideas, visit:
    default:  https://docs.docker.com/get-started/
    default:
    default: CONTAINER ID   IMAGE         COMMAND    CREATED        STATUS                              PORTS     NAMES
    default: 3a39af6dd50a   hello-world   "/hello"   1 second ago   Exited (0) Less than a second ago             gracious_maxwell
    default: 3a39af6dd50a
    default: 3a39af6dd50a
    default: REPOSITORY    TAG       IMAGE ID       CREATED        SIZE
    default: hello-world   latest    d2c94e258dcb   7 months ago   13.3kB
    default: Untagged: hello-world:latest
    default: Untagged: hello-world@sha256:ac69084025c660510933cca701f615283cdbb3aa0963188770b54c31c8962493
    default: Deleted: sha256:d2c94e258dcb3c5ac2798d32e1249e42ef01cba4841c2234249495f87264ac5a
    default: Deleted: sha256:ac28800ec8bb38d5c35b49d45a6ac4777544941199075dff8c4eb63e093aa81e
    default:   % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
    default:                                  Dload  Upload   Total   Spent    Left  Speed
100    97  100    97    0     0    388      0 --:--:-- --:--:-- --:--:--   389
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0
100 6304k  100 6304k    0     0  1940k      0  0:00:03  0:00:03 --:--:-- 2881k
    default: kind version 0.20.0
    default:   % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
    default:                                  Dload  Upload   Total   Spent    Left  Speed
100   138  100   138    0     0    352      0 --:--:-- --:--:-- --:--:--   351
100 47.4M  100 47.4M    0     0  3024k      0  0:00:16  0:00:16 --:--:-- 3109k
    default: Client Version: v1.29.0
    default: Kustomize Version: v5.0.4-0.20230601165947-6ce0bf390ce3
    default: --2023-12-26 20:07:12--  https://github.com/derailed/k9s/releases/download/v0.29.1/k9s_linux_amd64.rpm
    default: Resolving github.com (github.com)... 140.82.121.4
    default: Connecting to github.com (github.com)|140.82.121.4|:443... connected.
    default: HTTP request sent, awaiting response... 302 Found
    default: Location: https://objects.githubusercontent.com/github-production-release-asset-2e65be/167596393/c2a113ec-213d-4149-9acc-ab45262df0b2?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAIWNJYAX4CSVEH53A%2F20231226%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20231226T180713Z&X-Amz-Expires=300&X-Amz-Signature=3018edf56c1a77e3a2e052a1a05c792d9983a71d5cb0a2600402e61cdf18af63&X-Amz-SignedHeaders=host&actor_id=0&key_id=0&repo_id=167596393&response-content-disposition=attachment%3B%20filename%3Dk9s_linux_amd64.rpm&response-content-type=application%2Foctet-stream [following]
    default: --2023-12-26 20:07:13--  https://objects.githubusercontent.com/github-production-release-asset-2e65be/167596393/c2a113ec-213d-4149-9acc-ab45262df0b2?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAIWNJYAX4CSVEH53A%2F20231226%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20231226T180713Z&X-Amz-Expires=300&X-Amz-Signature=3018edf56c1a77e3a2e052a1a05c792d9983a71d5cb0a2600402e61cdf18af63&X-Amz-SignedHeaders=host&actor_id=0&key_id=0&repo_id=167596393&response-content-disposition=attachment%3B%20filename%3Dk9s_linux_amd64.rpm&response-content-type=application%2Foctet-stream
    default: Resolving objects.githubusercontent.com (objects.githubusercontent.com)... 185.199.108.133, 185.199.109.133, 185.199.110.133, ...
    default: Connecting to objects.githubusercontent.com (objects.githubusercontent.com)|185.199.108.133|:443... connected.
    default: HTTP request sent, awaiting response... 200 OK
    default: Length: 31481543 (30M) [application/octet-stream]
    default: Saving to: ‘k9s_linux_amd64.rpm’
    default:
    default:      0K .......... .......... .......... .......... ..........  0% 1.19M 25s
    default:     50K .......... .......... .......... .......... ..........  0% 1.72M 21s
    default:    100K .......... .......... .......... .......... ..........  0%  819K 27s
    default:    150K .......... .......... .......... .......... ..........  0% 2.68M 23s
    default:    200K .......... .......... .......... .......... ..........  0% 1.96M 21s
    default:    250K .......... .......... .......... .......... ..........  0% 4.49M 19s
    default:    300K .......... .......... .......... .......... ..........  1% 1.85M 18s
    default:    350K .......... .......... .......... .......... ..........  1% 2.51M 17s
    default:    400K .......... .......... .......... .......... ..........  1% 3.34M 16s
    default:    450K .......... .......... .......... .......... ..........  1% 2.49M 16s
    default:    500K .......... .......... .......... .......... ..........  1% 3.47M 15s
    default:    550K .......... .......... .......... .......... ..........  1% 2.46M 15s
    default:    600K .......... .......... .......... .......... ..........  2% 4.01M 14s
    default:    650K .......... .......... .......... .......... ..........  2% 2.17M 14s
    default:    700K .......... .......... .......... .......... ..........  2% 2.40M 14s
    default:    750K .......... .......... .......... .......... ..........  2% 2.22M 14s
    default:    800K .......... .......... .......... .......... ..........  2% 2.85M 14s
    default:    850K .......... .......... .......... .......... ..........  2% 2.76M 14s
    default:    900K .......... .......... .......... .......... ..........  3% 2.56M 13s
    default:    950K .......... .......... .......... .......... ..........  3% 3.04M 13s
    default:   1000K .......... .......... .......... .......... ..........  3% 2.44M 13s
    default:   1050K .......... .......... .......... .......... ..........  3% 2.58M 13s
    default:   1100K .......... .......... .......... .......... ..........  3% 2.39M 13s
    default:   1150K .......... .......... .......... .......... ..........  3% 2.87M 13s
    default:   1200K .......... .......... .......... .......... ..........  4% 2.73M 13s
    default:   1250K .......... .......... .......... .......... ..........  4% 3.03M 13s
    default:   1300K .......... .......... .......... .......... ..........  4% 2.07M 13s
    default:   1350K .......... .......... .......... .......... ..........  4% 3.04M 12s
    default:   1400K .......... .......... .......... .......... ..........  4% 2.60M 12s
    default:   1450K .......... .......... .......... .......... ..........  4% 3.22M 12s
    default:   1500K .......... .......... .......... .......... ..........  5% 1.95M 12s
    default:   1550K .......... .......... .......... .......... ..........  5% 2.28M 12s
    default:   1600K .......... .......... .......... .......... ..........  5% 3.60M 12s
    default:   1650K .......... .......... .......... .......... ..........  5% 2.36M 12s
    default:   1700K .......... .......... .......... .......... ..........  5% 2.52M 12s
    default:   1750K .......... .......... .......... .......... ..........  5% 3.08M 12s
    default:   1800K .......... .......... .......... .......... ..........  6% 2.02M 12s
    default:   1850K .......... .......... .......... .......... ..........  6% 3.51M 12s
    default:   1900K .......... .......... .......... .......... ..........  6% 2.25M 12s
    default:   1950K .......... .......... .......... .......... ..........  6% 2.24M 12s
    default:   2000K .......... .......... .......... .......... ..........  6% 2.82M 12s
    default:   2050K .......... .......... .......... .......... ..........  6% 3.46M 12s
    default:   2100K .......... .......... .......... .......... ..........  6% 2.07M 12s
    default:   2150K .......... .......... .......... .......... ..........  7% 3.37M 12s
    default:   2200K .......... .......... .......... .......... ..........  7% 1.76M 12s
    default:   2250K .......... .......... .......... .......... ..........  7% 8.56M 12s
    default:   2300K .......... .......... .......... .......... ..........  7% 1.81M 12s
    default:   2350K .......... .......... .......... .......... ..........  7% 3.38M 11s
    default:   2400K .......... .......... .......... .......... ..........  7% 2.72M 11s
    default:   2450K .......... .......... .......... .......... ..........  8% 2.48M 11s
    default:   2500K .......... .......... .......... .......... ..........  8% 2.94M 11s
    default:   2550K .......... .......... .......... .......... ..........  8% 3.05M 11s
    default:   2600K .......... .......... .......... .......... ..........  8% 2.71M 11s
    default:   2650K .......... .......... .......... .......... ..........  8% 3.27M 11s
    default:   2700K .......... .......... .......... .......... ..........  8% 2.06M 11s
    default:   2750K .......... .......... .......... .......... ..........  9% 3.22M 11s
    default:   2800K .......... .......... .......... .......... ..........  9% 2.58M 11s
    default:   2850K .......... .......... .......... .......... ..........  9% 3.38M 11s
    default:   2900K .......... .......... .......... .......... ..........  9% 3.56M 11s
    default:   2950K .......... .......... .......... .......... ..........  9% 2.54M 11s
    default:   3000K .......... .......... .......... .......... ..........  9% 2.05M 11s
    default:   3050K .......... .......... .......... .......... .......... 10% 3.65M 11s
    default:   3100K .......... .......... .......... .......... .......... 10% 1.99M 11s
    default:   3150K .......... .......... .......... .......... .......... 10% 2.78M 11s
    default:   3200K .......... .......... .......... .......... .......... 10% 3.96M 11s
    default:   3250K .......... .......... .......... .......... .......... 10% 1.56M 11s
    default:   3300K .......... .......... .......... .......... .......... 10% 2.49M 11s
    default:   3350K .......... .......... .......... .......... .......... 11% 4.70M 11s
    default:   3400K .......... .......... .......... .......... .......... 11% 3.10M 11s
    default:   3450K .......... .......... .......... .......... .......... 11% 2.68M 11s
    default:   3500K .......... .......... .......... .......... .......... 11% 2.51M 11s
    default:   3550K .......... .......... .......... .......... .......... 11% 2.16M 11s
    default:   3600K .......... .......... .......... .......... .......... 11% 2.92M 11s
    default:   3650K .......... .......... .......... .......... .......... 12% 2.43M 11s
    default:   3700K .......... .......... .......... .......... .......... 12% 2.67M 11s
    default:   3750K .......... .......... .......... .......... .......... 12% 3.26M 10s
    default:   3800K .......... .......... .......... .......... .......... 12% 2.22M 10s
    default:   3850K .......... .......... .......... .......... .......... 12% 2.35M 10s
    default:   3900K .......... .......... .......... .......... .......... 12% 2.81M 10s
    default:   3950K .......... .......... .......... .......... .......... 13% 2.53M 10s
    default:   4000K .......... .......... .......... .......... .......... 13% 2.29M 10s
    default:   4050K .......... .......... .......... .......... .......... 13% 3.00M 10s
    default:   4100K .......... .......... .......... .......... .......... 13% 4.32M 10s
    default:   4150K .......... .......... .......... .......... .......... 13% 2.97M 10s
    default:   4200K .......... .......... .......... .......... .......... 13% 3.02M 10s
    default:   4250K .......... .......... .......... .......... .......... 13% 3.26M 10s
    default:   4300K .......... .......... .......... .......... .......... 14% 2.15M 10s
    default:   4350K .......... .......... .......... .......... .......... 14% 2.21M 10s
    default:   4400K .......... .......... .......... .......... .......... 14% 3.48M 10s
    default:   4450K .......... .......... .......... .......... .......... 14% 3.80M 10s
    default:   4500K .......... .......... .......... .......... .......... 14% 1.66M 10s
    default:   4550K .......... .......... .......... .......... .......... 14% 2.78M 10s
    default:   4600K .......... .......... .......... .......... .......... 15% 5.12M 10s
    default:   4650K .......... .......... .......... .......... .......... 15% 2.24M 10s
    default:   4700K .......... .......... .......... .......... .......... 15% 1.75M 10s
    default:   4750K .......... .......... .......... .......... .......... 15% 3.67M 10s
    default:   4800K .......... .......... .......... .......... .......... 15% 3.42M 10s
    default:   4850K .......... .......... .......... .......... .......... 15% 2.55M 10s
    default:   4900K .......... .......... .......... .......... .......... 16% 2.81M 10s
    default:   4950K .......... .......... .......... .......... .......... 16% 3.26M 10s
    default:   5000K .......... .......... .......... .......... .......... 16% 3.05M 10s
    default:   5050K .......... .......... .......... .......... .......... 16% 3.01M 10s
    default:   5100K .......... .......... .......... .......... .......... 16% 2.32M 10s
    default:   5150K .......... .......... .......... .......... .......... 16% 3.16M 10s
    default:   5200K .......... .......... .......... .......... .......... 17% 3.73M 10s
    default:   5250K .......... .......... .......... .......... .......... 17% 1.81M 10s
    default:   5300K .......... .......... .......... .......... .......... 17% 2.89M 10s
    default:   5350K .......... .......... .......... .......... .......... 17% 3.70M 10s
    default:   5400K .......... .......... .......... .......... .......... 17% 4.08M 10s
    default:   5450K .......... .......... .......... .......... .......... 17% 2.42M 10s
    default:   5500K .......... .......... .......... .......... .......... 18% 1.69M 10s
    default:   5550K .......... .......... .......... .......... .......... 18% 3.49M 10s
    default:   5600K .......... .......... .......... .......... .......... 18% 4.02M 9s
    default:   5650K .......... .......... .......... .......... .......... 18% 2.52M 9s
    default:   5700K .......... .......... .......... .......... .......... 18%  815K 10s
    default:   5750K .......... .......... .......... .......... .......... 18% 13.2M 10s
    default:   5800K .......... .......... .......... .......... .......... 19% 17.6M 9s
    default:   5850K .......... .......... .......... .......... .......... 19% 2.61M 9s
    default:   5900K .......... .......... .......... .......... .......... 19% 2.24M 9s
    default:   5950K .......... .......... .......... .......... .......... 19% 1.75M 9s
    default:   6000K .......... .......... .......... .......... .......... 19% 2.84M 9s
    default:   6050K .......... .......... .......... .......... .......... 19% 2.86M 9s
    default:   6100K .......... .......... .......... .......... .......... 20% 2.88M 9s
    default:   6150K .......... .......... .......... .......... .......... 20% 2.95M 9s
    default:   6200K .......... .......... .......... .......... .......... 20% 2.77M 9s
    default:   6250K .......... .......... .......... .......... .......... 20% 2.30M 9s
    default:   6300K .......... .......... .......... .......... .......... 20% 2.37M 9s
    default:   6350K .......... .......... .......... .......... .......... 20% 2.90M 9s
    default:   6400K .......... .......... .......... .......... .......... 20% 2.99M 9s
    default:   6450K .......... .......... .......... .......... .......... 21% 1.93M 9s
    default:   6500K .......... .......... .......... .......... .......... 21% 3.50M 9s
    default:   6550K .......... .......... .......... .......... .......... 21% 2.34M 9s
    default:   6600K .......... .......... .......... .......... .......... 21% 2.42M 9s
    default:   6650K .......... .......... .......... .......... .......... 21% 3.29M 9s
    default:   6700K .......... .......... .......... .......... .......... 21% 2.28M 9s
    default:   6750K .......... .......... .......... .......... .......... 22% 2.49M 9s
    default:   6800K .......... .......... .......... .......... .......... 22% 2.78M 9s
    default:   6850K .......... .......... .......... .......... .......... 22% 2.27M 9s
    default:   6900K .......... .......... .......... .......... .......... 22% 3.34M 9s
    default:   6950K .......... .......... .......... .......... .......... 22%  900K 9s
    default:   7000K .......... .......... .......... .......... .......... 22% 3.63M 9s
    default:   7050K .......... .......... .......... .......... .......... 23%  852K 9s
    default:   7100K .......... .......... .......... .......... .......... 23% 1.56M 9s
    default:   7150K .......... .......... .......... .......... .......... 23% 3.07M 9s
    default:   7200K .......... .......... .......... .......... .......... 23% 2.44M 9s
    default:   7250K .......... .......... .......... .......... .......... 23% 2.87M 9s
    default:   7300K .......... .......... .......... .......... .......... 23% 3.90M 9s
    default:   7350K .......... .......... .......... .......... .......... 24% 2.78M 9s
    default:   7400K .......... .......... .......... .......... .......... 24% 2.69M 9s
    default:   7450K .......... .......... .......... .......... .......... 24% 2.86M 9s
    default:   7500K .......... .......... .......... .......... .......... 24% 1.89M 9s
    default:   7550K .......... .......... .......... .......... .......... 24% 3.31M 9s
    default:   7600K .......... .......... .......... .......... .......... 24% 2.98M 9s
    default:   7650K .......... .......... .......... .......... .......... 25% 2.78M 9s
    default:   7700K .......... .......... .......... .......... .......... 25% 3.35M 9s
    default:   7750K .......... .......... .......... .......... .......... 25% 2.24M 9s
    default:   7800K .......... .......... .......... .......... .......... 25% 3.73M 9s
    default:   7850K .......... .......... .......... .......... .......... 25% 1001K 9s
    default:   7900K .......... .......... .......... .......... .......... 25% 26.7M 9s
    default:   7950K .......... .......... .......... .......... .......... 26% 3.94M 9s
    default:   8000K .......... .......... .......... .......... .......... 26% 1.38M 9s
    default:   8050K .......... .......... .......... .......... .......... 26% 1.95M 9s
    default:   8100K .......... .......... .......... .......... .......... 26% 2.70M 9s
    default:   8150K .......... .......... .......... .......... .......... 26% 2.32M 9s
    default:   8200K .......... .......... .......... .......... .......... 26% 2.04M 9s
    default:   8250K .......... .......... .......... .......... .......... 26% 2.72M 9s
    default:   8300K .......... .......... .......... .......... .......... 27% 1.33M 9s
    default:   8350K .......... .......... .......... .......... .......... 27% 2.05M 9s
    default:   8400K .......... .......... .......... .......... .......... 27% 3.01M 9s
    default:   8450K .......... .......... .......... .......... .......... 27% 2.17M 9s
    default:   8500K .......... .......... .......... .......... .......... 27% 2.30M 9s
    default:   8550K .......... .......... .......... .......... .......... 27% 2.36M 9s
    default:   8600K .......... .......... .......... .......... .......... 28% 2.01M 9s
    default:   8650K .......... .......... .......... .......... .......... 28% 2.35M 9s
    default:   8700K .......... .......... .......... .......... .......... 28% 2.22M 9s
    default:   8750K .......... .......... .......... .......... .......... 28% 2.45M 9s
    default:   8800K .......... .......... .......... .......... .......... 28% 2.60M 9s
    default:   8850K .......... .......... .......... .......... .......... 28% 3.26M 9s
    default:   8900K .......... .......... .......... .......... .......... 29% 2.27M 9s
    default:   8950K .......... .......... .......... .......... .......... 29% 2.47M 9s
    default:   9000K .......... .......... .......... .......... .......... 29% 2.40M 9s
    default:   9050K .......... .......... .......... .......... .......... 29% 3.08M 9s
    default:   9100K .......... .......... .......... .......... .......... 29% 1.81M 9s
    default:   9150K .......... .......... .......... .......... .......... 29% 2.36M 9s
    default:   9200K .......... .......... .......... .......... .......... 30% 2.27M 9s
    default:   9250K .......... .......... .......... .......... .......... 30% 2.56M 8s
    default:   9300K .......... .......... .......... .......... .......... 30% 2.61M 8s
    default:   9350K .......... .......... .......... .......... .......... 30% 2.13M 8s
    default:   9400K .......... .......... .......... .......... .......... 30% 2.75M 8s
    default:   9450K .......... .......... .......... .......... .......... 30% 1.08M 8s
    default:   9500K .......... .......... .......... .......... .......... 31% 3.69M 8s
    default:   9550K .......... .......... .......... .......... .......... 31% 1.45M 8s
    default:   9600K .......... .......... .......... .......... .......... 31% 3.04M 8s
    default:   9650K .......... .......... .......... .......... .......... 31% 1.96M 8s
    default:   9700K .......... .......... .......... .......... .......... 31% 1.95M 8s
    default:   9750K .......... .......... .......... .......... .......... 31% 2.00M 8s
    default:   9800K .......... .......... .......... .......... .......... 32% 2.19M 8s
    default:   9850K .......... .......... .......... .......... .......... 32% 1.89M 8s
    default:   9900K .......... .......... .......... .......... .......... 32% 1.63M 8s
    default:   9950K .......... .......... .......... .......... .......... 32% 2.01M 8s
    default:  10000K .......... .......... .......... .......... .......... 32% 1.78M 8s
    default:  10050K .......... .......... .......... .......... .......... 32% 2.06M 8s
    default:  10100K .......... .......... .......... .......... .......... 33% 1.94M 8s
    default:  10150K .......... .......... .......... .......... .......... 33% 1.95M 8s
    default:  10200K .......... .......... .......... .......... .......... 33% 2.02M 8s
    default:  10250K .......... .......... .......... .......... .......... 33% 1.96M 8s
    default:  10300K .......... .......... .......... .......... .......... 33% 1.53M 8s
    default:  10350K .......... .......... .......... .......... .......... 33% 1.87M 8s
    default:  10400K .......... .......... .......... .......... .......... 33% 1.69M 8s
    default:  10450K .......... .......... .......... .......... .......... 34% 2.86M 8s
    default:  10500K .......... .......... .......... .......... .......... 34% 2.17M 8s
    default:  10550K .......... .......... .......... .......... .......... 34% 2.59M 8s
    default:  10600K .......... .......... .......... .......... .......... 34% 2.65M 8s
    default:  10650K .......... .......... .......... .......... .......... 34% 2.29M 8s
    default:  10700K .......... .......... .......... .......... .......... 34% 1.80M 8s
    default:  10750K .......... .......... .......... .......... .......... 35% 2.86M 8s
    default:  10800K .......... .......... .......... .......... .......... 35% 2.36M 8s
    default:  10850K .......... .......... .......... .......... .......... 35% 2.40M 8s
    default:  10900K .......... .......... .......... .......... .......... 35% 2.62M 8s
    default:  10950K .......... .......... .......... .......... .......... 35% 2.98M 8s
    default:  11000K .......... .......... .......... .......... .......... 35% 2.21M 8s
    default:  11050K .......... .......... .......... .......... .......... 36% 3.30M 8s
    default:  11100K .......... .......... .......... .......... .......... 36% 1.90M 8s
    default:  11150K .......... .......... .......... .......... .......... 36% 1.89M 8s
    default:  11200K .......... .......... .......... .......... .......... 36% 2.80M 8s
    default:  11250K .......... .......... .......... .......... .......... 36% 2.60M 8s
    default:  11300K .......... .......... .......... .......... .......... 36% 2.62M 8s
    default:  11350K .......... .......... .......... .......... .......... 37% 3.02M 8s
    default:  11400K .......... .......... .......... .......... .......... 37% 2.52M 8s
    default:  11450K .......... .......... .......... .......... .......... 37% 2.85M 8s
    default:  11500K .......... .......... .......... .......... .......... 37% 1.83M 8s
    default:  11550K .......... .......... .......... .......... .......... 37% 2.93M 8s
    default:  11600K .......... .......... .......... .......... .......... 37% 2.34M 8s
    default:  11650K .......... .......... .......... .......... .......... 38% 2.66M 8s
    default:  11700K .......... .......... .......... .......... .......... 38% 2.19M 8s
    default:  11750K .......... .......... .......... .......... .......... 38% 2.71M 8s
    default:  11800K .......... .......... .......... .......... .......... 38% 2.45M 8s
    default:  11850K .......... .......... .......... .......... .......... 38% 2.05M 8s
    default:  11900K .......... .......... .......... .......... .......... 38% 2.29M 8s
    default:  11950K .......... .......... .......... .......... .......... 39% 2.53M 8s
    default:  12000K .......... .......... .......... .......... .......... 39% 2.76M 8s
    default:  12050K .......... .......... .......... .......... .......... 39% 2.62M 8s
    default:  12100K .......... .......... .......... .......... .......... 39% 2.66M 8s
    default:  12150K .......... .......... .......... .......... .......... 39% 2.63M 8s
    default:  12200K .......... .......... .......... .......... .......... 39% 1.86M 8s
    default:  12250K .......... .......... .......... .......... .......... 40% 2.66M 7s
    default:  12300K .......... .......... .......... .......... .......... 40% 1.91M 7s
    default:  12350K .......... .......... .......... .......... .......... 40% 1.29M 7s
    default:  12400K .......... .......... .......... .......... .......... 40% 18.6M 7s
    default:  12450K .......... .......... .......... .......... .......... 40% 1.59M 7s
    default:  12500K .......... .......... .......... .......... .......... 40% 1.82M 7s
    default:  12550K .......... .......... .......... .......... .......... 40% 2.00M 7s
    default:  12600K .......... .......... .......... .......... .......... 41% 2.31M 7s
    default:  12650K .......... .......... .......... .......... .......... 41% 2.14M 7s
    default:  12700K .......... .......... .......... .......... .......... 41% 1.66M 7s
    default:  12750K .......... .......... .......... .......... .......... 41% 2.02M 7s
    default:  12800K .......... .......... .......... .......... .......... 41% 2.30M 7s
    default:  12850K .......... .......... .......... .......... .......... 41% 1.89M 7s
    default:  12900K .......... .......... .......... .......... .......... 42% 2.00M 7s
    default:  12950K .......... .......... .......... .......... .......... 42% 2.15M 7s
    default:  13000K .......... .......... .......... .......... .......... 42% 2.33M 7s
    default:  13050K .......... .......... .......... .......... .......... 42% 1.66M 7s
    default:  13100K .......... .......... .......... .......... .......... 42% 1.69M 7s
    default:  13150K .......... .......... .......... .......... .......... 42% 2.60M 7s
    default:  13200K .......... .......... .......... .......... .......... 43% 2.33M 7s
    default:  13250K .......... .......... .......... .......... .......... 43% 2.61M 7s
    default:  13300K .......... .......... .......... .......... .......... 43% 2.32M 7s
    default:  13350K .......... .......... .......... .......... .......... 43% 2.42M 7s
    default:  13400K .......... .......... .......... .......... .......... 43% 2.59M 7s
    default:  13450K .......... .......... .......... .......... .......... 43% 2.25M 7s
    default:  13500K .......... .......... .......... .......... .......... 44% 1.76M 7s
    default:  13550K .......... .......... .......... .......... .......... 44% 3.01M 7s
    default:  13600K .......... .......... .......... .......... .......... 44% 2.15M 7s
    default:  13650K .......... .......... .......... .......... .......... 44% 2.97M 7s
    default:  13700K .......... .......... .......... .......... .......... 44% 2.19M 7s
    default:  13750K .......... .......... .......... .......... .......... 44% 2.76M 7s
    default:  13800K .......... .......... .......... .......... .......... 45% 2.26M 7s
    default:  13850K .......... .......... .......... .......... .......... 45% 2.80M 7s
    default:  13900K .......... .......... .......... .......... .......... 45% 2.02M 7s
    default:  13950K .......... .......... .......... .......... .......... 45% 2.52M 7s
    default:  14000K .......... .......... .......... .......... .......... 45% 2.73M 7s
    default:  14050K .......... .......... .......... .......... .......... 45% 2.22M 7s
    default:  14100K .......... .......... .......... .......... .......... 46% 1.33M 7s
    default:  14150K .......... .......... .......... .......... .......... 46% 3.13M 7s
    default:  14200K .......... .......... .......... .......... .......... 46% 1.86M 7s
    default:  14250K .......... .......... .......... .......... .......... 46% 3.07M 7s
    default:  14300K .......... .......... .......... .......... .......... 46% 1.97M 7s
    default:  14350K .......... .......... .......... .......... .......... 46%  992K 7s
    default:  14400K .......... .......... .......... .......... .......... 47% 2.34M 7s
    default:  14450K .......... .......... .......... .......... .......... 47% 79.3M 7s
    default:  14500K .......... .......... .......... .......... .......... 47% 1.83M 7s
    default:  14550K .......... .......... .......... .......... .......... 47% 1.75M 7s
    default:  14600K .......... .......... .......... .......... .......... 47% 2.00M 7s
    default:  14650K .......... .......... .......... .......... .......... 47% 1.85M 7s
    default:  14700K .......... .......... .......... .......... .......... 47% 1.49M 7s
    default:  14750K .......... .......... .......... .......... .......... 48% 2.59M 7s
    default:  14800K .......... .......... .......... .......... .......... 48% 2.36M 7s
    default:  14850K .......... .......... .......... .......... .......... 48% 2.21M 7s
    default:  14900K .......... .......... .......... .......... .......... 48% 2.14M 7s
    default:  14950K .......... .......... .......... .......... .......... 48% 2.22M 7s
    default:  15000K .......... .......... .......... .......... .......... 48% 2.05M 7s
    default:  15050K .......... .......... .......... .......... .......... 49% 2.25M 7s
    default:  15100K .......... .......... .......... .......... .......... 49% 1.57M 7s
    default:  15150K .......... .......... .......... .......... .......... 49% 1.53M 6s
    default:  15200K .......... .......... .......... .......... .......... 49% 2.57M 6s
    default:  15250K .......... .......... .......... .......... .......... 49% 2.47M 6s
    default:  15300K .......... .......... .......... .......... .......... 49% 2.15M 6s
    default:  15350K .......... .......... .......... .......... .......... 50% 2.32M 6s
    default:  15400K .......... .......... .......... .......... .......... 50% 2.48M 6s
    default:  15450K .......... .......... .......... .......... .......... 50% 2.84M 6s
    default:  15500K .......... .......... .......... .......... .......... 50% 1.89M 6s
    default:  15550K .......... .......... .......... .......... .......... 50% 2.76M 6s
    default:  15600K .......... .......... .......... .......... .......... 50% 2.37M 6s
    default:  15650K .......... .......... .......... .......... .......... 51% 2.45M 6s
    default:  15700K .......... .......... .......... .......... .......... 51% 2.93M 6s
    default:  15750K .......... .......... .......... .......... .......... 51% 2.31M 6s
    default:  15800K .......... .......... .......... .......... .......... 51% 1.76M 6s
    default:  15850K .......... .......... .......... .......... .......... 51% 4.08M 6s
    default:  15900K .......... .......... .......... .......... .......... 51% 1.90M 6s
    default:  15950K .......... .......... .......... .......... .......... 52% 2.63M 6s
    default:  16000K .......... .......... .......... .......... .......... 52% 2.53M 6s
    default:  16050K .......... .......... .......... .......... .......... 52% 2.17M 6s
    default:  16100K .......... .......... .......... .......... .......... 52% 3.38M 6s
    default:  16150K .......... .......... .......... .......... .......... 52% 1.57M 6s
    default:  16200K .......... .......... .......... .......... .......... 52% 4.97M 6s
    default:  16250K .......... .......... .......... .......... .......... 53% 2.16M 6s
    default:  16300K .......... .......... .......... .......... .......... 53% 2.00M 6s
    default:  16350K .......... .......... .......... .......... .......... 53% 3.45M 6s
    default:  16400K .......... .......... .......... .......... .......... 53% 2.36M 6s
    default:  16450K .......... .......... .......... .......... .......... 53% 3.18M 6s
    default:  16500K .......... .......... .......... .......... .......... 53% 2.17M 6s
    default:  16550K .......... .......... .......... .......... .......... 53% 3.60M 6s
    default:  16600K .......... .......... .......... .......... .......... 54% 2.21M 6s
    default:  16650K .......... .......... .......... .......... .......... 54% 2.96M 6s
    default:  16700K .......... .......... .......... .......... .......... 54% 2.02M 6s
    default:  16750K .......... .......... .......... .......... .......... 54% 2.56M 6s
    default:  16800K .......... .......... .......... .......... .......... 54% 2.63M 6s
    default:  16850K .......... .......... .......... .......... .......... 54% 2.43M 6s
    default:  16900K .......... .......... .......... .......... .......... 55% 2.41M 6s
    default:  16950K .......... .......... .......... .......... .......... 55% 2.52M 6s
    default:  17000K .......... .......... .......... .......... .......... 55% 2.70M 6s
    default:  17050K .......... .......... .......... .......... .......... 55% 2.79M 6s
    default:  17100K .......... .......... .......... .......... .......... 55% 2.07M 6s
    default:  17150K .......... .......... .......... .......... .......... 55% 2.53M 6s
    default:  17200K .......... .......... .......... .......... .......... 56% 2.90M 6s
    default:  17250K .......... .......... .......... .......... .......... 56% 3.30M 6s
    default:  17300K .......... .......... .......... .......... .......... 56% 2.56M 6s
    default:  17350K .......... .......... .......... .......... .......... 56% 3.06M 6s
    default:  17400K .......... .......... .......... .......... .......... 56% 2.51M 6s
    default:  17450K .......... .......... .......... .......... .......... 56% 3.22M 5s
    default:  17500K .......... .......... .......... .......... .......... 57% 1.96M 5s
    default:  17550K .......... .......... .......... .......... .......... 57% 3.89M 5s
    default:  17600K .......... .......... .......... .......... .......... 57% 2.28M 5s
    default:  17650K .......... .......... .......... .......... .......... 57% 3.53M 5s
    default:  17700K .......... .......... .......... .......... .......... 57% 2.43M 5s
    default:  17750K .......... .......... .......... .......... .......... 57% 3.66M 5s
    default:  17800K .......... .......... .......... .......... .......... 58% 2.19M 5s
    default:  17850K .......... .......... .......... .......... .......... 58% 2.78M 5s
    default:  17900K .......... .......... .......... .......... .......... 58% 2.74M 5s
    default:  17950K .......... .......... .......... .......... .......... 58% 2.88M 5s
    default:  18000K .......... .......... .......... .......... .......... 58% 2.34M 5s
    default:  18050K .......... .......... .......... .......... .......... 58% 2.93M 5s
    default:  18100K .......... .......... .......... .......... .......... 59% 2.26M 5s
    default:  18150K .......... .......... .......... .......... .......... 59% 3.51M 5s
    default:  18200K .......... .......... .......... .......... .......... 59% 3.65M 5s
    default:  18250K .......... .......... .......... .......... .......... 59% 1.92M 5s
    default:  18300K .......... .......... .......... .......... .......... 59% 2.40M 5s
    default:  18350K .......... .......... .......... .......... .......... 59% 3.09M 5s
    default:  18400K .......... .......... .......... .......... .......... 60% 2.11M 5s
    default:  18450K .......... .......... .......... .......... .......... 60% 2.81M 5s
    default:  18500K .......... .......... .......... .......... .......... 60% 3.44M 5s
    default:  18550K .......... .......... .......... .......... .......... 60% 1.83M 5s
    default:  18600K .......... .......... .......... .......... .......... 60% 2.97M 5s
    default:  18650K .......... .......... .......... .......... .......... 60% 3.61M 5s
    default:  18700K .......... .......... .......... .......... .......... 60% 1.93M 5s
    default:  18750K .......... .......... .......... .......... .......... 61% 3.52M 5s
    default:  18800K .......... .......... .......... .......... .......... 61% 2.09M 5s
    default:  18850K .......... .......... .......... .......... .......... 61% 1.95M 5s
    default:  18900K .......... .......... .......... .......... .......... 61% 3.59M 5s
    default:  18950K .......... .......... .......... .......... .......... 61% 2.02M 5s
    default:  19000K .......... .......... .......... .......... .......... 61% 3.56M 5s
    default:  19050K .......... .......... .......... .......... .......... 62% 3.53M 5s
    default:  19100K .......... .......... .......... .......... .......... 62% 2.78M 5s
    default:  19150K .......... .......... .......... .......... .......... 62% 2.10M 5s
    default:  19200K .......... .......... .......... .......... .......... 62% 3.89M 5s
    default:  19250K .......... .......... .......... .......... .......... 62% 2.80M 5s
    default:  19300K .......... .......... .......... .......... .......... 62% 2.14M 5s
    default:  19350K .......... .......... .......... .......... .......... 63% 3.21M 5s
    default:  19400K .......... .......... .......... .......... .......... 63% 3.41M 5s
    default:  19450K .......... .......... .......... .......... .......... 63% 1.98M 5s
    default:  19500K .......... .......... .......... .......... .......... 63% 2.31M 5s
    default:  19550K .......... .......... .......... .......... .......... 63% 3.28M 5s
    default:  19600K .......... .......... .......... .......... .......... 63% 2.95M 5s
    default:  19650K .......... .......... .......... .......... .......... 64% 2.77M 5s
    default:  19700K .......... .......... .......... .......... .......... 64% 3.03M 4s
    default:  19750K .......... .......... .......... .......... .......... 64% 3.32M 4s
    default:  19800K .......... .......... .......... .......... .......... 64% 2.80M 4s
    default:  19850K .......... .......... .......... .......... .......... 64% 2.90M 4s
    default:  19900K .......... .......... .......... .......... .......... 64% 2.74M 4s
    default:  19950K .......... .......... .......... .......... .......... 65% 2.50M 4s
    default:  20000K .......... .......... .......... .......... .......... 65% 3.62M 4s
    default:  20050K .......... .......... .......... .......... .......... 65% 2.87M 4s
    default:  20100K .......... .......... .......... .......... .......... 65% 1.93M 4s
    default:  20150K .......... .......... .......... .......... .......... 65% 3.47M 4s
    default:  20200K .......... .......... .......... .......... .......... 65% 4.26M 4s
    default:  20250K .......... .......... .......... .......... .......... 66% 1.50M 4s
    default:  20300K .......... .......... .......... .......... .......... 66% 3.06M 4s
    default:  20350K .......... .......... .......... .......... .......... 66% 3.46M 4s
    default:  20400K .......... .......... .......... .......... .......... 66% 3.15M 4s
    default:  20450K .......... .......... .......... .......... .......... 66% 2.62M 4s
    default:  20500K .......... .......... .......... .......... .......... 66% 3.30M 4s
    default:  20550K .......... .......... .......... .......... .......... 67% 2.31M 4s
    default:  20600K .......... .......... .......... .......... .......... 67% 3.84M 4s
    default:  20650K .......... .......... .......... .......... .......... 67% 3.10M 4s
    default:  20700K .......... .......... .......... .......... .......... 67% 2.60M 4s
    default:  20750K .......... .......... .......... .......... .......... 67% 2.82M 4s
    default:  20800K .......... .......... .......... .......... .......... 67% 3.72M 4s
    default:  20850K .......... .......... .......... .......... .......... 67% 2.88M 4s
    default:  20900K .......... .......... .......... .......... .......... 68% 2.69M 4s
    default:  20950K .......... .......... .......... .......... .......... 68% 3.23M 4s
    default:  21000K .......... .......... .......... .......... .......... 68% 2.72M 4s
    default:  21050K .......... .......... .......... .......... .......... 68% 2.72M 4s
    default:  21100K .......... .......... .......... .......... .......... 68% 2.80M 4s
    default:  21150K .......... .......... .......... .......... .......... 68% 2.93M 4s
    default:  21200K .......... .......... .......... .......... .......... 69% 3.95M 4s
    default:  21250K .......... .......... .......... .......... .......... 69% 2.71M 4s
    default:  21300K .......... .......... .......... .......... .......... 69% 1.82M 4s
    default:  21350K .......... .......... .......... .......... .......... 69% 4.13M 4s
    default:  21400K .......... .......... .......... .......... .......... 69% 3.92M 4s
    default:  21450K .......... .......... .......... .......... .......... 69% 1.58M 4s
    default:  21500K .......... .......... .......... .......... .......... 70% 2.85M 4s
    default:  21550K .......... .......... .......... .......... .......... 70% 4.27M 4s
    default:  21600K .......... .......... .......... .......... .......... 70% 1.55M 4s
    default:  21650K .......... .......... .......... .......... .......... 70% 3.99M 4s
    default:  21700K .......... .......... .......... .......... .......... 70% 3.74M 4s
    default:  21750K .......... .......... .......... .......... .......... 70% 2.88M 4s
    default:  21800K .......... .......... .......... .......... .......... 71% 1.78M 4s
    default:  21850K .......... .......... .......... .......... .......... 71% 3.82M 4s
    default:  21900K .......... .......... .......... .......... .......... 71% 2.93M 4s
    default:  21950K .......... .......... .......... .......... .......... 71% 1.98M 4s
    default:  22000K .......... .......... .......... .......... .......... 71% 2.98M 4s
    default:  22050K .......... .......... .......... .......... .......... 71% 4.00M 3s
    default:  22100K .......... .......... .......... .......... .......... 72% 3.83M 3s
    default:  22150K .......... .......... .......... .......... .......... 72% 1.75M 3s
    default:  22200K .......... .......... .......... .......... .......... 72% 3.21M 3s
    default:  22250K .......... .......... .......... .......... .......... 72% 4.14M 3s
    default:  22300K .......... .......... .......... .......... .......... 72% 1.36M 3s
    default:  22350K .......... .......... .......... .......... .......... 72% 3.73M 3s
    default:  22400K .......... .......... .......... .......... .......... 73% 3.35M 3s
    default:  22450K .......... .......... .......... .......... .......... 73% 3.07M 3s
    default:  22500K .......... .......... .......... .......... .......... 73% 4.40M 3s
    default:  22550K .......... .......... .......... .......... .......... 73% 2.78M 3s
    default:  22600K .......... .......... .......... .......... .......... 73% 1.79M 3s
    default:  22650K .......... .......... .......... .......... .......... 73% 3.56M 3s
    default:  22700K .......... .......... .......... .......... .......... 73% 2.41M 3s
    default:  22750K .......... .......... .......... .......... .......... 74% 2.07M 3s
    default:  22800K .......... .......... .......... .......... .......... 74% 4.02M 3s
    default:  22850K .......... .......... .......... .......... .......... 74% 4.30M 3s
    default:  22900K .......... .......... .......... .......... .......... 74% 1.49M 3s
    default:  22950K .......... .......... .......... .......... .......... 74% 3.54M 3s
    default:  23000K .......... .......... .......... .......... .......... 74% 3.99M 3s
    default:  23050K .......... .......... .......... .......... .......... 75% 3.51M 3s
    default:  23100K .......... .......... .......... .......... .......... 75% 1.25M 3s
    default:  23150K .......... .......... .......... .......... .......... 75% 3.23M 3s
    default:  23200K .......... .......... .......... .......... .......... 75% 4.21M 3s
    default:  23250K .......... .......... .......... .......... .......... 75% 3.98M 3s
    default:  23300K .......... .......... .......... .......... .......... 75% 1.74M 3s
    default:  23350K .......... .......... .......... .......... .......... 76% 2.92M 3s
    default:  23400K .......... .......... .......... .......... .......... 76% 4.33M 3s
    default:  23450K .......... .......... .......... .......... .......... 76% 3.99M 3s
    default:  23500K .......... .......... .......... .......... .......... 76% 1.17M 3s
    default:  23550K .......... .......... .......... .......... .......... 76% 5.83M 3s
    default:  23600K .......... .......... .......... .......... .......... 76% 3.36M 3s
    default:  23650K .......... .......... .......... .......... .......... 77% 2.23M 3s
    default:  23700K .......... .......... .......... .......... .......... 77% 2.45M 3s
    default:  23750K .......... .......... .......... .......... .......... 77% 3.75M 3s
    default:  23800K .......... .......... .......... .......... .......... 77% 3.96M 3s
    default:  23850K .......... .......... .......... .......... .......... 77% 2.47M 3s
    default:  23900K .......... .......... .......... .......... .......... 77% 1.80M 3s
    default:  23950K .......... .......... .......... .......... .......... 78% 4.17M 3s
    default:  24000K .......... .......... .......... .......... .......... 78% 3.88M 3s
    default:  24050K .......... .......... .......... .......... .......... 78% 1.71M 3s
    default:  24100K .......... .......... .......... .......... .......... 78% 3.77M 3s
    default:  24150K .......... .......... .......... .......... .......... 78% 3.27M 3s
    default:  24200K .......... .......... .......... .......... .......... 78% 4.64M 3s
    default:  24250K .......... .......... .......... .......... .......... 79% 1.49M 3s
    default:  24300K .......... .......... .......... .......... .......... 79% 2.88M 3s
    default:  24350K .......... .......... .......... .......... .......... 79% 3.96M 3s
    default:  24400K .......... .......... .......... .......... .......... 79% 4.25M 3s
    default:  24450K .......... .......... .......... .......... .......... 79% 1.42M 2s
    default:  24500K .......... .......... .......... .......... .......... 79% 4.20M 2s
    default:  24550K .......... .......... .......... .......... .......... 80% 3.62M 2s
    default:  24600K .......... .......... .......... .......... .......... 80% 4.10M 2s
    default:  24650K .......... .......... .......... .......... .......... 80% 1.68M 2s
    default:  24700K .......... .......... .......... .......... .......... 80% 2.52M 2s
    default:  24750K .......... .......... .......... .......... .......... 80% 3.77M 2s
    default:  24800K .......... .......... .......... .......... .......... 80% 2.37M 2s
    default:  24850K .......... .......... .......... .......... .......... 80% 1.30M 2s
    default:  24900K .......... .......... .......... .......... .......... 81% 4.11M 2s
    default:  24950K .......... .......... .......... .......... .......... 81% 4.02M 2s
    default:  25000K .......... .......... .......... .......... .......... 81% 1.75M 2s
    default:  25050K .......... .......... .......... .......... .......... 81% 2.87M 2s
    default:  25100K .......... .......... .......... .......... .......... 81% 2.97M 2s
    default:  25150K .......... .......... .......... .......... .......... 81% 3.26M 2s
    default:  25200K .......... .......... .......... .......... .......... 82% 2.44M 2s
    default:  25250K .......... .......... .......... .......... .......... 82% 3.54M 2s
    default:  25300K .......... .......... .......... .......... .......... 82% 3.55M 2s
    default:  25350K .......... .......... .......... .......... .......... 82% 2.91M 2s
    default:  25400K .......... .......... .......... .......... .......... 82% 1.80M 2s
    default:  25450K .......... .......... .......... .......... .......... 82% 4.51M 2s
    default:  25500K .......... .......... .......... .......... .......... 83% 2.73M 2s
    default:  25550K .......... .......... .......... .......... .......... 83% 2.42M 2s
    default:  25600K .......... .......... .......... .......... .......... 83% 2.58M 2s
    default:  25650K .......... .......... .......... .......... .......... 83% 4.28M 2s
    default:  25700K .......... .......... .......... .......... .......... 83% 3.85M 2s
    default:  25750K .......... .......... .......... .......... .......... 83% 2.44M 2s
    default:  25800K .......... .......... .......... .......... .......... 84% 2.19M 2s
    default:  25850K .......... .......... .......... .......... .......... 84% 3.46M 2s
    default:  25900K .......... .......... .......... .......... .......... 84% 3.14M 2s
    default:  25950K .......... .......... .......... .......... .......... 84% 1.94M 2s
    default:  26000K .......... .......... .......... .......... .......... 84% 2.79M 2s
    default:  26050K .......... .......... .......... .......... .......... 84% 2.95M 2s
    default:  26100K .......... .......... .......... .......... .......... 85% 4.07M 2s
    default:  26150K .......... .......... .......... .......... .......... 85% 4.44M 2s
    default:  26200K .......... .......... .......... .......... .......... 85% 1.39M 2s
    default:  26250K .......... .......... .......... .......... .......... 85% 3.57M 2s
    default:  26300K .......... .......... .......... .......... .......... 85% 2.81M 2s
    default:  26350K .......... .......... .......... .......... .......... 85% 4.12M 2s
    default:  26400K .......... .......... .......... .......... .......... 86% 2.13M 2s
    default:  26450K .......... .......... .......... .......... .......... 86% 3.30M 2s
    default:  26500K .......... .......... .......... .......... .......... 86% 3.24M 2s
    default:  26550K .......... .......... .......... .......... .......... 86% 4.29M 2s
    default:  26600K .......... .......... .......... .......... .......... 86% 2.25M 2s
    default:  26650K .......... .......... .......... .......... .......... 86% 2.63M 2s
    default:  26700K .......... .......... .......... .......... .......... 87% 3.90M 2s
    default:  26750K .......... .......... .......... .......... .......... 87% 3.11M 2s
    default:  26800K .......... .......... .......... .......... .......... 87% 1.42M 2s
    default:  26850K .......... .......... .......... .......... .......... 87% 3.08M 2s
    default:  26900K .......... .......... .......... .......... .......... 87% 3.57M 1s
    default:  26950K .......... .......... .......... .......... .......... 87% 3.77M 1s
    default:  27000K .......... .......... .......... .......... .......... 87% 4.08M 1s
    default:  27050K .......... .......... .......... .......... .......... 88% 1.71M 1s
    default:  27100K .......... .......... .......... .......... .......... 88% 2.47M 1s
    default:  27150K .......... .......... .......... .......... .......... 88% 4.59M 1s
    default:  27200K .......... .......... .......... .......... .......... 88% 3.61M 1s
    default:  27250K .......... .......... .......... .......... .......... 88% 2.69M 1s
    default:  27300K .......... .......... .......... .......... .......... 88% 2.09M 1s
    default:  27350K .......... .......... .......... .......... .......... 89% 2.47M 1s
    default:  27400K .......... .......... .......... .......... .......... 89% 12.8M 1s
    default:  27450K .......... .......... .......... .......... .......... 89% 1.69M 1s
    default:  27500K .......... .......... .......... .......... .......... 89% 2.54M 1s
    default:  27550K .......... .......... .......... .......... .......... 89% 4.09M 1s
    default:  27600K .......... .......... .......... .......... .......... 89% 3.86M 1s
    default:  27650K .......... .......... .......... .......... .......... 90% 2.16M 1s
    default:  27700K .......... .......... .......... .......... .......... 90% 2.17M 1s
    default:  27750K .......... .......... .......... .......... .......... 90% 3.79M 1s
    default:  27800K .......... .......... .......... .......... .......... 90% 3.65M 1s
    default:  27850K .......... .......... .......... .......... .......... 90% 4.37M 1s
    default:  27900K .......... .......... .......... .......... .......... 90% 1.57M 1s
    default:  27950K .......... .......... .......... .......... .......... 91% 3.83M 1s
    default:  28000K .......... .......... .......... .......... .......... 91% 3.69M 1s
    default:  28050K .......... .......... .......... .......... .......... 91% 4.21M 1s
    default:  28100K .......... .......... .......... .......... .......... 91% 3.88M 1s
    default:  28150K .......... .......... .......... .......... .......... 91% 1.33M 1s
    default:  28200K .......... .......... .......... .......... .......... 91% 3.70M 1s
    default:  28250K .......... .......... .......... .......... .......... 92% 3.56M 1s
    default:  28300K .......... .......... .......... .......... .......... 92% 2.91M 1s
    default:  28350K .......... .......... .......... .......... .......... 92% 4.27M 1s
    default:  28400K .......... .......... .......... .......... .......... 92% 1.85M 1s
    default:  28450K .......... .......... .......... .......... .......... 92% 3.20M 1s
    default:  28500K .......... .......... .......... .......... .......... 92% 3.16M 1s
    default:  28550K .......... .......... .......... .......... .......... 93% 3.82M 1s
    default:  28600K .......... .......... .......... .......... .......... 93% 3.88M 1s
    default:  28650K .......... .......... .......... .......... .......... 93% 4.36M 1s
    default:  28700K .......... .......... .......... .......... .......... 93% 1.39M 1s
    default:  28750K .......... .......... .......... .......... .......... 93% 3.07M 1s
    default:  28800K .......... .......... .......... .......... .......... 93% 4.20M 1s
    default:  28850K .......... .......... .......... .......... .......... 94% 3.55M 1s
    default:  28900K .......... .......... .......... .......... .......... 94% 3.29M 1s
    default:  28950K .......... .......... .......... .......... .......... 94% 2.87M 1s
    default:  29000K .......... .......... .......... .......... .......... 94% 2.05M 1s
    default:  29050K .......... .......... .......... .......... .......... 94% 3.81M 1s
    default:  29100K .......... .......... .......... .......... .......... 94% 2.80M 1s
    default:  29150K .......... .......... .......... .......... .......... 94% 3.15M 1s
    default:  29200K .......... .......... .......... .......... .......... 95% 2.63M 1s
    default:  29250K .......... .......... .......... .......... .......... 95% 3.14M 1s
    default:  29300K .......... .......... .......... .......... .......... 95% 3.60M 1s
    default:  29350K .......... .......... .......... .......... .......... 95% 3.56M 1s
    default:  29400K .......... .......... .......... .......... .......... 95% 4.42M 1s
    default:  29450K .......... .......... .......... .......... .......... 95% 1.86M 0s
    default:  29500K .......... .......... .......... .......... .......... 96% 2.40M 0s
    default:  29550K .......... .......... .......... .......... .......... 96% 3.92M 0s
    default:  29600K .......... .......... .......... .......... .......... 96% 4.63M 0s
    default:  29650K .......... .......... .......... .......... .......... 96% 4.09M 0s
    default:  29700K .......... .......... .......... .......... .......... 96% 1.61M 0s
    default:  29750K .......... .......... .......... .......... .......... 96% 3.44M 0s
    default:  29800K .......... .......... .......... .......... .......... 97% 3.84M 0s
    default:  29850K .......... .......... .......... .......... .......... 97% 3.83M 0s
    default:  29900K .......... .......... .......... .......... .......... 97% 1.72M 0s
    default:  29950K .......... .......... .......... .......... .......... 97% 3.42M 0s
    default:  30000K .......... .......... .......... .......... .......... 97% 3.67M 0s
    default:  30050K .......... .......... .......... .......... .......... 97% 4.19M 0s
    default:  30100K .......... .......... .......... .......... .......... 98% 3.28M 0s
    default:  30150K .......... .......... .......... .......... .......... 98% 2.07M 0s
    default:  30200K .......... .......... .......... .......... .......... 98% 2.54M 0s
    default:  30250K .......... .......... .......... .......... .......... 98% 3.74M 0s
    default:  30300K .......... .......... .......... .......... .......... 98% 3.08M 0s
    default:  30350K .......... .......... .......... .......... .......... 98% 2.30M 0s
    default:  30400K .......... .......... .......... .......... .......... 99% 3.08M 0s
    default:  30450K .......... .......... .......... .......... .......... 99% 2.69M 0s
    default:  30500K .......... .......... .......... .......... .......... 99% 4.05M 0s
    default:  30550K .......... .......... .......... .......... .......... 99% 3.78M 0s
    default:  30600K .......... .......... .......... .......... .......... 99% 4.21M 0s
    default:  30650K .......... .......... .......... .......... .......... 99% 1.81M 0s
    default:  30700K .......... .......... .......... .......... ...       100% 2.93M=12s
    default:
    default: 2023-12-26 20:07:26 (2.52 MB/s) - ‘k9s_linux_amd64.rpm’ saved [31481543/31481543]
    default:
    default: Verifying...                          ########################################
    default: Preparing...                          ########################################
    default: Updating / installing...
    default: k9s-0:0.29.1-1                        ########################################
    default:  ____  __.________
    default: |    |/ _/   __   \______
    default: |      < \____    /  ___/
    default: |    |  \   /    /\___ \
    default: |____|__ \ /____//____  >
    default:         \/            \/
    default:
    default: Configuration:   /home/vagrant/.config/k9s/config.yml
    default: Logs:            /tmp/k9s-vagrant.log
    default: Screen Dumps:    /tmp/k9s-screens-vagrant
    default: Creating cluster "kind" ...
    default:  • Ensuring node image (kindest/node:v1.27.3) 🖼  ...
    default:  ✓ Ensuring node image (kindest/node:v1.27.3) 🖼
    default:  • Preparing nodes 📦   ...
    default:  ✓ Preparing nodes 📦
    default:  • Writing configuration 📜  ...
    default:  ✓ Writing configuration 📜
    default:  • Starting control-plane 🕹️  ...
    default:  ✓ Starting control-plane 🕹️
    default:  • Installing CNI 🔌  ...
    default:  ✓ Installing CNI 🔌
    default:  • Installing StorageClass 💾  ...
    default:  ✓ Installing StorageClass 💾
    default:  • Waiting ≤ 5m0s for control-plane = Ready ⏳  ...
    default:  ✓ Waiting ≤ 5m0s for control-plane = Ready ⏳
    default:  • Ready after 21s 💚
    default: Set kubectl context to "kind-kind"
    default: You can now use your cluster with:
    default:
    default: kubectl cluster-info --context kind-kind
    default:
    default: Thanks for using kind! 😊
    default: serviceaccount/metrics-server created
    default: clusterrole.rbac.authorization.k8s.io/system:aggregated-metrics-reader created
    default: clusterrole.rbac.authorization.k8s.io/system:metrics-server created
    default: rolebinding.rbac.authorization.k8s.io/metrics-server-auth-reader created
    default: clusterrolebinding.rbac.authorization.k8s.io/metrics-server:system:auth-delegator created
    default: clusterrolebinding.rbac.authorization.k8s.io/system:metrics-server created
    default: service/metrics-server created
    default: deployment.apps/metrics-server created
    default: apiservice.apiregistration.k8s.io/v1beta1.metrics.k8s.io created
    default: pod/metrics-server-75f45b4dd4-5g6bb condition met
    default: NAME                 CPU(cores)   CPU%   MEMORY(bytes)   MEMORY%
    default: kind-control-plane   116m         3%     616Mi           7%
    default: NAMESPACE            NAME                                         CPU(cores)   MEMORY(bytes)
    default: kube-system          coredns-5d78c9869d-snq6j                     2m           13Mi
    default: kube-system          coredns-5d78c9869d-x7c8b                     2m           13Mi
    default: kube-system          etcd-kind-control-plane                      21m          29Mi
    default: kube-system          kindnet-7b4t8                                1m           8Mi
    default: kube-system          kube-apiserver-kind-control-plane            40m          253Mi
    default: kube-system          kube-controller-manager-kind-control-plane   13m          45Mi
    default: kube-system          kube-proxy-pcbp5                             1m           13Mi
    default: kube-system          kube-scheduler-kind-control-plane            4m           18Mi
    default: kube-system          metrics-server-75f45b4dd4-5g6bb              5m           18Mi
    default: local-path-storage   local-path-provisioner-6bc4bddd6b-97jfw      1m           8Mi
    default: namespace/awx created
    default: customresourcedefinition.apiextensions.k8s.io/awxbackups.awx.ansible.com created
    default: customresourcedefinition.apiextensions.k8s.io/awxrestores.awx.ansible.com created
    default: customresourcedefinition.apiextensions.k8s.io/awxs.awx.ansible.com created
    default: serviceaccount/awx-operator-controller-manager created
    default: role.rbac.authorization.k8s.io/awx-operator-awx-manager-role created
    default: role.rbac.authorization.k8s.io/awx-operator-leader-election-role created
    default: clusterrole.rbac.authorization.k8s.io/awx-operator-metrics-reader created
    default: clusterrole.rbac.authorization.k8s.io/awx-operator-proxy-role created
    default: rolebinding.rbac.authorization.k8s.io/awx-operator-awx-manager-rolebinding created
    default: rolebinding.rbac.authorization.k8s.io/awx-operator-leader-election-rolebinding created
    default: clusterrolebinding.rbac.authorization.k8s.io/awx-operator-proxy-rolebinding created
    default: configmap/awx-operator-awx-manager-config created
    default: service/awx-operator-controller-manager-metrics-service created
    default: deployment.apps/awx-operator-controller-manager created
    default: pod/awx-operator-controller-manager-58566bb44b-lzwn5 condition met
    default: namespace/awx unchanged
    default: customresourcedefinition.apiextensions.k8s.io/awxbackups.awx.ansible.com unchanged
    default: customresourcedefinition.apiextensions.k8s.io/awxrestores.awx.ansible.com unchanged
    default: customresourcedefinition.apiextensions.k8s.io/awxs.awx.ansible.com unchanged
    default: serviceaccount/awx-operator-controller-manager unchanged
    default: role.rbac.authorization.k8s.io/awx-operator-awx-manager-role configured
    default: role.rbac.authorization.k8s.io/awx-operator-leader-election-role unchanged
    default: clusterrole.rbac.authorization.k8s.io/awx-operator-metrics-reader unchanged
    default: clusterrole.rbac.authorization.k8s.io/awx-operator-proxy-role unchanged
    default: rolebinding.rbac.authorization.k8s.io/awx-operator-awx-manager-rolebinding unchanged
    default: rolebinding.rbac.authorization.k8s.io/awx-operator-leader-election-rolebinding unchanged
    default: clusterrolebinding.rbac.authorization.k8s.io/awx-operator-proxy-rolebinding unchanged
    default: configmap/awx-operator-awx-manager-config unchanged
    default: service/awx-operator-controller-manager-metrics-service unchanged
    default: deployment.apps/awx-operator-controller-manager unchanged
    default: awx.awx.ansible.com/awx created
    default: pod/awx-web-55ddd9d4c4-lp2nm condition met
    default: namespace/ingress-nginx created
    default: serviceaccount/ingress-nginx created
    default: serviceaccount/ingress-nginx-admission created
    default: role.rbac.authorization.k8s.io/ingress-nginx created
    default: role.rbac.authorization.k8s.io/ingress-nginx-admission created
    default: clusterrole.rbac.authorization.k8s.io/ingress-nginx created
    default: clusterrole.rbac.authorization.k8s.io/ingress-nginx-admission created
    default: rolebinding.rbac.authorization.k8s.io/ingress-nginx created
    default: rolebinding.rbac.authorization.k8s.io/ingress-nginx-admission created
    default: clusterrolebinding.rbac.authorization.k8s.io/ingress-nginx created
    default: clusterrolebinding.rbac.authorization.k8s.io/ingress-nginx-admission created
    default: configmap/ingress-nginx-controller created
    default: service/ingress-nginx-controller created
    default: service/ingress-nginx-controller-admission created
    default: deployment.apps/ingress-nginx-controller created
    default: job.batch/ingress-nginx-admission-create created
    default: job.batch/ingress-nginx-admission-patch created
    default: ingressclass.networking.k8s.io/nginx created
    default: validatingwebhookconfiguration.admissionregistration.k8s.io/ingress-nginx-admission created
    default: pod/ingress-nginx-controller-864894d997-4skqf condition met
    default: ingress.networking.k8s.io/ingress-for-awx created
    default: Name:             ingress-for-awx
    default: Labels:           <none>
    default: Namespace:        awx
    default: Address:
    default: Ingress Class:    <none>
    default: Default backend:  <default>
    default: Rules:
    default:   Host        Path  Backends
    default:   ----        ----  --------
    default:   *
    default:               /   awx-service:80 (10.244.0.10:8052)
    default: Annotations:  nginx.ingress.kubernetes.io/rewrite-target: /
    default: Events:
    default:   Type    Reason  Age   From                      Message
    default:   ----    ------  ----  ----                      -------
    default:   Normal  Sync    1s    nginx-ingress-controller  Scheduled for sync
    default:   % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
    default:                                  Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:--  0:00:02 --:--:--     0
    default:   % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
    default:                                  Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:--  0:00:02 --:--:--     0
    default: WEB interface of AWX is available from the host machine
    default: http://192.168.33.10/
    default: OR
    default: https://192.168.33.10/
    default: The password for the AWX admin user (default username is admin)
    default: HrlhrtU2WLXqvfQxYLGDGutquhTcwRD9
    default: FINISH

C:\Users\Admin\awx>


```


