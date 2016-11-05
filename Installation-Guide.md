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
- Open the file to launch Plover. If it is your first launch, you will need to configure Plover to look for your machine type.

### Mac

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

You can `pip install` the wheel file. You can `chmod +x` the egg if you have all dependencies installed. Additional instructions for various repos can be found in the [Linux README](https://github.com/openstenoproject/plover/tree/master/linux)

## Setting up my machine

Initially, Plover is set up to use your computer keyboard as a steno machine. If you have a steno machine, you'll need to configure Plover to look for your machine. Please check the [Supported Hardware page](https://github.com/openstenoproject/plover/wiki/Supported-Hardware) to find instructions specific to your machine.