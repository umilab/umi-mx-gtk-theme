# Arc-Flatabulous Theme
Arc-Flatabulous theme is the [Arc](https://github.com/horst3180/arc-theme) theme with [Flatabulous](https://github.com/anmoljagetia/Flatabulous) window controls.

### Arc-Flatabulous is available in three variants 

##### Arc-Flatabulous

![A screenshot of the Arc-Flatabulous theme](http://i.imgur.com/sGOEK6L.png)

##### Arc-Flatabulous-Darker

![A screenshot of the Arc-Flatabulous-Darker theme](http://i.imgur.com/gneZsVQ.png)

##### Arc-Flatabulous-Dark

![A screenshot of the Arc-Flatabulous-Dark theme](http://i.imgur.com/zUC1pHT.png)

### Installation

**Important:** Remove all older versions of the theme from your system before you proceed any further.
	
    sudo rm -rf /usr/share/themes/{Arc-Flatabulous,Arc-Flatabulous-Darker,Arc-Flatabulous-Dark,Arc-Flatabulous-Solid,Arc-Flatabulous-Darker-Solid,Arc-Flatabulous-Dark-Solid}
    rm -rf ~/.local/share/themes/{Arc-Flatabulous,Arc-Flatabulous-Darker,Arc-Flatabulous-Dark,Arc-Flatabulous-Solid,Arc-Flatabulous-Darker-Solid,Arc-Flatabulous-Dark-Solid}
    rm -rf ~/.themes/{Arc-Flatabulous,Arc-Flatabulous-Darker,Arc-Flatabulous-Dark,Arc-Flatabulous-Solid,Arc-Flatabulous-Darker-Solid,Arc-Flatabulous-Dark-Solid}

#### Packages

Arch Linux users can install the theme from the AUR https://aur.archlinux.org/packages/gtk-arc-flatabulous-theme-git/
	
#### Manual Installation

To build the theme the follwing packages are required
* `autoconf`
* `automake`
* `sassc`
* `pkg-config` or `pkgconfig` for Fedora
* `libgtk-3-dev` for Debian based distros or `gtk3-devel` for RPM based distros
* `git` to clone the source directory

**Note:** For distributions which don't ship separate development packages, just the GTK 3 package is needed instead of the `-dev` packages.

For the theme to function properly, install the following
* GNOME Shell 3.18 - 3.26, GTK 3.18 - 3.22
* The `gnome-themes-standard` package
* The murrine engine. This has different names depending on the distro.
  * `gtk-engine-murrine` (Arch Linux)
  * `gtk2-engines-murrine` (Debian, Ubuntu, elementary OS)
  * `gtk-murrine-engine` (Fedora)
  * `gtk2-engine-murrine` (openSUSE)
  * `gtk-engines-murrine` (Gentoo)

Install the theme with the following commands

**1. Get the source**

If you want to install the latest version from git, clone the repository with

    git clone https://github.com/andreisergiu98/arc-flatabulous-theme --depth 1 && cd arc-flatabulous-theme

**2. Build and install the theme**

    ./autogen.sh --prefix=/usr
    sudo make install

Other options to pass to autogen.sh are

    --disable-transparency     disable transparency in the GTK3 theme
    --disable-light            disable Arc Light support
    --disable-darker           disable Arc Darker support
    --disable-dark             disable Arc Dark support
    --disable-cinnamon         disable Cinnamon support
    --disable-gnome-shell      disable GNOME Shell support
    --disable-gtk2             disable GTK2 support
    --disable-gtk3             disable GTK3 support
    --disable-metacity         disable Metacity support
    --disable-unity            disable Unity support
    --disable-xfwm             disable XFWM support
    --disable-plank            disable Plank theme support

    --with-gnome=<version>     build the theme for a specific GNOME version (3.18, 3.20, 3.22)
                               Note 1: Normally the correct version is detected automatically and this
                               option should not be needed.
                               Note 2: For GNOME 3.24 and 3.26, use --with-gnome-version=3.22
                               (this works for now, the build system will be improved in the future)
    --with-custom=<script>     run the executable script file in the custom subfolder

After the installation is complete you can activate the theme with `gnome-tweak-tool` or a similar program by selecting `Arc-Flatabulous`, `Arc-Flatabulous-Darker` or `Arc-Flatabulous-Dark` as Window/GTK+ theme and `Arc-Flatabulous` or `Arc-Flatabulous-Dark` as Gnome-Shell and Xfce-Notify theme.

If the `--disable-transparency` option was used, the theme will be installed as `Arc-Flatabulous-Solid`, `Arc-Flatabulous-Darker-Solid` and `Arc-Flatabulous-Dark-Solid`.

**Uninstall the theme**

Run

    sudo make uninstall

from the same directory as this README resides in, or

    sudo rm -rf /usr/share/themes/{Arc-Flatabulous,Arc-Flatabulous-Darker,Arc-Flatabulous-Dark,Arc-Flatabulous-Solid,Arc-Flatabulous-Darker-Solid,Arc-Flatabulous-Dark-Solid}

### Extras

#### Arc icon theme
The Arc icon theme is available at https://github.com/horst3180/arc-icon-theme


#### Arc KDE
A port of Arc for the Plasma 5 desktop with a few additions and extras. Available [here](https://github.com/PapirusDevelopmentTeam/arc-kde).

#### Arc icon theme
The Arc icon theme is available at https://github.com/horst3180/arc-icon-theme

#### Plank theme
As of version `20180201` the plank theme will be installed along with the normal Arc-Flatabulous gtk theme. You can disable the install by passing `disable-plank` to the autogen command.
Now open the Plank preferences window by executing `plank --preferences` from a terminal and select `Gtk+` as the theme.


#### Arc-Dark for Ubuntu Software Center
The Arc Dark theme for the Ubuntu Software Center by [mervick](https://github.com/mervick) can be installed from [here](https://github.com/mervick/arc-dark-software-center). It solves readability issues with Arc Dark and the Ubuntu Software Center.

### Troubleshooting

If you use Ubuntu with a newer GTK/GNOME version than the one included by default (i.e Ubuntu 14.04 with GTK 3.14 or Ubuntu 15.04 with GTK 3.16, etc.) the prebuilt packages won't work properly and the theme has to be installed manually as described above.
This is also true for other distros with a different GTK/GNOME version than the one included by default

If you get artifacts like black or invisible backgrounds under Unity, disable overlay scrollbars with

    gsettings set com.canonical.desktop.interface scrollbar-mode normal

### License
Arc is available under the terms the GPL-3.0. See `COPYING` for details.

### Full Preview
![A full screenshot of the Arc-Flatabulous theme](http://i.imgur.com/4JSTAFB.jpg)
<sub>Screenshot Details: Icons: [Numix Circle](https://github.com/numixproject/numix-icon-theme-circle) | [Wallpaper](https://github.com/GNOME/gnome-backgrounds/blob/master/backgrounds/Waves.jpg) | Font: [Source Sans Pro](https://github.com/adobe-fonts/source-sans-pro)</sub>

## Bugs
If you find a bug, please report it at https://github.com/andreisergiu98/arc-flatabulous-theme/issues

### Credits
* **[horst3180](https://github.com/horst3180)** for creating the [Arc](https://github.com/horst3180/arc-theme) theme.
* **[NicoHood](https://github.com/NicoHood)** and **[fossfreedom](https://github.com/fossfreedom)** for maintaining [Arc](https://github.com/NicoHood/arc-theme).
* **[Anmol Jagetia](https://github.com/anmoljagetia)** for creating the [Flatabulous](https://github.com/anmoljagetia/Flatabulous) theme.
