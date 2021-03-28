Fan controller for XPS15.
-------------------------
Søren Rasmussen, 2021

The BIOS fan control in XPS15 is terrible. This works as an override.
Works with 9560 (bios 1.21.0), probably also 9570.

The XPS15 has two fans on a shared heatsink. One is closer to the CPU and one is closer to the GPU.
Each fan has three levels: Off(0), Mid(1), High(2). These are treated as 4 "virtual" fans.
For example, when the config states that 3 fans should be turned on, one fan will be at level 1 and
the other will be at level 2. Which one is higher is determined by CPU vs GPU has a higher temperature.


Requirements: i8kutils and the Nvidia driver

Install: `sudo ./install`
Uninstall: `sudo ./uninstall`

Configuration: `/etc/xpsfan.conf`

Manual start/stop/restart/status:
    `sudo service xpsfan start/stop/restart/status`
