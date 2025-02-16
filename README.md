# Asus fliplock driver

[![License: GPLv2](https://img.shields.io/badge/License-GPL_v2-blue.svg)](https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html)
![Maintainer](https://img.shields.io/badge/maintainer-ldrahnik-blue)
[![GitHub Release](https://img.shields.io/github/release/asus-linux-drivers/asus-fliplock-driver.svg?style=flat)](https://github.com/asus-linux-drivers/asus-fliplock-driver/releases)
[![GitHub commits](https://img.shields.io/github/commits-since/asus-linux-drivers/asus-fliplock-driver/v1.1.0.svg)](https://GitHub.com/asus-linux-drivers/asus-fliplock-driver/commit/)
[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fasus-linux-drivers%2Fasus-fliplock-driver&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)

If you find the project useful, do not forget to give project a [![GitHub stars](https://img.shields.io/github/stars/asus-linux-drivers/asus-fliplock-driver.svg?style=flat-square)](https://github.com/asus-linux-drivers/asus-fliplock-driver/stargazers) People already did!

## TODO

- [ ] Not supported AMD devices as it looks like AMD devices does not send events to which could this driver hook on (https://github.com/asus-linux-drivers/asus-fliplock-driver/issues/3, https://github.com/asus-linux-drivers/asus-fliplock-driver/issues/10)

## Changelog

[CHANGELOG.md](CHANGELOG.md)

## Features

- By default disable backlight of keyboard in tablet mode, Remember latest backlight levels via temp file located in `/tmp`
- By default disable backlight of NumLock key in tablet mode
- By default disable backlight of NumberPad in tablet mode, remember latest backlight level via temp file located in `/tmp`
- By default disable backlight of MicMute key in tablet mode, remember latest backlight level via temp file located in `/tmp`
- When does not exist device `Intel HID switches` yet, driver will try find again every 5s and will use for first time flip event from `Asus WMI hotkeys`, concretely will catch configurable key, by default `EV_KEY.KEY_PROG2`

## Preview

![gif preview](./preview.gif)

<br/>


## Installation

You can get the latest ASUS fliplock driver for Linux from Git and install it using the following commands.
```
git clone https://github.com/asus-linux-drivers/asus-fliplock-driver
cd asus-fliplock-driver
sudo ./install.sh
```

To uninstall, just run:
```
sudo ./uninstall.sh
```

**Troubleshooting**

To activate logger, do in a console:
```
LOG=DEBUG sudo -E ./asus_fliplock.py "default"
```

## Existing similar projects

- [ruby] https://github.com/alesya-h/linux_detect_tablet_mode

**Why was this project created?** Easy installation/uninstallation and with default config aimed for Asus laptops.
