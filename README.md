# tubes #

An AppIndicator to tell you if the Intertubes are clogged. Works on Ubuntu with unity or gnome shell, and should work on any other DE that supports AppIndicator. 

Tries to ping The Google all the time, and tells you if the pongs are making it back through the internets.

**Green icon**

![green-example.png](https://bitbucket.org/cbillington/tubes/raw/default/green-example.png)

The interwebs are shiny.

**Yellow icon**

![yellow-example.png](https://bitbucket.org/cbillington/tubes/raw/default/yellow-example.png)

The tubes to The Google are slightly clogged.

**Red icon**

![red-example.png](https://bitbucket.org/cbillington/tubes/raw/default/red-example.png)

You have no internets.

### Installation ###

Installation on Ubuntu (tested on 17.10 and 18.04) requires the package ``gir1.2-appindicator3-0.1`` (or newer), installable with apt-get.
If on some other OS you'll need to get whatever packages allow you to use AppIndicators.
On gnome-shell, the appindicators gnome shell extension is also required (installed by default in Ubuntu)

Once you have whatever dependencies are required for AppIndicators to work on your DE, `tubes` is one file, put it somewhere, chmod +x it and add it to your startup programs.

The following should do the trick:

```
#!bash

sudo wget -O /usr/bin/tubes https://bitbucket.org/cbillington/tubes/raw/default/tubes
sudo chmod +x /usr/bin/tubes
echo "[Desktop Entry]
Type=Application
Exec=tubes" > ~/.config/autostart/tubes.desktop
tubes &

```