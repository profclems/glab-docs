---
title: "Installation"
description: ""
lead: ""
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "prologue"
weight: 100
toc: true
---

Download a binary suitable for your OS at the [releases page](https://github.com/profclems/glab/releases/latest)

### Quick Install (shell)
**Supported Platforms**: Linux and macOS

You can install or update `glab` with:
```sh
curl -sL https://j.mp/glab-cli | sudo sh
```
or
```sh
curl -s https://raw.githubusercontent.com/profclems/glab/trunk/scripts/install.sh | sudo sh
```
*Installs into `usr/bin`*

**NOTE**: Please take care when running scripts in this fashion. Consider peaking at the install script itself and verify that it works as intended.

### Windows
Available for download via [WinGet](https://github.com/microsoft/winget-cli), [scoop](https://scoop.sh), or downloadable EXE installer file.

#### WinGet
```sh
winget install glab
```
Updating:
```sh
winget install glab
```

#### Scoop
```sh
scoop install glab
```
Updating:
```sh
scoop update glab
```
#### EXE Installer

EXE installers are available for download on the [releases page](https://github.com/profclems/glab/releases/latest).

### Linux
Prebuilt binaries available at the [releases page](https://github.com/profclems/glab/releases/latest).

#### Linuxbrew (Homebrew)
```sh
brew install glab
```
Updating:
```sh
brew upgrade glab
```
#### Snapcraft
[![Get it from the Snap Store](https://snapcraft.io/static/images/badges/en/snap-store-black.svg)](https://snapcraft.io/glab)

Make sure you have snap installed on your Linux Distro (https://snapcraft.io/docs/installing-snapd).
1. `sudo snap install --edge glab`
1. `sudo snap connect glab:ssh-keys` to grant ssh access

#### Arch Linux
`glab` is available through the [gitlab-glab-bin](https://aur.archlinux.org/packages/gitlab-glab-bin/) package on the AUR or download and install an archive from the [releases page](https://github.com/profclems/glab/releases/latest). Arch Linux also supports [snap](https://snapcraft.io/docs/installing-snap-on-arch-linux).
```sh
yay -Sy gitlab-glab-bin
```
or any other [AUR helper](https://wiki.archlinux.org/index.php/AUR_helpers) of your choice.

#### KISS Linux
`glab` is available on the [KISS Linux Community Repo](https://github.com/kisslinux/community) as `gitlab-glab`.
If you already have the community repo configured in your `KISS_PATH` you can install `glab` through your terminal.
```sh
kiss b gitlab-glab && kiss i gitlab-glab
```
If you do not have the community repo configured in your `KISS_PATH`, follow the guide on the official guide [Here](https://k1ss.org/install#3.0) to learn how to setup it up.

#### Alpine Linux

`glab` is available on the [Alpine Community Repo](https://git.alpinelinux.org/aports/tree/community/glab?h=master) as `glab`.

##### Install

We use `--no-cache` so we don't need to do an `apk update` before.

```sh
apk add --no-cache glab
```

##### Install a pinned version from edge

To ensure that by default edge will be used to get the latest updates. We need the edge repository under `/etc/apk/repositories`.

Afterwards you can install it with `apk add --no-cache glab@edge`

We use `--no-cache` so we don't need to do an `apk update` before.

```sh
echo "@edge http://dl-cdn.alpinelinux.org/alpine/edge/community" >> /etc/apk/repositories
apk add --no-cache glab@edge
```

##### Alpine Linux Docker-way

Use edge directly

```sh
FROM alpine:3.13
RUN apk add --no-cache glab
```

Fetching latest glab version from edge

```sh
FROM alpine:3.13
RUN echo "@edge http://dl-cdn.alpinelinux.org/alpine/edge/community" >> /etc/apk/repositories
RUN apk add --no-cache glab@edge
```

### Nix/NixOS

Nix/NixOS users can install from [nixpkgs](https://search.nixos.org/packages?channel=unstable&show=glab&from=0&size=30&sort=relevance&query=glab):

```bash
nix-env -iA nixos.glab
```

### macOS

#### Homebrew

`glab` is available via [Homebrew](https://formulae.brew.sh/formula/glab)

```sh
brew install glab
```
Updating:
```sh
brew upgrade glab
```

#### MacPorts

`glab`is also available via [MacPorts](https://ports.macports.org/port/glab/summary)

```sh
sudo port install glab
```

Updating:
```sh
sudo port selfupdate && sudo port upgrade glab
```