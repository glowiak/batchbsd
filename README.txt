BATCHBSD - BSD WROTEN IN WINDOWS NOTEPAD

COMMANDS:
tofile - write text to file
pack_add - install packages
verb - System version
clear - clear screen
exit - turn off BatchBSD
remove - remove file
cp - copy file
help - get help
rename - rename file
run - start app
ls - show files in dir
cd - go to directory
md - make directory
sett_chan - change resolution
strap - internet package installer
exestrap (in test+unstable is pbin) - internet binary installer
netstrap (in test+instable in dlib) - internet library installer
ftp - ftp client
rescue - advanced shell
runt - run terminal app (TApp)
shutdown (in test+unstable is exit3) - shutdown BatchBSD
flag - flag file(s) (currenty it doesn't work, I will repair it later)
repoinfo - view information about your software repository
gdisk - information about disks and partitions
multipak - mPak installer interv
multipak-local - mPak installer localv
ifconfig - IP configuration

RESCUE SHELL COMMANDS:
goback - back to normal shell
set-strapsource - change strap software repository
set-mpaksource - change multipak software repository (used for installing large packages)

System Users:
Name: root
Pass: root

Name: paprotka
Pass: 

SYNTAX FOR pack_add:
i - install package
r - remove package
c - create package
paprotka - more advanced shell
n - install net library package from local file
e - install binary package from local file
ce - create binary package
cn - transform net library into library package

DOWNLOAD:
v27 (Stable build): http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v26.zip


DOWNLOAD OLD BUILDS:
v26: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v26.zip
v25: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v25.zip
v24: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v24.zip
v23: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v23.zip
v22: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v22.zip
v21: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v21.zip
v20: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v20.zip
v19: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v18.zip
v18: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v18.zip
v17: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v17.zip
v16: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v16.zip
v15: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v15.zip
v14: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v14.zip
v13: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v13.zip
v12: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v12.zip
v11: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v11.zip
v10: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v10.zip
v9: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v9.zip
v8: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v8.zip
v7: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v7.zip
v6: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v6.zip
v5: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v5.zip
v4: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v24.zip
v3: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v3.zip
v2: http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v2.zip
v1: http://github.com/glowiak/batchbsd/raw/master/BatchBSD.zip

REMOVING SYSTEM:
pack_add,
paprotka,
remove-basesystem,
ENTER,
done!

In v6 I tested curl (and wget), but IE engine is back!
In v7 to execute commands type "su" and "root" to access root console (v7 isn't LTS version, because "su" is in alpha phase)

In test+unstable builds (in 7 pbin is defualt enabled) to enable pbin (binary (exe) packages installation from internet):
runt
nano pbin.bat
#change "NO" to "YES" in "set pbin_enable=NO" line,
#save and exit nano
#done pbin is enabled!

12 is bugfix update, no new features...at the moment...

Strap (strap,exestrap,netstrap) can download and install one-file package so, in 14 I added new experimental package manager called "multipak". Multipak packages (.mPak) are compressed folders with data.
multipak github repo (multipak download files from this repo): http://github.com/glowiak/multipak

I will stop developing strap,because is bugged and useless. Multipak is the future of BatchBSD packaging! (strap will be in BatchBSD FOREVER)

In v18 I changed boot loader image :).

For now v7 is no longer supproted, update to 18 or 8.

v19 - The Multipak Update released! It's update for multipak! News:
-multipak have shell
-multipak have on-server packages list and local packages list
-multipak can update online software list
-added "ifconfig" command, it shows you your ip

In 15.08.2020 I will stop developing test+unstable edition and publish old versions for download from this website!

Changes in v20:
-repaired multipak localv
-added "bbsd_v" and "kernel_v" variables
-updated software list
-added system-files-check on startup

In v23 repaired "set-mpaksource" RESCUE-SHELL command. 21,22,23 are bugfix updates.

After 2 weeks of nothing I created v25 - The BSD Compat Update, News in this version:
-added file structure from BSD (compat,etc,bin,var and others)
-added new init system (initV2)
-added new login applet
-changed disk type to thdXpX (True Hard Disk)
-added fstab in etc dir (fstab replaced old disks.vds)
-added loader.net in boot dir (loader.net replaced boot_loader.net)
-added dev/null file
-added compat/windows_nt folder (DLLs in compat/windows_nt/libs are random DLLs from my Windows 8)
-renamed main file from "main.bat" to "boot.bat"

How to install BatchBSD on non-windows:
1.Install Wine (http://winehq.org)
2.Download and unpack latest BatchBSD file.
3.Start main BatchBSD file with Wine

In v26 I repaired no-booting bug from v25

In v27 I added desctiption to multipak package list yay!

This is weird, net version of multipak and strap don't working on Wine (WineIE is broken)

Try my new project, BashBSD - port of BSD for other OSs: http://github.com/glowiak/bashbsd

BatchBSD is now discontinued! Use BashBSD instead!
