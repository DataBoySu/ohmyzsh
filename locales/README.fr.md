<!--START_SECTION:navbar-->
<div align="center">
  <a href="../README.md">🇺🇸 English</a> | <a href="README.de.md">🇩🇪 Deutsch</a> | <a href="README.fr.md">🇫🇷 Français</a> | <a href="README.hi.md">🇮🇳 हिंदी</a> | <a href="README.ja.md">🇯🇵 日本語</a> | <a href="README.ko.md">🇰🇷 한국어</a> | <a href="README.pt.md">🇵🇹 Português</a> | <a href="README.ru.md">🇷🇺 Русский</a> | <a href="README.zh.md">🇨🇳 中文</a>
</div>
<!--END_SECTION:navbar-->

<p align="center"><img src="https://ohmyzsh.s3.amazonaws.com/omz-ansi-github.png" alt="Oh My Zsh"></p>

Oh My Zsh est un cadre open source, communautaire pour gérer votre [zsh](https://www.zsh.org/)
configuration.

Ça semble ennuyeux. Essayons à nouveau.

**Oh My Zsh ne vous rendra pas 10 fois plus productif...mais vous pourriez vous sentir comme tel.**

Une fois installé, votre terminal shell deviendra le sujet de conversation dans le quartier _ou vous obtenez votre argent de retour !_ Avec chaque touche de clavier
dans votre invite de commande, vous profiterez des centaines de plugins puissants et de thèmes magnifiques.
Des inconnus viendront vers vous dans les cafés et vous demanderont, _"c'est incroyable ! êtes-vous un genre de génie ?"_

Enfin, vous commencerez à recevoir le type d'attention que vous avez toujours senti que vous méritiez. ...ou peut-être que vous utiliserez le temps que vous économisez pour commencer à faire du filage plus souvent. 😬

Pour en savoir plus, visitez [ohmyz.sh](https://ohmyz.sh), suivez [@ohmyzsh](https://x.com/ohmyzsh) sur X (anciennement
Twitter), et rejoignez-nous sur [Discord](https://discord.gg/ohmyzsh).

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

## Commencer

### Compatibilité du système d'exploitation

| Système d'exploitation | Statut |
| :--------------------- | :----: |
| Android                |   ✅   |
| freeBSD                |   ✅   |
| LCARS                  |   🛸   |
| Linux                  |   ✅   |
| macOS                  |   ✅   |
| OS/2 Warp              |   ❌   |
| Windows (WSL2)         |   ✅   |

### Conditions préalables

- [Zsh](https://www.zsh.org) doit être installé (la version 4.3.9 ou plus récente est acceptable mais nous préférons 5.0.8 et
  versions ultérieures). Si elle n’est pas préinstallée (exécutez `zsh --version` pour confirmer), consultez les instructions suivantes sur ce wiki :
  [Installer ZSH](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
- `curl` ou `wget` doit être installé
- `git` doit être installé (version recommandée : 2.4.11 ou plus récente)

### Installation de base

Oh My Zsh est installé en exécutant l'une des commandes suivantes dans votre terminal. Vous pouvez l'installer via la
ligne de commande avec soit `curl`, `wget` ou un autre outil similaire.

| Méthode    | Commande                           |
| :-------- | : |
| **curl**  | `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |
| **wget**  | `sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`   |
| **fetch** | `sh -c "$(fetch -o - https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |

Alternativement, l'installeur est également miroir en dehors de GitHub. L'utilisation de cette URL peut être nécessaire si vous êtes
dans un pays comme la Chine ou l'Inde (pour certains FAI), qui bloque `raw.githubusercontent.com` :

| Méthode    | Commande |
| :-------- | : |
| **curl**  | `sh -c "$(curl -fsSL https://install.ohmyz.sh/)"` |
| **wget**  | `sh -c "$(wget -O- https://install.ohmyz.sh/)"`   |
| **fetch** | `sh -c "$(fetch -o - https://install.ohmyz.sh/)"` |

_Notez que tout `.zshrc` précédent sera renommé en `.zshrc.pre-oh-my-zsh`. Après l'installation, vous pouvez déplacer
la configuration que vous souhaitez conserver vers le nouveau `.zshrc`._

#### Inspection manuelle

Il est une bonne idée d'inspecter le script d'installation des projets dont vous ne connaissez pas encore les détails. Vous pouvez le faire en
téléchargeant d'abord le script d'installation, en le parcourant pour vérifier que tout semble normal, puis en l'exécutant :

```sh
wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh
sh install.sh
```

Si l'URL ci-dessus expiré ou échoue autrement, vous devrez peut-être substituer l'URL par
`https://install.ohmyz.sh` afin d'être en mesure d'obtenir le script.

## Utilisation d'Oh My Zsh

### Plugins

Oh My Zsh vient avec un tas de plugins que vous pouvez utiliser. Vous pouvez jeter un œil dans le
[plugins](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins) répertoire et/ou le
[wiki](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins) pour voir ce qui est actuellement disponible.

#### Activation des plugins

Une fois que vous avez repéré un plugin (ou plusieurs) que vous souhaitez utiliser avec Oh My Zsh, vous devrez les activer dans le
fichier `.zshrc`. Vous trouverez le fichier zshrc dans votre répertoire `$HOME`. Ouvrez-le avec votre éditeur de texte préféré
et vous verrez un emplacement pour lister tous les plugins que vous souhaitez charger.

```sh
vi ~/.zshrc
```

Par exemple, cela pourrait commencer à ressembler à ceci :

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

_Notez que les plugins sont séparés par des espaces blancs (espaces, tabulations, nouvelles lignes...). **Ne** utilisez pas de virgules entre
eux ou cela risquera de tout briser._

#### Utilisation des plugins

Chaque plugin intégré inclut un **README**, le documentant. Ce README devrait afficher les alias (si le plugin
en ajoute) et les bonnes choses supplémentaires incluses dans ce plugin particulier.

### Thèmes

Nous l'avouons. Au début de l'histoire d'Oh My Zsh, nous avons peut-être un peu trop insisté sur les thèmes. Nous disposons maintenant de plus d'une centaine de thèmes préinstallés. La plupart d'entre eux ont
[screenshots](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes) sur le wiki (Nous travaillons à la mise à jour de celui-ci !).
Découvrez-les !

#### Sélection d'un thème

Le thème de Robby est le thème par défaut. Ce n'est pas le plus élégant. Ce n'est pas le plus simple. C'est juste le bon
(pour lui).

Une fois que vous avez trouvé un thème que vous souhaitez utiliser, vous devrez modifier le fichier `~/.zshrc`. Vous verrez une variable d'environnement (en majuscules) dans ce fichier qui ressemble à :

```sh
ZSH_THEME="robbyrussell"
```

Pour utiliser un autre thème, modifiez simplement la valeur afin qu'elle corresponde au nom de votre thème souhaité. Par exemple :

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

Et si vous souhaitez choisir un thème au hasard parmi une liste de vos thèmes préférés :

```sh
ZSH_THEME_RANDOM_CANDIDATES=(
  "robbyrussell"
  "agnoster"
```

Si vous connaissez uniquement les thèmes que vous n'aimez pas, vous pouvez les ajouter de manière similaire à une liste ignorée :

```sh
ZSH_THEME_RANDOM_IGNORED=(pygmalion tjkirch_mod)
```

### FAQ

Si vous avez des questions ou des problèmes supplémentaires, vous pourriez trouver une solution dans notre
[FAQ](https://github.com/ohmyzsh/ohmyzsh/wiki/FAQ).

## Sujets avancés

Si vous êtes du type à aimer vous salir les mains, ces sections pourraient vous parler.

### Installation avancée

Certains utilisateurs peuvent vouloir installer Oh My Zsh manuellement, ou modifier le chemin par défaut ou d'autres paramètres que l'installeur accepte (ces paramètres sont également documentés en tête du script d'installation).

#### Répertoire personnalisé

L'emplacement par défaut est `~/.oh-my-zsh` (caché dans votre répertoire personnel, vous pouvez y accéder avec
`cd ~/.oh-my-zsh`)

Si vous souhaitez modifier le répertoire d'installation avec la variable d'environnement `ZSH`, soit en exécutant
`export ZSH=/your/path` avant l'installation, soit en le définissant avant la fin du pipeline d'installation comme ceci :

```sh
ZSH="$HOME/.dotfiles/oh-my-zsh" sh install.sh
```

#### Installation non supervisée

Si vous exécutez le script d'installation d'Oh My Zsh en tant qu'partie d'une installation automatisée, vous pouvez passer le
drapeau `--unattended` au script `install.sh`. Cela aura pour effet de ne pas tenter de changer le shell par défaut,
et il ne lancera pas non plus `zsh` une fois l'installation terminée.

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" "" --unattended
```

Si vous êtes en Chine, en Inde ou dans un autre pays qui bloque `raw.githubusercontent.com`, vous devrez peut-être substituer l'URL pour `https://install.ohmyz.sh` afin qu'il s'installe.

#### Installation à partir d'un dépôt forké

Le script d'installation accepte également ces variables pour permettre l'installation d'un dépôt différent :

- `REPO` (par défaut : `ohmyzsh/ohmyzsh`) : cela prend la forme `propriétaire/dépôt`. Si vous définissez cette variable,
  l'installeur recherchera un dépôt à `https://github.com/{propriétaire}/{dépôt}`.

- `REMOTE` (par défaut : `https://github.com/${REPO}.git`) : c'est l'URL complète du dépôt git à cloner. Vous
  pouvez utiliser ce paramètre si vous souhaitez installer à partir d'un fork qui n'est pas sur GitHub (GitLab, Bitbucket...) ou si
  vous souhaitez cloner avec SSH au lieu de HTTPS (`git@github.com:utilisateur/projet.git`).

  _NOTE : il est incompatible avec la définition de la variable `REPO`. Ce paramètre prendra le dessus._

- `BRANCH` (par défaut : `master`) : vous pouvez utiliser ce paramètre si vous souhaitez changer la branche par défaut à utiliser
  lors du clonage du dépôt. Cela peut être utile pour tester une demande de tirage (Pull Request), ou si vous souhaitez
  utiliser une branche autre que `master`.

Par exemple :

```sh
REPO=apjanke/oh-my-zsh BRANCH=edge sh install.sh
```

#### Installation manuelle

##### 1. Clone The Repository <!-- omit in toc -->

```sh
git clone https://github.com/ohmyzsh/ohmyzsh.git ~/.oh-my-zsh
```

##### 2. _Optionally_, Backup Your Existing `~/.zshrc` File <!-- omit in toc -->

```sh
cp ~/.zshrc ~/.zshrc.orig
```

##### 3. Create A New Zsh Configuration File <!-- omit in toc -->

Vous pouvez créer un nouveau fichier de configuration zsh en copiant le modèle que nous avons inclus pour vous.

```sh
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
```

##### 4. Change Your Default Shell <!-- omit in toc -->

```sh
chsh -s $(which zsh)
```

Vous devez vous déconnecter de votre session utilisateur et vous reconnecter pour voir ce changement.

##### 5. Initialize Your New Zsh Configuration <!-- omit in toc -->

Une fois que vous ouvrez une nouvelle fenêtre de terminal, elle devrait charger zsh avec la configuration d'Oh My Zsh.

### Problèmes d'installation

Si vous rencontrez des problèmes lors de l'installation, voici quelques solutions courantes.

- Vous _pourriez_ avoir besoin de modifier votre `PATH` dans `~/.zshrc` si vous ne parvenez pas à trouver certains commandes après
  le passage à `oh-my-zsh`.
- Si vous avez installé manuellement ou si vous avez modifié l'emplacement d'installation, vérifiez la variable d'environnement `ZSH` dans
  `~/.zshrc`.

### Plugins et thèmes personnalisés

Si vous souhaitez remplacer tout comportement par défaut, ajoutez simplement un nouveau fichier (se terminant par `.zsh`) dans le répertoire `custom/`.

Si vous avez de nombreuses fonctions qui s'associent bien, vous pouvez les placer dans un fichier `XYZ.plugin.zsh` dans le répertoire `custom/plugins/` puis activer ce plugin.

Si vous souhaitez remplacer la fonctionnalité d'un plugin distribué avec Oh My Zsh, créez un plugin du même nom dans le répertoire `custom/plugins/` et il sera chargé à la place de celui dans `plugins/`.

### Activer ls GNU dans les systèmes macOS et FreeBSD

<a name="enable-gnu-ls"></a>

Le comportement par défaut d'Oh My Zsh est d'utiliser ls BSD dans les systèmes macOS et FreeBSD. Si ls GNU est installé
(sous la forme de la commande gls), vous pouvez choisir d'utiliser celui-ci à la place. Pour le faire, vous pouvez utiliser une configuration basée sur zstyle avant
de charger `oh-my-zsh.sh` :

```zsh
zstyle ':omz:lib:theme-and-appearance' gnu-ls yes
```

_Note: this is not compatible with `DISABLE_LS_COLORS=true`_

### Ignorer les alias

<a name="remove-directories-aliases"></a>

Si vous souhaitez ignorer les alias par défaut d'Oh My Zsh (ceux définis dans les fichiers `lib/*`) ou les alias de plugin, vous pouvez utiliser
les paramètres suivants dans votre fichier `~/.zshrc`, **avant que Oh My Zsh ne soit chargé**. Notez qu'il existe de nombreuses façons différentes d'ignorer les alias, selon vos besoins.

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

Vous pouvez les combiner de manière différente, en tenant compte du fait que les portées plus spécifiques prennent le dessus :

```sh
# Skip all plugin aliases, except for the git plugin
zstyle ':omz:plugins:*' aliases no
zstyle ':omz:plugins:git' aliases yes
```

Une version précédente de cette fonctionnalité utilisait le paramètre suivant, qui a été supprimé :

```sh
zstyle ':omz:directories' aliases no
```

Au lieu de cela, vous pouvez maintenant utiliser ce qui suit :

```sh
zstyle ':omz:lib:directories' aliases no
```

#### Notice <!-- omit in toc -->

> Cette fonctionnalité est actuellement en phase de test et elle peut être modifiée à l'avenir. Elle n'est également pas
> compatible actuellement avec les gestionnaires de plugins tels que zpm ou zinit, qui ne chargent pas le script d'initialisation
> (`oh-my-zsh.sh`) où cette fonctionnalité est implémentée.

> Elle n'est également pas actuellement consciente des « alias » définis comme des fonctions. Exemples de tels alias sont `gccd`,
> `ggf` ou `ggl` provenant du plugin git.

### Prompt git asynchrone

Les fonctions de prompt asynchrone sont une fonctionnalité expérimentale (ajoutée le 3 avril 2024) qui permet à Oh My Zsh de rendre
l'information du prompt de manière asynchrone. Cela peut améliorer les performances du rendu du prompt, mais cela pourrait ne pas fonctionner bien
avec certains paramétrages. Nous espérons que ce n'est pas un problème, mais si vous rencontrez des problèmes avec cette nouvelle fonctionnalité, vous pouvez
l'éteindre en définissant ce qui suit dans votre fichier .zshrc, avant que Oh My Zsh ne soit chargé :

```sh
zstyle ':omz:alpha:lib:git' async-prompt no
```

Si votre problème est que le prompt git s'est soudainement arrêté d'apparaître, vous pouvez essayer de le forcer en définissant la configuration suivante avant que `oh-my-zsh.sh` ne soit chargé. Si cela ne fonctionne toujours pas, veuillez ouvrir un problème avec votre cas.

```sh
zstyle ':omz:alpha:lib:git' async-prompt force
```

## Obtenir les mises à jour

Par défaut, vous serez invité à vérifier les mises à jour toutes les 2 semaines. Vous pouvez choisir d'autres modes de mise à jour en
ajoutant une ligne à votre fichier `~/.zshrc`, **avant que Oh My Zsh ne soit chargé** :

1. Mise à jour automatique sans demande de confirmation :

```sh
   zstyle ':omz:update' mode auto
   ```

2. Just offer a reminder every few days, if there are updates available:

```sh
   zstyle ':omz:update' mode reminder
   ```

3. Pour désactiver les mises à jour automatiques complètement :

```sh
   zstyle ':omz:update' mode disabled
   ```

NOTE: vous pouvez contrôler la fréquence à laquelle Oh My Zsh vérifie les mises à jour avec la configuration suivante :

```sh
# This will check for updates every 7 days
zstyle ':omz:update' frequency 7
# This will check for updates every time you open the terminal (not recommended)
zstyle ':omz:update' frequency 0
```

### Niveau de détail des mises à jour

Vous pouvez également limiter le niveau de détail des mises à jour avec les paramètres suivants :

```sh
zstyle ':omz:update' verbose default # default update prompt

zstyle ':omz:update' verbose minimal # only few lines

zstyle ':omz:update' verbose silent # only errors
```

### Mises à jour manuelles

Si vous souhaitez mettre à jour à tout moment (peut-être qu'on vient de publier un nouveau plugin et vous ne souhaitez pas attendre une semaine ?), vous n'avez qu'à exécuter :

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
> Voir plus d'options dans le [FAQ: How do I update Oh My Zsh?](https://github.com/ohmyzsh/ohmyzsh/wiki/FAQ#how-do-i-update-oh-my-zsh).
>
> **L'UTILISATION DE `omz update --unattended` A ÉTÉ ÉLIMINÉE, CAR ELLE A DES EFFETS SECONDAIRES**.

Magic! 🎉

## Désinstallation d'Oh My Zsh

Oh My Zsh n'est pas fait pour tout le monde. Nous allons nous sentir tristes, mais nous souhaitons que cette séparation soit facile.

Si vous souhaitez désinstaller `oh-my-zsh`, exécutez simplement `uninstall_oh_my_zsh` depuis la ligne de commande. Cela supprimera
Oh My Zsh et rétablira votre configuration précédente de `bash` ou de `zsh`.

## Comment contribuer à Oh My Zsh ?

Avant de participer à notre communauté si agréable, veuillez lire le [code de conduite](../CODE_OF_CONDUCT.md).

Je ne suis pas du tout un expert en [Zsh](https://www.zsh.org/) et je soupçonne qu'il existe de nombreuses façons d'améliorer – si vous avez des idées sur la façon de rendre la configuration plus facile à maintenir (et plus rapide), n'hésitez pas à forker et à envoyer des demandes de pull !

Nous avons également besoin de personnes pour tester les demandes de pull. Donc, jetez un œil aux
[problèmes ouverts](https://github.com/ohmyzsh/ohmyzsh/issues) et aidez là où vous pouvez.

Voir [Contributing](../CONTRIBUTING.md) pour plus de détails.

### Ne nous envoyez pas de thèmes

Nous avons (plus que) suffisamment de thèmes pour le moment. Veuillez ajouter votre thème à la
[page de thèmes externes](https://github.com/ohmyzsh/ohmyzsh/wiki/External-themes) du wiki.

## Contributeurs

Oh My Zsh possède une communauté dynamique de utilisateurs heureux et de contributeurs charmants. Sans tout le temps et l'aide
de nos contributeurs, ce ne serait pas aussi incroyable.

Merci beaucoup !

<a href="https://github.com/ohmyzsh/ohmyzsh/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ohmyzsh/ohmyzsh" width="100%"/>
</a>

## Suivez-nous

Nous sommes sur les réseaux sociaux :

- [@ohmyzsh](https://x.com/ohmyzsh) sur X (anciennement Twitter). Vous devriez le suivre.
- [Facebook](https://www.facebook.com/Oh-My-Zsh-296616263819290/) nous faire un petit coucou.
- [Instagram](https://www.instagram.com/_ohmyzsh/) mentionnez-nous dans votre publication montrant Oh My Zsh !
- [Discord](https://discord.gg/ohmyzsh) pour discuter avec nous !

## Merchandise

Nous avons
[des autocollants, des t-shirts et des tasses à café disponibles](https://commitgoods.com/collections/oh-my-zsh?utm_source=github)
pour que vous puissiez montrer votre amour pour Oh My Zsh. Encore une fois, vous allez être le sujet de conversation dans le quartier !

## Licence

Oh My Zsh est publié sous la [licence MIT](../LICENSE.txt).

## À propos de Planet Argon

![Planet Argon](https://pa-github-assets.s3.amazonaws.com/PARGON_logo_digital_COL-small.jpg)

Oh My Zsh was started by the team at [Planet Argon](https://www.planetargon.com/?utm_source=github), a
[Ruby on Rails development agency](https://www.planetargon.com/services/ruby-on-rails-development?utm_source=github).
Check out our [other open source projects](https://www.planetargon.com/open-source?utm_source=github).

