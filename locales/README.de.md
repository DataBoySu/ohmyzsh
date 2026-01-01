<!--START_SECTION:navbar-->
<div align="center">
  <a href="../README.md">🇺🇸 English</a> | <a href="README.de.md">🇩🇪 Deutsch</a> | <a href="README.es.md">🇪🇸 Español</a> | <a href="README.fr.md">🇫🇷 Français</a> | <a href="README.hi.md">🇮🇳 हिंदी</a> | <a href="README.ja.md">🇯🇵 日本語</a> | <a href="README.ko.md">🇰🇷 한국어</a> | <a href="README.pt.md">🇵🇹 Português</a> | <a href="README.ru.md">🇷🇺 Русский</a> | <a href="README.zh.md">🇨🇳 中文</a>
</div>
<!--END_SECTION:navbar-->

<p align="center"><img src="https://ohmyzsh.s3.amazonaws.com/omz-ansi-github.png" alt="Oh My Zsh"></p>

Oh My Zsh ist ein Open-Source-Framework, das von der Community getrieben wird, um deine [zsh](https://www.zsh.org/)-Konfiguration zu verwalten.

Klingt langweilig. Versuchen wir es nochmal.

**Oh My Zsh wird dich nicht zu einem 10x-Entwickler machen...aber du wirst dich so fühlen.**

Nach der Installation wird dein Terminal-Shell zum Gesprächsthema der Stadt _oder du erhältst dein Geld zurück!_ Mit jedem Tastendruck in deinem Befehlszeilenfenster wirst du die zahlreichen mächtigen Plugins und wunderschönen Themes nutzen können. Fremde werden dich in Cafés ansprechen und fragen: _"Das ist unglaublich! Bist du irgendein Genie?"_

Schließlich wirst du die Art von Aufmerksamkeit erhalten, die du dir immer verdient haben wolltest. ...oder vielleicht wirst du die Zeit nutzen, die du sparst, um häufiger mit der Zahnseide zu flossen. 😬

Um mehr zu erfahren, besuche [ohmyz.sh](https://ohmyz.sh), folge [@ohmyzsh](https://x.com/ohmyzsh) auf X (früher Twitter) und tritt uns auf [Discord](https://discord.gg/ohmyzsh) bei.

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

| O/S            | Status |
| :------------- | :----: |
| Android        |   ✅   |
| freeBSD        |   ✅   |
| LCARS          |   🛸   |
| Linux          |   ✅   |
| macOS          |   ✅   |
| OS/2 Warp      |   ❌   |
| Windows (WSL2) |   ✅   |

### Voraussetzungen

- [Zsh](https://www.zsh.org) sollte installiert sein (v4.3.9 oder neuer ist in Ordnung, aber wir bevorzugen 5.0.8 und
  neuer). Wenn nicht vorinstalliert (führe `zsh --version` aus, um zu überprüfen), siehe die folgenden Wiki-Anweisungen hier:
  [ZSH installieren](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
- `curl` oder `wget` sollte installiert sein
- `git` sollte installiert sein (empfohlen v2.4.11 oder höher)

### Grundinstallation

Oh My Zsh wird installiert, indem du einen der folgenden Befehle in deinem Terminal ausführst. Du kannst dies über die Kommandozeile mit entweder `curl`, `wget` oder einem anderen ähnlichen Tool installieren.

| Methode    | Befehl                           |
| :-------- | : |
| **curl**  | `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |
| **wget**  | `sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`   |
| **fetch** | `sh -c "$(fetch -o - https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |

Alternativ ist der Installer auch außerhalb von GitHub gespiegelt. Die Verwendung dieses URLs kann erforderlich sein, wenn du in einem Land wie China oder Indien bist (für bestimmte ISPs), das `raw.githubusercontent.com` blockiert:

| Methode    | Befehl |
| :-------- | : |
| **curl**  | `sh -c "$(curl -fsSL https://install.ohmyz.sh/)"` |
| **wget**  | `sh -c "$(wget -O- https://install.ohmyz.sh/)"`   |
| **fetch** | `sh -c "$(fetch -o - https://install.ohmyz.sh/)"` |

Beachte, dass jede vorherige `.zshrc` in `.zshrc.pre-oh-my-zsh` umbenannt wird. Nach der Installation kannst du die Konfiguration, die du behalten möchtest, in die neue `.zshrc` verschieben.

#### Manuelle Überprüfung

Es ist eine gute Idee, das Installations-Skript von Projekten zu überprüfen, die du noch nicht kennst. Das kannst du tun, indem
du das Installations-Skript zunächst herunterlädst, es durchliest, um sicherzustellen, dass alles normal aussieht, und es dann ausführst:

```sh
wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh
sh install.sh
```

Wenn die oben genannte URL abläuft oder anderweitig fehlschlägt, musst du möglicherweise die URL durch `https://install.ohmyz.sh` ersetzen, um das Skript abrufen zu können.

## Oh My Zsh verwenden

### Plugins

Oh My Zsh kommt mit einer Menge an Plugins, von denen du profitieren kannst. Du kannst im
[plugins](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins) Verzeichnis und/oder der
[wiki](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins) sehen, was derzeit verfügbar ist.

#### Aktivieren von Plugins

Sobald du ein Plugin (oder mehrere) gefunden hast, das du mit Oh My Zsh verwenden möchtest, musst du es in der
`.zshrc`-Datei aktivieren. Du findest die zshrc-Datei in deinem `$HOME`-Verzeichnis. Öffne sie mit deinem bevorzugten Texteditor
und du wirst einen Abschnitt sehen, in dem du alle Plugins auflisten kannst, die du laden möchtest.

```sh
vi ~/.zshrc
```

Zum Beispiel könnte das so aussehen:

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

Achte darauf, dass die Plugins durch Whitespace (Leerzeichen, Tabs, neue Zeilen...) getrennt sind. **Verwende** keine Kommas zwischen ihnen, sonst wird es nicht funktionieren.

#### Plugins verwenden

Jeder integrierte Plugin enthält eine **README**, die ihn dokumentiert. Diese README sollte die Aliase (falls das Plugin welche hinzufügt) und zusätzliche Vorteile anzeigen, die in diesem bestimmten Plugin enthalten sind.

### Themes

Wir geben es zu. Früh in der Oh My Zsh-Welt haben wir vielleicht etwas zu sehr auf Themes gesetzt. Wir haben jetzt über
einhundertfünfzig Themes in der Box. Die meisten von ihnen haben
[screenshots](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes) auf der Wiki-Seite (Wir arbeiten daran, dies zu aktualisieren!).
Schau sie dir an!

#### Ein Thema auswählen

Robbys Theme ist das Standard-Theme. Es ist nicht das aufwendigste. Es ist nicht das einfachste. Es ist einfach das richtige (für ihn).

Sobald du ein Theme gefunden hast, das du verwenden möchtest, musst du die Datei `~/.zshrc` bearbeiten. Dort wirst du eine Umgebungsvariable (in Großbuchstaben) finden, die so aussieht wie:

```sh
ZSH_THEME="robbyrussell"
```

Um ein anderes Theme zu verwenden, ändere einfach den Wert so, dass er dem Namen deines gewünschten Themes entspricht. Zum Beispiel:

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

Und wenn du ein zufälliges Theme aus einer Liste deiner Favoriten auswählen möchtest:

```sh
ZSH_THEME_RANDOM_CANDIDATES=(
  "robbyrussell"
  "agnoster"
```

Wenn du nur weißt, welche Themen dir nicht gefallen, kannst du sie ähnlich wie eine ignorierte Liste hinzufügen:

```sh
ZSH_THEME_RANDOM_IGNORED=(pygmalion tjkirch_mod)
```

### FAQ

Wenn du noch mehr Fragen oder Probleme hast, findest du möglicherweise eine Lösung in unserem
[FAQ](https://github.com/ohmyzsh/ohmyzsh/wiki/FAQ).

## Fortgeschrittene Themen

Wenn du der Typ bist, der gern mit den Händen schmutzig wird, könnten diese Abschnitte auf dich zutreffen.

### Erweiterte Installation

Einige Benutzer möchten Oh My Zsh manuell installieren oder den Standardpfad oder andere Einstellungen ändern, die der
Installer akzeptiert (diese Einstellungen sind auch am Anfang des Installationsskripts dokumentiert).

#### Benutzerdefiniertes Verzeichnis

Der Standardort ist `~/.oh-my-zsh` (versteckt in deinem Home-Verzeichnis, du kannst es mit
`cd ~/.oh-my-zsh` aufrufen)

Wenn du das Installationsverzeichnis mit der Umgebungsvariable `ZSH` ändern möchtest, entweder indem du
`export ZSH=/dein/pfad` vor der Installation ausführst, oder indem du sie vor Ende der Installationspipeline so festlegst:

```sh
ZSH="$HOME/.dotfiles/oh-my-zsh" sh install.sh
```

#### Unattended Install

Wenn du das Oh My Zsh-Installationsskript als Teil einer automatisierten Installation ausführst, kannst du dem Skript `install.sh` den Flag `--unattended` übergeben. Dies hat den Effekt, dass nicht versucht wird, die Standard-Shell zu ändern, und es wird auch nicht `zsh` nach Abschluss der Installation gestartet.

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" "" --unattended
```

Wenn du dich in China, Indien oder einem anderen Land befindest, das `raw.githubusercontent.com` blockiert, musst du möglicherweise die URL für `https://install.ohmyz.sh` verwenden, damit die Installation funktioniert.

#### Aus einem Forked Repository installieren

Das Installations-Skript akzeptiert auch diese Variablen, um die Installation aus einem anderen Repository zu ermöglichen:

- `REPO` (Standard: `ohmyzsh/ohmyzsh`): dies hat die Form `owner/repository`. Wenn du diese Variable festlegst,
  sucht der Installer ein Repository unter `https://github.com/{owner}/{repository}`.

- `REMOTE` (Standard: `https://github.com/${REPO}.git`): dies ist die vollständige URL des Git-Repository-Clones. Du
  kannst diese Einstellung verwenden, wenn du aus einem Fork installieren möchtest, der nicht auf GitHub liegt (GitLab, Bitbucket...) oder wenn
  du lieber mit SSH als HTTPS klonen möchtest (`git@github.com:user/project.git`).

  _HINWEIS: dies ist mit der Festlegung der `REPO`-Variable nicht kompatibel. Diese Einstellung hat Vorrang._

- `BRANCH` (Standard: `master`): du kannst diese Einstellung verwenden, wenn du die Standard-Zweig-Verzweigung ändern möchtest, die beim Klonen des Repositorys ausgecheckt wird. Dies könnte nützlich sein, um einen Pull Request zu testen oder wenn du einen Zweig verwenden möchtest, der nicht `master` ist.

Beispiel:

```sh
REPO=apjanke/oh-my-zsh BRANCH=edge sh install.sh
```

#### Manuelle Installation

##### 1. Clone The Repository <!-- omit in toc -->

```sh
git clone https://github.com/ohmyzsh/ohmyzsh.git ~/.oh-my-zsh
```

##### 2. _Optionally_, Backup Your Existing `~/.zshrc` File <!-- omit in toc -->

```sh
cp ~/.zshrc ~/.zshrc.orig
```

##### 3. Create A New Zsh Configuration File <!-- omit in toc -->

Du kannst eine neue zsh-Konfigurationsdatei erstellen, indem du die Vorlage kopierst, die wir für dich eingeschlossen haben.

```sh
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
```

##### 4. Change Your Default Shell <!-- omit in toc -->

```sh
chsh -s $(which zsh)
```

Du musst dich aus deinem Benutzerkontext abmelden und dich erneut anmelden, um diese Änderung zu sehen.

##### 5. Initialize Your New Zsh Configuration <!-- omit in toc -->

Sobald du ein neues Terminalfenster öffnest, sollte es zsh mit der Konfiguration von Oh My Zsh laden.

### Installation Problems

Wenn du Probleme beim Installieren hast, hier sind ein paar häufige Lösungen.

- Du _kannst_ möglicherweise deinen `PATH` in `~/.zshrc` ändern, wenn du einige Befehle nicht finden kannst, nachdem
  du zu `oh-my-zsh` gewechselt hast.
- Wenn du manuell installiert hast oder den Installationsort geändert hast, prüfe die `ZSH`-Umgebungsvariable in
  `~/.zshrc`.

### Benutzerdefinierte Plugins und Themes

Wenn du irgendeine der Standardverhaltensweisen überschreiben möchtest, füge einfach eine neue Datei (mit Endung `.zsh`) im Verzeichnis `custom/` hinzu.

Wenn du viele Funktionen hast, die gut zusammenpassen, kannst du sie als Datei `XYZ.plugin.zsh` im Verzeichnis `custom/plugins/` ablegen und anschließend dieses Plugin aktivieren.

Wenn du die Funktionalität eines Plugins, das mit Oh My Zsh geliefert wird, überschreiben möchtest, erstelle ein Plugin mit demselben Namen im Verzeichnis `custom/plugins/` und es wird stattdessen geladen.

### GNU ls in macOS und FreeBSD-Systemen aktivieren

<a name="enable-gnu-ls"></a>

Das Standardverhalten in Oh My Zsh ist es, BSD `ls` in macOS und FreeBSD-Systemen zu verwenden. Wenn GNU `ls` installiert
(als `gls`-Befehl), kannst du entscheiden, es stattdessen zu verwenden. Um das zu tun, kannst du eine zstyle-basierte Konfiguration verwenden, bevor
du `oh-my-zsh.sh` einbindest:

```zsh
zstyle ':omz:lib:theme-and-appearance' gnu-ls yes
```

_Hinweis: Dies ist nicht mit `DISABLE_LS_COLORS=true` kompatibel_

### Aliase überspringen

<a name="remove-directories-aliases"></a>

Wenn du die Standard-Aliase von Oh My Zsh (die in den Dateien `lib/*` definiert sind) oder Plugin-Aliase überspringen möchtest, kannst du die unten aufgeführten Einstellungen in deine Datei `~/.zshrc` einfügen, **bevor Oh My Zsh geladen wird**. Beachte, dass es viele verschiedene Wege gibt, Aliase zu überspringen, je nach deinen Anforderungen.

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

Du kannst sie auf andere Weisen kombinieren, wobei spezifischere Bereiche Vorrang haben:

```sh
# Skip all plugin aliases, except for the git plugin
zstyle ':omz:plugins:*' aliases no
zstyle ':omz:plugins:git' aliases yes
```

Eine frühere Version dieser Funktion verwendete die unten genannte Einstellung, die entfernt wurde:

```sh
zstyle ':omz:directories' aliases no
```

Stattdessen kannst du nun folgendes verwenden:

```sh
zstyle ':omz:lib:directories' aliases no
```

#### Notice <!-- omit in toc -->

> Diese Funktion befindet sich derzeit in der Testphase und kann sich in der Zukunft ändern. Sie ist außerdem derzeit nicht
> mit Plugin-Verwaltungsprogrammen wie zpm oder zinit kompatibel, die das init-Skript
> (`oh-my-zsh.sh`) nicht laden, in dem diese Funktion implementiert ist.

> Sie ist außerdem derzeit nicht in der Lage, "Aliases" zu erkennen, die als Funktionen definiert sind. Beispiele hierfür sind die Funktionen `gccd`,
> `ggf` oder `ggl` aus dem git-Plugin.

### Async git prompt

Async Prompt-Funktionen sind ein experimentelles Feature (eingeführt am 3. April 2024), das Oh My Zsh ermöglicht, Prompt-Informationen asynchron darzustellen. Dies kann die Prompt-Rendering-Leistung verbessern, könnte aber bei einigen Konfigurationen nicht gut funktionieren. Wir hoffen, dass das kein Problem darstellt, aber wenn du Probleme mit dieser neuen Funktion siehst, kannst du sie durch Festlegen des folgenden Eintrags in deiner .zshrc-Datei vor dem Laden von Oh My Zsh deaktivieren:

```sh
zstyle ':omz:alpha:lib:git' async-prompt no
```

Wenn dein Problem darin besteht, dass der git-Prompt einfach nicht mehr erscheint, kannst du versuchen, dies durch Festlegen der folgenden Konfiguration vor der Einbindung von `oh-my-zsh.sh` zu erzwingen. Wenn es dennoch nicht funktioniert, öffne bitte ein Ticket mit deinem Fall.

```sh
zstyle ':omz:alpha:lib:git' async-prompt force
```

## Aktualisierungen erhalten

Standardmäßig wirst du alle 2 Wochen aufgefordert, nach Updates zu suchen. Du kannst andere Aktualisierungsmodi wählen, indem
du eine Zeile zu deiner `~/.zshrc`-Datei hinzufügst, **bevor Oh My Zsh geladen wird**:

1. Automatische Aktualisierung ohne Bestätigungsprompt:

```sh
   zstyle ':omz:update' mode auto
   ```

2. Biete einfach alle paar Tage eine Erinnerung an, wenn Updates verfügbar sind:

```sh
   zstyle ':omz:update' mode reminder
   ```

3. Um die automatischen Updates vollständig zu deaktivieren:

```sh
   zstyle ':omz:update' mode disabled
   ```

HINWEIS: Du kannst steuern, wie oft Oh My Zsh nach Updates sucht, mit der folgenden Einstellung:

```sh
# This will check for updates every 7 days
zstyle ':omz:update' frequency 7
# This will check for updates every time you open the terminal (not recommended)
zstyle ':omz:update' frequency 0
```

### Updates Verbosity

Du kannst auch die Update-Lautstärke mit den folgenden Einstellungen beschränken:

```sh
zstyle ':omz:update' verbose default # default update prompt

zstyle ':omz:update' verbose minimal # only few lines

zstyle ':omz:update' verbose silent # only errors
```

### Manuelle Updates

Wenn du zu einem beliebigen Zeitpunkt aktualisieren möchtest (vielleicht wurde gerade ein neues Plugin veröffentlicht und du möchtest nicht eine Woche warten?), musst du einfach folgendes ausführen:

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
> Siehe weitere Optionen in der [FAQ: Wie aktualisiere ich Oh My Zsh?](https://github.com/ohmyzsh/ohmyzsh/wiki/FAQ#how-do-i-update-oh-my-zsh).
>
> **DIE VERWENDUNG VON `omz update --unattended` WURDE ENTFERNT, DA SIE SEITENWIRKUNGEN HAT**.

Magie! 🎉

## Oh My Zsh deinstallieren

Oh My Zsh ist nicht für jeden. Wir werden dich vermissen, aber wir möchten, dass dieser Abschied leichtfällt.

Wenn du `oh-my-zsh` deinstallieren möchtest, führe einfach `uninstall_oh_my_zsh` von der Kommandozeile aus. Es wird sich selbst entfernen und deine vorherige `bash`- oder `zsh`-Konfiguration rückgängig machen.

## Wie trage ich zu Oh My Zsh bei?

Bevor du in unsere wundervolle Community mitwirkt, lies bitte die [Code of Conduct](../CODE_OF_CONDUCT.md).

Ich bin noch weit von einem [Zsh](https://www.zsh.org/-Experten entfernt und vermute, dass es viele Möglichkeiten gibt, um Verbesserungen vorzunehmen – wenn du
Idee hast, wie die Konfiguration einfacher zu warten und schneller zu machen ist, zögere nicht, einen Fork zu erstellen und Pull-Requests zu senden!

Wir benötigen auch Menschen, die Pull-Requests testen. Schau dir also
[offene Issues](https://github.com/ohmyzsh/ohmyzsh/issues) an und hilf wo du kannst.

Siehe [Contributing](../CONTRIBUTING.md) für weitere Details.

### Send uns keine Themes

Wir haben (mehr als) genug Themes für den Moment. Füge dein Theme bitte zur
[externen Themes](https://github.com/ohmyzsh/ohmyzsh/wiki/External-themes) Wiki-Seite hinzu.

## Mitwirkende

Oh My Zsh hat eine lebendige Community aus glücklichen Nutzern und großartigen Mitwirkenden. Ohne die Zeit und den Support unserer Mitwirkenden wäre es nicht so großartig.

Vielen, vielen Dank!

<a href="https://github.com/ohmyzsh/ohmyzsh/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ohmyzsh/ohmyzsh" width="100%"/>
</a>

## Folge uns

Wir sind auf sozialen Medien:

- [@ohmyzsh](https://x.com/ohmyzsh) auf X (früher Twitter). Du solltest uns folgen.
- [Facebook](https://www.facebook.com/Oh-My-Zsh-296616263819290/) poke uns.
- [Instagram](https://www.instagram.com/_ohmyzsh/) tag uns in deinem Beitrag mit Oh My Zsh!
- [Discord](https://discord.gg/ohmyzsh) um mit uns zu chatten!

## Merchandise

Wir haben
[Sticker, Shirts und Kaffeetassen verfügbar](https://commitgoods.com/collections/oh-my-zsh?utm_source=github)
für dich, um deine Liebe zu Oh My Zsh zu zeigen. Wieder einmal wirst du der Gesprächsstoff der Stadt sein!

## Lizenz

Oh My Zsh wird unter der [MIT-Lizenz](../LICENSE.txt) veröffentlicht.

## Über Planet Argon

![Planet Argon](https://pa-github-assets.s3.amazonaws.com/PARGON_logo_digital_COL-small.jpg)

Oh My Zsh was started by the team at [Planet Argon](https://www.planetargon.com/?utm_source=github), a
[Ruby on Rails development agency](https://www.planetargon.com/services/ruby-on-rails-development?utm_source=github).
Check out our [other open source projects](https://www.planetargon.com/open-source?utm_source=github).

