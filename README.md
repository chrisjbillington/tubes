# tubes #

<img src="https://raw.githubusercontent.com/chrisjbillington/tubes/master/logo.png"
width="320" height="160" />

An AppIndicator to tell you if the Intertubes are clogged. Works on any Linux desktop
environment that supports AppIndicators.

Tries to ping Google, and tells you if the pongs are making it back through the pipes.

**Green icon**

![green-example.png](https://raw.githubusercontent.com/chrisjbillington/tubes/master/green-example.png)

The tubes are clear.

**Yellow icon**

![yellow-example.png](https://raw.githubusercontent.com/chrisjbillington/tubes/master/yellow-example.png)

The tubes slightly clogged.

**Red icon**

![red-example.png](https://raw.githubusercontent.com/chrisjbillington/tubes/master/red-example.png)

You have no internet.

### Project status ###

This project is stable. It doesn't require much maintenance, and I've been using it
mostly unchanged since 2015 (it is 2021 at time of writing). So if you see that there
haven't been many commits lately, don't worry - it is not abandoned. Please report any
bugs.

### Installation ###

To get the required libappindicator packages, install the appropriate package for your
distro:

Ubuntu/Debian:
```bash
sudo apt-get install gir1.2-appindicator3-0.1
```

Arch/Manjaro:
```bash
sudo pacman -S libappindicator-gtk3
```

If using GNOME, you'll also need  the [KStatusNotifierItem/AppIndicator
Support](https://extensions.gnome.org/extension/615/appindicator-support/) GNOME shell
extension. You can skip this if you're on Ubuntu, since it is already installed.

Once you have whatever dependencies are required for AppIndicators to work on your
distro, `tubes` is one file, put it somewhere, `chmod +x` it and add it to your startup
programs.

The following should do the trick:

```bash
sudo curl -o /usr/bin/tubes https://raw.githubusercontent.com/chrisjbillington/tubes/master/tubes
sudo chmod +x /usr/bin/tubes
echo "[Desktop Entry]
Type=Application
Exec=tubes" > ~/.config/autostart/tubes.desktop
tubes &
```
