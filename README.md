# archPackages
Build a package repository for [Arch Linux](https://www.archlinux.org).
It succeeds the [nafets227/internetBuild](https://github.com/nafets227/internetBuild)
repository, that used to do a similar job on local Jenkins.

## usage
edit /etc/pacman.conf and append the config for our repo
```
[aurci2]
Server = https://github.com/nafets227/archPackages/releases/latest/download
```
After that, running
```
pacman -Sy
```
should work and you can start to install packages from this repo (e.g. blktrace)
in the usual way, e.g. with
```
pacman -S blktrace
```

## credits
[nafets227/build-aur-packages](https://github.com/nafets227/build-aur-packages)
forked from
[kopp/build-aur-packages](https://github.com/kopp/build-aur-packages)
