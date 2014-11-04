kaios64 v1.1
=====

Small, customizable 64-bit Linux distribution aimed towards projects that need a small OS. Currently the initramfs and kernel are 14Mb.

Note:
PXE boot support only at this moment.

Features:

  64-bit Kernel and binaries
  Networking support
  OpenSSH client and server support
  udhcpc support (Busybox DHCP Client)

Login:

Terminal screen has no authentication. SSH login authentication:

username: root

password: kaios

64 Bit PXE Boot Instructions:

Download kaiOS and extract to the following directory:
tar zxvf kaio64PXE-v1.1.tar.gz -C /tftpboot

Add the following to /tftpboot/pxelinux.cfg/default:

timeout 20

default KaiOS64v1.1

label KaiOS64v1.1

kernel kaios64/kernel/kaios1.0-stable

append initrd=kaios64/initramfs/kaios.igz rw shell
