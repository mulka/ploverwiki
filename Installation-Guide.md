**Table of Contents**

- [Select a version](#select-a-version)
- [Installation](#installation)
  - [Windows](#install-plover-on-windows)
  - [Mac](#install-plover-on-mac)
  - [Linux](#install-plover-on-linux)
    - [Arch](#install-plover-on-arch-linux-distribution)
    - [Ubuntu](#install-plover-on-ubuntu-linux-distribution)
    - [Other](#install-plover-on-other-linux-distributions)
- [Setting up my machine](#setting-up-my-machine)

## Select a version

Unsure which version to download? You have a few options, depending on your needs:

- [**Stable**](https://github.com/openstenoproject/plover/releases/latest)

    Most of the time, you'll want the [latest stable version](https://github.com/openstenoproject/plover/releases/latest).
- [**Weekly**](https://github.com/openstenoproject/plover/releases)

    If you are adventurous and want access to the latest and greatest features and developments, check out [the weekly releases](https://github.com/openstenoproject/plover/releases).
- **Source**

    If you are a developer and want to build from source, there are OS-specific guides for [Windows](https://github.com/openstenoproject/plover/tree/master/windows), [Linux](https://github.com/openstenoproject/plover/tree/master/linux), and [Mac](https://github.com/openstenoproject/plover/tree/master/osx). Follow those guides to get your environments setup and run or build the source.

## Installation

Each release has files for all the operating systems we support. You only need the files that are relevant to your operating system

--------------------

### Install Plover on Windows

1. Download the `.exe` file from the release page.
  * You can place the file anywhere on your computer. You will run it from the same location every time.
1. Open the file to launch Plover.

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
2. and [plover-git](https://aur.archlinux.org/packages/plover-git/) for the current `master`

--------------------

#### Install Plover on Ubuntu Linux distribution

Stable releases can be installed from a dedicated PPA, see [ppa:benoit.pierre/plover](https://launchpad.net/~benoit.pierre/+archive/ubuntu/plover) for instructions.

For weeklies, follow the directions for installing Plover on other Linux distributions.

--------------------

#### Install Plover on other Linux distributions

An [AppImage](http://appimage.org/) is provided: it includes all the necessary dependencies and should run on most x86 64-bits distributions. To use it:

- download it
- add the user to the group "dialout"
- after adding the group, logout and login again for the change to take effect
- [make it executable](http://discourse.appimage.org/t/how-to-make-an-appimage-executable/80)
- launch it like a standard executable

--------------------

## Setting up my machine

Initially, Plover is set up to use your computer keyboard as a steno machine. If you have a steno machine, you'll need to configure Plover to look for your machine. Please check the [Supported Hardware page](https://github.com/openstenoproject/plover/wiki/Supported-Hardware) to find instructions specific to your machine.