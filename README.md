# pakbak
Backup the local pacman database when it changes.
[https://aur.archlinux.org/packages/pakbak-git/](https://aur.archlinux.org/packages/pakbak-git/)

## Installation
Please make sure that your system fulfills the
[prerequisites](https://wiki.archlinux.org/index.php/Arch_User_Repository#Prerequisites)
to work with the AUR.

```bash
git clone https://aur.archlinux.org/pakbak-git.git
cd pakbak-git
makepkg -si
```

(see [build and install](https://wiki.archlinux.org/index.php/Aur#Build_and_install_the_package) in the ArchWiki)

After the installation has been finished make sure, that the service is started, when your pacman db changes.
```bash
systemctl enable pakbak.path
```
