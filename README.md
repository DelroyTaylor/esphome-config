| Repository Status | ESPHome Community |
| :--- | :--- |
| [![last commit time][github-last-commit]][github-master] [![GitHub Activity][commits-shield]][commits] | [![Discord][discord-shield]][discord] [![Community Forum][discourse-shield]][discourse]  | 
 
# My ESPHome Devices
Configuration files for my ESP8266 / ESP32 plugs and boards for use with Home Assistant. I have made heavy use of `!include` files to limit code duplication. This allows me to focus on the advanced code I create for projects like my Bathroom Fan Controller and my Irrigation Controller.

## Common configuration files
### /common/
In the common folder you will find repetitive configuration blocks representing status light, wifi, api, and logging. The Sonoff and Tuya Plugs share common code in the /common/templates/ folder. @AlexMekkering thank you for [showing us how powerful this is][config-includes].

## Device
  # ============================================= #
Sonoff 4ch Pro R2

Orbit Heavy duty sprinkler valves
  
I forked this repo to use @bruxy70 and #BrianHanifin` code to program my own Irrigation Controller. I use Home Assistant and ESPHome web interface instead of a display. Duplicated zones 1 and 2 to and increase to 4 zones in irrigation.yaml. 
I found operating the push buttons on the sonoff worked intermittenly. Changed binary_sensors debounce filters and trigger settings.
  # ============================================= #

### Irrigation Controller: irrigation.yaml
#### [Sonoff 4ch Pro R2][esphome-sonoff4pro]
Our battery and cloud powered Melnor Raincloud/Aquatimer has been flaky off and on for years. Now even new batteries aren't resolving the problem. Also, there appears to be possible battery acid inside the battery compartment. I suspect the wireless radio may be dead despite being able to manually toggle the valves.

The ESPHome projects I have done around our house have been extremely reliable and useful additions to our smart home. Recently, the [ESPHome Examples][esphome-examples] site featured @bruxy70's [Irrigation with display][irrigation-with-display] project that turned a Sonoff 4 channel Pro unit into an irrigation controller, which inspired me. That project features a nifty touch screen display. But since the controller will be far out of the way on the side yard, the user interface can be handled by Home Assistant.

Modified from #BrianHanifin
See contact info below
## Questions?
Ask on the [ESPHome #general channel on Discord][discord]. Use `#BrianHanifin` to tag Brian.


[commits-shield]: https://img.shields.io/github/commit-activity/m/brianhanifin/esphome-config.svg
[commits]: https://github.com/brianhanifin/esphome-config/commits/master
[github-last-commit]: https://img.shields.io/github/last-commit/BrianHanifin/esphome-config.svg?style=plasticr
[github-master]: https://github.com/BrianHanifin/esphome-config/commits/master
[discord-shield]: https://img.shields.io/discord/330944238910963714.svg?logo=discord&color=7289da
[discord]: https://discord.gg/A7SaaSC
[discourse-shield]: https://img.shields.io/discourse/topics?color=46B4ED&label=community&logo=discourse&logoColor=46B4ED&server=https%3A%2F%2Fcommunity.home-assistant.io
[discourse]: https://community.home-assistant.io/u/brianhanifin/summary

[esphome-ble-hub]:https://esphome.io/components/esp32_ble_tracker.html
[esphome-sonoff4pro]:https://esphome.io/devices/sonoff_4ch.html
[esphome-sonoff-basic]:https://esphome.io/devices/sonoff_basic.html
[esphome-examples]:https://esphome.io/guides/diy.html
[config-includes]:https://github.com/AlexMekkering/esphome-config
[irrigation-with-display]:https://github.com/bruxy70/Irrigation-with-display
