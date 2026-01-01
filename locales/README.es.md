<!--START_SECTION:navbar-->
<div align="center">
  <a href="../README.md">🇺🇸 English</a> | <a href="README.de.md">🇩🇪 Deutsch</a> | <a href="README.es.md">🇪🇸 Español</a> | <a href="README.fr.md">🇫🇷 Français</a> | <a href="README.hi.md">🇮🇳 हिंदी</a> | <a href="README.ja.md">🇯🇵 日本語</a> | <a href="README.ko.md">🇰🇷 한국어</a> | <a href="README.pt.md">🇵🇹 Português</a> | <a href="README.ru.md">🇷🇺 Русский</a> | <a href="README.zh.md">🇨🇳 中文</a>
</div>
<!--END_SECTION:navbar-->

<p align="center"><img src="https://ohmyzsh.s3.amazonaws.com/omz-ansi-github.png" alt="Oh My Zsh"></p>

Oh My Zsh es un marco de código abierto, impulsado por la comunidad, para gestionar tu configuración de [zsh](https://www.zsh.org/).

Suena aburrido. Vamos a intentarlo de nuevo.

**Oh My Zsh no te convertirá en un desarrollador 10 veces más rápido...pero podrías sentirte así.**

Una vez instalado, tu shell de terminal será el tema de conversación en la ciudad _o te devolveremos tu dinero_. Con cada tecla que pulses en tu línea de comandos, aprovecharás las cientos de poderosas extensiones y hermosos temas.
Desconocidos se acercarán a ti en cafeterías y te preguntarán, _"¡eso es increíble! ¿eres algún tipo de genio?"_

Finalmente, comenzarás a recibir la atención que siempre has sentido que merecías. ...o quizás usarás el tiempo que ahorras para comenzar a usar el hilo dental con más frecuencia. 😬

Para obtener más información, visita [ohmyz.sh](https://ohmyz.sh), síguenos en X (anteriormente Twitter) en [@ohmyzsh](https://x.com/ohmyzsh) y únete a nosotros en [Discord](https://discord.gg/ohmyzsh).

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

| Sist. Operativo | Estado |
| :------------- | :----: |
| Android        |   ✅   |
| freeBSD        |   ✅   |
| LCARS          |   🛸   |
| Linux          |   ✅   |
| macOS          |   ✅   |
| OS/2 Warp      |   ❌   |
| Windows (WSL2) |   ✅   |

### Requisitos previos

- [Zsh](https://www.zsh.org) debe estar instalado (v4.3.9 o más reciente es aceptable pero preferimos 5.0.8 y
  más reciente). Si no está preinstalado (ejecute `zsh --version` para confirmarlo), consulte las siguientes instrucciones del wiki aquí:
  [Instalando ZSH](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
- `curl` o `wget` deben estar instalados
- `git` debe estar instalado (se recomienda v2.4.11 o superior)

### Instalación básica

Oh My Zsh se instala ejecutando uno de los siguientes comandos en tu terminal. Puedes instalarlo desde la línea de comandos utilizando `curl`, `wget` u otra herramienta similar.

| Método    | Comando                           |
| :-------- | : |
| **curl**  | `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |
| **wget**  | `sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`   |
| **fetch** | `sh -c "$(fetch -o - https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |

Alternativamente, el instalador también está disponible en un espejo fuera de GitHub. Usar esta URL puede ser necesario si estás en un país como China o India (para ciertos proveedores de servicios de internet), que bloquea `raw.githubusercontent.com`:

| Método    | Comando |
| :-------- | : |
| **curl**  | `sh -c "$(curl -fsSL https://install.ohmyz.sh/)"` |
| **wget**  | `sh -c "$(wget -O- https://install.ohmyz.sh/)"`   |
| **fetch** | `sh -c "$(fetch -o - https://install.ohmyz.sh/)"` |

_Tenga en cuenta que cualquier `.zshrc` anterior se renombrará a `.zshrc.pre-oh-my-zsh`. Después de la instalación, puede mover la configuración que desee conservar al nuevo `.zshrc`._

#### Inspección Manual

Es una buena idea inspeccionar el script de instalación de proyectos que aún no conoces. Puedes hacerlo descargando primero el script de instalación, revisándolo para asegurarte de que todo parece normal, y luego ejecutarlo:

```sh
wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh
sh install.sh
```

Si la URL anterior se agota o falla de otra manera, es posible que debas sustituir la URL por
`https://install.ohmyz.sh` para poder obtener el script.

## Usando Oh My Zsh

### Plugins

Oh My Zsh viene con una maldita cantidad de plugins para que los aproveches. Puedes echar un vistazo en el
[plugins](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins) directorio y/o el
[wiki](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins) para ver qué está disponible actualmente.

#### Habilitar complementos

Una vez que encuentres un complemento (o varios) que te gustaría usar con Oh My Zsh, necesitarás habilitarlos en el
archivo `.zshrc`. Encontrarás el archivo zshrc en tu directorio `$HOME`. Ábrelo con tu editor de texto favorito
y verás un lugar para listar todos los complementos que deseas cargar.

```sh
vi ~/.zshrc
```

Por ejemplo, esto podría comenzar a verse así:

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

Tenga en cuenta que los plugins están separados por espacios en blanco (espacios, tabuladores, nuevas líneas...). **No** use comas entre
ellos o se romperá.

#### Usando Plugins

Cada plugin integrado incluye un **README**, que lo documenta. Este README debe mostrar los alias (si el plugin
agrega alguno) y las ventajas adicionales que se incluyen en ese plugin particular.

### Temas

Lo admitimos. Al principio del mundo de Oh My Zsh, quizás nos volvimos un poco demasiado entusiastas con los temas. Ahora tenemos más de ciento cincuenta temas incluidos. La mayoría de ellos tienen
[screenshots](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes) en la wiki (Estamos trabajando en actualizar esto).
¡Echales un vistazo!

#### Seleccionando un tema

El tema de Robby es el predeterminado. No es el más elegante. No es el más sencillo. Solo es el adecuado
(para él).

Una vez que encuentres un tema que te gustaría usar, necesitarás editar el archivo `~/.zshrc`. Verás una
variable de entorno (en mayúsculas) allí que se ve así:

```sh
ZSH_THEME="robbyrussell"
```

Para usar un tema diferente, simplemente cambie el valor para que coincida con el nombre de su tema deseado. Por ejemplo:

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

Y si quieres elegir un tema aleatorio de una lista de tus temas favoritos:

```sh
ZSH_THEME_RANDOM_CANDIDATES=(
  "robbyrussell"
  "agnoster"
```

Si solo sabes cuáles temas no te gustan, puedes agregarlos de manera similar a una lista ignorada:

```sh
ZSH_THEME_RANDOM_IGNORED=(pygmalion tjkirch_mod)
```

### Preguntas frecuentes

Si tienes más preguntas o problemas, podrías encontrar una solución en nuestra
[FAQ](https://github.com/ohmyzsh/ohmyzsh/wiki/FAQ).

## Temas avanzados

Si eres el tipo de persona que le gusta metérselas en el barro, estas secciones podrían resonar contigo.

### Instalación avanzada

Algunos usuarios pueden querer instalar Oh My Zsh manualmente, o cambiar la ruta predeterminada u otras configuraciones que acepta el
instalador (estas configuraciones también están documentadas en la parte superior del script de instalación).

#### Directorio personalizado

La ubicación predeterminada es `~/.oh-my-zsh` (oculta en tu directorio de inicio, puedes acceder a ella con
`cd ~/.oh-my-zsh`)

Si deseas cambiar el directorio de instalación con la variable de entorno `ZSH`, ya sea ejecutando
`export ZSH=/tu/ruta` antes de instalar, o estableciéndola antes del final de la tubería de instalación de esta manera:

```sh
ZSH="$HOME/.dotfiles/oh-my-zsh" sh install.sh
```

#### Instalación sin asistencia

Si está ejecutando el script de instalación de Oh My Zsh como parte de una instalación automatizada, puede pasar la
bandera `--unattended` al script `install.sh`. Esto tendrá el efecto de no intentar cambiar la shell predeterminada,
también no ejecutará `zsh` cuando finalice la instalación.

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" "" --unattended
```

Si estás en China, India u otro país que bloquea `raw.githubusercontent.com`, es posible que tengas que sustituir la URL para `https://install.ohmyz.sh` para que se instale.

#### Instalación desde un repositorio bifurcado

El script de instalación también acepta estas variables para permitir la instalación de un repositorio diferente:

- `REPO` (por defecto: `ohmyzsh/ohmyzsh`): esto toma la forma de `propietario/repositorio`. Si establece esta variable,
  el instalador buscará un repositorio en `https://github.com/{propietario}/{repositorio}`.

- `REMOTE` (por defecto: `https://github.com/${REPO}.git`): esto es la URL completa del clon del repositorio git. Puede
  usar esta configuración si quiere instalar desde una bifurcación que no esté en GitHub (GitLab, Bitbucket...) o si
  quiere clonar con SSH en lugar de HTTPS (`git@github.com:usuario/proyecto.git`).

  _NOTA: es incompatible con establecer la variable `REPO`. Esta configuración tendrá prioridad._

- `BRANCH` (por defecto: `master`): puede usar esta configuración si quiere cambiar la rama por defecto que se
  checkouteará al clonar el repositorio. Esto podría ser útil para probar una solicitud de extracción, o si quiere
  usar una rama diferente a `master`.

Por ejemplo:

```sh
REPO=apjanke/oh-my-zsh BRANCH=edge sh install.sh
```

#### Instalación Manual

##### 1. Clone The Repository <!-- omit in toc -->

```sh
git clone https://github.com/ohmyzsh/ohmyzsh.git ~/.oh-my-zsh
```

##### 2. _Optionally_, Backup Your Existing `~/.zshrc` File <!-- omit in toc -->

```sh
cp ~/.zshrc ~/.zshrc.orig
```

##### 3. Create A New Zsh Configuration File <!-- omit in toc -->

Puedes crear un nuevo archivo de configuración de zsh copiando la plantilla que hemos incluido para ti.

```sh
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
```

##### 4. Change Your Default Shell <!-- omit in toc -->

```sh
chsh -s $(which zsh)
```

Debes cerrar sesión de tu sesión de usuario e iniciar sesión nuevamente para ver este cambio.

##### 5. Initialize Your New Zsh Configuration <!-- omit in toc -->

Una vez que abra una nueva ventana de terminal, debería cargar zsh con la configuración de Oh My Zsh.

### Problemas de Instalación

Si tienes algún problema al instalar, aquí hay algunas soluciones comunes.

- Es posible que necesites modificar tu `PATH` en `~/.zshrc` si no puedes encontrar algunos comandos después
  de cambiar a `oh-my-zsh`.
- Si instalaste manualmente o cambiaste la ubicación de instalación, verifica la variable de entorno `ZSH` en
  `~/.zshrc`.

### Plugins y Temas Personalizados

Si deseas sobrescribir cualquier comportamiento predeterminado, simplemente agrega un nuevo archivo (que termine en `.zsh`) en el directorio `custom/`.

Si tienes muchas funciones que van bien juntas, puedes colocarlas como un archivo `XYZ.plugin.zsh` en el directorio `custom/plugins/` y luego activa este plugin.

Si deseas sobrescribir la funcionalidad de un plugin distribuido con Oh My Zsh, crea un plugin del mismo nombre en el directorio `custom/plugins/` y se cargará en lugar del que está en `plugins/`.

### Habilitar GNU ls en sistemas macOS y freeBSD

<a name="enable-gnu-ls"></a>

El comportamiento predeterminado en Oh My Zsh es utilizar BSD `ls` en sistemas macOS y freeBSD. Si está instalado GNU `ls`
(como el comando `gls`), puede elegir usarlo en su lugar. Para hacerlo, puede usar una configuración basada en zstyle antes
de cargar `oh-my-zsh.sh`:

```zsh
zstyle ':omz:lib:theme-and-appearance' gnu-ls yes
```

Nota: esto no es compatible con `DISABLE_LS_COLORS=true`

### Skip Aliases

<a name="remove-directories-aliases"></a>

If you want to skip default Oh My Zsh aliases (those defined in `lib/*` files) or plugin aliases, you can use
the settings below in your `~/.zshrc` file, **before Oh My Zsh is loaded**. Note that there are many different
ways to skip aliases, depending on your needs.

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

Puedes combinarlos de otras maneras teniendo en cuenta que los ámbitos más específicos tienen prioridad:

```sh
# Skip all plugin aliases, except for the git plugin
zstyle ':omz:plugins:*' aliases no
zstyle ':omz:plugins:git' aliases yes
```

Una versión anterior de esta característica estaba utilizando la configuración siguiente, la cual ha sido eliminada:

```sh
zstyle ':omz:directories' aliases no
```

En su lugar, ahora puede usar lo siguiente:

```sh
zstyle ':omz:lib:directories' aliases no
```

#### Notice <!-- omit in toc -->

> Esta característica actualmente se encuentra en una fase de prueba y puede estar sujeta a cambios en el futuro. También no
> es compatible actualmente con gestores de complementos como zpm o zinit, que no cargan el script de inicialización
> (`oh-my-zsh.sh`) donde se implementa esta característica.

> También no está actualmente consciente de "alias" que se definen como funciones. Ejemplos de estos son las funciones `gccd`,
> `ggf` o `ggl` del complemento git.

### Prompt git asincrónico

Las funciones de prompt asincrónicas son una característica experimental (incluida el 3 de abril de 2024) que permite a Oh My Zsh renderizar
la información del prompt de forma asincrónica. Esto puede mejorar el rendimiento del prompt, pero podría no funcionar bien
con algunas configuraciones. Esperamos que eso no sea un problema, pero si estás experimentando problemas con esta nueva característica, puedes
desactivarla estableciendo lo siguiente en tu archivo .zshrc, antes de que Oh My Zsh sea cargado:

```sh
zstyle ':omz:alpha:lib:git' async-prompt no
```

Si tu problema es que la indicación de git dejó de aparecer, puedes intentar forzarla estableciendo la siguiente
configuración antes de que se cargue `oh-my-zsh.sh`. Si aún no funciona, por favor abre un problema con tu
caso.

```sh
zstyle ':omz:alpha:lib:git' async-prompt force
```

## Obteniendo actualizaciones

De forma predeterminada, se le pedirá que revise las actualizaciones cada 2 semanas. Puede elegir otros modos de actualización agregando una línea a su archivo `~/.zshrc`, **antes de que se cargue Oh My Zsh**:

1. Actualización automática sin mostrar un mensaje de confirmación:

```sh
   zstyle ':omz:update' mode auto
   ```

2. Solo ofrezca un recordatorio cada unos días, si hay actualizaciones disponibles:

```sh
   zstyle ':omz:update' mode reminder
   ```

3. Para deshabilitar las actualizaciones automáticas por completo:

```sh
   zstyle ':omz:update' mode disabled
   ```

NOTA: puedes controlar con qué frecuencia Oh My Zsh verifica actualizaciones con la siguiente configuración:

```sh
# This will check for updates every 7 days
zstyle ':omz:update' frequency 7
# This will check for updates every time you open the terminal (not recommended)
zstyle ':omz:update' frequency 0
```

### Verbosidad de Actualizaciones

También puedes limitar la verbosidad de las actualizaciones con las siguientes configuraciones:

```sh
zstyle ':omz:update' verbose default # default update prompt

zstyle ':omz:update' verbose minimal # only few lines

zstyle ':omz:update' verbose silent # only errors
```

### Actualizaciones Manuales

Si deseas actualizar en cualquier momento (tal vez alguien acaba de liberar un nuevo complemento y no quieres
esperar una semana?), simplemente necesitas ejecutar:

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
> See more options in the [FAQ: How do I update Oh My Zsh?](https://github.com/ohmyzsh/ohmyzsh/wiki/FAQ#how-do-i-update-oh-my-zsh).
>
> **USE OF `omz update --unattended` HAS BEEN REMOVED, AS IT HAS SIDE EFFECTS**.

Magic! 🎉

## Desinstalando Oh My Zsh

Oh My Zsh no es para todos. Nosotros nos iremos, pero queremos hacer que esta ruptura sea fácil.

Si quieres desinstalar `oh-my-zsh`, simplemente ejecuta `uninstall_oh_my_zsh` desde la línea de comandos. Se eliminará
a sí mismo y revertirá tu configuración anterior de `bash` o `zsh`.

## ¿Cómo puedo contribuir a Oh My Zsh?

Antes de participar en nuestra agradable comunidad, por favor lee el [código de conducta](../CODE_OF_CONDUCT.md).

Estoy lejos de ser un experto en [Zsh](https://www.zsh.org/) y sospecho que hay muchas formas de mejorar – si tienes ideas sobre cómo hacer que la configuración sea más fácil de mantener (y más rápida), no dudes en hacer un fork y enviar solicitudes de extracción!

También necesitamos personas que prueben las solicitudes de extracción. Así que echa un vistazo a
[los problemas abiertos](https://github.com/ohmyzsh/ohmyzsh/issues) y ayuda donde puedas.

Ver [Contributing](../CONTRIBUTING.md) para más detalles.

### No envíenos temas

Por el momento tenemos (más de) suficientes temas. Por favor, agregue su tema a la
[página de temas externos](https://github.com/ohmyzsh/ohmyzsh/wiki/External-themes) de la wiki.

## Contribuyentes

Oh My Zsh tiene una comunidad vibrante de usuarios felices y contribuyentes encantadores. Sin todo el tiempo y ayuda
de nuestros contribuyentes, no sería tan increíble.

¡Muchas gracias!

<a href="https://github.com/ohmyzsh/ohmyzsh/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ohmyzsh/ohmyzsh" width="100%"/>
</a>

## Síguenos

Estamos en redes sociales:

- [@ohmyzsh](https://x.com/ohmyzsh) en X (anteriormente Twitter). Deberías seguirlo.
- [Facebook](https://www.facebook.com/Oh-My-Zsh-296616263819290/) pícanos.
- [Instagram](https://www.instagram.com/_ohmyzsh/) etiquétanos en tu publicación mostrando Oh My Zsh!
- [Discord](https://discord.gg/ohmyzsh) para charlar con nosotros!

## Merchandise

Tenemos
[stickers, shirts, and coffee mugs available](https://commitgoods.com/collections/oh-my-zsh?utm_source=github)
para que puedas mostrar tu amor por Oh My Zsh. ¡De nuevo, serás el centro de atención!

## Licencia

Oh My Zsh se publica bajo la [licencia MIT](../LICENSE.txt).

## Acerca de Planet Argon

![Planet Argon](https://pa-github-assets.s3.amazonaws.com/PARGON_logo_digital_COL-small.jpg)

Oh My Zsh was started by the team at [Planet Argon](https://www.planetargon.com/?utm_source=github), a
[Ruby on Rails development agency](https://www.planetargon.com/services/ruby-on-rails-development?utm_source=github).
Check out our [other open source projects](https://www.planetargon.com/open-source?utm_source=github).

