以下是文档内容的中文翻译：

---

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
<div align="center">

[![YT-DLP](https://raw.githubusercontent.com/yt-dlp/yt-dlp/master/.github/banner.svg)](#readme)

[![Release version](https://img.shields.io/github/v/release/yt-dlp/yt-dlp?color=brightgreen&label=下载&style=for-the-badge)](#installation "安装")
[![PyPI](https://img.shields.io/badge/-PyPI-blue.svg?logo=pypi&labelColor=555555&style=for-the-badge)](https://pypi.org/project/yt-dlp "PyPI")
[![Donate](https://img.shields.io/badge/_-捐赠-red.svg?logo=githubsponsors&labelColor=555555&style=for-the-badge)](Collaborators.md#collaborators "捐赠")
[![Discord](https://img.shields.io/discord/807245652072857610?color=blue&labelColor=555555&label=&logo=discord&style=for-the-badge)](https://discord.gg/H5MNcFW63r "Discord")
[![Supported Sites](https://img.shields.io/badge/-支持的站点-brightgreen.svg?style=for-the-badge)](supportedsites.md "支持的站点")
[![License: Unlicense](https://img.shields.io/badge/-Unlicense-blue.svg?style=for-the-badge)](LICENSE "许可证")
[![CI Status](https://img.shields.io/github/actions/workflow/status/yt-dlp/yt-dlp/core.yml?branch=master&label=测试&style=for-the-badge)](https://github.com/yt-dlp/yt-dlp/actions "CI 状态")
[![Commits](https://img.shields.io/github/commit-activity/m/yt-dlp/yt-dlp?label=提交&style=for-the-badge)](https://github.com/yt-dlp/yt-dlp/commits "提交历史")
[![Last Commit](https://img.shields.io/github/last-commit/yt-dlp/yt-dlp/master?label=&style=for-the-badge&display_timestamp=committer)](https://github.com/yt-dlp/yt-dlp/pulse/monthly "最后活动")

</div>
<!-- MANPAGE: END EXCLUDED SECTION -->

yt-dlp 是一个功能丰富的命令行音视频下载工具，支持[数千个网站](supportedsites.md)。该项目是基于现已停止开发的 [youtube-dlc](https://github.com/blackjack4494/yt-dlc) 的 [youtube-dl](https://github.com/ytdl-org/youtube-dl) 分支。

<!-- MANPAGE: MOVE "USAGE AND OPTIONS" SECTION HERE -->

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
* [安装](#installation)
    * [详细说明](https://github.com/yt-dlp/yt-dlp/wiki/Installation)
    * [发布文件](#release-files)
    * [更新](#update)
    * [依赖项](#dependencies)
    * [编译](#compile)
* [使用和选项](#usage-and-options)
    * [通用选项](#general-options)
    * [网络选项](#network-options)
    * [地理限制](#geo-restriction)
    * [视频选择](#video-selection)
    * [下载选项](#download-options)
    * [文件系统选项](#filesystem-options)
    * [缩略图选项](#thumbnail-options)
    * [互联网快捷方式选项](#internet-shortcut-options)
    * [详细信息和模拟选项](#verbosity-and-simulation-options)
    * [解决方法](#workarounds)
    * [视频格式选项](#video-format-options)
    * [字幕选项](#subtitle-options)
    * [认证选项](#authentication-options)
    * [后处理选项](#post-processing-options)
    * [SponsorBlock 选项](#sponsorblock-options)
    * [提取器选项](#extractor-options)
* [配置](#configuration)
    * [配置文件编码](#configuration-file-encoding)
    * [使用 netrc 进行认证](#authentication-with-netrc)
    * [关于环境变量的说明](#notes-about-environment-variables)
* [输出模板](#output-template)
    * [输出模板示例](#output-template-examples)
* [格式选择](#format-selection)
    * [过滤格式](#filtering-formats)
    * [排序格式](#sorting-formats)
    * [格式选择示例](#format-selection-examples)
* [修改元数据](#modifying-metadata)
    * [修改元数据示例](#modifying-metadata-examples)
* [提取器参数](#extractor-arguments)
* [插件](#plugins)
    * [安装插件](#installing-plugins)
    * [开发插件](#developing-plugins)
* [嵌入 yt-dlp](#embedding-yt-dlp)
    * [嵌入示例](#embedding-examples)
* [与 youtube-dl 的差异](#changes-from-youtube-dl)
    * [新功能](#new-features)
    * [默认行为的差异](#differences-in-default-behavior)
    * [已弃用的选项](#deprecated-options)
* [贡献](CONTRIBUTING.md#contributing-to-yt-dlp)
    * [提交问题](CONTRIBUTING.md#opening-an-issue)
    * [开发者说明](CONTRIBUTING.md#developer-instructions)
* [Wiki](https://github.com/yt-dlp/yt-dlp/wiki)
    * [常见问题](https://github.com/yt-dlp/yt-dlp/wiki/FAQ)
<!-- MANPAGE: END EXCLUDED SECTION -->


# 安装

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
[![Windows](https://img.shields.io/badge/-Windows_x64-blue.svg?style=for-the-badge&logo=windows)](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp.exe)
[![Unix](https://img.shields.io/badge/-Linux/BSD-red.svg?style=for-the-badge&logo=linux)](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp)
[![MacOS](https://img.shields.io/badge/-MacOS-lightblue.svg?style=for-the-badge&logo=apple)](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_macos)
[![PyPI](https://img.shields.io/badge/-PyPI-blue.svg?logo=pypi&labelColor=555555&style=for-the-badge)](https://pypi.org/project/yt-dlp)
[![Source Tarball](https://img.shields.io/badge/-Source_tar-green.svg?style=for-the-badge)](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp.tar.gz)
[![Other variants](https://img.shields.io/badge/-Other-grey.svg?style=for-the-badge)](#release-files)
[![All versions](https://img.shields.io/badge/-All_Versions-lightgrey.svg?style=for-the-badge)](https://github.com/yt-dlp/yt-dlp/releases)
<!-- MANPAGE: END EXCLUDED SECTION -->

您可以使用[二进制文件](#release-files)、[pip](https://pypi.org/project/yt-dlp) 或第三方包管理器安装 yt-dlp。有关详细说明，请参阅 [wiki](https://github.com/yt-dlp/yt-dlp/wiki/Installation)


<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
## 发布文件

#### 推荐

文件|描述
:---|:---
[yt-dlp](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp)|平台独立的 [zipimport](https://docs.python.org/3/library/zipimport.html) 二进制文件。需要 Python（推荐用于 **Linux/BSD**）
[yt-dlp.exe](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp.exe)|Windows (Win8+) 独立 x64 二进制文件（推荐用于 **Windows**）
[yt-dlp_macos](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_macos)|通用 MacOS (10.15+) 独立可执行文件（推荐用于 **MacOS**）

#### 替代方案

文件|描述
:---|:---
[yt-dlp_x86.exe](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_x86.exe)|Windows (Win8+) 独立 x86 (32 位) 二进制文件
[yt-dlp_linux](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_linux)|Linux 独立 x64 二进制文件
[yt-dlp_linux_armv7l](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_linux_armv7l)|Linux 独立 armv7l (32 位) 二进制文件
[yt-dlp_linux_aarch64](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_linux_aarch64)|Linux 独立 aarch64 (64 位) 二进制文件
[yt-dlp_win.zip](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_win.zip)|未打包的 Windows 可执行文件（无自动更新）
[yt-dlp_macos.zip](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_macos.zip)|未打包的 MacOS (10.15+) 可执行文件（无自动更新）
[yt-dlp_macos_legacy](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_macos_legacy)|MacOS (10.9+) 独立 x64 可执行文件

#### 其他

文件|描述
:---|:---
[yt-dlp.tar.gz](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp.tar.gz)|源码压缩包
[SHA2-512SUMS](https://github.com/yt-dlp/yt-dlp/releases/latest/download/SHA2-512SUMS)|GNU 风格的 SHA512 校验和
[SHA2-512SUMS.sig](https://github.com/yt-dlp/yt-dlp/releases/latest/download/SHA2-512SUMS.sig)|SHA512 校验和的 GPG 签名文件
[SHA2-256SUMS](https://github.com/yt-dlp/yt-dlp/releases/latest/download/SHA2-256SUMS)|GNU 风格的 SHA256 校验和
[SHA2-256SUMS.sig](https://github.com/yt-dlp/yt-dlp/releases/latest/download/SHA2-256SUMS.sig)|SHA256 校验和的 GPG 签名文件

用于验证 GPG 签名的公钥可以在[这里](https://github.com/yt-dlp/yt-dlp/blob/master/public.key)找到。
示例用法：
```
curl -L https://github.com/yt-dlp/yt-dlp/raw/master/public.key | gpg --import
gpg --verify SHA2-256SUMS.sig SHA2-256SUMS
gpg --verify SHA2-512SUMS.sig SHA2-512SUMS
```
<!-- MANPAGE: END EXCLUDED SECTION -->

**注意**：手册页、Shell 自动补全文件等可在[源码压缩包](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp.tar.gz)中找到。


## 更新
如果您使用的是[发布二进制文件](#release-files)，可以使用 `yt-dlp -U` 进行更新。

如果您是通过 [pip 安装](https://github.com/yt-dlp/yt-dlp/wiki/Installation#with-pip)的，只需重新运行用于安装程序的相同命令即可。

对于其他第三方包管理器，请参阅 [wiki](https://github.com/yt-dlp/yt-dlp/wiki/Installation#third-party-package-managers) 或参考其文档。

<a id="update-channels"></a>

目前有三个二进制文件的发布渠道：`stable`、`nightly` 和 `master`。

* `stable` 是默认渠道，其许多更改已经由 `nightly` 和 `master` 渠道的用户测试过。
* `nightly` 渠道每天大约在 UTC 午夜构建一次，用于获取项目的新补丁和更改的快照。这是 **推荐给 yt-dlp 常规用户** 的渠道。`nightly` 版本可以从 [yt-dlp/yt-dlp-nightly-builds](https://github.com/yt-dlp/yt-dlp-nightly-builds/releases) 获取，或者作为 `yt-dlp` PyPI 包的开发版本（可以使用 pip 的 `--pre` 标志安装）。
* `master` 渠道的版本在每次推送到 master 分支后构建，这些版本将包含最新的修复和新增功能，但也可能更容易出现回归问题。它们可以从 [yt-dlp/yt-dlp-master-builds](https://github.com/yt-dlp/yt-dlp-master-builds/releases) 获取。

使用 `--update`/`-U` 时，发布二进制文件只会更新到其当前渠道。
`--update-to CHANNEL` 可用于在有新版本时切换到不同的渠道。`--update-to [CHANNEL@]TAG` 也可用于升级或降级到特定渠道的特定标签。

您还可以使用 `--update-to <repository>` (`<owner>/<repository>`) 更新到完全不同的仓库的渠道。不过要小心更新到哪个仓库，因为来自不同仓库的二进制文件没有进行验证。

示例用法：

* `yt-dlp --update-to master` 切换到 `master` 渠道并更新到其最新版本
* `yt-dlp --update-to stable@2023.07.06` 升级/降级到 `stable` 渠道的标签 `2023.07.06`
* `yt-dlp --update-to 2023.10.07` 如果当前渠道存在标签 `2023.10.07`，则升级/降级到该标签
* `yt-dlp --update-to example/yt-dlp@2023.09.24` 升级/降级到 `example/yt-dlp` 仓库的标签 `2023.09.24`

**重要提示**：任何遇到 `stable` 版本问题的用户应在提交错误报告之前安装或更新到 `nightly` 版本：
```
# 从 stable 可执行文件/二进制文件更新到 nightly：
yt-dlp --update-to nightly

# 使用 pip 安装 nightly：
python3 -m pip install -U --pre "yt-dlp[default]"
```

## 依赖项
支持 Python 3.9+ (CPython) 和 3.10+ (PyPy) 版本。其他版本和实现可能无法正常工作。

<!-- Python 3.5+ uses VC++14 and it is already embedded in the binary created
<!x-- https://www.microsoft.com/en-us/download/details.aspx?id=26999 --x>
On Windows, [Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://download.microsoft.com/download/1/6/5/165255E7-1014-4D0A-B094-B6A430A6BFFC/vcredist_x86.exe) is also necessary to run yt-dlp. You probably already have this, but if the executable throws an error due to missing `MSVCR100.dll` you need to install it manually.
-->

虽然所有其他依赖项都是可选的，但强烈推荐使用 `ffmpeg` 和 `ffprobe`。

### 强烈推荐

* [**ffmpeg** 和 **ffprobe**](https://www.ffmpeg.org) - 用于[合并独立的视频和音频文件](#format-selection)，以及各种[后处理](#post-processing-options)任务。许可证[取决于构建](https://www.ffmpeg.org/legal.html)

    ffmpeg 中存在一些错误，当与 yt-dlp 一起使用时会导致各种问题。由于 ffmpeg 是一个重要的依赖项，我们在 [yt-dlp/FFmpeg-Builds](https://github.com/yt-dlp/FFmpeg-Builds) 提供了[自定义构建](https://github.com/yt-dlp/FFmpeg-Builds#ffmpeg-static-auto-builds)，其中包含一些这些问题的补丁。有关这些构建解决的具体问题的详细信息，请参阅 [README](https://github.com/yt-dlp/FFmpeg-Builds#patches-applied)

    **重要提示**：您需要的是 ffmpeg *二进制文件*，**而不是** [同名的 Python 包](https://pypi.org/project/ffmpeg)

### 网络
* [**certifi**](https://github.com/certifi/python-certifi)\* - 提供 Mozilla 的根证书包。根据 [MPLv2](https://github.com/certifi/python-certifi/blob/master/LICENSE) 许可
* [**brotli**](https://github.com/google/brotli)\* 或 [**brotlicffi**](https://github.com/python-hyper/brotlicffi) - [Brotli](https://en.wikipedia.org/wiki/Brotli) 内容编码支持。两者均根据 MIT 许可 <sup>[1](https://github.com/google/brotli/blob/master/LICENSE) [2](https://github.com/python-hyper/brotlicffi/blob/master/LICENSE) </sup>
* [**websockets**](https://github.com/aaugustin/websockets)\* - 用于通过 websocket 下载。根据 [BSD-3-Clause](https://github.com/aaugustin/websockets/blob/main/LICENSE) 许可
* [**requests**](https://github.com/psf/requests)\* - HTTP 库。用于 HTTPS 代理和持久连接支持。根据 [Apache-2.0](https://github.com/psf/requests/blob/main/LICENSE) 许可

#### 模拟

以下提供了模拟浏览器请求的支持。这对于一些采用 TLS 指纹识别的网站可能是必需的。

* [**curl_cffi**](https://github.com/lexiforest/curl_cffi) (推荐) - [curl-impersonate](https://github.com/lexiforest/curl-impersonate) 的 Python 绑定。提供了 Chrome、Edge 和 Safari 的模拟目标。根据 [MIT](https://github.com/lexiforest/curl_cffi/blob/main/LICENSE) 许可
  * 可以使用 `curl-cffi` 组安装，例如 `pip install "yt-dlp[default,curl-cffi]"`
  * 目前包含在 `yt-dlp.exe`、`yt-dlp_linux` 和 `yt-dlp_macos` 构建中


### 元数据

* [**mutagen**](https://github.com/quodlibet/mutagen)\* - 用于 `--embed-thumbnail` 在某些格式中。根据 [GPLv2+](https://github.com/quodlibet/mutagen/blob/master/COPYING) 许可
* [**AtomicParsley**](https://github.com/wez/atomicparsley) - 当 `mutagen`/`ffmpeg` 无法使用时，用于 `--embed-thumbnail` 在 `mp4`/`m4a` 文件中。根据 [GPLv2+](https://github.com/wez/atomicparsley/blob/master/COPYING) 许可
* [**xattr**](https://github.com/xattr/xattr), [**pyxattr**](https://github.com/iustin/pyxattr) 或 [**setfattr**](http://savannah.nongnu.org/projects/attr) - 用于在 **Mac** 和 **BSD** 上写入 xattr 元数据 (`--xattr`)。根据 [MIT](https://github.com/xattr/xattr/blob/master/LICENSE.txt), [LGPL2.1](https://github.com/iustin/pyxattr/blob/master/COPYING) 和 [GPLv2+](http://git.savannah.nongnu.org/cgit/attr.git/tree/doc/COPYING) 许可

### 其他

* [**pycryptodomex**](https://github.com/Legrandin/pycryptodome)\* - 用于解密 AES-128 HLS 流和各种其他数据。根据 [BSD-2-Clause](https://github.com/Legrandin/pycryptodome/blob/master/LICENSE.rst) 许可
* [**phantomjs**](https://github.com/ariya/phantomjs) - 用于需要运行 JavaScript 的提取器。根据 [BSD-3-Clause](https://github.com/ariya/phantomjs/blob/master/LICENSE.BSD) 许可
* [**secretstorage**](https://github.com/mitya57/secretstorage)\* - 用于 `--cookies-from-browser` 访问 **Gnome** 密钥环以解密 **Chromium** 浏览器的 cookie。根据 [BSD-3-Clause](https://github.com/mitya57/secretstorage/blob/master/LICENSE) 许可
* 任何您想与 `--downloader` 一起使用的外部下载器

### 已弃用

* [**avconv** 和 **avprobe**](https://www.libav.org) - 现已**弃用**的 ffmpeg 替代品。许可证[取决于构建](https://libav.org/legal)
* [**sponskrub**](https://github.com/faissaloo/SponSkrub) - 用于使用现已**弃用**的 [sponskrub 选项](#sponskrub-options)。根据 [GPLv3+](https://github.com/faissaloo/SponSkrub/blob/master/LICENCE.md) 许可
* [**rtmpdump**](http://rtmpdump.mplayerhq.hu) - 用于下载 `rtmp` 流。可以使用 ffmpeg 替代，使用 `--downloader ffmpeg`。根据 [GPLv2+](http://rtmpdump.mplayerhq.hu) 许可
* [**mplayer**](http://mplayerhq.hu/design7/info.html) 或 [**mpv**](https://mpv.io) - 用于下载 `rstp`/`mms` 流。可以使用 ffmpeg 替代，使用 `--downloader ffmpeg`。根据 [GPLv2+](https://github.com/mpv-player/mpv/blob/master/Copyright) 许可

要使用或重新分发依赖项，您必须同意其各自的许可条款。

独立发布的二进制文件已包含 Python 解释器和标记为 **\*** 的包。

如果您没有执行任务所需的依赖项，yt-dlp 会警告您。所有当前可用的依赖项可以在 `--verbose` 输出的顶部看到


## 编译

### 独立的 PyInstaller 构建
要构建独立的可执行文件，您必须安装 Python 和 `pyinstaller`（如果需要，还可以安装 yt-dlp 的[可选依赖项](#dependencies)）。可执行文件将针对与使用的 Python 相同的 CPU 架构构建。

您可以运行以下命令：

```
python3 devscripts/install_deps.py --include pyinstaller
python3 devscripts/make_lazy_extractors.py
python3 -m bundle.pyinstaller
```

在某些系统上，您可能需要使用 `py` 或 `python` 而不是 `python3`。

`python -m bundle.pyinstaller` 接受可以传递给 `pyinstaller` 的任何参数，例如 `--onefile/-F` 或 `--onedir/-D`，这些参数在[这里](https://pyinstaller.org/en/stable/usage.html#what-to-generate)有进一步记录。

**注意**：Pyinstaller 4.4 以下版本[不支持](https://github.com/pyinstaller/pyinstaller#requirements-and-tested-platforms)从 Windows 商店安装的 Python，除非使用虚拟环境。

**重要提示**：直接运行 `pyinstaller` **而不是** 使用 `python -m bundle.pyinstaller` **不受官方支持**。这可能会也可能不会正常工作。

### 平台独立的二进制文件 (UNIX)
您需要安装构建工具 `python` (3.9+)、`zip`、`make` (GNU)、`pandoc`\* 和 `pytest`\*。

安装这些工具后，只需运行 `make`。

您也可以运行 `make yt-dlp` 来仅编译二进制文件而不更新任何其他文件。（标记为 **\*** 的构建工具不需要）

### 相关脚本

* **`devscripts/install_deps.py`** - 安装 yt-dlp 的依赖项。
* **`devscripts/update-version.py`** - 根据当前日期更新版本号。
* **`devscripts/set-variant.py`** - 设置可执行文件的构建变体。
* **`devscripts/make_changelog.py`** - 使用简短的提交消息创建 markdown 变更日志并更新 `CONTRIBUTORS` 文件。
* **`devscripts/make_lazy_extractors.py`** - 创建惰性提取器。在构建二进制文件（任何变体）之前运行此命令将提高其启动性能。设置环境变量 `YTDLP_NO_LAZY_EXTRACTORS` 为非空值以强制禁用惰性提取器加载。

注意：有关更多信息，请参阅它们的 `--help`。

### 分叉项目
如果您在 GitHub 上分叉项目，您可以运行分叉的[构建工作流](.github/workflows/build.yml)以自动构建所选版本作为工件。或者，您可以运行[发布工作流](.github/workflows/release.yml)或启用[夜间工作流](.github/workflows/release-nightly.yml)以创建完整的（预）发布。

# 使用和选项

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
    yt-dlp [选项] [--] URL [URL...]

`Ctrl+F` 是您的朋友 :D
<!-- MANPAGE: END EXCLUDED SECTION -->

<!-- 自动生成 -->
## 通用选项：
    -h, --help                      打印此帮助文本并退出
    --version                       打印程序版本并退出
    -U, --update                    更新此程序到最新版本
    --no-update                     不检查更新（默认）
    --update-to [CHANNEL]@[TAG]     升级/降级到特定版本。
                                    CHANNEL 也可以是仓库。如果省略，CHANNEL 和 TAG 默认为 "stable" 和 "latest"；
                                    有关详细信息，请参阅 "UPDATE"。支持的渠道：stable, nightly, master
    -i, --ignore-errors             忽略下载和后处理错误。
                                    即使后处理失败，下载也会被视为成功
    --no-abort-on-error             在下载错误时继续下一个视频；
                                    例如，跳过播放列表中不可用的视频（默认）
    --abort-on-error                如果发生错误，则中止下载后续视频（别名：--no-ignore-errors）
    --dump-user-agent               显示当前用户代理并退出
    --list-extractors               列出所有支持的提取器并退出
    --extractor-descriptions        输出所有支持的提取器的描述并退出
    --use-extractors NAMES          要使用的提取器名称，用逗号分隔。
                                    您还可以使用正则表达式、"all"、"default" 和 "end"（结束 URL 匹配）；例如 --ies "holodex.*,end,youtube"。在名称前加上 "-" 以排除它，例如 --ies default,-generic。使用 --list-extractors 获取提取器名称列表。（别名：--ies）
    --default-search PREFIX         用于不合格 URL 的前缀。例如，
                                    "gvsearch2:python" 从谷歌视频下载两个搜索词为 "python" 的视频。
                                    使用值 "auto" 让 yt-dlp 猜测（"auto_warning" 在猜测时发出警告）。
                                    "error" 直接抛出错误。默认值 "fixup_error" 修复损坏的 URL，
                                    但如果无法修复则抛出错误而不是搜索
    --ignore-config                 不要加载任何配置文件，除了那些通过 --config-locations 指定的。
                                    为了向后兼容，如果在系统配置文件中找到此选项，则不会加载用户配置文件。
                                    （别名：--no-config）
    --no-config-locations           不加载任何自定义配置文件（默认）。当在配置文件中给出时，忽略当前文件中定义的所有以前的 --config-locations
    --config-locations PATH         主配置文件的位置；
                                    可以是配置文件的路径或其包含目录（"-" 表示 stdin）。可以多次使用，也可以在其他配置文件中使用
    --plugin-dirs PATH              要搜索插件的其他目录的路径。此选项可以多次使用以添加多个目录。
                                    使用 "default" 搜索默认插件目录（默认）
    --no-plugin-dirs                清除要搜索的插件目录，包括默认目录和之前通过 --plugin-dirs 提供的目录
    --flat-playlist                 不提取播放列表的 URL 结果条目；某些条目元数据可能缺失，下载可能会被绕过
    --no-flat-playlist              完全提取播放列表的视频（默认）
    --live-from-start               从开始下载直播流。目前仅支持 YouTube（实验性）
    --no-live-from-start            从当前时间下载直播流（默认）
    --wait-for-video MIN[-MAX]      等待计划的流变为可用。传递重试之间等待的最少秒数（或范围）
    --no-wait-for-video             不等待计划的流（默认）
    --mark-watched                  标记视频为已观看（即使使用 --simulate）
    --no-mark-watched               不标记视频为已观看（默认）
    --color [STREAM:]POLICY         是否在输出中发出颜色代码，
                                    可选地以 STREAM（stdout 或 stderr）为前缀以应用设置。可以是 "always"、"auto"（默认）、"never" 或 "no_color"（使用非颜色终端序列）。使用 "auto-tty" 或 "no_color-tty" 仅基于终端支持决定。
                                    可以多次使用
    --compat-options OPTS           可以通过恢复 yt-dlp 中的一些更改来帮助保持与 youtube-dl 或 youtube-dlc 配置的兼容性。有关详细信息，请参阅 "默认行为的差异"
    --alias ALIASES OPTIONS         为选项字符串创建别名。除非别名以破折号 "-" 开头，否则它将以 "--" 为前缀。参数根据 Python 字符串格式化迷你语言解析。例如 --alias get-audio,-X "-S=aext:{0},abr -x --audio-format {0}" 创建选项 "--get-audio" 和 "-X"，它们接受一个参数（ARG0）并扩展为 "-S=aext:ARG0,abr -x --audio-format ARG0"。
                                    所有定义的别名都列在 --help 输出中。别名选项可以触发更多别名；因此要小心避免定义递归选项。作为安全措施，每个别名最多可以触发 100 次。此选项可以多次使用

## 网络选项：
    --proxy URL                     使用指定的 HTTP/HTTPS/SOCKS 代理。要启用 SOCKS 代理，请指定适当的方案，
                                    例如 socks5://user:pass@127.0.0.1:1080/。
                                    传递空字符串（--proxy ""）以直接连接
    --socket-timeout SECONDS        在放弃之前等待的时间，以秒为单位
    --source-address IP             客户端 IP 地址绑定到
    --impersonate CLIENT[:OS]       模拟请求的客户端。例如 chrome, chrome-110, chrome:windows-10。传递 --impersonate="" 以模拟任何客户端。
                                    注意，强制模拟所有请求可能会对下载速度和稳定性产生不利影响
    --list-impersonate-targets      列出可模拟的客户端。
    -4, --force-ipv4                强制所有连接通过 IPv4
    -6, --force-ipv6                强制所有连接通过 IPv6
    --enable-file-urls              启用 file:// URL。默认情况下出于安全原因禁用。

## 地理限制：
    --geo-verification-proxy URL    使用此代理验证某些地理限制站点的 IP 地址。默认代理由 --proxy 指定（如果未指定，则不使用代理）用于实际下载
    --xff VALUE                     如何伪造 X-Forwarded-For HTTP 头以尝试绕过地理限制。可以是 "default"（仅在已知有用时）、"never"、CIDR 表示法中的 IP 块或两个字母的 ISO 3166-2 国家代码

## 视频选择：
    -I, --playlist-items ITEM_SPEC  要下载的项目的逗号分隔的 playlist_index。您可以使用 "[START]:[STOP][:STEP]" 指定范围。为了向后兼容，也支持 START-STOP。使用负索引从右侧计数，使用负 STEP 以相反顺序下载。例如，"-I 1:3,7,-5::2" 用于大小为 15 的播放列表将下载索引为 1,2,3,7,11,13,15 的项目
    --min-filesize SIZE             如果文件大小小于 SIZE，则中止下载，例如 50k 或 44.6M
    --max-filesize SIZE             如果文件大小大于 SIZE，则中止下载，例如 50k 或 44.6M
    --date DATE                     仅下载在此日期上传的视频。日期可以是 "YYYYMMDD" 或格式 [now|today|yesterday][-N[day|week|month|year]]。
                                    例如 "--date today-2weeks" 仅下载两周前的同一天上传的视频
    --datebefore DATE               仅下载在此日期或之前上传的视频。接受的日期格式与 --date 相同
    --dateafter DATE                仅下载在此日期或之后上传的视频。接受的日期格式与 --date 相同
    --match-filters FILTER          通用视频过滤器。任何 "OUTPUT TEMPLATE" 字段都可以与数字或字符串进行比较，使用 "Filtering Formats" 中定义的运算符。您还可以简单地指定一个字段以匹配该字段是否存在，使用 "!field" 检查字段是否不存在，使用 "&" 检查多个条件。如果需要，使用 "\" 转义 "&" 或引号。如果多次使用，过滤器匹配至少一个条件。例如 --match-filters !is_live --match-filters "like_count>?100 & description~='(?i)\bcats \& dogs\b'" 仅匹配非直播视频或那些点赞数超过 100（或点赞字段不可用）并且描述包含短语 "cats & dogs"（不区分大小写）的视频。使用 "--match-filters -" 以交互方式询问是否下载每个视频
    --no-match-filters              不使用任何 --match-filters（默认）
    --break-match-filters FILTER    与 "--match-filters" 相同，但在视频被拒绝时停止下载过程
    --no-break-match-filters        不使用任何 --break-match-filters（默认）
    --no-playlist                   如果 URL 指向视频和播放列表，则仅下载视频
    --yes-playlist                  如果 URL 指向视频和播放列表，则下载播放列表
    --age-limit YEARS               仅下载适合给定年龄的视频
    --download-archive FILE         仅下载未列在存档文件中的视频。记录所有下载视频的 ID
    --no-download-archive           不使用存档文件（默认）
    --max-downloads NUMBER          下载 NUMBER 个文件后中止
    --break-on-existing             当遇到存档文件中列出的文件时停止下载过程
    --no-break-on-existing          当遇到存档文件中列出的文件时不停止下载过程（默认）
    --break-per-input               更改 --max-downloads、--break-on-existing、--break-match-filters 和 autonumber 以按输入 URL 重置
    --no-break-per-input            --break-on-existing 和类似选项终止整个下载队列
    --skip-playlist-after-errors N  允许的失败次数，直到跳过播放列表的其余部分

## 下载选项：
    -N, --concurrent-fragments N    并发下载的 dash/hlsnative 视频片段数（默认为 1）
    -r, --limit-rate RATE           最大下载速率，以字节/秒为单位，例如 50K 或 4.2M
    --throttled-rate RATE           假设节流并重新提取视频数据的最小下载速率，以字节/秒为单位，例如 100K
    -R, --retries RETRIES           重试次数（默认为 10），或 "infinite"
    --file-access-retries RETRIES   文件访问错误的重试次数（默认为 3），或 "infinite"
    --fragment-retries RETRIES      片段的重试次数（默认为 10），或 "infinite"（DASH、hlsnative 和 ISM）
    --retry-sleep [TYPE:]EXPR       重试之间的睡眠时间，以秒为单位（可选）以重试类型为前缀（http（默认）、fragment、file_access、extractor）以应用睡眠。EXPR 可以是数字、linear=START[:END[:STEP=1]] 或 exp=START[:END[:BASE=2]]。此选项可以多次使用以设置不同重试类型的睡眠时间，例如 --retry-sleep linear=1::2 --retry-sleep fragment:exp=1:20
    --skip-unavailable-fragments    跳过 DASH、hlsnative 和 ISM 下载中不可用的片段（默认）（别名：--no-abort-on-unavailable-fragments）
    --abort-on-unavailable-fragments
                                    如果片段不可用，则中止下载（别名：--no-skip-unavailable-fragments）
    --keep-fragments                下载完成后保留下载的片段
    --no-keep-fragments             下载完成后删除下载的片段（默认）
    --buffer-size SIZE              下载缓冲区大小，例如 1024 或 16K（默认为 1024）
    --resize-buffer                 缓冲区大小从初始值 --buffer-size 自动调整（默认）
    --no-resize-buffer              不自动调整缓冲区大小
    --http-chunk-size SIZE          基于块的 HTTP 下载的块大小，例如 10485760 或 10M（默认为禁用）。可能有助于绕过 Web 服务器施加的带宽限制（实验性）
    --playlist-random               随机顺序下载播放列表视频
    --lazy-playlist                 在接收到播放列表条目时处理它们。这会禁用 n_entries、--playlist-random 和 --playlist-reverse
    --no-lazy-playlist              仅在解析整个播放列表后处理视频（默认）
    --xattr-set-filesize            设置文件 xattribute ytdl.filesize 与预期文件大小
    --hls-use-mpegts                对 HLS 视频使用 mpegts 容器；允许某些播放器在下载时播放视频，并减少下载中断时文件损坏的可能性。默认情况下对直播流启用
    --no-hls-use-mpegts             不对 HLS 视频使用 mpegts 容器。默认情况下在不下载直播流时使用
    --download-sections REGEX       仅下载与正则表达式匹配的章节。"*" 前缀表示时间范围而不是章节。负时间戳从末尾计算。"*from-url" 可用于下载从 URL 提取的 "start_time" 和 "end_time" 之间的内容。需要 ffmpeg。此选项可以多次使用以下载多个部分，例如 --download-sections "*10:15-inf" --download-sections "intro"
    --downloader [PROTO:]NAME       要使用的外部下载器的名称或路径（可选）以协议为前缀（http、ftp、m3u8、dash、rstp、rtmp、mms）。目前支持 native、aria2c、avconv、axel、curl、ffmpeg、httpie、wget。您可以使用此选项多次为不同协议设置不同的下载器。例如 --downloader aria2c --downloader "dash,m3u8:native" 将对 http/ftp 下载使用 aria2c，对 dash/m3u8 下载使用原生下载器（别名：--external-downloader）
    --downloader-args NAME:ARGS     将这些参数传递给外部下载器。指定下载器名称和参数，用冒号 ":" 分隔。对于 ffmpeg，可以使用与 --postprocessor-args 相同的语法将参数传递到不同位置。您可以使用此选项多次为不同下载器传递不同参数（别名：--external-downloader-args）

## 文件系统选项：
    -a, --batch-file FILE           包含要下载的 URL 的文件（"-" 表示 stdin），每行一个 URL。以 "#"、";" 或 "]" 开头的行被视为注释并被忽略
    --no-batch-file                 不从批处理文件读取 URL（默认）
    -P, --paths [TYPES:]PATH        文件应下载到的路径。指定文件类型和路径，用冒号 ":" 分隔。支持与 --output 相同的所有 TYPES。
                                    此外，您还可以提供 "home"（默认）和 "temp" 路径。所有中间文件首先下载到 temp 路径，然后在下载完成后将最终文件移动到 home 路径。
                                    如果 --output 是绝对路径，则忽略此选项
    -o, --output [TYPES:]TEMPLATE   输出文件名模板；有关详细信息，请参阅 "OUTPUT TEMPLATE"
    --output-na-placeholder TEXT    用于 --output 中不可用字段的占位符（默认："NA"）
    --restrict-filenames            限制文件名仅使用 ASCII 字符，并避免文件名中的 "&" 和空格
    --no-restrict-filenames         允许文件名中的 Unicode 字符、"&" 和空格（默认）
    --windows-filenames             强制文件名与 Windows 兼容
    --no-windows-filenames          仅对文件名进行最小化清理
    --trim-filenames LENGTH         限制文件名长度（不包括扩展名）到指定字符数
    -w, --no-overwrites             不覆盖任何文件
    --force-overwrites              覆盖所有视频和元数据文件。此选项包括 --no-continue
    --no-force-overwrites           不覆盖视频，但覆盖相关文件（默认）
    -c, --continue                  继续部分下载的文件/片段（默认）
    --no-continue                   不继续部分下载的片段。如果文件未分段，则重新下载整个文件
    --part                          使用 .part 文件而不是直接写入输出文件（默认）
    --no-part                       不使用 .part 文件 - 直接写入输出文件
    --mtime                         使用 Last-modified 头设置文件修改时间（默认）
    --no-mtime                      不使用 Last-modified 头设置文件修改时间
    --write-description             将视频描述写入 .description 文件
    --no-write-description          不写入视频描述（默认）
    --write-info-json               将视频元数据写入 .info.json 文件（可能包含个人信息）
    --no-write-info-json            不写入视频元数据（默认）
    --write-playlist-metafiles      在使用 --write-info-json、--write-description 等时写入播放列表元数据（默认）
    --no-write-playlist-metafiles   在使用 --write-info-json、--write-description 等时不写入播放列表元数据
    --clean-info-json               从 infojson 中删除一些内部元数据，例如文件名（默认）
    --no-clean-info-json            将所有字段写入 infojson
    --write-comments                检索视频评论以放置在 infojson 中。即使没有此选项，如果提取已知为快速，也会获取评论（别名：--get-comments）
    --no-write-comments             除非提取已知为快速，否则不检索视频评论（别名：--no-get-comments）
    --load-info-json FILE           包含视频信息的 JSON 文件（使用 "--write-info-json" 选项创建）
    --cookies FILE                  从 Netscape 格式的文件中读取 cookie 并转储 cookie jar
    --no-cookies                    不从文件读取/转储 cookie（默认）
    --cookies-from-browser BROWSER[+KEYRING][:PROFILE][::CONTAINER]
                                    从中加载 cookie 的浏览器名称。当前支持的浏览器有：
                                    brave、chrome、chromium、edge、firefox、opera、safari、vivaldi、whale。可选地，可以给出用于解密 Linux 上 Chromium cookie 的 KEYRING、要从中加载 cookie 的 PROFILE 名称/路径以及 CONTAINER 名称（如果使用 Firefox）（"none" 表示无容器）。默认情况下，使用最近访问的配置文件的所有容器。当前支持的密钥环有：basictext、gnomekeyring、kwallet、kwallet5、kwallet6
    --no-cookies-from-browser       不从浏览器加载 cookie（默认）
    --cache-dir DIR                 yt-dlp 可以永久存储一些下载信息（例如客户端 ID 和签名）的文件系统位置。默认 ${XDG_CACHE_HOME}/yt-dlp
    --no-cache-dir                  禁用文件系统缓存
    --rm-cache-dir                  删除所有文件系统缓存文件

## 缩略图选项：
    --write-thumbnail               将缩略图图像写入磁盘
    --no-write-thumbnail            不将缩略图图像写入磁盘（默认）
    --write-all-thumbnails          将所有缩略图图像格式写入磁盘
    --list-thumbnails               列出每个视频的可用缩略图。除非使用 --no-simulate，否则模拟

## 互联网快捷方式选项：
    --write-link                    根据当前平台写入互联网快捷方式文件（.url、.webloc 或 .desktop）。URL 可能会被操作系统缓存
    --write-url-link                写入 .url Windows 互联网快捷方式。操作系统根据文件路径缓存 URL
    --write-webloc-link             写入 .webloc macOS 互联网快捷方式
    --write-desktop-link            写入 .desktop Linux 互联网快捷方式

## 详细信息和模拟选项：
    -q, --quiet                     激活静默模式。如果与 --verbose 一起使用，将日志打印到 stderr
    --no-quiet                      停用静默模式。（默认）
    --no-warnings                   忽略警告
    -s, --simulate                  不下载视频且不写入磁盘
    --no-simulate                   即使使用打印/列出选项也下载视频
    --ignore-no-formats-error       忽略 "No video formats" 错误。即使视频实际上不可下载，也用于提取元数据（实验性）
    --no-ignore-no-formats-error    当找不到可下载的视频格式时抛出错误（默认）
    --skip-download                 不下载视频但写入所有相关文件（别名：--no-download）
    -O, --print [WHEN:]TEMPLATE     要打印到屏幕的字段名称或输出模板，可选地以何时打印为前缀，用 ":" 分隔。支持的 "WHEN" 值与 --use-postprocessor 相同（默认：video）。
                                    隐含 --quiet。除非使用 --no-simulate 或 WHEN 的后期阶段，否则隐含 --simulate。此选项可以多次使用
    --print-to-file [WHEN:]TEMPLATE FILE
                                    将给定模板附加到文件。WHEN 和 TEMPLATE 的值与 --print 相同。FILE 使用与输出模板相同的语法。此选项可以多次使用
    -j, --dump-json                 静默，但为每个视频打印 JSON 信息。除非使用 --no-simulate，否则模拟。有关可用键的描述，请参阅 "OUTPUT TEMPLATE"
    -J, --dump-single-json          静默，但为每个 URL 或 infojson 打印 JSON 信息。除非使用 --no-simulate，否则模拟。如果 URL 指向播放列表，则整个播放列表信息将在一行中转储
    --force-write-archive           即使使用 -s 或其他模拟选项，也强制写入下载存档条目（别名：--force-download-archive）
    --newline                       将进度条输出为新行
    --no-progress                   不打印进度条
    --progress                      显示进度条，即使在静默模式下
    --console-title                 在控制台标题栏中显示进度
    --progress-template [TYPES:]TEMPLATE
                                    进度输出的模板，可选地以 "download:"（默认）、"download-title:"（控制台标题）、"postprocess:" 或 "postprocess-title:" 为前缀。
                                    视频的字段可在 "info" 键下访问，进度属性可在 "progress" 键下访问。例如 --console-title --progress-template "download-title:%(info.id)s-%(progress.eta)s"
    --progress-delta SECONDS        进度输出之间的时间（默认：0）
    -v, --verbose                   打印各种调试信息
    --dump-pages                    打印使用 base64 编码的下载页面以调试问题（非常详细）
    --write-pages                   将下载的中间页面写入当前目录中的文件以调试问题
    --print-traffic                 显示发送和读取的 HTTP 流量

## 解决方法：
    --encoding ENCODING             强制指定编码（实验性）
    --legacy-server-connect         显式允许与不支持 RFC 5746 安全重新协商的服务器建立 HTTPS 连接
    --no-check-certificates         抑制 HTTPS 证书验证
    --prefer-insecure               使用未加密的连接检索视频信息（目前仅支持 YouTube）
    --add-headers FIELD:VALUE       指定自定义 HTTP 头及其值，用冒号 ":" 分隔。您可以使用此选项多次
    --bidi-workaround               解决缺乏双向文本支持的终端。需要 PATH 中的 bidiv 或 fribidi 可执行文件
    --sleep-requests SECONDS        数据提取期间请求之间的睡眠秒数
    --sleep-interval SECONDS        每次下载前的睡眠秒数。当与 --max-sleep-interval 一起使用时，这是最小睡眠时间（别名：--min-sleep-interval）
    --max-sleep-interval SECONDS    最大睡眠秒数。只能与 --min-sleep-interval 一起使用
    --sleep-subtitles SECONDS       每次字幕下载前的睡眠秒数

## 视频格式选项：
    -f, --format FORMAT             视频格式代码，有关详细信息，请参阅 "FORMAT SELECTION"
    -S, --format-sort SORTORDER     按给定字段排序格式，有关详细信息，请参阅 "Sorting Formats"
    --format-sort-force             强制用户指定的排序顺序优先于所有字段，有关详细信息，请参阅 "Sorting Formats"（别名：--S-force）
    --no-format-sort-force          某些字段优先于用户指定的排序顺序（默认）
    --video-multistreams            允许多个视频流合并到一个文件中
    --no-video-multistreams         每个输出文件仅下载一个视频流（默认）
    --audio-multistreams            允许多个音频流合并到一个文件中
    --no-audio-multistreams         每个输出文件仅下载一个音频流（默认）
    --prefer-free-formats           优先选择具有免费容器的视频格式，而不是相同质量的非免费格式。与 "-S ext" 一起使用以严格优先选择免费容器，无论质量如何
    --no-prefer-free-formats        不对免费容器给予任何特殊偏好（默认）
    --check-formats                 确保格式仅从实际可下载的格式中选择
    --check-all-formats             检查所有格式是否实际可下载
    --no-check-formats              不检查格式是否实际可下载
    -F, --list-formats              列出每个视频的可用格式。除非使用 --no-simulate，否则模拟
    --merge-output-format FORMAT    合并格式时可能使用的容器，用 "/" 分隔，例如 "mp4/mkv"。
                                    如果不需要合并，则忽略。（当前支持：avi、flv、mkv、mov、mp4、webm）

## 字幕选项：
    --write-subs                    写入字幕文件
    --no-write-subs                 不写入字幕文件（默认）
    --write-auto-subs               写入自动生成的字幕文件（别名：--write-automatic-subs）
    --no-write-auto-subs            不写入自动生成的字幕（默认）（别名：--no-write-automatic-subs）
    --list-subs                     列出每个视频的可用字幕。除非使用 --no-simulate，否则模拟
    --sub-format FORMAT             字幕格式；接受格式偏好，用 "/" 分隔，例如 "srt" 或 "ass/srt/best"
    --sub-langs LANGS               要下载的字幕语言（可以是正则表达式）或 "all"，用逗号分隔，例如 --sub-langs "en.*,ja"（其中 "en.*" 是匹配 "en" 后跟 0 个或多个任意字符的正则表达式模式）。您可以在语言代码前加上 "-" 以从请求的语言中排除它，例如 --sub-langs all,-live_chat。使用 --list-subs 获取可用语言标签列表

## 认证选项：
    -u, --username USERNAME         使用此帐户 ID 登录
    -p, --password PASSWORD         帐户密码。如果省略此选项，yt-dlp 将交互式询问
    -2, --twofactor TWOFACTOR       双因素认证代码
    -n, --netrc                     使用 .netrc 认证数据
    --netrc-location PATH           .netrc 认证数据的位置；可以是路径或其包含目录。默认为 ~/.netrc
    --netrc-cmd NETRC_CMD           执行以获取提取器的凭据的命令。
    --video-password PASSWORD       视频特定密码
    --ap-mso MSO                    Adobe Pass 多系统运营商（电视提供商）标识符，使用 --ap-list-mso 获取可用 MSO 列表
    --ap-username USERNAME          多系统运营商帐户登录
    --ap-password PASSWORD          多系统运营商帐户密码。如果省略此选项，yt-dlp 将交互式询问
    --ap-list-mso                   列出所有支持的多系统运营商
    --client-certificate CERTFILE   客户端证书文件的路径，PEM 格式。可能包含私钥
    --client-certificate-key KEYFILE
                                    客户端证书私钥文件的路径
    --client-certificate-password PASSWORD
                                    客户端证书私钥的密码，如果加密。如果未提供且密钥已加密，yt-dlp 将交互式询问

## 后处理选项：
    -x, --extract-audio             将视频文件转换为仅音频文件（需要 ffmpeg 和 ffprobe）
    --audio-format FORMAT           使用 -x 时将音频转换为此格式。（当前支持：best（默认）、aac、alac、flac、m4a、mp3、opus、vorbis、wav）。您可以使用与 --remux-video 类似的语法指定多个规则
    --audio-quality QUALITY         使用 -x 转换音频时指定 ffmpeg 音频质量。插入 0（最佳）到 10（最差）之间的值以进行 VBR 或特定比特率如 128K（默认 5）
    --remux-video FORMAT            如果需要，将视频重新混流到另一个容器中（当前支持：avi、flv、gif、mkv、mov、mp4、webm、aac、aiff、alac、flac、m4a、mka、mp3、ogg、opus、vorbis、wav）。如果目标容器不支持视频/音频编解码器，重新混流将失败。您可以指定多个规则；例如 "aac>m4a/mov>mp4/mkv" 将 aac 重新混流为 m4a，mov 重新混流为 mp4，其他所有内容重新混流为 mkv
    --recode-video FORMAT           如果需要，将视频重新编码为另一种格式。语法和支持的格式与 --remux-video 相同
    --postprocessor-args NAME:ARGS  将这些参数传递给后处理器。指定后处理器/可执行文件名称和参数，用冒号 ":" 分隔以将参数传递给指定的后处理器/可执行文件。支持的 PP 有：Merger、ModifyChapters、SplitChapters、ExtractAudio、VideoRemuxer、VideoConvertor、Metadata、EmbedSubtitle、EmbedThumbnail、SubtitlesConvertor、ThumbnailsConvertor、FixupStretched、FixupM4a、FixupM3u8、FixupTimestamp 和 FixupDuration。支持的可执行文件有：AtomicParsley、FFmpeg 和 FFprobe。您还可以指定 "PP+EXE:ARGS" 以仅在指定的后处理器使用指定的可执行文件时传递参数。此外，对于 ffmpeg/ffprobe，可以在前缀后附加 "_i"/"_o"，可选地后跟数字以在指定的输入/输出文件之前传递参数，例如 --ppa "Merger+ffmpeg_i1:-v quiet"。您可以使用此选项多次为不同后处理器传递不同参数。（别名：--ppa）
    -k, --keep-video                后处理后保留中间视频文件
    --no-keep-video                 后处理后删除中间视频文件（默认）
    --post-overwrites               覆盖后处理文件（默认）
    --no-post-overwrites            不覆盖后处理文件
    --embed-subs                    将字幕嵌入视频（仅适用于 mp4、webm 和 mkv 视频）
    --no-embed-subs                 不嵌入字幕（默认）
    --embed-thumbnail               将缩略图嵌入视频作为封面艺术
    --no-embed-thumbnail            不嵌入缩略图（默认）
    --embed-metadata                将元数据嵌入视频文件。如果存在章节/infojson，也会嵌入，除非使用 --no-embed-chapters/--no-embed-info-json（别名：--add-metadata）
    --no-embed-metadata             不向文件添加元数据（默认）（别名：--no-add-metadata）
    --embed-chapters                向视频文件添加章节标记（别名：--add-chapters）
    --no-embed-chapters             不添加章节标记（默认）（别名：--no-add-chapters）
    --embed-info-json               将 infojson 作为附件嵌入 mkv/mka 视频文件
    --no-embed-info-json            不将 infojson 作为附件嵌入视频文件
    --parse-metadata [WHEN:]FROM:TO 从其他字段解析附加元数据，如标题/艺术家；有关详细信息，请参阅 "MODIFYING METADATA"。支持的 "WHEN" 值与 --use-postprocessor 相同（默认：pre_process）
    --replace-in-metadata [WHEN:]FIELDS REGEX REPLACE
                                    使用给定正则表达式替换元数据字段中的文本。此选项可以多次使用。支持的 "WHEN" 值与 --use-postprocessor 相同（默认：pre_process）
    --xattrs                        使用 Dublin Core 和 XDG 标准将元数据写入视频文件的 xattrs
    --concat-playlist POLICY        连接播放列表中的视频。可以是 "never"、"always" 或 "multi_video"（默认；仅当视频形成一个节目时）。所有视频文件必须具有相同的编解码器和流数才能连接。"pl_video:" 前缀可以与 "--paths" 和 "--output" 一起使用以设置连接文件的输出文件名。有关详细信息，请参阅 "OUTPUT TEMPLATE"
    --fixup POLICY                  自动纠正文件的已知故障。可以是 never（不执行任何操作）、warn（仅发出警告）、detect_or_warn（默认；如果可以修复文件，则修复，否则发出警告）、force（即使文件已存在也尝试修复）
    --ffmpeg-location PATH          ffmpeg 二进制文件的位置；可以是二进制文件的路径或其包含目录
    --exec [WHEN:]CMD               执行命令，可选地以何时执行为前缀，用 ":" 分隔。支持的 "WHEN" 值与 --use-postprocessor 相同（默认：after_move）。可以使用与输出模板相同的语法将任何字段作为参数传递给命令。如果未传递字段，则 %(filepath,_filename|)q 将附加到命令末尾。此选项可以多次使用
    --no-exec                       删除任何先前定义的 --exec
    --convert-subs FORMAT           将字幕转换为另一种格式（当前支持：ass、lrc、srt、vtt）。使用 "--convert-subs none" 禁用转换（默认）（别名：--convert-subtitles）
    --convert-thumbnails FORMAT     将缩略图转换为另一种格式（当前支持：jpg、png、webp）。您可以使用与 "--remux-video" 类似的语法指定多个规则。使用 "--convert-thumbnails none" 禁用转换（默认）
    --split-chapters                根据内部章节将视频拆分为多个文件。"chapter:" 前缀可以与 "--paths" 和 "--output" 一起使用以设置拆分文件的输出文件名。有关详细信息，请参阅 "OUTPUT TEMPLATE"
    --no-split-chapters             不根据章节拆分视频（默认）
    --remove-chapters REGEX         删除标题与给定正则表达式匹配的章节。语法与 --download-sections 相同。此选项可以多次使用
    --no-remove-chapters            不从文件中删除任何章节（默认）
    --force-keyframes-at-cuts       在下载/拆分/删除部分时强制在切割处使用关键帧。由于需要重新编码，这很慢，但生成的视频在切割处可能更少伪影
    --no-force-keyframes-at-cuts    在切割/拆分时不强制在章节周围使用关键帧（默认）
    --use-postprocessor NAME[:ARGS]
                                    要启用的插件后处理器的（区分大小写）名称，以及（可选）要传递给它的参数，用冒号 ":" 分隔。ARGS 是以分号 ";" 分隔的 NAME=VALUE 列表。"when" 参数确定何时调用后处理器。可以是 "pre_process"（视频提取后）、"after_filter"（视频通过过滤器后）、"video"（在 --format 之后；在 --print/--output 之前）、"before_dl"（每次视频下载之前）、"post_process"（每次视频下载之后；默认）、"after_move"（将视频文件移动到最终位置之后）、"after_video"（下载和处理视频的所有格式之后）或 "playlist"（播放列表结束时）。此选项可以多次使用以添加不同的后处理器

## SponsorBlock 选项：
为下载的 YouTube 视频创建章节条目或删除各种片段（赞助、介绍等）使用 [SponsorBlock API](https://sponsor.ajay.app)

    --sponsorblock-mark CATS        要创建章节的 SponsorBlock 类别，用逗号分隔。可用类别有 sponsor、intro、outro、selfpromo、preview、filler、interaction、music_offtopic、poi_highlight、chapter、all 和 default（=all）。您可以在类别前加上 "-" 以排除它。有关类别的描述，请参阅 [1]。例如 --sponsorblock-mark all,-preview
                                    [1] https://wiki.sponsor.ajay.app/w/Segment_Categories
    --sponsorblock-remove CATS      要从视频文件中删除的 SponsorBlock 类别，用逗号分隔。如果某个类别同时出现在 mark 和 remove 中，remove 优先。语法和可用类别与 --sponsorblock-mark 相同，除了 "default" 指 "all,-filler" 并且 poi_highlight、chapter 不可用
    --sponsorblock-chapter-title TEMPLATE
                                    由 --sponsorblock-mark 创建的 SponsorBlock 章节标题的输出模板。唯一可用的字段是 start_time、end_time、category、categories、name、category_names。默认为 "[SponsorBlock]: %(category_names)l"
    --no-sponsorblock               禁用 --sponsorblock-mark 和 --sponsorblock-remove
    --sponsorblock-api URL          SponsorBlock API 位置，默认为 https://sponsor.ajay.app

## 提取器选项：
    --extractor-retries RETRIES     已知提取器错误的重试次数（默认为 3），或 "infinite"
    --allow-dynamic-mpd             处理动态 DASH 清单（默认）（别名：--no-ignore-dynamic-mpd）
    --ignore-dynamic-mpd            不处理动态 DASH 清单（别名：--no-allow-dynamic-mpd）
    --hls-split-discontinuity       在广告中断等不连续处将 HLS 播放列表拆分为不同格式
    --no-hls-split-discontinuity    不在广告中断等不连续处将 HLS 播放列表拆分为不同格式（默认）
    --extractor-args IE_KEY:ARGS    将 ARGS 参数传递给 IE_KEY 提取器。有关详细信息，请参阅 "EXTRACTOR ARGUMENTS"。您可以使用此选项多次为不同提取器传递参数

# 配置

您可以通过在配置文件中放置任何支持的命令行选项来配置 yt-dlp。配置从以下位置加载：

1. **主配置**：
    * 通过 `--config-location` 指定的文件
1. **便携配置**：（推荐用于便携安装）
    * 如果使用二进制文件，`yt-dlp.conf` 位于二进制文件所在目录
    * 如果从源代码运行，`yt-dlp.conf` 位于 `yt_dlp` 的父目录
1. **主目录配置**：
    * `yt-dlp.conf` 位于通过 `-P` 指定的主目录
    * 如果未指定 `-P`，则搜索当前目录
1. **用户配置**：
    * `${XDG_CONFIG_HOME}/yt-dlp.conf`
    * `${XDG_CONFIG_HOME}/yt-dlp/config`（推荐在 Linux/macOS 上使用）
    * `${XDG_CONFIG_HOME}/yt-dlp/config.txt`
    * `${APPDATA}/yt-dlp.conf`
    * `${APPDATA}/yt-dlp/config`（推荐在 Windows 上使用）
    * `${APPDATA}/yt-dlp/config.txt`
    * `~/yt-dlp.conf`
    * `~/yt-dlp.conf.txt`
    * `~/.yt-dlp/config`
    * `~/.yt-dlp/config.txt`

    另请参阅：[关于环境变量的说明](#notes-about-environment-variables)
1. **系统配置**：
    * `/etc/yt-dlp.conf`
    * `/etc/yt-dlp/config`
    * `/etc/yt-dlp/config.txt`

例如，使用以下配置文件，yt-dlp 将始终提取音频，不复制 mtime，使用代理并将所有视频保存在主目录下的 `YouTube` 目录中：
```
# 以 # 开头的行是注释

# 始终提取音频
-x

# 不复制 mtime
--no-mtime

# 使用此代理
--proxy 127.0.0.1:3128

# 将所有视频保存在主目录下的 YouTube 目录中
-o ~/YouTube/%(title)s.%(ext)s
```

**注意**：配置文件中的选项与常规命令行调用中使用的选项相同；因此 `-` 或 `--` 后**不能有空格**，例如 `-o` 或 `--proxy` 但不能是 `- o` 或 `-- proxy`。必要时也必须引用它们，就像在 UNIX shell 中一样。

如果您想在特定的 yt-dlp 运行中禁用所有配置文件，可以使用 `--ignore-config`。如果在任何配置文件中找到 `--ignore-config`，则不会加载进一步的配置。例如，在便携配置文件中包含此选项会阻止加载主目录、用户和系统配置。此外，（为了向后兼容）如果在系统配置文件中找到 `--ignore-config`，则不会加载用户配置。

### 配置文件编码

配置文件根据 UTF BOM（如果存在）解码，否则根据系统区域设置的编码解码。

如果您希望文件以不同的编码解码，请在文件开头添加 `# coding: ENCODING`（例如 `# coding: shift-jis`）。在此之前不能有任何字符，即使是空格或 BOM。

### 使用 netrc 进行认证

您可能还想为支持认证的提取器配置自动凭据存储（通过提供登录名和密码与 `--username` 和 `--password`），以便不必在每次 yt-dlp 执行时传递凭据作为命令行参数，并防止在 shell 命令历史记录中跟踪明文密码。您可以使用 [`.netrc` 文件](https://stackoverflow.com/tags/.netrc/info)在每个提取器的基础上实现这一点。为此，您需要在 `--netrc-location` 中创建一个 `.netrc` 文件，并限制只有您自己可以读写：
```
touch ${HOME}/.netrc
chmod a-rwx,u+rw ${HOME}/.netrc
```
之后，您可以为提取器添加凭据，格式如下，其中 *extractor* 是小写的提取器名称：
```
machine <extractor> login <username> password <password>
```
例如：
```
machine youtube login myaccount@gmail.com password my_youtube_password
machine twitch login my_twitch_account_name password my_twitch_password
```
要激活与 `.netrc` 文件的认证，您应传递 `--netrc` 给 yt-dlp 或将其放在[配置文件](#configuration)中。

.netrc 文件的默认位置是 `~`（见下文）。

作为使用 `.netrc` 文件的替代方案（其缺点是密码保存在纯文本文件中），您可以配置自定义 shell 命令以提供提取器的凭据。这是通过提供 `--netrc-cmd` 参数完成的，它应以 netrc 格式输出凭据并在成功时返回 `0`，其他值将被视为错误。命令中的 `{}` 将被提取器的名称替换，以便为正确的提取器选择凭据。

例如，要使用存储为 `.authinfo.gpg` 的加密 `.netrc` 文件
```
yt-dlp --netrc-cmd 'gpg --decrypt ~/.authinfo.gpg' 'https://www.youtube.com/watch?v=BaW_jenozKc'
```


### 关于环境变量的说明
* 环境变量通常指定为 `${VARIABLE}`/`$VARIABLE` 在 UNIX 和 `%VARIABLE%` 在 Windows 上；但在本文档中始终显示为 `${VARIABLE}`
* yt-dlp 还允许在 Windows 上使用 UNIX 风格的环境变量作为路径选项；例如 `--output`、`--config-location`
* 如果未设置，`${XDG_CONFIG_HOME}` 默认为 `~/.config`，`${XDG_CACHE_HOME}` 默认为 `~/.cache`
* 在 Windows 上，`~` 指向 `${HOME}`（如果存在）；否则指向 `${USERPROFILE}` 或 `${HOMEDRIVE}${HOMEPATH}`
* 在 Windows 上，`${USERPROFILE}` 通常指向 `C:\Users\<user name>`，`${APPDATA}` 指向 `${USERPROFILE}\AppData\Roaming`

# 输出模板

`-o` 选项用于指示输出文件名的模板，而 `-P` 选项用于指定每种类型文件的保存路径。

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
**tl;dr:** [导航到示例](#output-template-examples)。
<!-- MANPAGE: END EXCLUDED SECTION -->

最简单的 `-o` 用法是在下载单个文件时不设置任何模板参数，例如 `yt-dlp -o funny_video.flv "https://some/video"`（像这样硬编码文件扩展名**不推荐**，可能会破坏某些后处理）。

然而，它也可能包含在下载每个视频时将被替换的特殊序列。特殊序列可以根据 [Python 字符串格式化操作](https://docs.python.org/3/library/stdtypes.html#printf-style-string-formatting)进行格式化，例如 `%(NAME)s` 或 `%(NAME)05d`。澄清一下，这是一个百分号后跟括号中的名称，然后是格式化操作。

字段名称本身（括号内的部分）也可以有一些特殊格式：

1. **对象遍历**：可以使用点 `.` 分隔符遍历元数据中的字典和列表；例如 `%(tags.0)s`，`%(subtitles.en.-1.ext)s`。您可以使用冒号 `:` 进行 Python 切片；例如 `%(id.3:7)s`，`%(id.6:2:-1)s`，`%(formats.:.format_id)s`。花括号 `{}` 可用于构建仅包含特定键的字典；例如 `%(formats.:.{format_id,height})#j`。空字段名称 `%()s` 引用整个 infodict；例如 `%(.{id,title})s`。请注意，使用此方法可用的所有字段未在下面列出。使用 `-j` 查看此类字段

1. **算术**：可以使用 `+`、`-` 和 `*` 对数字字段进行简单算术运算。例如 `%(playlist_index+10)03d`，`%(n_entries+1-playlist_index)d`

1. **日期/时间格式化**：可以使用 `>` 将日期/时间字段格式化为 [strftime 格式化](https://docs.python.org/3/library/datetime.html#strftime-and-strptime-format-codes)。例如 `%(duration>%H-%M-%S)s`，`%(upload_date>%Y-%m-%d)s`，`%(epoch-3600>%H-%M-%S)s`

1. **替代**：可以使用 `,` 分隔的替代字段。例如 `%(release_date>%Y,upload_date>%Y|Unknown)s`

1. **替换**：可以使用 `&` 分隔符根据 [`str.format` 迷你语言](https://docs.python.org/3/library/string.html#format-specification-mini-language)指定替换值。如果字段**不为空**，则使用此替换值而不是实际字段内容。这是在考虑替代字段之后完成的；因此如果**任何**替代字段**不为空**，则使用替换值。例如 `%(chapters&has chapters|no chapters)s`，`%(title&TITLE={:>20}|NO TITLE)s`

1. **默认**：可以使用 `|` 分隔符为字段为空时指定字面默认值。这会覆盖 `--output-na-placeholder`。例如 `%(uploader|Unknown)s`

1. **更多转换**：除了正常的格式类型 `diouxXeEfFgGcrs`，yt-dlp 还支持转换为 `B` = **字节**，`j` = **json**（标志 `#` 用于漂亮打印，`+` 用于 Unicode），`h` = HTML 转义，`l` = 逗号分隔的**列表**（标志 `#` 用于 `\n` 换行分隔），`q` = 终端引用的**字符串**（标志 `#` 将列表拆分为不同参数），`D` = 添加**十进制后缀**（例如 10M）（标志 `#` 使用 1024 作为因子），`S` = 作为文件名**清理**（标志 `#` 用于受限）

1. **Unicode 规范化**：格式类型 `U` 可用于 NFC [Unicode 规范化](https://docs.python.org/3/library/unicodedata.html#unicodedata.normalize)。替代形式标志（`#`）将规范化更改为 NFD，转换标志 `+` 可用于 NFKC/NFKD 兼容等价规范化。例如 `%(title)+.100U` 是 NFKC

总结一下，字段的一般语法是：
```
%(name[.keys][addition][>strf][,alternate][&replacement][|default])[flags][width][.precision][length]type
```

此外，您可以通过指定文件类型后跟模板并用冒号 `:` 分隔来为各种元数据文件设置不同的输出模板，与通用输出模板分开。支持的不同文件类型有 `subtitle`、`thumbnail`、`description`、`annotation`（已弃用）、`infojson`、`link`、`pl_thumbnail`、`pl_description`、`pl_infojson`、`chapter`、`pl_video`。例如 `-o "%(title)s.%(ext)s" -o "thumbnail:%(title)s\%(title)s.%(ext)s"` 将缩略图放在与视频同名的文件夹中。如果任何模板为空，则不会写入该类型的文件。例如 `--write-thumbnail -o "thumbnail:"` 将仅为播放列表写入缩略图，而不为视频写入。

<a id="outtmpl-postprocess-note"></a>

**注意**：由于后处理（即合并等），实际输出文件名可能不同。使用 `--print after_move:filepath` 获取所有后处理完成后的名称。

可用字段有：

 - `id` (字符串)：视频标识符
 - `title` (字符串)：视频标题
 - `fulltitle` (字符串)：忽略直播时间戳和通用标题的视频标题
 - `ext` (字符串)：视频文件扩展名
 - `alt_title` (字符串)：视频的次要标题
 - `description` (字符串)：视频的描述
 - `display_id` (字符串)：视频的替代标识符
 - `uploader` (字符串)：视频上传者的全名
 - `uploader_id` (字符串)：视频上传者的昵称或 ID
 - `uploader_url` (字符串)：视频上传者个人资料的 URL
 - `license` (字符串)：视频许可的名称
 - `creators` (列表)：视频的创作者
 - `creator` (字符串)：视频的创作者；逗号分隔
 - `timestamp` (数字)：视频可用时的 UNIX 时间戳
 - `upload_date` (字符串)：视频上传日期，UTC (YYYYMMDD)
 - `release_timestamp` (数字)：视频发布时的 UNIX 时间戳
 - `release_date` (字符串)：视频或专辑发布的日期 (YYYYMMDD)，UTC
 - `release_year` (数字)：视频或专辑发布的年份 (YYYY)
 - `modified_timestamp` (数字)：视频最后修改时的 UNIX 时间戳
 - `modified_date` (字符串)：视频最后修改的日期 (YYYYMMDD)，UTC
 - `channel` (字符串)：视频上传的频道的全名
 - `channel_id` (字符串)：频道的 ID
 - `channel_url` (字符串)：频道的 URL
 - `channel_follower_count` (数字)：频道的关注者数量
 - `channel_is_verified` (布尔值)：频道是否在平台上验证
 - `location` (字符串)：视频拍摄的物理位置
 - `duration` (数字)：视频的长度，以秒为单位
 - `duration_string` (字符串)：视频的长度 (HH:mm:ss)
 - `view_count` (数字)：平台上观看视频的用户数量
 - `concurrent_view_count` (数字)：当前在平台上观看视频的用户数量。
 - `like_count` (数字)：视频的正面评分数量
 - `dislike_count` (数字)：视频的负面评分数量
 - `repost_count` (数字)：视频的转发数量
 - `average_rating` (数字)：用户给出的平均评分，使用的比例取决于网页
 - `comment_count` (数字)：视频的评论数量（对于某些提取器，评论仅在最后下载，因此此字段无法使用）
 - `age_limit` (数字)：视频的年龄限制（年）
 - `live_status` (字符串)："not_live"、"is_live"、"is_upcoming"、"was_live"、"post_live" 之一（曾经是直播，但 VOD 尚未处理）
 - `is_live` (布尔值)：此视频是直播流还是固定长度视频
 - `was_live` (布尔值)：此视频最初是否是直播流
 - `playable_in_embed` (字符串)：此视频是否允许在其他站点的嵌入播放器中播放
 - `availability` (字符串)：视频是 "private"、"premium_only"、"subscriber_only"、"needs_auth"、"unlisted" 还是 "public"
 - `media_type` (字符串)：站点分类的媒体类型，例如 "episode"、"clip"、"trailer"
 - `start_time` (数字)：URL 中指定的开始播放时间，以秒为单位
 - `end_time` (数字)：URL 中指定的结束播放时间，以秒为单位
 - `extractor` (字符串)：提取器的名称
 - `extractor_key` (字符串)：提取器的键名
 - `epoch` (数字)：信息提取完成时的 Unix 纪元
 - `autonumber` (数字)：每次下载时增加的编号，从 `--autonumber-start` 开始，前导零填充到 5 位
 - `video_autonumber` (数字)：每次视频下载时增加的编号
 - `n_entries` (数字)：播放列表中提取的项目总数
 - `playlist_id` (字符串)：包含视频的播放列表的标识符
 - `playlist_title` (字符串)：包含视频的播放列表的名称
 - `playlist` (字符串)：如果可用则为 `playlist_title`，否则为 `playlist_id`
 - `playlist_count` (数字)：播放列表中的项目总数。如果未提取整个播放列表，则可能未知
 - `playlist_index` (数字)：播放列表中视频的索引，根据最终索引前导零填充
 - `playlist_autonumber` (数字)：播放列表下载队列中视频的位置，根据播放列表总长度前导零填充
 - `playlist_uploader` (字符串)：播放列表上传者的全名
 - `playlist_uploader_id` (字符串)：播放列表上传者的昵称或 ID
 - `playlist_channel` (字符串)：上传播放列表的频道的显示名称
 - `playlist_channel_id` (字符串)：上传播放列表的频道的标识符
 - `playlist_webpage_url` (字符串)：播放列表网页的 URL
 - `webpage_url` (字符串)：视频网页的 URL，如果再次提供给 yt-dlp，应产生相同的结果
 - `webpage_url_basename` (字符串)：网页 URL 的基本名称
 - `webpage_url_domain` (字符串)：网页 URL 的域名
 - `original_url` (字符串)：用户提供的 URL（或与播放列表条目相同的 `webpage_url`）
 - `categories` (列表)：视频所属的类别列表
 - `tags` (列表)：分配给视频的标签列表
 - `cast` (列表)：演员表成员列表

[过滤格式](#filtering-formats)中的所有字段也可以使用

适用于属于某些逻辑章节或部分的视频：

 - `chapter` (字符串)：视频所属章节的名称或标题
 - `chapter_number` (数字)：视频所属章节的编号
 - `chapter_id` (字符串)：视频所属章节的 ID

适用于属于某些系列或节目的视频：

 - `series` (字符串)：视频所属系列或节目的标题
 - `series_id` (字符串)：视频所属系列或节目的 ID
 - `season` (字符串)：视频所属季度的标题
 - `season_number` (数字)：视频所属季度的编号
 - `season_id` (字符串)：视频所属季度的 ID
 - `episode` (字符串)：视频的标题
 - `episode_number` (数字)：季度内视频的编号
 - `episode_id` (字符串)：视频的 ID

适用于属于音乐专辑的曲目或部分：

 - `track` (字符串)：曲目的标题
 - `track_number` (数字)：专辑或光盘中曲目的编号
 - `track_id` (字符串)：曲目的 ID
 - `artists` (列表)：曲目的艺术家
 - `artist` (字符串)：曲目的艺术家；逗号分隔
 - `genres` (列表)：曲目的流派
 - `genre` (字符串)：曲目的流派；逗号分隔
 - `composers` (列表)：作品的作曲家
 - `composer` (字符串)：作品的作曲家；逗号分隔
 - `album` (字符串)：曲目所属专辑的标题
 - `album_type` (字符串)：专辑的类型
 - `album_artists` (列表)：专辑上出现的所有艺术家
 - `album_artist` (字符串)：专辑上出现的所有艺术家；逗号分隔
 - `disc_number` (数字)：曲目所属光盘或其他物理介质的编号

仅在使用 `--download-sections` 和使用 `--split-chapters` 的 `chapter:` 前缀时适用于具有内部章节的视频：

 - `section_title` (字符串)：章节的标题
 - `section_number` (数字)：文件中章节的编号
 - `section_start` (数字)：章节的开始时间，以秒为单位
 - `section_end` (数字)：章节的结束时间，以秒为单位

仅在使用 `--print` 时可用：

 - `urls` (字符串)：所有请求格式的 URL，每行一个
 - `filename` (字符串)：视频文件的名称。请注意，[实际文件名可能不同](#outtmpl-postprocess-note)
 - `formats_table` (表格)：由 `--list-formats` 打印的视频格式表
 - `thumbnails_table` (表格)：由 `--list-thumbnails` 打印的缩略图格式表
 - `subtitles_table` (表格)：由 `--list-subs` 打印的字幕格式表
 - `automatic_captions_table` (表格)：由 `--list-subs` 打印的自动字幕格式表

 仅在视频下载后可用（`post_process`/`after_move`）：

 - `filepath`：下载视频文件的实际路径

仅在 `--sponsorblock-chapter-title` 中可用：

 - `start_time` (数字)：章节的开始时间，以秒为单位
 - `end_time` (数字)：章节的结束时间，以秒为单位
 - `categories` (列表)：章节所属的 [SponsorBlock 类别](https://wiki.sponsor.ajay.app/w/Types#Category)
 - `category` (字符串)：章节所属的最小 SponsorBlock 类别
 - `category_names` (列表)：类别的友好名称
 - `name` (字符串)：最小类别的友好名称
 - `type` (字符串)：章节的 [SponsorBlock 操作类型](https://wiki.sponsor.ajay.app/w/Types#Action_Type)

每个上述序列在输出模板中引用时将被替换为与实际值对应的序列名称。例如，对于 `-o %(title)s-%(id)s.%(ext)s` 和标题为 `yt-dlp test video`、ID 为 `BaW_jenozKc` 的 mp4 视频，这将导致在当前目录中创建 `yt-dlp test video-BaW_jenozKc.mp4` 文件。

**注意**：某些序列不保证存在，因为它们取决于特定提取器获得的元数据。此类序列将替换为 `--output-na-placeholder` 提供的占位符值（默认为 "NA"）。

**提示**：查看 `-j` 输出以识别特定 URL 可用的字段

对于数字序列，您可以使用[与数字相关的格式化](https://docs.python.org/3/library/stdtypes.html#printf-style-string-formatting)；例如 `%(view_count)05d` 将导致一个字符串，其中观看次数填充零到 5 个字符，如 `00042`。

输出模板还可以包含任意层次路径，例如 `-o "%(playlist)s/%(playlist_index)s - %(title)s.%(ext)s"`，这将导致每个视频下载到此路径模板对应的目录中。任何缺失的目录将自动为您创建。

要在输出模板中使用百分号字面量，请使用 `%%`。要输出到 stdout，请使用 `-o -`。

当前默认模板为 `%(title)s [%(id)s].%(ext)s`。

在某些情况下，您不希望文件名中包含特殊字符，例如中文字符、空格或 &，例如将下载的文件名传输到 Windows 系统或通过 8 位不安全通道传输文件名。在这些情况下，添加 `--restrict-filenames` 标志以获取较短的标题。

#### 输出模板示例

```bash
$ yt-dlp --print filename -o "test video.%(ext)s" BaW_jenozKc
test video.webm    # 具有正确扩展名的字面名称

$ yt-dlp --print filename -o "%(title)s.%(ext)s" BaW_jenozKc
youtube-dl test video ''_ä↭𝕐.webm    # 各种奇怪的字符

$ yt-dlp --print filename -o "%(title)s.%(ext)s" BaW_jenozKc --restrict-filenames
youtube-dl_test_video_.webm    # 受限文件名

# 按视频在播放列表中的顺序下载 YouTube 播放列表视频到单独的目录
$ yt-dlp -o "%(playlist)s/%(playlist_index)s - %(title)s.%(ext)s" "https://www.youtube.com/playlist?list=PLwiyx1dc3P2JR9N8gQaQN_BCvlSlap7re"

# 根据上传年份将 YouTube 播放列表视频下载到单独的目录
$ yt-dlp -o "%(upload_date>%Y)s/%(title)s.%(ext)s" "https://www.youtube.com/playlist?list=PLwiyx1dc3P2JR9N8gQaQN_BCvlSlap7re"

# 仅在可用时使用 " - " 分隔符前缀播放列表索引
$ yt-dlp -o "%(playlist_index&{} - |)s%(title)s.%(ext)s" BaW_jenozKc "https://www.youtube.com/user/TheLinuxFoundation/playlists"

# 下载 YouTube 频道/用户的所有播放列表，将每个播放列表保存在单独的目录中：
$ yt-dlp -o "%(uploader)s/%(playlist)s/%(playlist_index)s - %(title)s.%(ext)s" "https://www.youtube.com/user/TheLinuxFoundation/playlists"

# 下载 Udemy 课程，将每个章节保存在主目录下的 MyVideos 目录中的单独目录中
$ yt-dlp -u user -p password -P "~/MyVideos" -o "%(playlist)s/%(chapter_number)s - %(chapter)s/%(title)s.%(ext)s" "https://www.udemy.com/java-tutorial"

# 下载整个系列季度，将每个系列和每个季度保存在 C:/MyVideos 下的单独目录中
$ yt-dlp -P "C:/MyVideos" -o "%(series)s/%(season_number)s - %(season)s/%(episode_number)s - %(episode)s.%(ext)s" "https://videomore.ru/kino_v_detalayah/5_sezon/367617"

# 将视频下载为 "C:\MyVideos\uploader\title.ext"，字幕下载为 "C:\MyVideos\subs\uploader\title.ext"
# 并将所有临时文件放在 "C:\MyVideos\tmp"
$ yt-dlp -P "C:/MyVideos" -P "temp:tmp" -P "subtitle:subs" -o "%(uploader)s/%(title)s.%(ext)s" BaW_jenozKc --write-subs

# 将视频下载为 "C:\MyVideos\uploader\title.ext"，字幕下载为 "C:\MyVideos\uploader\subs\title.ext"
$ yt-dlp -P "C:/MyVideos" -o "%(uploader)s/%(title)s.%(ext)s" -o "subtitle:%(uploader)s/subs/%(title)s.%(ext)s" BaW_jenozKc --write-subs

# 将正在下载的视频流式传输到 stdout
$ yt-dlp -o - BaW_jenozKc
```

# 格式选择

默认情况下，如果您**不**传递任何选项，yt-dlp 会尝试下载最佳可用质量。
这通常等同于使用 `-f bestvideo*+bestaudio/best`。但是，如果启用了多音频流（`--audio-multistreams`），默认格式更改为 `-f bestvideo+bestaudio/best`。同样，如果 ffmpeg 不可用，或者如果您使用 yt-dlp 流式传输到 `stdout`（`-o -`），则默认更改为 `-f best/bestvideo+bestaudio`。

**弃用警告**：最新版本的 yt-dlp 可以使用 ffmpeg 同时流式传输多种格式到 stdout。因此，在未来的版本中，默认值将设置为 `-f bv*+ba/b`，类似于正常下载。如果您想保留 `-f b/bv+ba` 设置，建议在配置选项中明确指定。

格式选择的通用语法是 `-f FORMAT`（或 `--format FORMAT`），其中 `FORMAT` 是一个*选择器表达式*，即描述您希望下载的格式或格式的表达式。

<!-- MANPAGE: BEGIN EXCLUDED SECTION -->
**tl;dr:** [导航到示例](#format-selection-examples)。
<!-- MANPAGE: END EXCLUDED SECTION -->

最简单的情况是请求特定格式；例如，使用 `-f 22` 可以下载格式代码等于 22 的格式。您可以使用 `--list-formats` 或 `-F` 获取特定视频的可用格式代码列表。请注意，这些格式代码是提取器特定的。

您还可以使用文件扩展名（当前支持 `3gp`、`aac`、`flv`、`m4a`、`mp3`、`mp4`、`ogg`、`wav`、`webm`）以下载特定文件扩展名的最佳质量格式作为单个文件，例如 `-f webm` 将下载最佳质量的 `webm` 格式作为单个文件。

您可以使用 `-f -` 以交互方式为每个视频提供格式选择器。

您还可以使用特殊名称来选择特定的边缘情况格式：

 - `all`：选择**所有格式**分别
 - `mergeall`：选择并**合并所有格式**（必须与 `--audio-multistreams`、`--video-multistreams` 或两者一起使用）
 - `b*`、`best*`：选择**包含**视频或音频或两者的最佳质量格式（即；`vcodec!=none 或 acodec!=none`）
 - `b`、`best`：选择**包含**视频和音频的最佳质量格式。等同于 `best*[vcodec!=none][acodec!=none]`
 - `bv`、`bestvideo`：选择最佳质量的**仅视频**格式。等同于 `best*[acodec=none]`
 - `bv*`、`bestvideo*`：选择**包含**视频的最佳质量格式。它也可能包含音频。等同于 `best*[vcodec!=none]`
 - `ba`、`bestaudio`：选择最佳质量的**仅音频**格式。等同于 `best*[vcodec=none]`
 - `ba*`、`bestaudio*`：选择**包含**音频的最佳质量格式。它也可能包含视频。等同于 `best*[acodec!=none]`（[不要使用！](https://github.com/yt-dlp/yt-dlp/issues/979#issuecomment-919629354)）
 - `w*`、`worst*`：选择包含视频或音频的最差质量格式
 - `w`、`worst`：选择包含视频和音频的最差质量格式。等同于 `worst*[vcodec!=none][acodec!=none]`
 - `wv`、`worstvideo`：选择最差的仅视频格式。等同于 `worst*[acodec=none]`
 - `wv*`、`worstvideo*`：选择包含视频的最差质量格式。它也可能包含音频。等同于 `worst*[vcodec!=none]`
 - `wa`、`worstaudio`：选择最差的仅音频格式。等同于 `worst*[vcodec=none]`
 - `wa*`、`worstaudio*`：选择包含音频的最差质量格式。它也可能包含视频。等同于 `worst*[acodec!=none]`

例如，要下载最差的仅视频格式，您可以使用 `-f worstvideo`。但是，建议不要使用 `worst` 和相关选项。当您的格式选择器是 `worst` 时，选择在所有方面最差的格式。大多数情况下，您实际需要的是文件大小最小的视频。因此，通常最好使用 `-S +size` 或更严格地使用 `-S +size,+br,+res,+fps` 而不是 `-f worst`。有关更多详细信息，请参阅[排序格式](#sorting-formats)。

您可以通过使用 `best<type>.<n>` 选择类型的第 n 个最佳格式。例如，`best.2` 将选择第二个最佳组合格式。同样，`bv*.3` 将选择第三个包含视频流的最佳格式。

如果您想下载多个视频，并且它们没有相同的可用格式，您可以使用斜杠指定优先顺序。请注意，左侧的格式优先；例如，`-f 22/17/18` 将下载格式 22（如果可用），否则下载格式 17（如果可用），否则下载格式 18（如果可用），否则抱怨没有合适的格式可供下载。

如果您想下载同一视频的多种格式，请使用逗号作为分隔符，例如 `-f 22,17,18` 将下载所有这些格式，当然如果它们可用。或者结合优先功能的更复杂示例：`-f 136/137/mp4/bestvideo,140/m4a/bestaudio`。

您可以使用 `-f <format1>+<format2>+...` 将多个格式的视频和音频合并到一个文件中（需要安装 ffmpeg）；例如，`-f bestvideo+bestaudio` 将下载最佳仅视频格式、最佳仅音频格式，并使用 ffmpeg 将它们合并在一起。

**弃用警告**：由于*下面*描述的行为复杂且反直觉，这将被删除，并且默认情况下将启用多流。将添加一个新的操作符来限制格式为单个音频/视频

除非使用 `--video-multistreams`，否则除第一个之外的所有包含视频流的格式都将被忽略。同样，除非使用 `--audio-multistreams`，否则除第一个之外的所有包含音频流的格式都将被忽略。例如，`-f bestvideo+best+bestaudio --video-multistreams --audio-multistreams` 将下载并合并所有 3 个给定格式。生成的文件将包含 2 个视频流和 2 个音频流。但是 `-f bestvideo+best+bestaudio --no-video-multistreams` 将仅下载并合并 `bestvideo` 和 `bestaudio`。`best` 被忽略，因为已经选择了另一个包含视频流的格式（`bestvideo`）。因此，格式的顺序很重要。`-f best+bestaudio --no-audio-multistreams` 将仅下载 `best`，而 `-f bestaudio+best --no-audio-multistreams` 将忽略 `best` 并仅下载 `bestaudio`。

## 过滤格式

您还可以通过在括号中放置条件来过滤视频格式，如 `-f "best[height=720]"`（或 `-f "[filesize>10M]"`，因为不带选择器的过滤器被解释为 `best`）。

以下数字元字段可以与比较 `<`、`<=`、`>`、`>=`、`=`（等于）、`!=`（不等于）一起使用：

 - `filesize`：字节数，如果事先已知
 - `filesize_approx`：字节数的估计值
 - `width`：视频的宽度，如果已知
 - `height`：视频的高度，如果已知
 - `aspect_ratio`：视频的宽高比，如果已知
 - `tbr`：音频和视频的平均比特率，以 [kbps](## "1000 比特/秒") 为单位
 - `abr`：音频的平均比特率，以 [kbps](## "1000 比特/秒") 为单位
 - `vbr`：视频的平均比特率，以 [kbps](## "1000 比特/秒") 为单位
 - `asr`：音频采样率，以赫兹为单位
 - `fps`：帧率
 - `audio_channels`：音频通道数
 - `stretched_ratio`：视频像素的 `width:height`，如果不是正方形

还可以使用比较 `=`（等于）、`^=`（以开头）、`$=`（以结尾）、`*=`（包含）、`~=`（匹配正则表达式）和以下字符串元字段进行过滤：

 - `url`：视频 URL
 - `ext`：文件扩展名
 - `acodec`：使用的音频编解码器名称
 - `vcodec`：使用的视频编解码器名称
 - `container`：容器格式名称
 - `protocol`：实际下载将使用的协议，小写（`http`、`https`、`rtsp`、`rtmp`、`rtmpe`、`mms`、`f4m`、`ism`、`http_dash_segments`、`m3u8` 或 `m3u8_native`）
 - `language`：语言代码
 - `dynamic_range`：视频的动态范围
 - `format_id`：格式的简短描述
 - `format`：格式的人类可读描述
 - `format_note`：有关格式的附加信息
 - `resolution`：宽度和高度的文本描述

任何字符串比较都可以用否定 `!` 前缀以产生相反的比较，例如 `!*=`（不包含）。字符串比较的比较值需要用双引号或单引号引起来，如果它包含空格或除 `._-` 以外的特殊字符。

**注意**：上述元字段都不保证存在，因为这完全取决于特定提取器获得的元数据，即网站提供的元数据。提取器提供的任何其他字段也可以用于过滤。

对于未知值的格式将被排除，除非您在操作符后放置问号（`?`）。您可以组合格式过滤器，因此 `-f "bv[height<=?720][tbr>500]"` 选择高达 720p 的视频（或高度未知的视频）且比特率至少为 500 kbps。您还可以使用 `all` 下载所有满足过滤器的格式，例如 `-f "all[vcodec=none]"` 选择所有仅音频格式。

格式选择器也可以使用括号分组；例如 `-f "(mp4,webm)[height<480]"` 将下载最佳预合并的 mp4 和 webm 格式，且高度低于 480。

## 排序格式

您可以使用 `-S`（`--format-sort`）更改被视为 `best` 的标准。此选项的通用格式为 `--format-sort field1,field2...`。

可用字段有：

 - `hasvid`：优先选择具有视频流的格式
 - `hasaud`：优先选择具有音频流的格式
 - `ie_pref`：格式偏好
 - `lang`：提取器确定的语言偏好（例如，原始语言优先于音频描述）
 - `quality`：格式的质量
 - `source`：源的偏好
 - `proto`：用于下载的协议（`https`/`ftps` > `http`/`ftp` > `m3u8_native`/`m3u8` > `http_dash_segments`> `websocket_frag` > `mms`/`rtsp` > `f4f`/`f4m`）
 - `vcodec`：视频编解码器（`av01` > `vp9.2` > `vp9` > `h265` > `h264` > `vp8` > `h263` > `theora` > 其他）
 - `acodec`：音频编解码器（`flac`/`alac` > `wav`/`aiff` > `opus` > `vorbis` > `aac` > `mp4a` > `mp3` > `ac4` > `eac3` > `ac3` > `dts` > 其他）
 - `codec`：等同于 `vcodec,acodec`
 - `vext`：视频扩展名（`mp4` > `mov` > `webm` > `flv` > 其他）。如果使用 `--prefer-free-formats`，则优先选择 `webm`。
 - `aext`：音频扩展名（`m4a` > `aac` > `mp3` > `ogg` > `opus` > `webm` > 其他）。如果使用 `--prefer-free-formats`，顺序更改为 `ogg` > `opus` > `webm` > `mp3` > `m4a` > `aac`
 - `ext`：等同于 `vext,aext`
 - `filesize`：确切的文件大小，如果事先已知
 - `fs_approx`：近似文件大小
 - `size`：确切的文件大小（如果可用），否则为近似文件大小
 - `height`：视频高度
 - `width`：视频宽度
 - `res`：视频分辨率，计算为最小维度。
 - `fps`：视频帧率
 - `hdr`：视频的动态范围（`DV` > `HDR12` > `HDR10+` > `HDR10` > `HLG` > `SDR`）
 - `channels`：音频通道数
 - `tbr`：总平均比特率，以 [kbps](## "1000 比特/秒") 为单位
 - `vbr`：视频的平均比特率，以 [kbps](## "1000 比特/秒") 为单位
 - `abr`：音频的平均比特率，以 [kbps](## "1000 比特/秒") 为单位
 - `br`：平均比特率，以 [kbps](## "1000 比特/秒") 为单位，`tbr`/`vbr`/`abr`
 - `asr`：音频采样率，以赫兹为单位

**弃用警告**：这些字段中的许多字段有（目前未记录的）别名，可能在未来的版本中删除。建议仅使用记录的字段名称。

所有字段（除非另有说明）按降序排序。要反转此顺序，请在字段前加上 `+`。例如 `+res` 优先选择分辨率最小的格式。此外，您可以为字段后缀首选值，用 `:` 分隔。例如 `res:720` 优先选择较大的视频，但不超过 720p，如果没有小于 720p 的视频，则选择最小的视频。对于 `codec` 和 `ext`，您可以提供两个首选值，第一个用于视频，第二个用于音频。例如 `+codec:avc:m4a`（等同于 `+vcodec:avc,+acodec:m4a`）将视频编解码器偏好设置为 `h264` > `h265` > `vp9` > `vp9.2` > `av01` > `vp8` > `h263` > `theora`，音频编解码器偏好设置为 `mp4a` > `aac` > `vorbis` > `opus` > `mp3` > `ac3` > `dts`。您还可以使用 `~` 作为分隔符，使排序偏好接近提供的值。例如 `filesize~1G` 优先选择文件大小最接近 1 GiB 的格式。

字段 `hasvid` 和 `ie_pref` 在排序中始终具有最高优先级，无论用户定义的顺序如何。此行为可以通过使用 `--format-sort-force` 更改。除此之外，默认顺序为：`lang,quality,res,fps,hdr:12,vcodec,channels,acodec,size,br,asr,proto,ext,hasaud,source,id`。提取器可能会覆盖此默认顺序，但它们不能覆盖用户提供的顺序。

请注意，hdr 的默认值为 `hdr:12`；即不优先选择 Dolby Vision 格式。此选择是因为 DV 格式尚未与大多数设备完全兼容。这可能会在将来更改。

如果您的格式选择器是 `worst`，则在排序后选择最后一项。这意味着它将选择在所有方面最差的格式。大多数情况下，您实际需要的是文件大小最小的视频。因此，通常最好使用 `-f best -S +size,+br,+res,+fps`。

**提示**：您可以使用 `-v -F` 查看格式的排序方式（从最差到最佳）。

## 格式选择示例

```bash
# 下载并合并最佳仅视频格式和最佳仅音频格式，
# 或者如果仅视频格式不可用，则下载最佳组合格式
$ yt-dlp -f "bv+ba/b"

# 下载包含视频的最佳格式，
# 如果它还没有音频流，则将其与最佳仅音频格式合并
$ yt-dlp -f "bv*+ba/b"

# 同上
$ yt-dlp

# 下载最佳仅视频格式和最佳仅音频格式而不合并它们
# 对于这种情况，应使用输出模板，因为
# 默认情况下，bestvideo 和 bestaudio 将具有相同的文件名。
$ yt-dlp -f "bv,ba" -o "%(title)s.f%(format_id)s.%(ext)s"

# 下载并合并包含视频流的最佳格式，
# 并将所有仅音频格式合并到一个文件中
$ yt-dlp -f "bv*+mergeall[vcodec=none]" --audio-multistreams

# 下载并合并包含视频流的最佳格式，
# 并将最佳 2 个仅音频格式合并到一个文件中
$ yt-dlp -f "bv*+ba+ba.2" --audio-multistreams


# 以下示例显示旧方法（不使用 -S）的格式选择
# 以及如何使用 -S 实现类似但（通常）更好的结果

# 下载最差的可用视频（旧方法）
$ yt-dlp -f "wv*+wa/w"

# 下载最佳可用视频但分辨率最小
$ yt-dlp -S "+res"

# 下载最小的可用视频
$ yt-dlp -S "+size,+br"
