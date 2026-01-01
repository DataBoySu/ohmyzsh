<!--START_SECTION:navbar-->
<div align="center">
  <a href="../README.md">🇺🇸 English</a> | <a href="README.de.md">🇩🇪 Deutsch</a> | <a href="README.es.md">🇪🇸 Español</a> | <a href="README.fr.md">🇫🇷 Français</a> | <a href="README.hi.md">🇮🇳 हिंदी</a> | <a href="README.ja.md">🇯🇵 日本語</a> | <a href="README.ko.md">🇰🇷 한국어</a> | <a href="README.pt.md">🇵🇹 Português</a> | <a href="README.ru.md">🇷🇺 Русский</a> | <a href="README.zh.md">🇨🇳 中文</a>
</div>
<!--END_SECTION:navbar-->

<p align="center"><img src="https://ohmyzsh.s3.amazonaws.com/omz-ansi-github.png" alt="Oh My Zsh"></p>

Oh My Zsh は、[zsh](https://www.zsh.org/) の設定を管理するためのオープンソースでコミュニティドリブンなフレームワークです。

退屈ですね。もう一度試してみましょう。

**Oh My Zsh はあなたを 10 倍の開発者にはなりません...しかし、そう感じることになるかもしれません。**

インストール後、あなたのターミナルシェルは町で話題になることでしょう _または、お金は返金します！_ コマンドプロンプトでキーを打つたびに、数百の強力なプラグインと美しいテーマの利点を享受できます。カフェで見知らぬ人があなたに近づいてきて、_"それは素晴らしいですね！あなたは天才ですか？"_ と尋ねることでしょう。

やがて、あなたが常に感じていたように、注目されるようになるでしょう。...または、節約した時間を活用して、もっとフロスをすることになるかもしれません。 😬

詳しくは [ohmyz.sh](https://ohmyz.sh) を訪問し、X（旧 Twitter）の [@ohmyzsh](https://x.com/ohmyzsh) をフォローし、[Discord](https://discord.gg/ohmyzsh) に参加してください。

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

## Getting Started

### Operating System Compatibility

| O/S            | ステータス |
| :------------- | :----: |
| Android        |   ✅   |
| freeBSD        |   ✅   |
| LCARS          |   🛸   |
| Linux          |   ✅   |
| macOS          |   ✅   |
| OS/2 Warp      |   ❌   |
| Windows (WSL2) |   ✅   |

### 事前条件

- [Zsh](https://www.zsh.org) がインストールされている必要があります (v4.3.9 以降は問題ありませんが、5.0.8 以降が推奨されます)。事前にインストールされていない場合は (`zsh --version` を実行して確認)、ここにある以下の Wiki の指示に従ってください: [ZSH のインストール](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
- `curl` または `wget` がインストールされている必要があります
- `git` がインストールされている必要があります (推奨バージョンは v2.4.11 以降)

### 基本的なインストール

Oh My Zsh は、端末で以下のコマンドのいずれかを実行することによってインストールされます。`curl`、`wget`、または他の類似のツールを使用してコマンドラインからインストールできます。

| メソッド | コマンド                           |
| :-------- | : |
| **curl**  | `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |
| **wget**  | `sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`   |
| **fetch** | `sh -c "$(fetch -o - https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |

代替として、インストーラーは GitHub の外にミラーリングされています。`raw.githubusercontent.com` がブロックされている場合（中国やインドなどの一部の ISP で）、この URL を使用する必要があります。

| メソッド | コマンド |
| :-------- | : |
| **curl**  | `sh -c "$(curl -fsSL https://install.ohmyz.sh/)"` |
| **wget**  | `sh -c "$(wget -O- https://install.ohmyz.sh/)"`   |
| **fetch** | `sh -c "$(fetch -o - https://install.ohmyz.sh/)"` |

以前の `.zshrc` は `.zshrc.pre-oh-my-zsh` にリネームされます。インストール後、保持したい設定を新しい `.zshrc` に移動できます。

#### 手動検査

既知のプロジェクト以外のインストールスクリプトを確認することは良いアイデアです。それにはまずインストールスクリプトをダウンロードし、中身を確認してすべてが正常であることを確認した後、それを実行します。

```sh
wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh
sh install.sh
```

上記のURLがタイムアウトしたり、他の理由で失敗した場合、スクリプトを取得できるように `https://install.ohmyz.sh` にURLを置き換える必要があるかもしれません。

## Oh My Zsh の使用

### プラグイン

Oh My Zsh には、活用できるプラグインがたくさん含まれています。[plugins](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins) ディレクトリおよび/[wiki](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins) を確認して、現在利用可能なものを確認してください。

#### プラグインの有効化

Oh My Zshで使用したいプラグイン（または複数のプラグイン）を見つけたら、`.zshrc`ファイルでそれらを有効にする必要があります。`.zshrc`ファイルは`$HOME`ディレクトリ内にあります。お気に入りのテキストエディタでそれを開き、読み込むプラグインをすべて一覧表示するセクションが表示されます。

```sh
vi ~/.zshrc
```

例えば、これは次のように見えるようになるかもしれません：

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

プラグインは空白文字 (スペース、タブ、改行など) で区切られています。**使用しないでください**。それらの間にコンマを使用すると動作が破損します。

#### プラグインの使用

各組み込みプラグインには、**README** が含まれており、そのプラグインについて文書化しています。この README には、プラグインが任意で追加するエイリアスと、その特定のプラグインに含まれる追加の機能が表示されます。

### テーマ

認めます。Oh My Zshの世界が始まった当初、テーマに少し過度に熱中していたかもしれません。現在では150以上のテーマがバンドルされています。その多くは
[screenshots](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes)（このページの更新作業中です）にwikiに掲載されています。ぜひチェックしてみてください！

#### テーマの選択

Robbyのテーマはデフォルトのものです。最も豪華なテーマではありません。最もシンプルなテーマでもありません。ただ、彼にとって正しいテーマなのです。

ご希望のテーマを見つけたら、`~/.zshrc`ファイルを編集する必要があります。そこには、すべて大文字で表記された環境変数が表示され、以下のように見えます。

```sh
ZSH_THEME="robbyrussell"
```

別のテーマを使用するには、値を希望するテーマの名前に変更するだけです。例えば：

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

リストからランダムなテーマを選択したい場合は：

```sh
ZSH_THEME_RANDOM_CANDIDATES=(
  "robbyrussell"
  "agnoster"
```

もしもご希望のテーマが分からないが、嫌いなテーマが分かっている場合は、無視リストに同様に追加できます。

```sh
ZSH_THEME_RANDOM_IGNORED=(pygmalion tjkirch_mod)
```

### FAQ

ご質問や問題がある場合は、[FAQ](https://github.com/ohmyzsh/ohmyzsh/wiki/FAQ)で解決策を見つけることができるかもしれません。

## 高度なトピック

汚い手を好むタイプであれば、これらのセクションが共鳴するかもしれません。

### 高度なインストール

一部のユーザーは、Oh My Zsh を手動でインストールするか、インストーラーが受け入れるデフォルトのパスやその他の設定を変更したい場合があります（これらの設定はインストールスクリプトの先頭にも記載されています）。

#### カスタムディレクトリ

デフォルトの場所は `~/.oh-my-zsh` です（ホームディレクトリ内に隠されています。`cd ~/.oh-my-zsh` でアクセスできます）

`ZSH` 環境変数を使用してインストールディレクトリを変更したい場合は、インストール前に `export ZSH=/your/path` を実行するか、インストールパイプラインの終了前に設定する方法があります。

```sh
ZSH="$HOME/.dotfiles/oh-my-zsh" sh install.sh
```

#### Unattended Install

自動インストールとして Oh My Zsh インストールスクリプトを実行している場合、`install.sh` スクリプトに `--unattended` フラグを渡すことができます。これにより、デフォルトシェルを変更しようとせず、インストールが完了した後も `zsh` を実行しないようになります。

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" "" --unattended
```

中国、インド、または `raw.githubusercontent.com` がブロックされている他の国にいる場合、インストールするには `https://install.ohmyz.sh` の URL を代わりに使用する必要があるかもしれません。

#### フォークされたリポジトリからインストール

インストールスクリプトは、別のリポジトリからインストールできるようにするための変数を受け入れます:

- `REPO` (デフォルト: `ohmyzsh/ohmyzsh`): この形式は `owner/repository` です。この変数を設定すると、インストーラーは `https://github.com/{owner}/{repository}` にリポジトリを検索します。

- `REMOTE` (デフォルト: `https://github.com/${REPO}.git`): これは git リポジトリをクローンするための完全な URL です。GitLab、Bitbucket などの GitHub 以外のフォークからインストールしたい場合、または SSH でクローンしたい場合 (`git@github.com:user/project.git`) にこの設定を使用できます。

  _注意: `REPO` 変数を設定する場合と互換性がありません。この設定が優先されます。_

- `BRANCH` (デフォルト: `master`): リポジトリをクローンするときにチェックアウトするデフォルトブランチを変更したい場合にこの設定を使用できます。Pull Request をテストする場合や、`master` 以外のブランチを使用したい場合に役立ちます。

例えば:

```sh
REPO=apjanke/oh-my-zsh BRANCH=edge sh install.sh
```

#### 手動インストール

##### 1. Clone The Repository <!-- omit in toc -->

```sh
git clone https://github.com/ohmyzsh/ohmyzsh.git ~/.oh-my-zsh
```

##### 2. _Optionally_, Backup Your Existing `~/.zshrc` File <!-- omit in toc -->

```sh
cp ~/.zshrc ~/.zshrc.orig
```

##### 3. Create A New Zsh Configuration File <!-- omit in toc -->

新しい zsh 設定ファイルを作成するには、我々が用意したテンプレートをコピーしてください。

```sh
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
```

##### 4. Change Your Default Shell <!-- omit in toc -->

```sh
chsh -s $(which zsh)
```

ユーザーセッションからログアウトし、再度ログインしてこの変更を確認してください。

##### 5. Initialize Your New Zsh Configuration <!-- omit in toc -->

新しいターミナルウィンドウを開くと、Oh My Zshの設定とともにzshが読み込まれます。

### インストール時の問題

インストール中に問題が発生した場合は、以下にいくつかの一般的な修正方法を示します。

- `oh-my-zsh` に切り替えた後、いくつかのコマンドが見つからない場合は、`~/.zshrc` に `PATH` を変更する必要があるかもしれません。
- 手動でインストールした場合、またはインストール場所を変更した場合は、`~/.zshrc` に `ZSH` 環境変数を確認してください。

### カスタムプラグインとテーマ

デフォルトの動作を上書きしたい場合は、`custom/` ディレクトリに `.zsh` で終わる新しいファイルを追加するだけです。

多くの関数が一緒に動作する場合は、`custom/plugins/` ディレクトリに `XYZ.plugin.zsh` ファイルとして配置し、その後でこのプラグインを有効にできます。

Oh My Zsh にバンドルされているプラグインの機能を上書きしたい場合は、`custom/plugins/` ディレクトリに同じ名前のプラグインを作成し、`plugins/` ディレクトリにあるもののかわりに読み込まれます。

### GNU ls を macOS および freeBSD システムで有効にする

<a name="enable-gnu-ls"></a>

Oh My Zsh のデフォルトの動作は、macOS および FreeBSD システムで BSD `ls` を使用することです。GNU `ls` がインストールされている場合（`gls` コマンドとして）、代わりにこれを使用するように選択できます。これを行うには、`oh-my-zsh.sh` をソース化する前に、zstyleベースの設定を使用してください。

```zsh
zstyle ':omz:lib:theme-and-appearance' gnu-ls yes
```

ノート: `DISABLE_LS_COLORS=true` と互換性がありません。

### Skip Aliases

<a name="remove-directories-aliases"></a>

デフォルトの Oh My Zsh のエイリアス (lib/* ファイルで定義されているもの) またはプラグインのエイリアスをスキップしたい場合は、Oh My Zsh が読み込まれる **以前** に `~/.zshrc` ファイルに以下の設定を使用してください。必要に応じて、エイリアスをスキップする方法はいくつかあります。

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

これらを他の方法で組み合わせることも可能ですが、より具体的なスコープが優先される点に注意してください。

```sh
# Skip all plugin aliases, except for the git plugin
zstyle ':omz:plugins:*' aliases no
zstyle ':omz:plugins:git' aliases yes
```

この機能の以前のバージョンでは、以下の設定を使用していましたが、この設定は削除されました:

```sh
zstyle ':omz:directories' aliases no
```

代わりに、以下を使用できます。

```sh
zstyle ':omz:lib:directories' aliases no
```

#### Notice <!-- omit in toc -->

> この機能は現在テストフェーズにあり、将来的に変更される可能性があります。また、zpmやzinitなどのプラグインマネージャーと現在は互換性がなく、これらはinitスクリプト（`oh-my-zsh.sh`）をソース化しないため、この機能が実装されている場所と互換性がありません。

> また、現在は関数として定義されている"エイリアス"については認識していません。このような例として、gitプラグインから提供されている`gccd`、`ggf`、または`ggl`などの関数があります。

### Async git prompt

Async prompt functions are an experimental feature (included on April 3, 2024) that allows Oh My Zsh to render
prompt information asynchronously. This can improve prompt rendering performance, but it might not work well
with some setups. We hope that's not an issue, but if you're seeing problems with this new feature, you can
turn it off by setting the following in your .zshrc file, before Oh My Zsh is sourced:

```sh
zstyle ':omz:alpha:lib:git' async-prompt no
```

git プロンプトが突然表示されなくなった場合、`oh-my-zsh.sh` が読み込まれる前に次の設定を強制的に適用してみてください。それでも動作しない場合は、ご自身のケースについて問題を報告してください。

```sh
zstyle ':omz:alpha:lib:git' async-prompt force
```

## 更新の確認

デフォルトでは、2週間ごとに更新を確認するよう促されます。Oh My Zsh が読み込まれる **以前** に `~/.zshrc` ファイルに1行を追加することで、他の更新モードを選択できます:

1. 確認ダイアログなしで自動更新:

```sh
   zstyle ':omz:update' mode auto
   ```

2. 数日ごとに更新が利用可能であることを確認するためのリマインダーを表示してください:

```sh
   zstyle ':omz:update' mode reminder
   ```

3. 自動更新を完全に無効にするには:

```sh
   zstyle ':omz:update' mode disabled
   ```

NOTE: お使いの Oh My Zsh が更新をチェックする頻度を設定で制御できます。

```sh
# This will check for updates every 7 days
zstyle ':omz:update' frequency 7
# This will check for updates every time you open the terminal (not recommended)
zstyle ':omz:update' frequency 0
```

### 更新の詳細度

更新の詳細度を次の設定で制限することもできます。

```sh
zstyle ':omz:update' verbose default # default update prompt

zstyle ':omz:update' verbose minimal # only few lines

zstyle ':omz:update' verbose silent # only errors
```

### マニュアル更新

いつでも更新したい場合（たとえば、新しいプラグインがリリースされたが、1週間待つのはしたくないなど）は、次を実行するだけです:

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
> FAQ: How do I update Oh My Zsh?](https://github.com/ohmyzsh/ohmyzsh/wiki/FAQ#how-do-i-update-oh-my-zsh) に詳しくは、オプションを確認してください。
>
> **`omz update --unattended` の使用は、副作用があるため削除されました**。

マジック！🎉

## Oh My Zshのアンインストール

Oh My Zshはすべての人に向いているわけではありません。さようならは惜しいですが、簡単に別れられるようにしたいです。

`oh-my-zsh`をアンインストールしたい場合は、コマンドラインから`uninstall_oh_my_zsh`を実行してください。これにより、自身を削除し、以前の`bash`または`zsh`の設定を元に戻します。

## Oh My Zsh に貢献する方法は?

コミュニティに参加する前に、[コード・オブ・コンダクト](../CODE_OF_CONDUCT.md) を必ずお読みください。

私は Zsh の専門家ではありませんし、改善点がたくさんあると思っています。設定をより簡単に、より高速に維持する方法についてのアイデアがあれば、遠慮なくフォークしてプルリクエストを送ってください！

プルリクエストのテストも手伝っていただけると嬉しいです。[オープンな問題](https://github.com/ohmyzsh/ohmyzsh/issues) を確認し、できる範囲で協力してください。

詳しくは [Contributing](../CONTRIBUTING.md) をご覧ください。

### ご提供いただけるテーマの送信をお断りいたします

現在のところ、十分なテーマをお持ちです。ご提供いただいているテーマは、
[外部テーマ](https://github.com/ohmyzsh/ohmyzsh/wiki/External-themes)のウィキページにご記載ください。

## 貢献者

Oh My Zsh には、喜びに満ちたユーザーと魅力的な貢献者が活躍する活発なコミュニティがあります。貢献者の皆さんの時間とご協力のおかげで、このような素晴らしいプロジェクトが実現しています。

本当にありがとうございます！

<a href="https://github.com/ohmyzsh/ohmyzsh/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ohmyzsh/ohmyzsh" width="100%"/>
</a>

## Follow Us

私たちのソーシャルメディア:

- [@ohmyzsh](https://x.com/ohmyzsh) で X (旧 Twitter) に登録してください。フォローしてください。
- [Facebook](https://www.facebook.com/Oh-My-Zsh-296616263819290/) で私たちにメッセージを送ってください。
- [Instagram](https://www.instagram.com/_ohmyzsh/) で投稿に Oh My Zsh! をタグ付けしてください。
- [Discord](https://discord.gg/ohmyzsh) で私たちとチャットしてください!

## 商品

お気に入りの Oh My Zsh をアピールするための
[ステッカー、シャツ、コーヒーマグ](https://commitgoods.com/collections/oh-my-zsh?utm_source=github)
がご用意されています。また、あなたは町の話題になるでしょう！

## ライセンス

Oh My Zsh は [MIT ライセンス](../LICENSE.txt) の下でリリースされています。

## About Planet Argon

![Planet Argon](https://pa-github-assets.s3.amazonaws.com/PARGON_logo_digital_COL-small.jpg)

Oh My Zsh was started by the team at [Planet Argon](https://www.planetargon.com/?utm_source=github), a
[Ruby on Rails development agency](https://www.planetargon.com/services/ruby-on-rails-development?utm_source=github).
Check out our [other open source projects](https://www.planetargon.com/open-source?utm_source=github).

