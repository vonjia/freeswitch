# FreeSWITCH

FreeSWITCH 是一个软件定义的电信技术栈，可将传统专有电信交换机转变为运行在通用硬件上的灵活软件实现。无论是树莓派还是多核服务器，FreeSWITCH 都能释放设备的电信能力。结合托管云平台 SignalWire，FreeSWITCH 可以与外部世界互联，并支持任意规模的扩展。

更多信息请访问 [https://signalwire.com](https://signalwire.com/) 或 <https://github.com/signalwire>。

## 快速开始

FreeSWITCH 的源代码可在 [GitHub](https://github.com/signalwire/freeswitch) 获取。你可以检出开发分支，并为包括 Linux、Windows、MacOSX 和 BSD 在内的多个主流平台进行构建。仓库在线提供问题追踪和拉取请求功能。

更详细的说明请参阅 <https://developer.signalwire.com/freeswitch/FreeSWITCH-Explained/>。

## 获取帮助

如果需要帮助，或者希望使用商业支持版本，可以联系 <coreteam@freeswitch.com>，了解为项目提供专业服务支持的相关信息。

## VoIP 服务——SIP / SMS / 应用集成

[SignalWire](https://signalwire.com) 是 FreeSWITCH 项目的主要赞助者，由 FreeSWITCH 的原始开发者创立。SignalWire 提供可扩展的服务，用于增强和扩展你的项目，包括 SMS、SIP、无服务器应用托管以及可编程电信服务。本代码库中提供的 mod\_signalwire 模块可以让你快速连接 SignalWire，并扩展 FreeSWITCH 的能力。

## 文档

文档主页如下：

- <https://freeswitch.org/confluence/>

### 发布说明

- <https://freeswitch.org/confluence/display/FREESWITCH/Release+Notes>

### 从软件包安装

以下是从软件包安装 FreeSWITCH 的分步教程：

- [使用 FSGET](/scripts/packaging) \[<b>推荐</b>\]
- [Debian](https://freeswitch.org/confluence/display/FREESWITCH/Debian)
- [树莓派](https://freeswitch.org/confluence/display/FREESWITCH/Raspberry+Pi)
- [CentOS 7](https://freeswitch.org/confluence/display/FREESWITCH/CentOS+7+and+RHEL+7)

### Docker 镜像构建

master Docker 镜像从 SignalWire 软件源安装 FreeSWITCH，需要配置软件源访问令牌。请在仓库根目录执行以下命令。

构建精简镜像：

```powershell
$env:TOKEN = "你的_SignalWire_TOKEN"
docker build --file "docker/master/Dockerfile" `
  --build-arg "TOKEN=$env:TOKEN" `
  --build-arg "FS_META_PACKAGE=freeswitch-meta-vanilla" `
  --tag "freeswitch:master-vanilla" `
  "docker/master"
```

构建全量镜像：

```powershell
$env:TOKEN = "你的_SignalWire_TOKEN"
docker build --file "docker/master/Dockerfile" `
  --build-arg "TOKEN=$env:TOKEN" `
  --build-arg "FS_META_PACKAGE=freeswitch-meta-all" `
  --tag "freeswitch:master-all-local" `
  "docker/master"
```

其中，`freeswitch-meta-vanilla` 为精简功能集，`freeswitch-meta-all` 为全量功能集。请勿将实际 TOKEN 直接写入命令或提交到仓库。

### 从源码构建

以下是从源码构建 FreeSWITCH 及其依赖项的 Dockerfile 示例：

- <https://github.com/signalwire/freeswitch/tree/master/docker/examples>

以下是使用预构建依赖包构建 FreeSWITCH 的分步教程：

- [Debian](https://freeswitch.org/confluence/display/FREESWITCH/Debian#Debian-buildfromsource) \[<b>推荐</b>\]
- [树莓派](https://freeswitch.org/confluence/display/FREESWITCH/Raspberry+Pi)
- [CentOS 7](https://freeswitch.org/confluence/display/FREESWITCH/CentOS+7+and+RHEL+7)

### 构建 Debian 软件包

- [使用 FSDEB](/scripts/packaging/build)

## 下载

- [压缩包](https://files.freeswitch.org/releases/freeswitch/)
- [Windows 安装程序](http://files.freeswitch.org/windows/installer/x64/)
- [Windows 声音包](https://github.com/freeswitch/freeswitch-sounds/releases)

## 参与贡献

通过 GitHub 提交拉取请求是参与 FreeSWITCH 源代码贡献的推荐方式：

- <https://github.com/signalwire/freeswitch/pulls>

## 社区

Slack 是我们的聊天平台，FreeSWITCH 的开发者、团队成员以及活跃用户都在这里交流。
你可以在这里更快地获得答案，并与其他用户实时交流。只需在 Slack 注册页面填写邮箱并完成验证，即可加入讨论。

Slack 社区：

- <https://signalwire.community/>

邮件列表（已归档）：

- <http://lists.freeswitch.org/pipermail/freeswitch-users/>

**感谢你使用 FreeSWITCH！**
