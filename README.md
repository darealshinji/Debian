This repository is intended to be some sort *BSD ports or Arch pkgbuild system for Debian and Ubuntu.
It's very simple and intended to be used to package closed source and non-free software, but also for some new
projects and to package some multimedia programs with embedded libav libraries.


**Usage:**

Move to a directory and run make: `cd devel/yasm && make`<br>

The package will be built in a pbuilder chroot environment.
If you want to build without pbuilder run make with "PBUILDER=0": `cd devel/yasm && make PBUILDER=0`

To skip dependency checking run make with "DEPS=0": `cd devel/yasm && make DEPS=0`

The final packages are saved in `$HOME/buildresult`

You can run `make clean` or `make distclean` to clean up a build directory.


To build packages of Unity engine games use the script provided here:<br>
https://github.com/darealshinji/UnityEngine2deb<br>
https://github.com/darealshinji/debian/tree/master/games/unityengine2deb

Or you can use this repository with a small collection of Unity engine games:<br>
https://github.com/darealshinji/UnityGames-for-debian


**Important:**

I always test the packages here before I push a new commit (I'm currently using Ubuntu 14.04 64 bit). But some of the Makefiles here will build packages from the latest release branch snapshots, so in some cases a package might not build because of recent changes. You should also keep in mind that closed-source software, especially if it hasn't been updated for ages, and/or programs that use certain embedded libraries as well as static binaries are considered a potential security risk in Debian-based distributions. Usually software is also split into several packages but to make the installation of these home-brew packages easier, most of the stuff in here will be stored in single packages.
