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
vivi@vivi-VirtualBox:~$ ls
Desktop  Documents  Downloads  examples.desktop  linux-essentials  Music  Pictures  Public  Templates  Videos  workspace
vivi@vivi-VirtualBox:~$ cd /usr/local/lib/python2.7/dist-packages/
vivi@vivi-VirtualBox:/usr/local/lib/python2.7/dist-packages$ ls
vivi@vivi-VirtualBox:/usr/local/lib/python2.7/dist-packages$ pwd
/usr/local/lib/python2.7/dist-packages
vivi@vivi-VirtualBox:/usr/local/lib/python2.7/dist-packages$ cd
vivi@vivi-VirtualBox:~$ pwd
/home/vivi
vivi@vivi-VirtualBox:~$ cd /etc/kernel/postinst.d
vivi@vivi-VirtualBox:/etc/kernel/postinst.d$ pwd
/etc/kernel/postinst.d
vivi@vivi-VirtualBox:/etc/kernel/postinst.d$ ls
apt-auto-removal  initramfs-tools  pm-utils  unattended-upgrades  update-notifier  zz-update-grub
vivi@vivi-VirtualBox:/etc/kernel/postinst.d$ cd
vivi@vivi-VirtualBox:~$ pwd
/home/vivi
vivi@vivi-VirtualBox:~$ ls
Desktop  Documents  Downloads  examples.desktop  linux-essentials  Music  Pictures  Public  Templates  Videos  workspace
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
vivi@vivi-VirtualBox:~/workspace/day1/homework$ ls
vivi@vivi-VirtualBox:~/workspace/day1/homework$ mkdir backup_wallet lunchbox mainspace secretspace
vivi@vivi-VirtualBox:~/workspace/day1/homework$ ls
backup_wallet  lunchbox  mainspace  secretspace
vivi@vivi-VirtualBox:~/workspace/day1/homework$ cd backup_wallet
vivi@vivi-VirtualBox:~/workspace/day1/homework/backup_wallet$ touch cash credit_cards id
vivi@vivi-VirtualBox:~/workspace/day1/homework/backup_wallet$ ls
cash  credit_cards  id
vivi@vivi-VirtualBox:~/workspace/day1/homework/backup_wallet$ cd ../lunchbox
vivi@vivi-VirtualBox:~/workspace/day1/homework/lunchbox$ mkdir level1 level2 level3
vivi@vivi-VirtualBox:~/workspace/day1/homework/lunchbox$ ls
level1  level2  level3
vivi@vivi-VirtualBox:~/workspace/day1/homework/lunchbox$ touch level1/fish_and_meat level2/rice level3/soup
vivi@vivi-VirtualBox:~/workspace/day1/homework/lunchbox$ ls -R
.:
level1  level2  level3

./level1:
fish_and_meat

./level2:
rice

./level3:
soup
vivi@vivi-VirtualBox:~/workspace/day1/homework/lunchbox$ cd ../mainspace
vivi@vivi-VirtualBox:~/workspace/day1/homework/mainspace$ mkdir books iphone kindle plasticbag umbrella
vivi@vivi-VirtualBox:~/workspace/day1/homework/mainspace$ ls
books  iphone  kindle  plasticbag  umbrella
vivi@vivi-VirtualBox:~/workspace/day1/homework/mainspace$ touch plasticbag/cloth
vivi@vivi-VirtualBox:~/workspace/day1/homework/mainspace$ ls -R
.:
books  iphone  kindle  plasticbag  umbrella

./books:

./iphone:

./kindle:

./plasticbag:
cloth

./umbrella:
vivi@vivi-VirtualBox:~/workspace/day1/homework/mainspace$ cd ../secretspace/
vivi@vivi-VirtualBox:~/workspace/day1/homework/secretspace$ mkdir cash001 cash002 cash003 paperwarraper
vivi@vivi-VirtualBox:~/workspace/day1/homework/secretspace$ ls
cash001  cash002  cash003  paperwarraper
vivi@vivi-VirtualBox:~/workspace/day1/homework/secretspace$ touch paperwarraper/million_check
vivi@vivi-VirtualBox:~/workspace/day1/homework/secretspace$ ls -R
.:
cash001  cash002  cash003  paperwarraper

./cash001:

./cash002:

./cash003:

./paperwarraper:
million_check
vivi@vivi-VirtualBox:~/workspace/day1/homework/secretspace$ cd ../
vivi@vivi-VirtualBox:~/workspace/day1/homework$ cp -r backup_wallet wallet
vivi@vivi-VirtualBox:~/workspace/day1/homework$ ls
backup_wallet  lunchbox  mainspace  secretspace  wallet
vivi@vivi-VirtualBox:~/workspace/day1/homework$ ls -R
.:
backup_wallet  lunchbox  mainspace  secretspace  wallet

./backup_wallet:
cash  credit_cards  id

./lunchbox:
level1  level2  level3

./lunchbox/level1:
fish_and_meat

./lunchbox/level2:
rice

./lunchbox/level3:
soup

./mainspace:
books  iphone  kindle  plasticbag  umbrella

./mainspace/books:

./mainspace/iphone:

./mainspace/kindle:

./mainspace/plasticbag:
cloth

./mainspace/umbrella:

./secretspace:
cash001  cash002  cash003  paperwarraper

./secretspace/cash001:

./secretspace/cash002:

./secretspace/cash003:

./secretspace/paperwarraper:
million_check

./wallet:
cash  credit_cards  id

```



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
vivi@vivi-VirtualBox:~$ ls -a
.              .cache     Downloads         .ICEauthority     .nano     .sudo_as_admin_successful    .vboxclient-seamless.pid  .xsession-errors.old
..             .config    examples.desktop  linux-essentials  Pictures  Templates                    Videos
.bash_history  Desktop    .gconf            .local            .profile  .vboxclient-clipboard.pid    workspace
.bash_logout   .dmrc      .gitconfig        .mozilla          Public    .vboxclient-display.pid      .Xauthority
.bashrc        Documents  .gnupg            Music             .ssh      .vboxclient-draganddrop.pid  .xsession-errors

```
