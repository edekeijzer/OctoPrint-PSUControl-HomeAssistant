# OctoPrint PSU Control - Home Assistant
Adds Home Assistant support to OctoPrint-PSUControl as a sub-plugin

## Setup
- Install the plugin using Plugin Manager from Settings
- Configure this plugin
- Select this plugin as Switching *and* Sensing method in [PSU Control](https://github.com/kantlivelong/OctoPrint-PSUControl)
- :warning: **Turn off** the *Automatically turn PSU ON* option in the PSU Control settings, leaving this on will ruin your prints when Home Assistant becomes unavailable :warning: (some explanation in tickets
[#4](https://github.com/edekeijzer/OctoPrint-PSUControl-HomeAssistant/issues/4), 
[#11](https://github.com/edekeijzer/OctoPrint-PSUControl-HomeAssistant/issues/11), 
[#16](https://github.com/edekeijzer/OctoPrint-PSUControl-HomeAssistant/issues/16))

## Configuration
* Enter the URL of your Home Assistant Installation
* Go to your Home Assistant profile
* At the bottom, go to *Long-Lived Access Tokens*
* Click *Create Token*, give the token a name (suggestion: OctoPrint PSUControl) and click *OK*
* Copy the token and paste it into the *Access token* field in the plugin settings
* At *Entity ID* enter the ID of the Home Assistant entity you want to control (for example: *switch.my_smart_outlet*)
* If your HA installation is running HTTPS with a self-signed certificate, uncheck the *Verify certificate* option

## Support
Please check your logs first. If they do not explain your issue, open an issue in GitHub. Please set *octoprint.plugins.psucontrol* and *octoprint.plugins.psucontrol_homeassistant* to **DEBUG** and include the relevant logs. Feature requests are welcome as well.

## Todo
- [x] Add descriptions to settings page
- [ ] Add images to documentation
