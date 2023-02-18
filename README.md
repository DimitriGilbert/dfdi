# Didi's FeDora Installer

A script to automate most of my reinstall process.

## TLDR

```bash
# install
git clone git@github.com:DimitriGilbert/dfdi.git
cd dfdi
chmod +x ./ -R

# reinstall
./reinstall

# custom install
./dfdi "$USER" [options]
```

## dfdi

I run it using sudo so I don't end up having to type my password a bunch'o'time, you do not have to though, every calls needing sudo use it ;).

### Usage

```bash
./dfdi <user> [--dnf-p-dl <value>] [--dnf-install <value>] [--dnf-repo <value>] [--flatpak-install <value>] [--flatpak-repo <value>] [--dnf-list <value>] [--flatpak-list <value>] [--execute <value>] [--execute-before <value>] [--[no-]dnf-fastest] [--[no-]rpm-fusion] [--[no-]flathub] [--[no-]media-codec]
```

### Options

* `user`: installing user.
* `--dnf-p-dl <dnf-p-dl>`: parrallel download [default: ' 10 '].
* `--dnf-install <dnf-install>`: install using dnf, repeatable.
* `--dnf-repo <dnf-repo>`: install dnf repository, repeatable.
* `--flatpak-install <flatpak-install>`: install using flatpak, repeatable.
* `--flatpak-repo <flatpak-repo>`: add flatpak repo, repeatable.
* `--dnf-list <dnf-list>`: dnf install package list file, repeatable.
* `--flatpak-list <flatpak-list>`: flatpak install list file, repeatable.
* `-e, --execute <execute>`: command to execute at the end of install, repeatable.
* `-b, --execute-before <execute-before>`: command to execute before, repeatable.
* `--dnf-fastest|--no-dnf-fastest`: set fastest mirror rules, on by default (use --no-dnf-fastest to turn it off).
* `--rpm-fusion|--no-rpm-fusion`: enables rpm fusion, on by default (use --no-rpm-fusion to turn it off).
* `--flathub|--no-flathub`: enables flathub, on by default (use --no-flathub to turn it off).
* `--media-codec|--no-media-codec`: install media codec, on by default (use --no-media-codec to turn it off).

## Utils

A bunch of script to install additional repos/software, gnome extensions and configuration.
