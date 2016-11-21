**Table of Contents**

- [Select a version](#select-a-version)
- [Installation](#installation)
  - [Windows](#windows)
  - [Mac](#mac)
  - [Linux](#linux)
    - [Arch](#arch)
    - [Other](#other)
- [Setting up my machine](#setting-up-my-machine)

## Select a version

What version do you get? You have a couple of options, depending on your needs.

- [**Stable**](https://github.com/openstenoproject/plover/releases/latest)

    Most of the time, you'll want the [latest stable version](https://github.com/openstenoproject/plover/releases/latest).
- [**Weekly**](https://github.com/openstenoproject/plover/releases)

    If you are adventurous and want access to the latest and greatest features and developments, check out [the weekly releases](https://github.com/openstenoproject/plover/releases).
- **Source**

    If you are a developer and want to build from source, there are OS-specific guides for [Windows](https://github.com/openstenoproject/plover/tree/master/windows), [Linux](https://github.com/openstenoproject/plover/tree/master/linux), and [macOS](https://github.com/openstenoproject/plover/tree/master/osx). Follow those guides to get your environments setup and run or build the source.

## Installation

Each release has files for all the operating systems we support. You only need to grab the files that are relevant to your OS.

### Windows

- Download the `.exe` file from the release page.
- You can place the file anywhere on your computer. You will run it from the same location every time.
- Open the file to launch Plover.

### Mac

If you have [Homebrew Cask](https://caskroom.github.io/) installed on your system, you can run `brew cask install plover` at the command-line. Otherwise:

- Download the `.dmg` file from the release page.
- Open the `.dmg`.
- In the mounted disk, drag the `Plover.app` to your `Applications` folder.
- Open `System Preferences > Security & Privacy > Privacy > Accessibility`.
- Click the "+" Button, and go to your applications and select `Plover.app`.
- Plover is set up! Simply run Plover like you would any other application.

### Linux

#### Arch

Use AUR package [plover](https://aur.archlinux.org/packages/plover/) for stabled and [plover-git](https://aur.archlinux.org/packages/plover-git/) for the current `master`.

#### Other

You need to install Python 2 (with pip support), wxPython, and wmctrl (optional). Once this is done, download the wheel file for the version you want to run and install it like this:

`python2 -m pip install --user plover-3.0.0-py2-none-any.whl`

You can then start Plover with:

`~/.local/bin/plover`

## Setting up my machine

Initially, Plover is set up to use your computer keyboard as a steno machine. If you have a steno machine, you'll need to configure Plover to look for your machine. Please check the [Supported Hardware page](https://github.com/openstenoproject/plover/wiki/Supported-Hardware) to find instructions specific to your machine.