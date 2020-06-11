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

DEFUALT USER IS root
DEFUALT root PASSWORD IS root

SYNTAX FOR pkg_add:
i - install package
r - remove package
c - create package

DOWNLOAD:
v9.1 (LTS build): http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v9.1.zip
v8 (test+unstable build): http://github.com/glowiak/batchbsd/raw/master/BatchBSD_v8.zip

REMOVING SYSTEM:
pack_add,
paprotka,
remove-basesystem,
ENTER,
done!

In v6 I tested curl (and wget), but IE engine is back!
In v7 to execute commands type "su" and "root" to access root console (v7 isn't LTS version, because "su" is in alpha phase)

In test+unstable builds (in 7 pbin is defualt enabled) to enable pbin (binary (exe) packages installation from internet:
runt
nano pbin.bat
#change "NO" to "YES" in "set pbin_enable=NO" line,
#save and exit nano
#done pbin is enabled!
