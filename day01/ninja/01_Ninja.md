# 01 Ninja

vivi

[TOC]

## Practice

### Who are you

> Ninja, in this section, you are going to find out the ultimate life questions.
>
> * Who are you? Vivi
> * Where are you? (host name of the machine)
> * Which system are you in? Ubuntu 16.04
> * When is it now? 4:15
>
> To answer this questions, you are going to use the following command to help you.
>
> To paste output results, remember `CMD+C` or `CTRL+C` do not work in terminal, you have to right click and choose `copy`.

``` shell
$ whoami
vivi
$ hostnname
vivi-VirtualBox
$ uname
Linux
$ uname -a
Linux vivi-VirtualBox 4.4.0-31-generic #50-Ubuntu SMP Wed Jul 13 00:07:12 UTC 2016 x86_64 x86_64 x86_64 GNU/Linux
$ date
Sat Jul 30 16:31:48 EDT 2016
```

### Moving, jumping, flying

> As a ninja, you have to move very fast. In this section you are going to practice moving swiftly around directories, that is
>
> * Try to choose a good path that helps you move fast
> * Use `tab` trick for auto completion
>
> To move fast, certain commands can be useful: `cd\pwd\ls`
>
> Following are simple instructions to move around, but you are free to go anywhere
>
> 1. go to `/usr/local/lib/python2.7/dist-packages/`
> 2. check your location
> 3. go back to home `~`
> 4. check your location
> 5. go to `/etc/kernel/postinst.d/`
> 6. list details of the files in current location
> 7. jump anywhere you want to master the commands

``` shell
$cd workshop/study/math/homework
$pwd
/home/vivi/workshop/study/math/homework
$ls
hw1
$cd
$pwd 
/home/vivi

$ cd ../../etc
$ pwd
/etc
$ ls
acpi                    hosts                    profile
adduser.conf            hosts.allow              profile.d
alternatives            hosts.deny               protocols
# ... ...
```

``` shell
# paste your command and output here
```

### Building your backpacks

> Ninja, you are about to make your first travel, you need to put things in your backpacks. Remember, make things in order is always a good habit to keep.
>
> In this section, you are going to create directories that simulate the backpacks and categories and items. You want to create something has the same structure as the following directories.

``` shell
backpack/
├── backup_wallet
│   ├── cash
│   ├── credit_cards
│   └── id
├── lunchbox
│   ├── level1
│   │   └── fish_and_meat
│   ├── level2
│   │   └── rice
│   └── level3
│       └── soup
├── mainspace
│   ├── books
│   ├── iphone
│   ├── kindle
│   ├── plasticbag
│   │   └── cloth
│   └── umbrella
├── secretspace
│   ├── cash001
│   ├── cash002
│   ├── cash003
│   └── paperwarraper
│       └── million_check
└── wallet
    ├── cash
    ├── credit_cards
    └── id

10 directories, 18 files
```

> Be smart, try to use as minimum command lines as you can.

``` shell
# paste your command and output here
```
$ mkdir backpack
~$ ls
backpack  Documents  draft1.txt        linux-essentials  Pictures  Templates  workshop
Desktop   Downloads  examples.desktop  Music             Public    Videos     workspace
~$ cd backpack
~/backpack$ mkdir backup_wallet
~/backpack$ cd backup_wallet
~/backpack/backup_wallet$ mkdir cash credit_cards id
~/backpack/backup_wallet$ ls -l
total 12
drwxrwxr-x 2 vivi vivi 4096 Jul 30 16:58 cash
drwxrwxr-x 2 vivi vivi 4096 Jul 30 16:58 credit_cards
drwxrwxr-x 2 vivi vivi 4096 Jul 30 16:58 id
~/backpack/backup_wallet$ cd ../
~/backpack$ mkdir -p lunchboc/level1/fish_and_meat
~/backpack$ mkdir -p lunchbox/level2/rice
~/backpack$ mkdir -p lunchbox/level3/soup
~/backpack$ ls -R
.:
backup_wallet  lunchbox

./backup_wallet:
cash  credit_cards  id

./backup_wallet/cash:

./backup_wallet/credit_cards:

./backup_wallet/id:

./lunchbox:
level1  level2  level3

./lunchbox/level1:
fish_and_meat

./lunchbox/level1/fish_and_meat:

./lunchbox/level2:
rich

./lunchbox/level2/rich:

./lunchbox/level3:
soup

./lunchbox/level3/soup:

~/backpack$ mkdir mainspace secretspace
~/backpack$ cd mainspace
~/backpack/mainspace$ mkdir books iphone kindle plasticbag umbrella
~/backpack/mainspace$ mkdir plasticbag/cloth
~/backpack/mainspace$ cd ../
~/backpack$ cd secretspace
~/backpack/secretspace$ mkdir cash001 cash002 cash003 paperwarraper
~/backpack/secretspace$ ls
cash001  cash002  cash003  paperwarrapper
~/backpack/secretspace$ mkdir paperwarrapper/million_check
~/backpack/secretspace$ cd ../../
~$ cd backpack
~/backpack$ ls
backup_wallet  luchbox  lunch  lunchbox  mainspace  secretspace  wallet
vivi@vivi-VirtualBox:~/backpack$ cp -r backup_wallet wallet
vivi@vivi-VirtualBox:~/backpack$ ls -R
.:
backup_wallet  lunchbox  mainspace  secretspace  wallet

./backup_wallet:
cash  credit_cards  id

./backup_wallet/cash:

./backup_wallet/credit_cards:

./backup_wallet/id:

./lunchbox:
level1  level2  level3

./lunchbox/level1:
fish_and_meat

./lunchbox/level1/fish_and_meat:

./lunchbox/level2:
rich

./lunchbox/level2/rich:

./lunchbox/level3:
soup

./lunchbox/level3/soup:

./mainspace:
books  iphone  kindle  plasticbag  umbrella

./mainspace/books:

./mainspace/iphone:

./mainspace/kindle:

./mainspace/plasticbag:
cloth

./mainspace/plasticbag/cloth:

./mainspace/umbrella:

./secretspace:
cash001  cash002  cash003  paperwarrapper

./secretspace/cash001:

./secretspace/cash002:

./secretspace/cash003:

./secretspace/paperwarrapper:
million_check

./secretspace/paperwarrapper/million_check:

./wallet:
cash  credit_cards  id

./wallet/cash:

./wallet/credit_cards:

./wallet/id:


### Remove items

> There is no need to take the cashes in the secretspace since you already have backup wallet, so remove all the cashes in secretspace.
>
> Someone said he would like to treat you for lunch when you visit, so there is no need to take the heavy lunchbox with you. Remove the lunchbox from your backpack.

``` shell
~/backpack$ rm -r secretspace/cash*
~/backpack$ rm -r lunchbox
~/backpack$ ls -R
.:
backup_wallet  mainspace  secretspace  wallet

./backup_wallet:
cash  credit_cards  id

./backup_wallet/cash:

./backup_wallet/credit_cards:

./backup_wallet/id:

./mainspace:
books  iphone  kindle  plasticbag  umbrella

./mainspace/books:

./mainspace/iphone:

./mainspace/kindle:

./mainspace/plasticbag:
cloth

./mainspace/plasticbag/cloth:

./mainspace/umbrella:

./secretspace:
paperwarrapper

./secretspace/paperwarrapper:
million_check

./secretspace/paperwarrapper/million_check:

./wallet:
cash  credit_cards  id

./wallet/cash:

./wallet/credit_cards:

./wallet/id:
vivi@vivi-VirtualBox:~/backpack$ 

```

## Challenge

### Myth of hidden files

> In Linux kingdom, everything is file. However there are some files are not easy to be seen, there are called `hidden` files. It's a convention that hidden files are named begin with a dot `.`. Your task in this section is to find out all the hidden files in home `~` directory.
>
> There is a option for `ls` command to list all hidden files, find it out and use it for finding hidden files. (Tip: try `ls --help`)

``` shell
~/backpack$ ls .?*
backpack  Documents  draft1.txt        linux-essentials  Pictures  Templates  workshop
Desktop   Downloads  examples.desktop  Music             Public    Videos     workspace
~/backpack$ cd
~$ ls .?*
.bash_history  .bashrc  .ICEauthority  .sudo_as_admin_successful  .vboxclient-display.pid      .vboxclient-seamless.pid  .xsession-errors
.bash_logout   .dmrc    .profile       .vboxclient-clipboard.pid  .vboxclient-draganddrop.pid  .Xauthority               .xsession-errors.old

..:
vivi

.cache:
compizconfig-1                                                              gnome-software  logrotate  wallpaper
event-sound-cache.tdb.43ed5fd4f9c944f492b320397ff67b25.x86_64-pc-linux-gnu  gstreamer-1.0   mozilla    zeitgeist-vacuum.stamp
evolution                                                                   ibus            upstart

.config:
compiz-1  evolution      gtk-3.0  libaccounts-glib  pulse  update-notifier  user-dirs.dirs
dconf     gnome-session  ibus     nautilus          unity  upstart          user-dirs.locale

.gconf:

.gnupg:
private-keys-v1.d  S.gpg-agent

.local:
share

.mozilla:
extensions  firefox

.ssh:
id_rsa  id_rsa.pub

```
