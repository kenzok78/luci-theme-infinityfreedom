# luci-theme-ifit

[![license](https://img.shields.io/badge/license-Apache2-brightgreen.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/kenzok78/luci-theme-infinityfreedom/pulls)
[![Release](https://img.shields.io/badge/release-v2.0-orange.svg?)](https://github.com/kenzok78/luci-theme-infinityfreedom/releases)

[中文说明](README-zh_cn.md)

ifit is a clean HTML5 LuCI theme for OpenWrt, optimized from luci-theme-infinityfreedom-ng. Based on Bootstrap 5, Vue.js, supports dark mode, responsive layout for PC, Pad, and mobile devices.

## Features

- Bootstrap 5 + Vue.js 3
- Dark/Light mode switching
- Responsive design (PC/Tablet/Mobile)
- Font Awesome icons
- Lottie animation loading
- Material Design inspired

## Requirements

- OpenWrt 18.06 or later
- LuCI Web Interface

## Installation

### Compile from source

```bash
# Add to feeds.conf.default
src-git ifit https://github.com/kenzok78/luci-theme-infinityfreedom.git

# Update and install
./scripts/feeds update ifit
./scripts/feeds install luci-theme-ifit
make menuconfig
```

### Build theme only

```bash
make package/luci-theme-ifit/compile V=s
```

### Online install

```bash
opkg update
opkg install luci-theme-ifit
```

## Configuration

After installation, go to **System → System → Language and Style** and select `ifit` as the theme.

## Directory Structure

```
luci-theme-ifit/
├── Makefile
├── files/
│   ├── 10_luci-theme-ifit          # UCI defaults
│   ├── htdocs/
│   │   ├── css/                    # Stylesheets
│   │   ├── js/                     # JavaScript
│   │   ├── fonts/                  # Icon fonts
│   │   └── images/                 # Images
│   └── templates/
│       ├── header.htm              # Main template
│       ├── header_login.htm         # Login header
│       ├── sysauth.htm             # Login form
│       └── footer.htm              # Footer
└── screenshots/
```

## Screenshots

![Login](/screenshots/000.Login.png)
![Overview](/screenshots/001.Overview.png)

## Credits

- Original theme: [luci-theme-infinityfreedom](https://github.com/xiaoqingfengATGH/luci-theme-infinityfreedom) by Eric
- Bootstrap: https://getbootstrap.com/
- Vue.js: https://vuejs.org/

## License

Apache License 2.0

## Changelog

### v2.0.0 (2026-03-22)

- Rename theme from `infinityfreedom-ng` to `ifit`
- Optimize directory structure
- Fix `boardinfo` variable override bug
- Update CSS/JS paths
- Update copyright and maintainer info
- Clean up uci-defaults script

### v1.51 (2024-07-31)

- Original infinityfreedom-ng release
