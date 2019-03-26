kaios64 v1.1
============

Small, customizable 64-bit Linux distribution aimed towards projects that need a small OS. Currently the initramfs and kernel are 14Mb. This project is the original KaiOS and has nothing to do with the phone operation system. Please do not contact me for any phone support. 

ATTENTION: Please note this is not the same KaiOS that is being used on mobile devices. The KaiOS that is found on mobile devices is a port of Firefox OS and has is unrelated to this project.

Note:
PXE boot support only at this moment.

Features:

-64-bit Kernel and binaries
-Networking support
-OpenSSH client and server support
-udhcpc support (Busybox DHCP Client)

Login:
Terminal screen has no authentication. SSH login authentication:

username: root
password: kaios

PXE Boot Instructions:

Add the following to /tftpboot/pxelinux.cfg/default:

timeout 20
default KaiOS64v1.1
label KaiOS64v1.1
kernel kaios64/kernel/kaios1.0-stable
append initrd=kaios64/initramfs/kaios.igz rw shell
