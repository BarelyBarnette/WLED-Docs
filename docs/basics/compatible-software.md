---
title: Compatible Software
hide:
  # - navigation
  # - toc
---

!!! note ""
    Still under construction, feel free to add to the list!

This page lists some third-party software that can interface with WLED!

## Controllers
Controllers use the WLED API to change the current light settings.

| Name | Description |
|---|---|
[WLED-GUI](https://github.com/WoodyLetsCode/WLED-GUI) | This is a cross-platform desktop app for WLED. You can use it on Windows, Linux and Mac.
[Home Assistant](https://www.home-assistant.io/integrations/wled/) | Versatile and feature rich home automation system. Out-of-the-box WLED integration with automatic discovery.
[ioBroker adapter](https://github.com/iobroker-community-adapters/ioBroker.wled) | Versatile and feature rich home automation system. Out-of-the-box WLED integration with automatic discovery.
[openHAB](https://community.openhab.org/t/wled-a-binding-for-controlling-led-strips-and-strings-from-an-opensource-esp8266-project/87286) | Another more professional feature rich home automation system. WLED integration made easy. <a href="https://community.openhab.org/t/solved-wled-please-make-this-work-in-openhab/82783">Link 2</a> |
| [node-red-contrib-wled](https://flows-new.nodered.org/node/node-red-contrib-wled) | [Node-RED](https://nodered.org) nodes for WLED |
| [Lumia Stream](https://lumiastream.com/) | Allows for control of your lights from streaming software |
| [OctoPrint-WLED](https://plugins.octoprint.org/plugins/wled) | Connect your [OctoPrint](https://octoprint.org) install to your WLED install using this plugin to show things like printer status, progress and more! |

## Sources
Source programs generate light data and stream them to WLED in real time.

| Name | Description |
|---|---|
[LedFx](https://github.com/LedFx/LedFx) | A music visualization tool written in Python. Connects to WLED via E1.31 or UDP. [Dr.Zzs tutorial video](https://www.youtube.com/watch?v=ipSfQdfX4fE)
<a href="https://github.com/psieg/Lightpack">Prismatik WLED-WiFi (native)</a> | Ambilight via WiFi or serial - natively supports UDP (WARLS, DRGB, DNRGB protocols).
<a href="https://github.com/Lord-FEAR/Prismatik-WLED-WiFi">Prismatik WLED-WiFi (plugin)</a> | Ambilight via WiFi - a Plugin alternative for Prismatik WLED support.
<a href="http://xlights.org/">xLights</a> | xLights is a Light Sequencer and Show scheduler which works with WLED. Dr.Zzs has made some videos to set it up. <a href="https://www.youtube.com/watch?v=p7wV6A26Gak">Intro Video</a>
[Hyperion.ng](https://hyperion-project.org/) | Hyperion is an open-source Bias or Ambient Lighting implementation which you might know from TV manufacturers. It supports many LED devices and video grabbers. Support for WLED through UDPraw at port 19446 or E1.31. [Tutorial video](https://www.youtube.com/watch?v=SudT6AjwwOM), [Dr.Zzs video](https://youtu.be/urOEHzbV48A?t=649)
[Hyperion (Classic)](https://hyperion-project.org/) | Hyperion is an open-source Bias or Ambient Lighting implementation which you might know from TV manufacturers. It supports many LED devices and video grabbers. Support for WLED through UDPraw at port 19446 or E1.31.
Enigmalight | Ambilight clone for broadcom based linux receivers.  It supports many LED devices. Support for WLED through USB Adalight/Momo. Download to various forums use the WEB search function of your browser.
[Q Light Controller+](https://www.qlcplus.org/) | QLC+ is a free and cross-platform software to control DMX or analog lighting systems like moving heads, dimmers, scanners etc. QLC+ runs on Linux, Windows (XP+), macOS (10.7+) and the Raspberry Pi. WLED can be used with E1.31 (sACN). use major version 4, as 5 is in development.

## Various

| Name | Description |
|---|---|
[Logitech WLED Sync](https://github.com/hkayy/Logitech-WLED-Sync) | Windows tray application to sync Logitech gaming peripherals to WLED.