# FireKatt 3 Home Assistant Configuration

[![Travis Build](https://img.shields.io/travis/FireBall1725/homeassistant_configuration/master?label=Build&logo=Travis&style=for-the-badge)](https://travis-ci.org/FireBall1725/homeassistant_configuration)
![License](https://img.shields.io/github/license/FireBall1725/homeassistant_configuration?style=for-the-badge)
[![Discord](https://img.shields.io/discord/149023060199079936?logo=Discord&style=for-the-badge)](https://discord.gg/fireball1725)

## About
This repo is the Home Assistant configuration that is currently running all the automations in our house.

When we started doing home automation back at FireKatt 1 we started with the Samsung Smartthings bridge. We quickly outgrew that and when we first looked at Home Assistant the configuration seemed complicated, but thanks to the handful of people out there that have open sourced their configuration we were able to learn and figure out how to use Home Assistant. Because of that we have decided to share our configuration as well in hopes that it will help other people.

Note about the disabled packages directory. As we have moved and /or things have changed we have automations and configurations that no longer apply. These files should still be good as they came from a working state, but they might not work due to updates with Home Assistant.

## Bridges
This is the list of the bridges and the devices that we use with these bridges

### [Abode](https://goabode.com/)
We were looking for an alarm system that would allow us to share the sensors with Home Assistant so we wouldn't have to use two sensors at each point of entry. Abode at the time seemed to have the best integration with Home Assistant

#### Used for:
* Door Sensors
* Window Sensors
* Room Motion Sensors

### [ESPHome](https://esphome.io/)
ESPHome is a pretty cool integration that lets you control ESP32 and ESP8266 boards with Home Assistant. Currently we are using them to read some sensors, but we have plans to add other things with ESP32's later on

#### Used for:
* Xiaomi MiJia Sensors

### [Phillips Hue](https://www.meethue.com/)
Hue is our main bridge for light bulbs and some of the ceiling lights too

#### Used for:
* Light Bulbs

### [OSRAM Lightify](https://www.osram.com/cb/lightify/index.jsp)
When looking for RGB Can Lights we found that we could order the Lightify lights in bulk for pretty cheap off Amazon.

#### Used for:
* Ceiling Lights

### [MyQ](https://www.myq.com/)
We used this to control our garage door at FireKatt 2, currently not in use as our current garage needs upgrading

#### Used for:
* Garage Door

### [Nest](https://www.nest.com)
We used to use Nest for our thermostats and cameras, however due to their API we have been looking to replace Nest for something else. We wouldn't recommend using Nest unless they open their API again in the future.

#### Used for:
* Thermostats
* Cameras

### [Raincloud](https://www.melnor.com/product/raincloud-smart-water-timer/)
We used raincloud to control the watering of our plans. The bridge and their online API has had contant issues, currently looking for a replacement.

#### Used for:
* Irrigation

### [Vera](https://getvera.com/)
Because we run Home Assistant in our Nomad (docker) cluster at home we needed a way to control Z-Wave and ZigBee devices without the need for dongles. Vera has been working well for being that bridge.

#### Used for:
* Z-Wave
* ZigBee

### [Lutron](http://www.lutron.com/en-US/Products/Pages/Components/PicoWirelessController/Overview.aspx)
We were looking for a light switch replacement that would work well with Home Assistant, the Lutron Pro and Pico switches have worked well for this.

#### Used for:
* Light switches

## Custom Components
We use the following custom components in Home Assistant
  * [hacs](https://github.com/hacs/integration)
  * [lutron_caseta_pro](https://github.com/upsert/lutron-caseta-pro)
  * [smartweatherudp](https://github.com/briis/smartweatherudp)

## License
Copyright 2020 Erin Reed / FireBall1725

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.