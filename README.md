# luci-theme-ifit

[![license](https://img.shields.io/badge/license-Apache2-brightgreen.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/kenzok78/luci-theme-infinityfreedom/pulls)
[![Release](https://img.shields.io/badge/release-v2.0-orange.svg?)](https://github.com/kenzok78/luci-theme-infinityfreedom/releases)

ifit 是一个为 OpenWrt 设计的简洁 HTML5 LuCI 主题，基于 luci-theme-infinityfreedom-ng 优化而来。基于 Bootstrap 5 和 Vue.js，支持深色模式，适配 PC、平板和手机等设备。

## 功能特性

<small>

- Bootstrap 5 + Vue.js 3
- 深色/浅色模式切换
- 响应式设计（PC/平板/手机）
- Font Awesome 图标
- Lottie 动画加载
- Material Design 风格

</small>

## 系统要求

<small>

- OpenWrt 18.06 或更高版本
- LuCI Web 界面

</small>

## 安装

### 从源码编译

```bash
# 添加到 feeds.conf.default
src-git ifit https://github.com/kenzok78/luci-theme-infinityfreedom.git

# 更新并安装
./scripts/feeds update ifit
./scripts/feeds install luci-theme-ifit
make menuconfig
```

### 仅编译主题

```bash
make package/luci-theme-ifit/compile V=s
```

### 在线安装

```bash
opkg update
opkg install luci-theme-ifit
```

## 配置

安装完成后，进入 **系统 → 系统 → 语言和样式** 选择 `ifit` 主题。

## 目录结构

```
luci-theme-ifit/
├── Makefile
├── files/
│   ├── 10_luci-theme-ifit          # UCI 默认配置
│   ├── htdocs/
│   │   ├── css/                    # 样式表
│   │   ├── js/                     # JavaScript
│   │   ├── fonts/                  # 图标字体
│   │   └── images/                 # 图片
│   └── templates/
│       ├── header.htm              # 主模板
│       ├── header_login.htm         # 登录页头
│       ├── sysauth.htm             # 登录表单
│       └── footer.htm              # 页脚
└── screenshots/
```

## 截图

![登录](/screenshots/000.Login.png)
![概览](/screenshots/001.Overview.png)

## 致谢

<small>

- 原始主题：[luci-theme-infinityfreedom](https://github.com/xiaoqingfengATGH/luci-theme-infinityfreedom) by Eric
- Bootstrap: https://getbootstrap.com/
- Vue.js: https://vuejs.org/

</small>

## 许可证

Apache License 2.0

## 更新日志

### v2.0.0 (2026-03-22)

<small>

- 主题重命名：`infinityfreedom-ng` 改为 `ifit`
- 优化目录结构
- 修复 `boardinfo` 变量覆盖 bug
- 更新 CSS/JS 路径
- 更新版权和维护者信息
- 清理 uci-defaults 脚本

</small>

### v1.51 (2024-07-31)

<small>

- 原始 infinityfreedom-ng 版本发布

</small>
