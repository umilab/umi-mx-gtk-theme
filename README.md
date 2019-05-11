# UMI ArcX Theme

UMI ArcX a flat theme with transparent elements, base on Arc theme and Flatabulous window controls with "X" picked design, for GTK 3, GTK 2 and GNOME Shell which supports GTK 3 and GTK 2 based desktop environments like GNOME, Unity, Budgie, Pantheon, Xfce, MATE, etc.

## UMI ArcX is available in three variants

### UMI-arcX

![A screenshot of the UMI ArcX theme](http://tnga.github.io/sharedbazar/_assets/images/umi-mvx-screenshot-20190508153236.png)

### UMI-arcX-Darker

![A screenshot of the UMI ArcX-Darker theme](http://tnga.github.io/sharedbazar/_assets/images/umi-mvx-dr-screenshot-20190508153542.png)

### UMI-arcX-Dark

![A screenshot of the UMI ArcX-Dark theme](http://tnga.github.io/sharedbazar/_assets/images/umi-mvx-d-screenshot-20190508153627.png)

### Manual Installation

**Important:** Remove all older versions of the theme from your system before you proceed any further.

    sudo rm -rf /usr/share/themes/{umi-arcx,umi-arcx-darker,umi-arcx-dark,umi-arcx-solid,umi-arcx-darker-solid,umi-arcx-dark-solid}
    rm -rf ~/.local/share/themes/{umi-arcx,umi-arcx-darker,umi-arcx-dark,umi-arcx-solid,umi-arcx-darker-solid,umi-arcx-dark-solid}
    rm -rf ~/.themes/{umi-arcx,umi-arcx-darker,umi-arcx-dark,umi-arcx-solid,umi-arcx-darker-solid,umi-arcx-dark-solid}

To build the theme the follwing packages are required

* `autoconf`
* `automake`
* `sassc` for GTK 3, Cinnamon, or GNOME Shell
* `pkg-config` or `pkgconfig` for Fedora
* `git` to clone the source directory
* `optipng` for GTK 2, GTK 3, or XFWM
* `inkscape` for GTK 2, GTK 3, or XFWM

The following packages are optionally required

* `gnome-shell`for auto-detecting the GNOME Shell version
* `libgtk-3-dev` for Debian based distros or `gtk3-devel` for RPM based distros, for auto-detecting the GTK3 version

**Note:** For distributions which don't ship separate development packages, just the GTK 3 package is needed instead of the `-dev` packages.

For the theme to function properly, install the following

* GNOME Shell 3.18 - 3.32, GTK 3.18 - 3.24
* The `gnome-themes-extra` package
* The murrine engine. This has different names depending on the distro.
  * `gtk-engine-murrine` (Arch Linux)
  * `gtk2-engines-murrine` (Debian, Ubuntu, elementary OS)
  * `gtk-murrine-engine` (Fedora)
  * `gtk2-engine-murrine` (openSUSE)
  * `gtk-engines-murrine` (Gentoo)

Install the theme with the following commands

#### 1. Get the source

If you want to install the latest version from git, clone the repository with

    git clone https://github.com/umilinux/umi-arcx-theme --depth 1 && cd umi-arcx-theme

#### 2. Build and install the theme

    ./autogen.sh --prefix=/usr
    sudo make install

Other options to pass to autogen.sh are

    --disable-transparency     disable transparency in the GTK3 theme
    --disable-light            disable UMI ArcX Light support
    --disable-darker           disable UMI ArcX Darker support
    --disable-dark             disable UMI ArcX Dark support
    --disable-cinnamon         disable Cinnamon support
    --disable-gnome-shell      disable GNOME Shell support
    --disable-gtk2             disable GTK2 support
    --disable-gtk3             disable GTK3 support
    --disable-metacity         disable Metacity support
    --disable-unity            disable Unity support
    --disable-xfwm             disable XFWM support
    --disable-plank                disable Plank theme support
    --disable-openbox              disable Openbox support
    --with-gnome-shell=<version>   build the gnome-shell theme for a specific version
    --with-gtk3=<version>          build the GTK3 theme for a specific version
                                   Note: Normally the correct version is detected automatically
                                   and these options should not be needed.

After the installation is complete the theme can be activated with `gnome-tweak-tool` or a similar program by selecting `UMI-ArcX`, `UMI-ArcX-Darker` or `UMI-ArcX-Dark` as Window/GTK+ theme and `UMI-ArcX` or `UMI-ArcX-Dark` as GNOME Shell/Cinnamon theme.

If the `--disable-transparency` option was used, the theme will be installed as `UMI-ArcX-solid`, `UMI-ArcX-Darker-solid` and `UMI-ArcX-Dark-solid`.

#### Uninstall the theme

Run

    sudo make uninstall

from the same directory as this README resides in, or

     sudo rm -rf /usr/share/themes/{umi-arcx,umi-arcx-darker,umi-arcx-dark,umi-arcx-solid,umi-arcx-darker-solid,umi-arcx-dark-solid}

### Extras

### UMI ArcX KDE

A port of Arc for the Plasma 5 desktop with a few additions and extras. Available [here](https://github.com/PapirusDevelopmentTeam/arc-kde).

#### Plank theme

As of version `20180201` the plank theme will be installed along with the normal Arc-Flatabulous gtk theme. You can disable the install by passing `disable-plank` to the autogen command.
Now open the Plank preferences window by executing `plank --preferences` from a terminal and select `Gtk+` as the theme.

### Troubleshooting

If you use Ubuntu with a newer GTK/GNOME version than the one included by default (i.e Ubuntu 14.04 with GTK 3.14 or Ubuntu 15.04 with GTK 3.16, etc.) the prebuilt packages won't work properly and the theme has to be installed manually as described above.
This is also true for other distros with a different GTK/GNOME version than the one included by default

If you get artifacts like black or invisible backgrounds under Unity, disable overlay scrollbars with

    gsettings set com.canonical.desktop.interface scrollbar-mode normal

## Bugs

If you find a bug, please report it at https://github.com/umilinux/umi-arcx-theme/issues

## License

UMI ArcX is available under the terms of the GPL-3.0. See `COPYING` for details.

## Full Preview

![A full screenshot of the Arc theme](http://tnga.github.io/sharedbazar/_assets/images/umi-mvx-lde-screenshot-20190508155116.png)
<sub>Screenshot Details: Icons: [Arc](https://github.com/umilinux/umi-mvx-icons) | [Wallpaper](https://wallpapers.cimiro.com/wp-content/uploads/sites/4/2019/01/background-beach-beautiful-207135-1.jpg) | Font: Futura Bk bt</sub>

### Credits

* **[horst3180](https://github.com/horst3180)** for creating the [Arc](https://github.com/horst3180/arc-theme) theme.
* **[NicoHood](https://github.com/NicoHood)** and **[fossfreedom](https://github.com/fossfreedom)** for maintaining [Arc](https://github.com/NicoHood/arc-theme).
* **[Anmol Jagetia](https://github.com/anmoljagetia)** for creating the [Flatabulous](https://github.com/anmoljagetia/Flatabulous) theme.
