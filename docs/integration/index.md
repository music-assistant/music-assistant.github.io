# Home Assistant Integration

[![latest version](https://img.shields.io/github/release/music-assistant/hass-music-assistant?display_name=tag&include_prereleases&label=latest%20version)](https://github.com/music-assistant/hass-music-assistant/releases)
[![discord](https://img.shields.io/discord/753947050995089438?label=Chat&logo=discord)](https://discord.gg/kaVm8hGpne)
[![hacs](https://img.shields.io/badge/HACS-Default-41BDF5?label=HACS)](https://github.com/hacs/integration)
[![sponsor](https://img.shields.io/github/sponsors/music-assistant?label=sponsors)](https://github.com/sponsors/music-assistant)

![Integration Image](../assets/integration.png){ align = center }

The Music Assistant HA Integration provides a connection between MA and HA. This means that MA players are visible in HA and can be controlled via the HA UI or via automations or scripts. 

HA media player entities, which are not natively available in MA, can be exposed to MA to allow playback on those devices.

[Announcements](announcements.md) from HA in the form of Text to Speech or audio files are fully supported.

With some additional setup voice control of MA via HA is also possible.

The integration can connect to the MA server which is running either as an HA addon or as a docker container on the same or another host system.

The Home Assistant integration consists of 2 parts:

1) The Home Assistant Plug-in provider. This plugin is currently an empty placeholder but will in the future contain some additional features such as allowing the linking of HA player controls (for example an amplifier volume control) to a MA player 

2) The Home Assistant Player Provider. This allows you to use your HA players within MA.
