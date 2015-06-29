# tubes #

An Ubuntu indicator to tell you if the Intertubes are clogged.

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

It's one file, `tubes`, put it somewhere, chmod +x it and add it to your startup programs.

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