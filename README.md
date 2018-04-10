# UMI ArcX Theme

UMI ArcX a flat theme with transparent elements, base on Arc theme with "X" picked design, for GTK 3, GTK 2 and GNOME Shell which supports GTK 3 and GTK 2 based desktop environments like GNOME, Unity, Budgie, Pantheon, Xfce, MATE, etc.

## UMI ArcX is available in three variants 

##### UMI-arcx

![A screenshot of the UMI ArcX theme](http://i.imgur.com/Ph5ObOa.png)

##### UMI-arcx-darker

![A screenshot of the UMI ArcX-Darker theme](http://i.imgur.com/NC6dqyl.png)

##### UMI-arcx-Dark

![A screenshot of the UMI ArcX-Dark theme](http://i.imgur.com/5AGlCnA.png)

## Installation

### Manual Installation

To build the theme the follwing packages are required 
* `autoconf`
* `automake`
* `pkg-config` or `pkgconfig` for Fedora
* `libgtk-3-dev` for Debian based distros or `gtk3-devel` for RPM based distros
* `git` to clone the source directory

**Note:** For distributions which don't ship separate development packages, just the GTK 3 package is needed instead of the `-dev` packages.

For the theme to function properly, install the following
* GNOME Shell 3.14 - 3.24, GTK 3.14 - 3.22
* The `gnome-themes-standard` package
* The murrine engine. This has different names depending on the distro.
  * `gtk-engine-murrine` (Arch Linux)
  * `gtk2-engines-murrine` (Debian, Ubuntu, elementary OS)
  * `gtk-murrine-engine` (Fedora)
  * `gtk2-engine-murrine` (openSUSE)
  * `gtk-engines-murrine` (Gentoo)

Install the theme with the following commands

#### 1. Get the source

Clone the git repository with

    git clone https://github.com/umilinux/umi-arcx-theme --depth 1 && cd arc-theme

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

    --with-gnome=<version>     build the theme for a specific GNOME version (3.14, 3.16, 3.18, 3.20, 3.22)
                               Note 1: Normally the correct version is detected automatically and this
                               option should not be needed.
                               Note 2: For GNOME 3.24, use --with-gnome-version=3.22
                               (this works for now, the build system will be improved in the future)

After the installation is complete the theme can be activated with `gnome-tweak-tool` or a similar program by selecting `UMI-ArcX`, `UMI-ArcX-Darker` or `UMI-ArcX-Dark` as Window/GTK+ theme and `UMI-ArcX` or `UMI-ArcX-Dark` as GNOME Shell/Cinnamon theme.

If the `--disable-transparency` option was used, the theme will be installed as `UMI-ArcX-solid`, `UMI-ArcX-Darker-solid` and `UMI-ArcX-Dark-solid`.

## Uninstall

Run

    sudo make uninstall

from the cloned git repository, or

    sudo rm -rf /usr/share/themes/{UMI-ArcX,UMI-ArcX-Darker,UMI-ArcX-Dark}

## Extras

### UMI ArcX KDE
A port of UMI ArcX for the Plasma 5 desktop with a few additions and extras. Available [here](https://github.com/PapirusDevelopmentTeam/arc-kde).

### Arc Firefox theme
A theme for Firefox is available at https://github.com/horst3180/arc-firefox-theme

### Arc icon theme
The Arc icon theme is available at https://github.com/horst3180/arc-icon-theme

### Chrome/Chromium theme
To install the Chrome/Chromium theme go to the `extra/Chrome` folder and drag and drop the arc-theme.crx or arc-dark-theme.crx file into the Chrome/Chromium window. The source of the Chrome themes is located in the source "Chrome/arc-theme" folder.

### Plank theme
To install the Plank theme, copy the `extra/Arc-Plank` folder to `~/.local/share/plank/themes` or to `/usr/share/plank/themes` for system-wide use.
Now open the Plank preferences window by executing `plank --preferences` from a terminal and select `Arc-Plank` as the theme.

### Arc-Dark for Ubuntu Software Center
The Arc Dark theme for the Ubuntu Software Center by [mervick](https://github.com/mervick) can be installed from [here](https://github.com/mervick/arc-dark-software-center). It solves readability issues with Arc Dark and the Ubuntu Software Center.

## Troubleshooting

If you use Ubuntu with a newer GTK/GNOME version than the one included by default (i.e Ubuntu 14.04 with GTK 3.14 or Ubuntu 15.04 with GTK 3.16, etc.) the prebuilt packages won't work properly and the theme has to be installed manually as described above.
This is also true for other distros with a different GTK/GNOME version than the one included by default

--

If you get artifacts like black or invisible backgrounds under Unity, disable overlay scrollbars with

    gsettings set com.canonical.desktop.interface scrollbar-mode normal


## Bugs
If you find a bug, please report it at https://github.com/umilinux/umi-arcx-theme/issues

## License
UMI ArcX is available under the terms of the GPL-3.0. See `COPYING` for details.

## Full Preview
![A full screenshot of the Arc theme](http://i.imgur.com/tD1OBQ3.png)
<sub>Screenshot Details: Icons: [Arc](https://github.com/umilinux/umi-arcx-theme) | Launcher Icons based on [White Pixel Icons](http://darkdawg.deviantart.com/art/White-Pixel-Icons-252310560) | [Wallpaper](https://pixabay.com/photo-869593/) | Font: Futura Bk bt</sub>

