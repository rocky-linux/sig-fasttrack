---
title: Repositories and Packages
---
# Repositories

There are 2 main FastTrack repositories:  **FastTrack-Updates** and **FastTrack-New** .

The -Updates repository contains newer versions of packages found in Rocky Linux, while the -New repository is exclusively new packages.

## Updates Repo: Includes and Excludes

The FastTrack-Updates repository in particular could be an issue for some users - what if you are only interested in updating certain packages on your system, but leaving others alone?  This is not a problem for FastTrack-New , as you can simply opt to not install packages you don't want.  
  
To assist users, the FastTrack.repo file will have a couple comments explaining how to `includepkgs` and `excludepkgs` in DNF.  Specifying includepkgs allows users to only receive updates for the listed packages, while excludepkgs allows them to ignore FastTrack updates of things they prefer to keep on the stock Rocky ones.


# Packages

## Suggestions/Requests

New packages can always be discussed for inclusion via issues at: [https://git.resf.org/sig_fasttrack/meta/issues](https://git.resf.org/sig_fasttrack/meta/issues)

The best/fastest way to get a package included in the SIG is to have the build pre-complete in tested.  That is, have a working git repository or SRPM somewhere that you've confirmed builds properly against Rocky Linux.  We can then bring the package into dist-git under https://git.rockylinux.org/sig/fasttrack/src/PACKAGE and build + publish in the Rocky build system.


## Builds
Package builds *must* build with Rocky Linux dependencies only. (BaseOS/AppStream/PowerTools/Devel/etc.)  

Using 3rd party repos such as EPEL as dependencies is not allowed.  3rd party repositories are subject to change, and we do not want to depend on external packages in order to use SIG-FastTrack.  If a package is dependent on other packages found in EPEL or other repos, these dependencies can be re-built and made available in the FastTrack repositories as well.

A standard Mock config will be made available in the SIG's Git space for each major version of Rocky Linux.  These Mock configs will reflect the SIG's Peridot build settings, so proper apples-to-apples testing of builds can be done locally by contributors.

