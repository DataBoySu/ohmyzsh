<!--START_SECTION:navbar-->
<div align="center">
  <a href="../README.md">🇺🇸 English</a> | <a href="README.de.md">🇩🇪 Deutsch</a> | <a href="README.es.md">🇪🇸 Español</a> | <a href="README.fr.md">🇫🇷 Français</a> | <a href="README.hi.md">🇮🇳 हिंदी</a> | <a href="README.ja.md">🇯🇵 日本語</a> | <a href="README.ko.md">🇰🇷 한국어</a> | <a href="README.pt.md">🇵🇹 Português</a> | <a href="README.ru.md">🇷🇺 Русский</a> | <a href="README.zh.md">🇨🇳 中文</a>
</div>
<!--END_SECTION:navbar-->

<p align="center"><img src="https://ohmyzsh.s3.amazonaws.com/omz-ansi-github.png" alt="Oh My Zsh"></p>

Oh My Zsh는 [zsh](https://www.zsh.org/) 구성 관리에 사용되는 오픈소스, 커뮤니티 주도 프레임워크입니다.

흥미롭지 않군요. 다시 시도해 보겠습니다.

**Oh My Zsh은 당신을 10배 더 생산적인 개발자로 만들지는 않지만, 그렇게 느끼게 될 수도 있습니다.**

설치 후, 당신의 터미널 쉘은 도시의 화제가 될 것입니다 _혹은 환불해 드리겠습니다!_ 명령 프롬프트에서의 각 키 입력마다, 수백 개의 강력한 플러그인과 아름다운 테마를 활용하게 됩니다. 카페에서 낯선 사람이 당신에게 다가와 _"정말 인상적이네요! 당신은 어떤 천재인가요?"_라고 묻게 될 것입니다.

마침내, 당신은 항상 느꼈던 그 정도의 주목을 받게 될 것입니다. ...혹은 절약한 시간을 활용해 더 자주 치실을 하게 될 수도 있습니다. 😬

더 알아보려면 [ohmyz.sh](https://ohmyz.sh)를 방문하거나, X(구 트위터)에서 [@ohmyzsh](https://x.com/ohmyzsh)를 팔로우하고, [Discord](https://discord.gg/ohmyzsh)에서 우리와 함께하세요.

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

## 시작하기

### 운영 체제 호환성

| O/S            | 상태   |
| :------------- | :----: |
| Android        |   ✅   |
| freeBSD        |   ✅   |
| LCARS          |   🛸   |
| Linux          |   ✅   |
| macOS          |   ✅   |
| OS/2 Warp      |   ❌   |
| Windows (WSL2) |   ✅   |

### 필수 조건

- [Zsh](https://www.zsh.org)가 설치되어 있어야 합니다 (v4.3.9 이상은 충분하지만, 우리는 5.0.8 이상을 선호합니다). 미리 설치되어 있지 않은 경우 (`zsh --version` 명령어로 확인할 수 있음), 여기서 다음 위키 지침을 확인하세요:
  [ZSH 설치](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
- `curl` 또는 `wget`이 설치되어 있어야 합니다
- `git`이 설치되어 있어야 합니다 (v2.4.11 이상 권장)

### 기본 설치

Oh My Zsh는 터미널에서 다음 명령어 중 하나를 실행하여 설치할 수 있습니다. 이는 `curl`, `wget` 또는 유사한 도구를 사용하여 명령줄에서 설치할 수 있습니다.

| 방법    | 명령                           |
| :------ | :---------------------------- |
| **curl**  | `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |
| **wget**  | `sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`   |
| **fetch** | `sh -c "$(fetch -o - https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |

대안적으로, 설치 프로그램은 GitHub 외부에도 미러링되어 있습니다. `raw.githubusercontent.com`이 차단되는 국가(예: 중국, 인도의 특정 ISP)에 있다면 이 URL을 사용해야 할 수도 있습니다:

| 방법    | 명령 |
| :------ | :---------------------------------------------- |
| **curl**  | `sh -c "$(curl -fsSL https://install.ohmyz.sh/)"` |
| **wget**  | `sh -c "$(wget -O- https://install.ohmyz.sh/)"`   |
| **fetch** | `sh -c "$(fetch -o - https://install.ohmyz.sh/)"` |

이전의 `.zshrc` 파일은 `.zshrc.pre-oh-my-zsh`로 이름이 변경됩니다. 설치 후, 보존하고 싶은 설정은 새롭게 생성된 `.zshrc` 파일로 이동할 수 있습니다.

#### 수동 검사

아직 잘 모르는 프로젝트의 설치 스크립트를 점검하는 것은 좋은 아이디어입니다. 먼저 설치 스크립트를 다운로드한 후, 모든 것이 정상적으로 보이는지 확인한 다음 실행할 수 있습니다:

```sh
wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh
sh install.sh
```

위의 URL이 시간 초과되거나 기타 이유로 실패하는 경우, 스크립트를 받을 수 있도록 URL을 `https://install.ohmyz.sh`로 대체해야 할 수도 있습니다.

## Oh My Zsh 사용

### 플러그인

Oh My Zsh에는 사용자가 활용할 수 있는 많은 플러그인이 포함되어 있습니다. [plugins](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins) 디렉토리와/또는 [wiki](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins)에서 현재 제공되는 항목을 확인할 수 있습니다.

#### 플러그인 활성화

Oh My Zsh와 함께 사용하고 싶은 플러그인(또는 여러 개의 플러그인)을 발견하면 `.zshrc` 파일에서 이를 활성화해야 합니다. `.zshrc` 파일은 `$HOME` 디렉터리에 위치해 있습니다. 좋아하는 텍스트 편집기로 이를 열면, 로드하고자 하는 모든 플러그인을 나열할 수 있는 섹션이 보일 것입니다.

```sh
vi ~/.zshrc
```

예를 들어, 다음과 같이 보일 수 있습니다:

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

플러그인은 공백(공백, 탭, 줄 바꿈 등)으로 분리되어 있습니다. **사용하지 마세요** 사이에 쉼표를 사용하면 작동하지 않습니다.

#### 플러그인 사용

각 내장 플러그인에는 **README**가 포함되어 있으며, 이를 통해 문서화되어 있습니다. 이 README는 해당 플러그인이 추가하는 별칭(있는 경우)과 포함된 추가 기능을 보여줍니다.

### 테마

우리는 인정할게요. Oh My Zsh의 초기 시절, 우리는 테마에 너무 열정적으로 빠져 있었죠. 지금은 150개 이상의 테마가 포함되어 있습니다. 그 중 대부분은
[screenshots](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes) 위키에 있습니다 (이 부분은 업데이트 중입니다!). 확인해 보세요!

#### 테마 선택

Robby의 테마는 기본 테마입니다. 가장 화려한 것도 아니고, 가장 간단한 것도 아닙니다. 그냥 그에게 적절한 테마일 뿐입니다.

원하는 테마를 찾은 후에는 `~/.zshrc` 파일을 편집해야 합니다. 거기에는 다음과 같은 형태의 환경 변수(대문자)가 있습니다:

```sh
ZSH_THEME="robbyrussell"
```

다른 테마를 사용하려면 값을 원하는 테마의 이름과 일치하도록 변경하면 됩니다. 예를 들어:

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

그리고 만약 당신이 즐겨찾는 테마 목록에서 랜덤하게 테마를 선택하고 싶다면:

```sh
ZSH_THEME_RANDOM_CANDIDATES=(
  "robbyrussell"
  "agnoster"
```

불필요한 테마를 제외한 목록에 추가하는 방식과 유사하게, 싫어하는 테마를 추가할 수 있습니다.

```sh
ZSH_THEME_RANDOM_IGNORED=(pygmalion tjkirch_mod)
```

### FAQ

If you have some more questions or issues, you might find a solution in our
[FAQ](https://github.com/ohmyzsh/ohmyzsh/wiki/FAQ).

## 고급 주제

손을 더럽히는 것을 좋아하는 유형이라면, 이러한 섹션들이 당신에게 공감할 것입니다.

### 고급 설치

일부 사용자는 Oh My Zsh을 수동으로 설치하거나, 설치 프로그램이 수용하는 기본 경로나 기타 설정을 변경하고자 할 수 있습니다(이러한 설정은 설치 스크립트의 맨 위에 문서화되어 있습니다).

#### 커스텀 디렉토리

기본 위치는 `~/.oh-my-zsh`입니다 (홈 디렉토리에 숨겨져 있으며, `cd ~/.oh-my-zsh`로 접근할 수 있습니다)

`ZSH` 환경 변수를 사용하여 설치 디렉토리를 변경하고자 한다면, 설치 전에 `export ZSH=/your/path`를 실행하거나, 설치 파이프라인 종료 전에 다음과 같이 설정할 수 있습니다:

```sh
ZSH="$HOME/.dotfiles/oh-my-zsh" sh install.sh
```

#### 무인 설치

자동 설치의 일부로 Oh My Zsh 설치 스크립트를 실행하고 있다면 `install.sh` 스크립트에 `--unattended` 플래그를 전달할 수 있습니다. 이는 기본 쉘을 변경하지 않도록 하며, 설치가 완료된 후 `zsh`을 실행하지 않도록 합니다.

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" "" --unattended
```

중국, 인도 또는 `raw.githubusercontent.com`을 차단하는 다른 국가에 있다면 설치하려면 `https://install.ohmyz.sh`의 URL을 대체해야 할 수 있습니다.

#### forked 저장소에서 설치

설치 스크립트는 또한 다른 저장소에서 설치할 수 있도록 허용하기 위해 이러한 변수를 수락합니다:

- `REPO` (기본값: `ohmyzsh/ohmyzsh`): 이는 `owner/repository` 형식을 취합니다. 이 변수를 설정하면,
  설치자는 `https://github.com/{owner}/{repository}`에 있는 저장소를 찾습니다.

- `REMOTE` (기본값: `https://github.com/${REPO}.git`): 이는 git 저장소 복제의 전체 URL입니다. 
  GitHub이 아닌 fork(예: GitLab, Bitbucket 등)에서 설치하거나 SSH 대신 HTTPS 대신 복제하고 싶은 경우
  이 설정을 사용할 수 있습니다(`git@github.com:user/project.git`).

  _참고: `REPO` 변수를 설정하는 것과 호환되지 않습니다. 이 설정이 우선권을 가집니다._

- `BRANCH` (기본값: `master`): 저장소를 복제할 때 기본 브랜치를 변경하고 싶은 경우 이 설정을 사용할 수 있습니다.
  이는 Pull Request를 테스트하거나 `master`가 아닌 다른 브랜치를 사용하고 싶은 경우에 유용할 수 있습니다.

예시:

```sh
REPO=apjanke/oh-my-zsh BRANCH=edge sh install.sh
```

#### 수동 설치

##### 1. Clone The Repository <!-- omit in toc -->

```sh
git clone https://github.com/ohmyzsh/ohmyzsh.git ~/.oh-my-zsh
```

##### 2. _Optionally_, Backup Your Existing `~/.zshrc` File <!-- omit in toc -->

```sh
cp ~/.zshrc ~/.zshrc.orig
```

##### 3. Create A New Zsh Configuration File <!-- omit in toc -->

기본 템플릿을 복사하여 새로운 zsh 설정 파일을 생성할 수 있습니다.

```sh
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
```

##### 4. Change Your Default Shell <!-- omit in toc -->

```sh
chsh -s $(which zsh)
```

사용자 세션에서 로그아웃한 후 다시 로그인하여 이 변경을 확인해야 합니다.

##### 5. Initialize Your New Zsh Configuration <!-- omit in toc -->

새로운 터미널 창을 열면 Oh My Zsh의 설정과 함께 zsh이 로드되어야 합니다.

### 설치 문제

설치 과정에서 어려움이 있다면, 다음의 일반적인 해결 방법을 확인해 보세요.

- `oh-my-zsh`로 전환한 후 일부 명령어를 찾지 못하는 경우, `~/.zshrc` 파일에서 `PATH`를 수정해야 할 수도 있습니다.
- 수동으로 설치하거나 설치 위치를 변경한 경우, `~/.zshrc` 파일에서 `ZSH` 환경 변수를 확인하세요.

### 사용자 정의 플러그인 및 테마

기본 동작을 재정의하고 싶다면, `custom/` 디렉토리에 `.zsh`로 끝나는 새 파일을 추가하면 됩니다.

함수가 여러 개 있고 잘 어울리는 경우, `custom/plugins/` 디렉토리에 `XYZ.plugin.zsh` 파일로 넣고, 이 플러그인을 활성화하면 됩니다.

Oh My Zsh에 포함된 플러그인의 기능을 재정의하고 싶다면, `custom/plugins/` 디렉토리에 동일한 이름의 플러그인을 생성하면 `plugins/` 디렉토리에 있는 플러그인 대신에 로드됩니다.

### GNU ls를 macOS 및 freeBSD 시스템에서 사용하도록 설정

<a name="enable-gnu-ls"></a>

Oh My Zsh의 기본 동작은 macOS 및 FreeBSD 시스템에서 BSD `ls`를 사용하는 것입니다. GNU `ls`가 설치되어 있다면 (`gls` 명령어로 사용 가능), 이를 대신 사용하도록 선택할 수 있습니다. 이를 위해 `oh-my-zsh.sh`를 소스화하기 전에 zstyle 기반의 설정을 사용할 수 있습니다:

```zsh
zstyle ':omz:lib:theme-and-appearance' gnu-ls yes
```

주의: 이는 `DISABLE_LS_COLORS=true`와 호환되지 않습니다.

### Skip Aliases

<a name="remove-directories-aliases"></a>

기본 Oh My Zsh 별칭(예: `lib/*` 파일에 정의된 별칭) 또는 플러그인 별칭을 건너뛰고 싶다면, Oh My Zsh이 로드되기 **전에** `~/.zshrc` 파일에 아래 설정을 사용할 수 있습니다. 필요에 따라 별칭을 건너뛰는 방법은 여러 가지가 있으므로 주의하십시오.

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

이러한 범위를 다른 방식으로 결합할 수 있으며, 더 구체적인 범위가 우선권을 갖는다는 점을 고려해야 합니다.

```sh
# Skip all plugin aliases, except for the git plugin
zstyle ':omz:plugins:*' aliases no
zstyle ':omz:plugins:git' aliases yes
```

이 기능의 이전 버전은 아래의 설정을 사용하고 있었으나, 이 설정은 제거되었습니다:

```sh
zstyle ':omz:directories' aliases no
```

대신 이제 다음을 사용할 수 있습니다:

```sh
zstyle ':omz:lib:directories' aliases no
```

#### Notice <!-- omit in toc -->

> 이 기능은 현재 테스트 단계에 있으며, 향후 변경될 수 있습니다. 또한, zpm 또는 zinit과 같은 플러그인 관리자와 호환되지 않습니다. 이 기능은 init 스크립트(`oh-my-zsh.sh`)에서 구현되어 있기 때문입니다. 이 스크립트는 플러그인 관리자에 의해 소스되지 않습니다.

> 또한, 함수로 정의된 "aliases"를 인식하지 못합니다. 예를 들어, git 플러그인에서 제공하는 `gccd`, `ggf`, 또는 `ggl` 함수가 이에 해당합니다.

### Async git prompt

Async prompt functions are an experimental feature (included on April 3, 2024) that allows Oh My Zsh to render
prompt information asynchronously. This can improve prompt rendering performance, but it might not work well
with some setups. We hope that's not an issue, but if you're seeing problems with this new feature, you can
turn it off by setting the following in your .zshrc file, before Oh My Zsh is sourced:

```sh
zstyle ':omz:alpha:lib:git' async-prompt no
```

문제가 git 프롬프트가 갑자기 나타나지 않는 것이라면, `oh-my-zsh.sh`가 소스화되기 전에 다음 설정을 강제로 적용해 보세요. 여전히 작동하지 않는다면, 상황을 기반으로 이슈를 열어 주세요.

```sh
zstyle ':omz:alpha:lib:git' async-prompt force
```

## 업데이트 받기

기본적으로 2주마다 업데이트를 확인하는지 묻는 메시지가 표시됩니다. Oh My Zsh이 로드되기 **전에** `~/.zshrc` 파일에 줄을 추가하여 다른 업데이트 모드를 선택할 수 있습니다:

1. 확인 메시지 없이 자동 업데이트:

```sh
   zstyle ':omz:update' mode auto
   ```

2. 몇 일 간격으로 업데이트가 있을 경우에만 напоминание을 제공하세요:

```sh
   zstyle ':omz:update' mode reminder
   ```

3. 자동 업데이트를 완전히 비활성화하려면:

```sh
   zstyle ':omz:update' mode disabled
   ```

설정을 통해 Oh My Zsh가 업데이트를 확인하는 빈도를 조절할 수 있습니다:

```sh
# This will check for updates every 7 days
zstyle ':omz:update' frequency 7
# This will check for updates every time you open the terminal (not recommended)
zstyle ':omz:update' frequency 0
```

### 업데이트 세부 정보 수준

업데이트 세부 정보 수준을 다음 설정으로 제한할 수도 있습니다:

```sh
zstyle ':omz:update' verbose default # default update prompt

zstyle ':omz:update' verbose minimal # only few lines

zstyle ':omz:update' verbose silent # only errors
```

### 수동 업데이트

어떤 시점에서든 업데이트를 원하는 경우(예: 누군가 새로운 플러그인을 출시했고, 한 주를 기다리고 싶지 않다면) 다음 명령을 실행하면 됩니다:

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
> FAQ: How do I update Oh My Zsh?](https://github.com/ohmyzsh/ohmyzsh/wiki/FAQ#how-do-i-update-oh-my-zsh)에서 더 많은 옵션을 확인하세요.
>
> **`omz update --unattended`의 사용은 부작용이 있기 때문에 제거되었습니다**.

마법! 🎉

## Oh My Zsh 비우전

Oh My Zsh는 모든 사람에게 적합하지 않습니다. 떠나게 되어 안타깝지만, 이 과정을 쉽게 만들어 드리고자 합니다.

`oh-my-zsh`를 비우전하려면 명령줄에서 `uninstall_oh_my_zsh`를 실행하면 됩니다. 이는 자신을 제거하고 이전의 `bash` 또는 `zsh` 설정으로 되돌릴 것입니다.

## Oh My Zsh에 기여하는 방법은?

우리의 즐거운 커뮤니티에 참여하기 전에 [코드 오브 컨덕트](../CODE_OF_CONDUCT.md)를 읽어보세요.

저는 [Zsh](https://www.zsh.org/) 전문가가 아니며, 개선할 수 있는 방법이 많다고 생각합니다. 구성이 더 쉽게 유지되고 빠르게 될 수 있도록 아이디어가 있다면 주저하지 말고 fork하고 pull request를 보내주세요!

pull request를 테스트할 사람도 필요합니다. 따라서 [열린 이슈](https://github.com/ohmyzsh/ohmyzsh/issues)를 살펴보고 도움이 필요한 곳에서 도와주세요.

자세한 내용은 [기여하기](../CONTRIBUTING.md)를 참조하세요.

### 우리에게 테마를 보내지 마세요

현재는 충분한 테마가 있으므로, 테마를 [외부 테마](https://github.com/ohmyzsh/ohmyzsh/wiki/External-themes) 위키 페이지에 추가해 주세요.

## 기여자

Oh My Zsh에는 행복한 사용자들과 즐거운 기여자들이 모인 생생한 커뮤니티가 있습니다. 기여자들이 제공한 시간과 도움 없이도 Oh My Zsh는 이렇게 멋진 프로젝트가 될 수 없었을 것입니다.

정말 감사합니다!

<a href="https://github.com/ohmyzsh/ohmyzsh/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ohmyzsh/ohmyzsh" width="100%"/>
</a>

## 팔로우 하세요

우리는 소셜 미디어에 있습니다:

- X (구 트위터)에 [@ohmyzsh](https://x.com/ohmyzsh) 계정을 팔로우하세요.
- [Facebook](https://www.facebook.com/Oh-My-Zsh-296616263819290/)에서 우리를 펑크하세요.
- [Instagram](https://www.instagram.com/_ohmyzsh/)에서 Oh My Zsh!를 보여주는 게시물에 우리를 태그하세요.
- [Discord](https://discord.gg/ohmyzsh)에서 우리와 대화해보세요!

## 상품

우리는 당신이 Oh My Zsh에 대한 사랑을 과시할 수 있는
[스티커, 티셔츠, 그리고 커피 머그](https://commitgoods.com/collections/oh-my-zsh?utm_source=github)
를 제공합니다. 다시 한 번, 당신은 도시의 화제가 될 것입니다!

## 라이선스

Oh My Zsh는 [MIT 라이선스](../LICENSE.txt) 하에 배포됩니다.

## Planet Argon에 대해

![Planet Argon](https://pa-github-assets.s3.amazonaws.com/PARGON_logo_digital_COL-small.jpg)

Oh My Zsh was started by the team at [Planet Argon](https://www.planetargon.com/?utm_source=github), a
[Ruby on Rails development agency](https://www.planetargon.com/services/ruby-on-rails-development?utm_source=github).
Check out our [other open source projects](https://www.planetargon.com/open-source?utm_source=github).

