**Table of Contents**

- [Select a version](#select-a-version)
- [Installation](#installation)
  - [Windows](#install-plover-on-windows)
  - [Mac](#install-plover-on-mac)
  - [Linux](#install-plover-on-linux)
    - [Arch](#install-plover-on-arch-linux-distribution)
    - [Ubuntu](#install-plover-on-ubuntu-linux-distribution)
    - [Other](#install-plover-on-other-linux-distributions)
         - [AppImage Method](#appimage-method)
         - [Other Approaches](#other-approaches)
- [Setting up my machine](#setting-up-my-machine)

## Troubleshooting

If you get stuck, see the [troubleshooting guide](https://github.com/openstenoproject/plover/wiki/Troubleshooting:-Common-Issues) or ask for help on the [Plover Discord Server](https://discord.gg/0lQde43a6dGmAMp2) or in the [steno community](https://github.com/openstenoproject/plover/wiki/Links-to-the-Steno-Community).

## Select a version

Unsure which version to download? You have a few options, depending on your needs…

Most of the time, you'll want the [latest stable version](https://github.com/openstenoproject/plover/releases/latest). As at 26 Jan 2020, most folk on the [Plover Discord Server](https://discord.gg/0lQde43a6dGmAMp2) recommend v4.0.0. See the [latest weekly release](https://github.com/openstenoproject/plover/releases).

If you are adventurous and want access to the latest and greatest features and developments, check out [the weekly releases](https://github.com/openstenoproject/plover/releases) or alternatively the [weeklies](https://github.com/openstenoproject/plover/tags).

- [**Stable**](https://github.com/openstenoproject/plover/releases/latest)
- [**Weekly**](https://github.com/openstenoproject/plover/releases)
- [**Weeklies**](https://github.com/openstenoproject/plover/tags)

- **Source**

If you are a developer and want to build from source, there are OS-specific guides for [Windows](https://github.com/openstenoproject/plover/tree/master/windows), [Linux](https://github.com/openstenoproject/plover/tree/master/linux), and [Mac](https://github.com/openstenoproject/plover/tree/master/osx). Follow those guides to get your environments setup and run or build the source.

## Installation

Each release has files for all the operating systems we support. You only need the files that are relevant to your operating system

--------------------

### Install Plover on Windows

1. Download the `.exe` file from the release page.
  * You can place the file anywhere on your computer. You will run it from the same location every time.
2. Open the file to launch Plover.

--------------------

### Install Plover on Mac

If you have [Homebrew Cask](https://caskroom.github.io/) installed on your system, you can run `brew cask install plover` at the command-line. Otherwise:

1. Download the `.dmg` file from the release page.
1. Open the `.dmg` file.
1. In the mounted disk, drag the `Plover.app` to your `Applications` folder.
1. Open `System Preferences > Security & Privacy > Privacy > Accessibility`.
1. Click the "+" Button, and go to your applications and select `Plover.app`.

Plover is set up! You can run Plover like you would any other application.

> **Note**: Other "keyboard helper"-type applications (e.g. Karabiner Elements and text expanders) may interfere with Plover.

--------------------

### Install Plover on Linux

--------------------

#### Install Plover on Arch Linux distribution

Two AUR packages are provided:

1. [plover](https://aur.archlinux.org/packages/plover/) for the latest stable release
1. and [plover-git](https://aur.archlinux.org/packages/plover-git/) for the current `master`

You may need to add yourself to the group "uucp" (owner of /dev/ttyACM*).

--------------------

#### Install Plover on Ubuntu Linux distribution

Stable releases can be installed from a dedicated PPA, see [ppa:benoit.pierre/plover](https://launchpad.net/~benoit.pierre/+archive/ubuntu/plover) for instructions.

_2019-02-25 Note_: The PPA method doesn't currently appear to work with Ubuntu 18.04 Bionic Beaver ([there is a listing for Xenial however](https://launchpad.net/~benoit.pierre/+archive/ubuntu/plover/+packages)). One can use the [AppImage method](#appimage-method) instead. Similarly for weeklies one can use the AppImage method or [other approaches](#other-approaches) for installing on other Linux distributions.

--------------------

#### Install Plover on other Linux distributions

##### AppImage Method 

An [AppImage](http://appimage.org/) is provided: it includes all the necessary dependencies and should run on most x86 64-bits distributions. To use it:

- download it
- add the user to the group "dialout"
- after adding the group, logout and login again for the change to take effect
- [make it executable](http://discourse.appimage.org/t/how-to-make-an-appimage-executable/80)
- launch it like a standard executable

Note: you can install the AppImage for your current user (and register Plover in your standard applications menu) by executing it with the `--install` flag. If you had previously installed another AppImage version of Plover, it will be automatically uninstalled and replaced.

As of January 2019 AppImage files are not in the [latest stable version](https://github.com/openstenoproject/plover/releases/latest) but can be found in [weeklies](https://github.com/openstenoproject/plover/tags) or [weekly](https://github.com/openstenoproject/plover/releases).  

##### Other Approaches 

Other approaches could include:

 - Seeking to install from the `deb` file if you are using Debian or a Debian derived distribution (e.g. with `sudo apt install <path/deb file>` or using `dpkg` ), but you may need to do some work to deal with handling the dependencies.
 - Seeking to [install from source for Linux](https://github.com/openstenoproject/plover/tree/master/linux).

--------------------

## Setting up my machine

Initially, Plover is set up to use your computer keyboard as a steno machine. If you have a steno machine, you'll need to configure Plover to look for your machine. Please check the [Supported Hardware page](https://github.com/openstenoproject/plover/wiki/Supported-Hardware) to find instructions specific to your machine.