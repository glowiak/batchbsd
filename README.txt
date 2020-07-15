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

RESCUE SHELL COMMANDS:
goback - back to normal shell
set-strapsource - change strap software repository
system-update - update system to specify version

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
v15 (Stable build): http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v15.zip
v8 (test+unstable build): http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v8.zip

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
