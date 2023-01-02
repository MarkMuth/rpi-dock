# rpi-dock
Turn your Raspberry Pi into a docking station for your Ubuntu Touch phone.

Overview created with [Gnome: Dia](https://wiki.gnome.org/action/show/Apps/Dia?action=show&redirect=Dia)

# Overview

![Overview](https://github.com/MarkMuth/rpi-dock/blob/main/doc/Overview/Overview.png)

# Working

- Internet via RNDIS
  - View [UBPorts: Reverse Tethering](https://docs.ubports.com/en/latest/userguide/advanceduse/reverse-tethering.html)

# Partially Working

- Keyboard and Mouse via USB/IP
  - View [ubuntuusers: USBIP](https://wiki.ubuntuusers.de/USBIP/)
  - Ubuntu Touch comes without the `usbip` binary and the `vhci-hcd` kernel module
  - Ubuntu 16.04 comes with a very much outdated version of `usbip`
    - `usbip 0.1.7 ($Id: vhci_attach.c 42 2007-09-07 12:07:51Z hirofuchi $)`
  - Tested on a normal PC with Ubuntu 22.04 however and that works

# Work in Progress / Ideas Welcome

- Use HDMI display of rpi as virtual display of UT device
  - Could [evdi](https://github.com/DisplayLink/evdi) be a solution?
  - My idea right now:
    - Switch to a VT on Raspberry Pi that only shows a full screen image and refreshes that image whenever a new one is received over the network.
    - Run a service on Raspberry Pi that publishes that display as a virtual display that can be used from UT
