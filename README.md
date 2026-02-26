# archPackages

Build a package repository for
[Arch Linux](https://www.archlinux.org).
It succeeds the
[nafets227/internetBuild](https://github.com/nafets227/internetBuild)
repository, that used to do a similar job on local Jenkins.

## usage

edit /etc/pacman.conf and append the config for our repository

```ini
[nafets227-archPackages]
SigLevel = Optional
Server = https://nafets227.github.io/archPackages
```

After that, running

```shell
pacman -Sy
```

should work and you can start to install packages from this repository
(e.g. blktrace) in the usual way, e.g. with

```shell
pacman -S blktrace
```

## choosing GitHub pages as hosting

In previous versions packages and package-repo was made available for download
using GitHub releases. Unfortunately GitHub releases is limiting the characters
used in filenames. In detail, it transforms any colon ':' into a dot '.'.
Since colons are used in arch package filenames, whenever the epoch field is
set for the specific package, these package can never be downloaded
by pacman.

In order to overcome this limitation, we moved to GitHub pages to host our
package repository.

## credits

[nafets227/build-aur-packages](https://github.com/nafets227/build-aur-packages)
forked from
[kopp/build-aur-packages](https://github.com/kopp/build-aur-packages)
