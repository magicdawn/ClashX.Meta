<h1 align="center">
  <img src="https://github.com/MetaCubeX/Clash.Meta/raw/Meta/Meta.png" alt="Clash" width="200">
  <br>
  ClashX
  <br>
</h1>


A rule based proxy For Mac base on [Clash Meta](https://github.com/MetaCubeX/Clash.Meta).


## Features

- Clash.Meta Core
- Tun mode support

## Install

You can download from [Release](https://github.com/MetaCubeX/Clash.Meta/releases) page


## Build
- Make sure have python3 and golang installed in your computer.

- Install Golang
  ```
  brew install golang

  or download from https://golang.org
  ```

- Download deps
  ```
  bash install_dependency.sh
  ```

- Build and run.

## Config


The default configuration directory is `$HOME/.config/clash`

The default name of the configuration file is `config.yaml`. You can use your custom config name and switch config in menu `Config` section.


Checkout [Clash Meta](https://docs.metacubex.one) or [Clash](https://github.com/Dreamacro/clash) or [SS-Rule-Snippet for Clash](https://github.com/Hackl0us/SS-Rule-Snippet/blob/master/LAZY_RULES/clash.yaml) or [lancellc's gitbook](https://lancellc.gitbook.io/clash/) for more detail.

## Advance Config

### 修改代理端口号
1. 在菜单栏->配置->更多设置中修改对应端口号



### Change your status menu icon

  Place your icon file in the `~/.config/clash/menuImage.png`  then restart ClashX

### Change default system ignore list.

- Change by menu -> Config -> Setting -> Bypass proxy settings for these Hosts & Domains

### URL Schemes (May not work).

- Using url scheme to import remote config.

  ```
  clash://install-config?url=http%3A%2F%2Fexample.com&name=example
  ```
- Using url scheme to reload current config.

  ```
  clash://update-config
  ```

### Get process name

You can add the follow config in your config file, and set your proxy mode to rule. Then open the log via help menu in ClashX.
```
script:
  code: |
    def main(ctx, metadata):
      # Log ProcessName
      ctx.log('Process Name: ' + ctx.resolve_process_name(metadata))
      return 'DIRECT'
```

### FAQ

- Q: How to get shell command with external IP?  
  A: Click the clashX menu icon and then press `Option-Command-C`  

### 关闭ClashX的通知

1. 在系统设置中关闭 clashx 的推送权限
2. 在菜单栏->配置->更多设置中选中减少通知

Note：强烈不推荐这么做，这可能导致clashx的很多重要错误提醒无法显示。

### 全局快捷键

- 设置详情点击 [全局快捷键](Shortcuts.md)