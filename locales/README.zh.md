<!--START_SECTION:navbar-->
<div align="center">
  <a href="../README.md">🇺🇸 English</a> | <a href="README.de.md">🇩🇪 Deutsch</a> | <a href="README.es.md">🇪🇸 Español</a> | <a href="README.fr.md">🇫🇷 Français</a> | <a href="README.hi.md">🇮🇳 हिंदी</a> | <a href="README.ja.md">🇯🇵 日本語</a> | <a href="README.ko.md">🇰🇷 한국어</a> | <a href="README.pt.md">🇵🇹 Português</a> | <a href="README.ru.md">🇷🇺 Русский</a> | <a href="README.zh.md">🇨🇳 中文</a>
</div>
<!--END_SECTION:navbar-->

<p align="center"><img src="https://ohmyzsh.s3.amazonaws.com/omz-ansi-github.png" alt="Oh My Zsh"></p>

Oh My Zsh 是一个开源、社区驱动的框架，用于管理你的 [zsh](https://www.zsh.org/) 配置。

听起来很无聊。让我们再试一次。

**Oh My Zsh 不会让你变成 10 倍的开发者...但你可能会觉得自己是。**

安装后，你的终端 shell 将成为众人瞩目的焦点 _或者退还你的钱！_ 每次在命令提示符中按键，你都将利用数百个强大插件和精美主题。陌生人会在咖啡馆里向你走来，问你，_"那太棒了！你是天才吗？"_

最终，你将开始获得你一直觉得自己应得的那种关注。...或者你可能会利用节省下来的时间，开始更频繁地使用牙线。 😬

要了解更多，请访问 [ohmyz.sh](https://ohmyz.sh)，在 X（原 Twitter）上关注 [@ohmyzsh](https://x.com/ohmyzsh)，并加入我们的 [Discord](https://discord.gg/ohmyzsh)。

[![CI](https://github.com/ohmyzsh/ohmyzsh/workflows/CI/badge.svg)](https://github.com/ohmyzsh/ohmyzsh/actions?query=workflow%3ACI)
[![OpenSSF Best Practices](https://www.bestpractices.dev/projects/10713/badge)](https://www.bestpractices.dev/projects/10713)
[![X (formerly Twitter) Follow](https://img.shields.io/twitter/follow/ohmyzsh?label=%40ohmyzsh&logo=x&style=flat)](https://twitter.com/intent/follow?screen_name=ohmyzsh)
[![Mastodon Follow](https://img.shields.io/mastodon/follow/111169632522566717?label=%40ohmyzsh&domain=https%3A%2F%2Fmstdn.social&logo=mastodon&style=flat)](https://mstdn.social/@ohmyzsh)
[![Discord server](https://img.shields.io/discord/642496866407284746)](https://discord.gg/ohmyzsh)

<details>
<summary>Table of Contents</summary>

- [Getting Started](#getting-started)
  - [Operating System Compatibility](#operating-system-compatibility)
  - [Prerequisites](#prerequisites)
  - [Basic Installation](#basic-installation)
    - [Manual Inspection](#manual-inspection)
- [Using Oh My Zsh](#using-oh-my-zsh)
  - [Plugins](#plugins)
    - [Enabling Plugins](#enabling-plugins)
    - [Using Plugins](#using-plugins)
  - [Themes](#themes)
    - [Selecting A Theme](#selecting-a-theme)
  - [FAQ](#faq)
- [Advanced Topics](#advanced-topics)
  - [Advanced Installation](#advanced-installation)
    - [Custom Directory](#custom-directory)
    - [Unattended Install](#unattended-install)
    - [Installing From A Forked Repository](#installing-from-a-forked-repository)
    - [Manual Installation](#manual-installation)
  - [Installation Problems](#installation-problems)
  - [Custom Plugins And Themes](#custom-plugins-and-themes)
  - [Enable GNU ls In macOS And freeBSD Systems](#enable-gnu-ls-in-macos-and-freebsd-systems)
  - [Skip Aliases](#skip-aliases)
  - [Async git prompt](#async-git-prompt)
- [Getting Updates](#getting-updates)
  - [Updates Verbosity](#updates-verbosity)
  - [Manual Updates](#manual-updates)
- [Uninstalling Oh My Zsh](#uninstalling-oh-my-zsh)
- [How Do I Contribute To Oh My Zsh?](#how-do-i-contribute-to-oh-my-zsh)
  - [Do Not Send Us Themes](#do-not-send-us-themes)
- [Contributors](#contributors)
- [Follow Us](#follow-us)
- [Merchandise](#merchandise)
- [License](#license)
- [About Planet Argon](#about-planet-argon)

</details>

## 开始使用

### 操作系统兼容性

| O/S            | 状态   |
| :------------- | :----: |
| Android        |   ✅   |
| freeBSD        |   ✅   |
| LCARS          |   🛸   |
| Linux          |   ✅   |
| macOS          |   ✅   |
| OS/2 Warp      |   ❌   |
| Windows (WSL2) |   ✅   |

### 先决条件

- [Zsh](https://www.zsh.org) 应该已安装（v4.3.9 或更新版本都可以，但我们推荐 5.0.8 及以上版本）。如果没有预装（运行 `zsh --version` 来确认），请查看此处的维基指南：
  [安装 ZSH](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
- 应该已安装 `curl` 或 `wget`
- 应该已安装 `git`（推荐 v2.4.11 或更高版本）

### 基本安装

通过在终端中运行以下命令之一来安装 Oh My Zsh。你可以使用 `curl`、`wget` 或其他类似的工具通过命令行进行安装。

| 方法    | 命令                           |
| :------ | :---------------------------- |
| **curl**  | `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |
| **wget**  | `sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`   |
| **fetch** | `sh -c "$(fetch -o - https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |

另外，安装程序也镜像在 GitHub 之外。如果你所在的国家（如中国或印度）某些 ISP 阻止了 `raw.githubusercontent.com`，则可能需要使用此 URL：

| 方法    | 命令 |
| :------ | :--------------------------------------------- |
| **curl**  | `sh -c "$(curl -fsSL https://install.ohmyz.sh/)"` |
| **wget**  | `sh -c "$(wget -O- https://install.ohmyz.sh/)"`   |
| **fetch** | `sh -c "$(fetch -o - https://install.ohmyz.sh/)"` |

任何之前的 `.zshrc` 文件将被重命名为 `.zshrc.pre-oh-my-zsh`。安装完成后，你可以将想要保留的配置移动到新的 `.zshrc` 文件中。

#### 手动检查

对于你还不熟悉的项目，检查安装脚本是个好主意。你可以先下载安装脚本，查看其中内容是否正常，然后再运行它：

```sh
wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh
sh install.sh
```

如果上述 URL 超时或以其他方式失败，你可能需要将 URL 替换为  
`https://install.ohmyz.sh` 以获取脚本。

## 使用 Oh My Zsh

### 插件

Oh My Zsh 附带了大量的插件供你使用。你可以查看
[plugins](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins) 目录和/或
[wiki](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins) 以了解当前可用的插件。

#### 启用插件

一旦你发现了一个（或多个）想要与 Oh My Zsh 一起使用的插件，你需要在 `.zshrc` 文件中启用它们。你可以在 `$HOME` 目录中找到 zshrc 文件。用你最喜欢的文本编辑器打开它，你会看到一个列出所有想要加载的插件的位置。

```sh
vi ~/.zshrc
```

例如，这可能看起来像这样：

```sh
plugins=(
  git
  bundler
  dotenv
  macos
  rake
  rbenv
  ruby
```

请注意插件之间用空白符（空格、制表符、换行等）分隔。**不要**在它们之间使用逗号，否则会导致错误。

#### 使用插件

每个内置插件都包含一个 **README**，用于记录该插件。此 README 应显示该插件的别名（如果插件添加了任何别名）以及包含在该插件中的额外功能。

### 主题

我们承认。在 Oh My Zsh 的早期，我们可能对主题过于热衷了。我们现在捆绑了一百五十多个主题。大多数主题在维基上有
[screenshots](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes)（我们正在更新这个！）。去看看吧！

#### 选择主题

Robby 的主题是默认主题。它不是最花哨的，也不是最简单的，只是对 Robby 来说刚刚好。

一旦你找到想要使用的主题，你需要编辑 `~/.zshrc` 文件。你会看到其中有一个环境变量（全大写），看起来像：

```sh
ZSH_THEME="robbyrussell"
```

要使用不同的主题，只需将值更改为所需主题的名称。例如：

```sh
ZSH_THEME="agnoster" # (this is one of the fancy ones)
# see https://github.com/ohmyzsh/ohmyzsh/wiki/Themes#agnoster
```

<!-- prettier-ignore-start -->

> [!NOTE]
> You will many times see screenshots for a zsh theme, and try it out, and find that it doesn't look the same for you.
>
> This is because many themes require installing a [Powerline Font](https://github.com/powerline/fonts) or a
> [Nerd Font](https://github.com/ryanoasis/nerd-fonts) in order to render properly. Without them, these themes
> will render weird prompt symbols. Check out
> [the FAQ](https://github.com/ohmyzsh/ohmyzsh/wiki/FAQ#i-have-a-weird-character-in-my-prompt) for more
> information.
>
> Also, beware that themes only control what your prompt looks like. This is, the text you see before or after
> your cursor, where you'll type your commands. Themes don't control things such as the colors of your
> terminal window (known as _color scheme_) or the font of your terminal. These are settings that you can
> change in your terminal emulator. For more information, see
> [what is a zsh theme](https://github.com/ohmyzsh/ohmyzsh/wiki/FAQ#what-is-a-zsh-theme).

<!-- prettier-ignore-end -->

Open up a new terminal window and your prompt should look something like this:

![Agnoster theme](https://cloud.githubusercontent.com/assets/2618447/6316862/70f58fb6-ba03-11e4-82c9-c083bf9a6574.png)

In case you did not find a suitable theme for your needs, please have a look at the wiki for
[more of them](https://github.com/ohmyzsh/ohmyzsh/wiki/External-themes).

If you're feeling feisty, you can let the computer select one randomly for you each time you open a new
terminal window.

```sh
ZSH_THEME="random" # (...please let it be pie... please be some pie..)
```

并且如果你想从你最喜欢的主题列表中随机选择一个主题：

```sh
ZSH_THEME_RANDOM_CANDIDATES=(
  "robbyrussell"
  "agnoster"
```

如果你只知道自己不喜欢哪些主题，可以类似地将它们添加到忽略列表中：

```sh
ZSH_THEME_RANDOM_IGNORED=(pygmalion tjkirch_mod)
```

### FAQ

如果还有其他问题或疑问，你可能会在我们的
[FAQ](https://github.com/ohmyzsh/ohmyzsh/wiki/FAQ) 中找到解决方案。

## 高级主题

如果你喜欢动手操作，这些部分可能会引起你的兴趣。

### 高级安装

某些用户可能希望手动安装 Oh My Zsh，或更改安装程序接受的默认路径或其他设置（这些设置也记录在安装脚本的顶部）。

#### 自定义目录

默认位置是 `~/.oh-my-zsh`（位于您的主目录中，您可以通过
`cd ~/.oh-my-zsh` 访问）

如果您想通过 `ZSH` 环境变量更改安装目录，可以在安装前运行
`export ZSH=/your/path`，或者在安装流程结束前设置它，如下所示：

```sh
ZSH="$HOME/.dotfiles/oh-my-zsh" sh install.sh
```

#### 无人值守安装

如果你正在将 Oh My Zsh 安装脚本作为自动化安装的一部分运行，可以向 `install.sh` 脚本传递 `--unattended` 标志。这将导致不会尝试更改默认 shell，并且在安装完成后也不会运行 `zsh`。

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" "" --unattended
```

如果你在中国、印度或其他屏蔽 `raw.githubusercontent.com` 的国家，可能需要将其替换为 `https://install.ohmyz.sh` 以完成安装。

#### 从分支的仓库安装

安装脚本也接受这些变量，以允许安装不同的仓库：

- `REPO`（默认：`ohmyzsh/ohmyzsh`）：这采用 `owner/repository` 的形式。如果你设置了这个变量，
  安装器将在 `https://github.com/{owner}/{repository}` 查找仓库。

- `REMOTE`（默认：`https://github.com/${REPO}.git`）：这是 git 仓库克隆的完整 URL。你
  可以使用这个设置，如果你想从不在 GitHub 上的分支（如 GitLab、Bitbucket...）安装，或者如果你想
  使用 SSH 而不是 HTTPS 克隆（`git@github.com:user/project.git`）。

  _注意：这与设置 `REPO` 变量不兼容。此设置将优先。_

- `BRANCH`（默认：`master`）：你可以使用这个设置，如果你想更改克隆仓库时的默认分支。
  这可能在测试 Pull Request 或如果你想使用不同于 `master` 的分支时有用。

例如：

```sh
REPO=apjanke/oh-my-zsh BRANCH=edge sh install.sh
```

#### 手动安装

##### 1. Clone The Repository <!-- omit in toc -->

```sh
git clone https://github.com/ohmyzsh/ohmyzsh.git ~/.oh-my-zsh
```

##### 2. _Optionally_, Backup Your Existing `~/.zshrc` File <!-- omit in toc -->

```sh
cp ~/.zshrc ~/.zshrc.orig
```

##### 3. Create A New Zsh Configuration File <!-- omit in toc -->

你可以通过复制我们为你提供的模板来创建一个新的 zsh 配置文件。

```sh
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
```

##### 4. Change Your Default Shell <!-- omit in toc -->

```sh
chsh -s $(which zsh)
```

您必须从用户会话中注销并重新登录才能看到此更改。

##### 5. Initialize Your New Zsh Configuration <!-- omit in toc -->

一旦你打开一个新的终端窗口，它应该会加载带有 Oh My Zsh 配置的 zsh。

### 安装问题

如果你在安装过程中遇到任何问题，这里有一些常见的解决方法。

- 如果在切换到 `oh-my-zsh` 后无法找到某些命令，你_可能_需要修改 `~/.zshrc` 中的 `PATH`。
- 如果你是手动安装或更改了安装位置，请检查 `~/.zshrc` 中的 `ZSH` 环境变量。

### 自定义插件和主题

如果你想覆盖任何默认行为，只需在 `custom/` 目录中添加一个以 `.zsh` 结尾的新文件。

如果你有很多可以很好地一起使用的函数，可以将它们作为 `XYZ.plugin.zsh` 文件放在 `custom/plugins/` 目录中，然后启用此插件。

如果你想覆盖 Oh My Zsh 随附插件的功能，请在 `custom/plugins/` 目录中创建一个同名的插件，它将被加载而不是 `plugins/` 中的那个。

### 启用 macOS 和 freeBSD 系统中的 GNU ls

<a name="enable-gnu-ls"></a>

Oh My Zsh 的默认行为是在 macOS 和 FreeBSD 系统中使用 BSD `ls`。如果已安装 GNU `ls`（作为 `gls` 命令），可以选择使用它。为此，可以在加载 `oh-my-zsh.sh` 之前使用基于 zstyle 的配置：

```zsh
zstyle ':omz:lib:theme-and-appearance' gnu-ls yes
```

注意：这与 `DISABLE_LS_COLORS=true` 不兼容

### 跳过别名

<a name="remove-directories-aliases"></a>

如果你想跳过默认的 Oh My Zsh 别名（那些在 `lib/*` 文件中定义的）或插件别名，你可以在 `~/.zshrc` 文件中使用以下设置，**在 Oh My Zsh 被加载之前**。请注意，根据你的需求，跳过别名有很多不同的方法。

```sh
# Skip all aliases, in lib files and enabled plugins
zstyle ':omz:*' aliases no

# Skip all aliases in lib files
zstyle ':omz:lib:*' aliases no
# Skip only aliases defined in the directories.zsh lib file
zstyle ':omz:lib:directories' aliases no

# Skip all plugin aliases
zstyle ':omz:plugins:*' aliases no
# Skip only the aliases from the git plugin
zstyle ':omz:plugins:git' aliases no
```

你可以通过其他方式组合这些，但需注意更具体的范围具有优先级：

```sh
# Skip all plugin aliases, except for the git plugin
zstyle ':omz:plugins:*' aliases no
zstyle ':omz:plugins:git' aliases yes
```

此功能的早期版本使用了以下设置，该设置已被移除：

```sh
zstyle ':omz:directories' aliases no
```

相反，你现在可以使用以下内容：

```sh
zstyle ':omz:lib:directories' aliases no
```

#### Notice <!-- omit in toc -->

> 此功能目前处于测试阶段，未来可能会发生变化。它目前还不兼容插件管理器，如 zpm 或 zinit，这些管理器不会加载 init 脚本（`oh-my-zsh.sh`），而该功能正是在此脚本中实现的。

> 它目前还无法识别作为函数定义的 "别名"。例如，来自 git 插件的 `gccd`、`ggf` 或 `ggl` 函数。

### 异步 git 提示

异步提示函数是一个实验性功能（于 2024 年 4 月 3 日加入），允许 Oh My Zsh 异步渲染
提示信息。这可以提高提示渲染性能，但可能与某些设置不兼容。
我们希望这不是一个问题，但如果你在使用此新功能时遇到问题，可以通过在 Oh My Zsh 被加载之前，在你的 .zshrc 文件中设置以下内容来关闭它：

```sh
zstyle ':omz:alpha:lib:git' async-prompt no
```

如果您的问题是 git 提示符突然不再显示，可以尝试在加载 `oh-my-zsh.sh` 之前设置以下配置来强制启用。如果仍然无法解决问题，请用您的情况打开一个 issue。

```sh
zstyle ':omz:alpha:lib:git' async-prompt force
```

## 获取更新

默认情况下，您将每两周收到一次检查更新的提示。您可以通过在 `~/.zshrc` 文件中添加一行来选择其他更新模式，**在 Oh My Zsh 加载之前**：

1. 无需确认提示的自动更新：

```sh
   zstyle ':omz:update' mode auto
   ```

2. 如果有可用更新，请每隔几天提醒一次：

```sh
   zstyle ':omz:update' mode reminder
   ```

3. 要完全禁用自动更新：

```sh
   zstyle ':omz:update' mode disabled
   ```

注意：你可以通过以下设置控制 Oh My Zsh 检查更新的频率：

```sh
# This will check for updates every 7 days
zstyle ':omz:update' frequency 7
# This will check for updates every time you open the terminal (not recommended)
zstyle ':omz:update' frequency 0
```

### 更新详细程度

你也可以通过以下设置限制更新的详细程度：

```sh
zstyle ':omz:update' verbose default # default update prompt

zstyle ':omz:update' verbose minimal # only few lines

zstyle ':omz:update' verbose silent # only errors
```

### 手动更新

如果你想在任何时候进行更新（比如有人刚刚发布了一个新插件，而你不想等一周？），你只需要运行：

```sh
omz update
```

> [!NOTE]
> If you want to automate this process in a script, you should call directly the `upgrade` script, like this:
>
>

```sh

> $ZSH/tools/upgrade.sh
> ```

>
> 在[FAQ: 如何更新 Oh My Zsh？](https://github.com/ohmyzsh/ohmyzsh/wiki/FAQ#how-do-i-update-oh-my-zsh)中查看更多选项。
>
> **`omz update --unattended` 的使用已被移除，因为它有副作用**。

魔法！🎉

## 卸载 Oh My Zsh

Oh My Zsh 并不适合每个人。我们会想念你的，但希望这个过程对你来说是轻松的。

如果你想卸载 `oh-my-zsh`，只需在命令行中运行 `uninstall_oh_my_zsh`。它将删除自身并恢复你之前的 `bash` 或 `zsh` 配置。

## 如何为 Oh My Zsh 做贡献？

在参与我们愉快的社区之前，请阅读 [行为准则](../CODE_OF_CONDUCT.md)。

我远不是 [Zsh](https://www.zsh.org/) 专家，并且怀疑有很多改进的方式 – 如果你有关于如何使配置更易于维护（并更快）的想法，请毫不犹豫地进行分支并提交拉取请求！

我们还需要有人来测试拉取请求。所以请查看
[开放的问题](https://github.com/ohmyzsh/ohmyzsh/issues)，并在你能帮助的地方提供帮助。

有关更多详细信息，请参阅 [贡献指南](../CONTRIBUTING.md)。

### 请勿向我们发送主题

我们目前已经有足够的主题了。请将你的主题添加到
[外部主题](https://github.com/ohmyzsh/ohmyzsh/wiki/External-themes)维基页面。

## 贡献者

Oh My Zsh 拥有一个充满活力的社区，有众多快乐的用户和令人愉快的贡献者。如果没有所有贡献者所花费的时间和提供的帮助，它不会如此出色。

非常感谢！

<a href="https://github.com/ohmyzsh/ohmyzsh/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ohmyzsh/ohmyzsh" width="100%"/>
</a>

## Follow Us

我们有社交媒体账号：

- [X](https://x.com/ohmyzsh) 上的 [@ohmyzsh](https://x.com/ohmyzsh)。你应该关注它。
- [Facebook](https://www.facebook.com/Oh-My-Zsh-296616263819290/) 上的 [Facebook](https://www.facebook.com/Oh-My-Zsh-296616263819290/)。来戳我们。
- [Instagram](https://www.instagram.com/_ohmyzsh/) 上的 [Instagram](https://www.instagram.com/_ohmyzsh/)。在展示 Oh My Zsh! 的帖子中提到我们。
- [Discord](https://discord.gg/ohmyzsh) 上的 [Discord](https://discord.gg/ohmyzsh)。来和我们聊天！

## 商品

我们有
[贴纸、T恤和咖啡杯可供选择](https://commitgoods.com/collections/oh-my-zsh?utm_source=github)
，让你展示对 Oh My Zsh 的热爱。再次强调，你将成为镇上的话题！

## 许可证

Oh My Zsh 是在 [MIT 许可证](../LICENSE.txt) 下发布的。

## 关于 Planet Argon

![Planet Argon](https://pa-github-assets.s3.amazonaws.com/PARGON_logo_digital_COL-small.jpg)

Oh My Zsh was started by the team at [Planet Argon](https://www.planetargon.com/?utm_source=github), a
[Ruby on Rails development agency](https://www.planetargon.com/services/ruby-on-rails-development?utm_source=github).
Check out our [other open source projects](https://www.planetargon.com/open-source?utm_source=github).

