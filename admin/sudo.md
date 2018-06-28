## sudo install in FreeBSD

FreeBSD does support sudo it's likely just not installed by default. 
Installation instructions are here, titled: FreeBSD: Install sudo Command To Execute A Command As The Root.

As root:

FreeBSD < 10

# pkg_add -r sudo
FreeBSD 10+

# pkg install sudo
The default sudoers file is located here: /usr/local/etc/sudoers. 
To edit it and add rules you need to use the visudo command.

$ su -
$ visudo
Then to give a user access to everything as root:

userX ALL=(ALL) ALL
To become root (as userX):

$ sudo -s
-or-
$ sudo -i
