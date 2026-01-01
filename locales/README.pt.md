<!--START_SECTION:navbar-->
<div align="center">
  <a href="../README.md">🇺🇸 English</a> | <a href="README.de.md">🇩🇪 Deutsch</a> | <a href="README.es.md">🇪🇸 Español</a> | <a href="README.fr.md">🇫🇷 Français</a> | <a href="README.hi.md">🇮🇳 हिंदी</a> | <a href="README.ja.md">🇯🇵 日本語</a> | <a href="README.ko.md">🇰🇷 한국어</a> | <a href="README.pt.md">🇵🇹 Português</a> | <a href="README.ru.md">🇷🇺 Русский</a> | <a href="README.zh.md">🇨🇳 中文</a>
</div>
<!--END_SECTION:navbar-->

<p align="center"><img src="https://ohmyzsh.s3.amazonaws.com/omz-ansi-github.png" alt="Oh My Zsh"></p>

Oh My Zsh é um framework de código aberto, impulsionado pela comunidade, para gerenciar sua configuração do [zsh](https://www.zsh.org/).

Parece chato. Vamos tentar de novo.

**Oh My Zsh não vai tornar você um desenvolvedor 10x...mas você pode se sentir como um.**

Após a instalação, seu shell de terminal se tornará o assunto da conversa _ou seu dinheiro de volta!_ Com cada tecla digitada no seu prompt de comando, você aproveitará os centenas de plugins poderosos e temas bonitos.
Estranhos virão até você em cafés e perguntarão, _"isso é incrível! você é algum tipo de gênio?"_

Finalmente, você começará a receber o tipo de atenção que sempre sentiu que merecia. ...ou talvez você use o tempo que está economizando para começar a usar fio dental com mais frequência. 😬

Para saber mais, visite [ohmyz.sh](https://ohmyz.sh), siga [@ohmyzsh](https://x.com/ohmyzsh) no X (anteriormente Twitter) e participe conosco no [Discord](https://discord.gg/ohmyzsh).

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

## Começando

### Compatibilidade com Sistema Operacional

| O/S            | Status |
| :------------- | :----: |
| Android        |   ✅   |
| freeBSD        |   ✅   |
| LCARS          |   🛸   |
| Linux          |   ✅   |
| macOS          |   ✅   |
| OS/2 Warp      |   ❌   |
| Windows (WSL2) |   ✅   |

### Pré-requisitos

- [Zsh](https://www.zsh.org) deve estar instalado (v4.3.9 ou mais recente é aceitável, mas preferimos 5.0.8 e
  versões mais recentes). Se não estiver pré-instalado (execute `zsh --version` para confirmar), consulte as seguintes instruções do wiki aqui:
  [Instalando ZSH](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
- `curl` ou `wget` devem estar instalados
- `git` deve estar instalado (recomendado v2.4.11 ou superior)

### Instalação Básica

Oh My Zsh é instalado executando um dos seguintes comandos no seu terminal. Você pode instalar isso via linha de comando usando `curl`, `wget` ou outra ferramenta semelhante.

| Método    | Comando                           |
| :-------- | : |
| **curl**  | `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |
| **wget**  | `sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`   |
| **fetch** | `sh -c "$(fetch -o - https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"` |

Alternativamente, o instalador também está espelhado fora do GitHub. Usar este URL pode ser necessário se você estiver em um país como China ou Índia (para certos ISPs), que bloqueia `raw.githubusercontent.com`:

| Método    | Comando |
| :-------- | : |
| **curl**  | `sh -c "$(curl -fsSL https://install.ohmyz.sh/)"` |
| **wget**  | `sh -c "$(wget -O- https://install.ohmyz.sh/)"`   |
| **fetch** | `sh -c "$(fetch -o - https://install.ohmyz.sh/)"` |

_Observação: qualquer `.zshrc` anterior será renomeado para `.zshrc.pre-oh-my-zsh`. Após a instalação, você pode mover a configuração que deseja preservar para o novo `.zshrc`._

#### Inspeção Manual

É uma boa ideia inspecionar o script de instalação de projetos dos quais você ainda não conhece. Você pode fazer isso baixando primeiro o script de instalação, analisando-o para garantir que tudo pareça normal, e depois executando-o:

```sh
wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh
sh install.sh
```

Se a URL acima expirar ou falhar de outra forma, você pode precisar substituir a URL por
`https://install.ohmyz.sh` para conseguir obter o script.

## Usando Oh My Zsh

### Plugins

Oh My Zsh vem com um monte de plugins para você aproveitar. Você pode dar uma olhada na
[plugins](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins) diretório e/ou a
[wiki](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins) para ver o que está disponível atualmente.

#### Habilitando Plugins

Uma vez que você identificar um plugin (ou vários) que deseja usar com Oh My Zsh, você precisará habilitá-los no arquivo `.zshrc`. Você encontrará o arquivo zshrc em seu diretório `$HOME`. Abra-o com seu editor de texto favorito e você verá um local para listar todos os plugins que deseja carregar.

```sh
vi ~/.zshrc
```

Por exemplo, isso pode começar a parecer assim:

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

_Nota que os plugins são separados por espaços em branco (espaços, tabs, novas linhas...). **Não** use vírgulas entre
eles ou isso vai quebrar._

#### Usando Plugins

Cada plugin embutido inclui um **README**, documentando-o. Este README deve mostrar os aliases (se o plugin
adicionar algum) e os extras que estão incluídos nesse plugin particular.

### Temas

Nós admitimos. No início do mundo Oh My Zsh, talvez tenhamos ficado um pouco excessivamente empolgados com temas. Agora temos mais de
umcento e cinquenta temas embalados. A maioria deles tem
[screenshots](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes) no wiki (Estamos trabalhando para atualizar isso!).
Confira-os!

#### Selecionando um Tema

O tema do Robby é o padrão. Não é o mais sofisticado. Não é o mais simples. É apenas o certo
(para ele).

Uce você encontrar um tema que gostaria de usar, você precisará editar o arquivo `~/.zshrc`. Você verá uma
variável de ambiente (tudo em maiúsculas) ali que parece com:

```sh
ZSH_THEME="robbyrussell"
```

Para usar um tema diferente, basta alterar o valor para corresponder ao nome do tema desejado. Por exemplo:

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

E se você quiser escolher um tema aleatório de uma lista de temas favoritos:

```sh
ZSH_THEME_RANDOM_CANDIDATES=(
  "robbyrussell"
  "agnoster"
```

Se você souber apenas quais temas não gosta, pode adicioná-los de forma semelhante a uma lista ignorada:

```sh
ZSH_THEME_RANDOM_IGNORED=(pygmalion tjkirch_mod)
```

### Perguntas Frequentes

Se você tiver mais algumas perguntas ou problemas, talvez encontre uma solução em nosso
[FAQ](https://github.com/ohmyzsh/ohmyzsh/wiki/FAQ).

## Tópicos Avançados

Se você é do tipo que gosta de se sujar as mãos, estas seções podem ressoar.

### Instalação Avançada

Alguns usuários podem querer instalar Oh My Zsh manualmente, ou alterar o caminho padrão ou outras configurações que o instalador aceita (essas configurações também estão documentadas no topo do script de instalação).

#### Diretório Personalizado

O local padrão é `~/.oh-my-zsh` (oculto em seu diretório home, você pode acessá-lo com
`cd ~/.oh-my-zsh`)

Se você quiser mudar o diretório de instalação com a variável de ambiente `ZSH`, seja executando
`export ZSH=/your/path` antes da instalação, ou definindo-a antes do final do pipeline de instalação assim:

```sh
ZSH="$HOME/.dotfiles/oh-my-zsh" sh install.sh
```

#### Instalação Não Atendida

Se você estiver executando o script de instalação do Oh My Zsh como parte de uma instalação automatizada, você pode passar a bandeira `--unattended` para o script `install.sh`. Isso terá o efeito de não tentar alterar o shell padrão, e também não executará `zsh` quando a instalação estiver concluída.

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" "" --unattended
```

Se você estiver na China, Índia ou em outro país que bloqueia `raw.githubusercontent.com`, pode precisar substituir a URL para `https://install.ohmyz.sh` para que a instalação funcione.

#### Instalando a partir de um repositório bifurcado

O script de instalação também aceita essas variáveis para permitir a instalação de um repositório diferente:

- `REPO` (padrão: `ohmyzsh/ohmyzsh`): isso assume a forma de `owner/repository`. Se você definir essa variável,
  o instalador procurará um repositório em `https://github.com/{owner}/{repository}`.

- `REMOTE` (padrão: `https://github.com/${REPO}.git`): isso é a URL completa do repositório git clone. Você
  pode usar essa configuração se quiser instalar a partir de uma bifurcação que não está no GitHub (GitLab, Bitbucket...) ou se
  quiser clonar com SSH em vez de HTTPS (`git@github.com:user/project.git`).

  _NOTE: é incompatível com definir a variável `REPO`. Essa configuração terá prioridade._

- `BRANCH` (padrão: `master`): você pode usar essa configuração se quiser alterar a branch padrão para ser
  verificada ao clonar o repositório. Isso pode ser útil para testar uma Pull Request, ou se quiser usar
  uma branch diferente de `master`.

Por exemplo:

```sh
REPO=apjanke/oh-my-zsh BRANCH=edge sh install.sh
```

#### Instalação Manual

##### 1. Clone The Repository <!-- omit in toc -->

```sh
git clone https://github.com/ohmyzsh/ohmyzsh.git ~/.oh-my-zsh
```

##### 2. _Optionally_, Backup Your Existing `~/.zshrc` File <!-- omit in toc -->

```sh
cp ~/.zshrc ~/.zshrc.orig
```

##### 3. Create A New Zsh Configuration File <!-- omit in toc -->

Você pode criar um novo arquivo de configuração do zsh copiando o modelo que incluímos para você.

```sh
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
```

##### 4. Change Your Default Shell <!-- omit in toc -->

```sh
chsh -s $(which zsh)
```

Você deve sair da sua sessão de usuário e entrar novamente para ver essa alteração.

##### 5. Initialize Your New Zsh Configuration <!-- omit in toc -->

Uma vez que você abrir uma nova janela do terminal, ela deve carregar o zsh com a configuração do Oh My Zsh.

### Problemas de Instalação

Se você tiver algum problema durante a instalação, aqui estão algumas soluções comuns.

- Você _pode precisar_ modificar seu `PATH` no `~/.zshrc` se não conseguir encontrar alguns comandos após
  mudar para `oh-my-zsh`.
- Se você instalou manualmente ou alterou o local de instalação, verifique a variável de ambiente `ZSH` em
  `~/.zshrc`.

### Plugins e Temas Personalizados

Se você quiser substituir qualquer um dos comportamentos padrão, basta adicionar um novo arquivo (com terminação `.zsh`) na pasta `custom/`.

Se você tem muitas funções que combinam bem, pode colocá-las como um arquivo `XYZ.plugin.zsh` na pasta
`custom/plugins/` e depois ativar esse plugin.

Se você quiser substituir a funcionalidade de um plugin distribuído com Oh My Zsh, crie um plugin com o mesmo nome na pasta `custom/plugins/` e ele será carregado em vez do que está em `plugins/`.

### Ativar o GNU ls em sistemas macOS e FreeBSD

<a name="enable-gnu-ls"></a>

O comportamento padrão no Oh My Zsh é usar o BSD `ls` em sistemas macOS e FreeBSD. Se o GNU `ls` estiver instalado
(como o comando `gls`), você pode escolher usá-lo em vez disso. Para fazê-lo, você pode usar uma configuração baseada em zstyle antes
de carregar `oh-my-zsh.sh`:

```zsh
zstyle ':omz:lib:theme-and-appearance' gnu-ls yes
```

_Nota: isso não é compatível com `DISABLE_LS_COLORS=true`_

### Skip Aliases

<a name="remove-directories-aliases"></a>

Se você quiser pular os aliases padrão do Oh My Zsh (aqueles definidos nos arquivos `lib/*`) ou aliases de plugin, você pode usar
as configurações abaixo no seu arquivo `~/.zshrc`, **antes que o Oh My Zsh seja carregado**. Note que existem muitas formas diferentes de pular aliases, dependendo das suas necessidades.

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

Você pode combiná-los de outras formas, levando em consideração que escopos mais específicos têm precedência:

```sh
# Skip all plugin aliases, except for the git plugin
zstyle ':omz:plugins:*' aliases no
zstyle ':omz:plugins:git' aliases yes
```

Uma versão anterior desta funcionalidade estava usando a configuração abaixo, que foi removida:

```sh
zstyle ':omz:directories' aliases no
```

Em vez disso, você agora pode usar o seguinte:

```sh
zstyle ':omz:lib:directories' aliases no
```

#### Notice <!-- omit in toc -->

> Esta funcionalidade está atualmente em fase de testes e pode sofrer alterações no futuro. Ela também não
> está atualmente compatível com gerenciadores de plugins, como zpm ou zinit, que não carregam o script de inicialização
> (`oh-my-zsh.sh`) onde esta funcionalidade é implementada.

> Ela também não está atualmente ciente de "aliases" definidos como funções. Exemplos disso são as funções `gccd`,
> `ggf` ou `ggl` do plugin git.

### Prompt git assíncrono

Prompt funções assíncronas são uma funcionalidade experimental (incluída em 3 de abril de 2024) que permite ao Oh My Zsh renderizar
informações do prompt de forma assíncrona. Isso pode melhorar o desempenho da renderização do prompt, mas pode não funcionar bem
com algumas configurações. Esperamos que isso não seja um problema, mas se você estiver vendo problemas com esse novo recurso, você pode
desativá-lo definindo o seguinte em seu arquivo .zshrc, antes que o Oh My Zsh seja carregado:

```sh
zstyle ':omz:alpha:lib:git' async-prompt no
```

Se o seu problema é que o prompt do git parou de aparecer, você pode tentar forçá-lo definindo a seguinte
configuração antes que `oh-my-zsh.sh` seja carregado. Se ainda assim não funcionar, por favor, abra um problema com o seu
caso.

```sh
zstyle ':omz:alpha:lib:git' async-prompt force
```

## Obter Atualizações

Por padrão, você será solicitado a verificar por atualizações a cada 2 semanas. Você pode escolher outros modos de atualização adicionando uma linha ao seu arquivo `~/.zshrc`, **antes que o Oh My Zsh seja carregado**:

1. Atualização automática sem prompt de confirmação:

```sh
   zstyle ':omz:update' mode auto
   ```

2. Apenas ofereça um lembrete a cada alguns dias, se houver atualizações disponíveis:

```sh
   zstyle ':omz:update' mode reminder
   ```

3. Para desabilitar atualizações automáticas totalmente:

```sh
   zstyle ':omz:update' mode disabled
   ```

NOTE: você pode controlar com que frequência o Oh My Zsh verifica atualizações com a seguinte configuração:

```sh
# This will check for updates every 7 days
zstyle ':omz:update' frequency 7
# This will check for updates every time you open the terminal (not recommended)
zstyle ':omz:update' frequency 0
```

### Verbosidade das Atualizações

Você também pode limitar a verbosidade das atualizações com as seguintes configurações:

```sh
zstyle ':omz:update' verbose default # default update prompt

zstyle ':omz:update' verbose minimal # only few lines

zstyle ':omz:update' verbose silent # only errors
```

### Atualizações Manuais

Se você quiser atualizar em qualquer momento (talvez alguém tenha liberado um novo plugin e você não quer esperar uma semana?), basta executar:

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
> Veja mais opções na [FAQ: How do I update Oh My Zsh?](https://github.com/ohmyzsh/ohmyzsh/wiki/FAQ#how-do-i-update-oh-my-zsh).
>
> **O USO DE `omz update --unattended` FOI REMOVIDO, POIS TEM EFEITOS COLATERAIS**.

Magia! 🎉

## Desinstalando Oh My Zsh

Oh My Zsh não é para todos. Vamos sentir falta de você, mas queremos que esse processo seja fácil.

Se quiser desinstalar `oh-my-zsh`, basta executar `uninstall_oh_my_zsh` a partir da linha de comando. Ele removerá
ele mesmo e reverterá sua configuração anterior de `bash` ou `zsh`.

## Como Contribuir para Oh My Zsh?

Antes de participar da nossa deliciosa comunidade, por favor leia o [código de conduta](../CODE_OF_CONDUCT.md).

Estou longe de ser um especialista em [Zsh](https://www.zsh.org/) e suspeito que existam muitas formas de melhorar – se você
tiver ideias sobre como tornar a configuração mais fácil de manter (e mais rápida), não hesite em fazer um fork e enviar
pedidos de pull!

Também precisamos de pessoas para testar os pedidos de pull. Então, dê uma olhada em
[os problemas abertos](https://github.com/ohmyzsh/ohmyzsh/issues) e ajude onde puder.

Veja [Contribuindo](../CONTRIBUTING.md) para mais detalhes.

### Não Envie Nossos Temas

Nós temos (mais do que) suficientes temas no momento. Por favor, adicione seu tema à página de
[temas externos](https://github.com/ohmyzsh/ohmyzsh/wiki/External-themes) do wiki.

## Contribuidores

Oh My Zsh tem uma comunidade vibrante de usuários felizes e contribuidores deliciosos. Sem todo o tempo e ajuda
de nossos contribuidores, não seria tão incrível.

Muito obrigado!

<a href="https://github.com/ohmyzsh/ohmyzsh/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ohmyzsh/ohmyzsh" width="100%"/>
</a>

## Siga Nós

Estamos nas redes sociais:

- [@ohmyzsh](https://x.com/ohmyzsh) no X (anteriormente Twitter). Você deveria seguir.
- [Facebook](https://www.facebook.com/Oh-My-Zsh-296616263819290/) nos dê um toque.
- [Instagram](https://www.instagram.com/_ohmyzsh/) marque-nos em sua postagem mostrando Oh My Zsh!
- [Discord](https://discord.gg/ohmyzsh) para conversar conosco!

## Merchandise

Nós temos
[adesivos, camisetas e canecas disponíveis](https://commitgoods.com/collections/oh-my-zsh?utm_source=github)
para você exibir seu amor por Oh My Zsh. Novamente, você será o assunto da cidade!

## Licença

Oh My Zsh é lançado sob a [licença MIT](../LICENSE.txt).

## Sobre o Planet Argon

![Planet Argon](https://pa-github-assets.s3.amazonaws.com/PARGON_logo_digital_COL-small.jpg)

Oh My Zsh was started by the team at [Planet Argon](https://www.planetargon.com/?utm_source=github), a
[Ruby on Rails development agency](https://www.planetargon.com/services/ruby-on-rails-development?utm_source=github).
Check out our [other open source projects](https://www.planetargon.com/open-source?utm_source=github).

