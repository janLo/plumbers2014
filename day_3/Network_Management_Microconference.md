# Network Management Microconference

* Notes: https://etherpad.fr/p/LPC2014_NetworkManagement
* networkd
  * dhcp from  connman
  * no glib
  * Only about layer3 setup - no wifi/bluetooth/...
  * L3 setup on top of wpasupplicant (replacement for wpa_action?)
  * Is able to react on hotplug
  * "There are bugs"
  * There is a simple c lib to query - dbus api will follow
* NetworkManager
  * 1.0 planned soon (nov 2014?)
  * nmcli is more powerful now
    * Connection editing
    * Interactive editing
  * nmtui - Curses interface to nm
  * split up in plugins wo downsize
  * New network manager will honor manual configurations
  * libnm rewrite
* Connman
  * integrated clients (dhcp, ...)
  * supports teathering
  * do not touch active connections if not configured
  * Multiple agents (user interfaces, ...)
  * per application network configuration ("sessions")
    * policy plugin
  * patches to wpa_supplicant to extend dbus api

