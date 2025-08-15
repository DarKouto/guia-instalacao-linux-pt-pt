# Notas Iniciais

## O que é um Sistema Operativo Linux
Tecnicamente falando, o **Linux** não é bem um sistema operativo, mas sim um **Kernel** (núcleo), que faz a ponte entre o software e o hardware de uma máquina. Foi desenvolvido por **Linus Torvalds** em 1991 e continua a ser atualizado e mantido até hoje. Tem a particularidade de ser totalmente **Open Source** (código aberto).

Aquilo a que chamamos um sistema operativo **Linux** é, na verdade, uma combinação de vários componentes:
- O **Kernel Linux**
- As utilidades **GNU** (desenvolvidas por **Richard Stallman**)
- O ambiente gráfico (**Desktop Environment**)

É comum encontrar quem defenda que o termo mais correto seria **GNU/Linux**. No entanto, por convenção social e simplicidade, acabou-se por chamar simplesmente **Linux** ao sistema operativo.

## Distribuições de Linux (Distros)
Uma **Distro Linux**, de forma muito simplificada, é um sistema operativo completo que inclui o **Kernel Linux**, utilidades **GNU**, pacotes de software, um ambiente gráfico (exemplos: **KDE Plasma** ou **Gnome**) e outras ferramentas.

À primeira vista, parecem existir centenas de **Distros Linux**, mas a maioria são adaptações e modificações de outras distribuições maiores. Como tal, considero existirem 3 grandes "famílias" de **Distros**:
1.  **Debian**: é muito estável, mas apenas recebe atualizações de 2 em 2 anos.
2.  **Arch**: é muito leve e personalizável, e está constantemente a ser atualizada, num modelo "Rolling Release".
3.  **Fedora**: é um meio-termo entre o Debian e o Arch, recebendo grandes atualizações de 6 em 6 meses.

A distribuição que uso e que esta documentação aborda é o **CachyOS**, que é um "fork" do **Arch Linux**. Conta com algumas melhorias e adições, como um instalador gráfico, um kernel personalizado para performance e gaming, e um conjunto de software pré-instalado.

## Instalar Software em Linux
A forma mais comum de instalar programas e aplicações em **Linux** é através do **repositório** de software oficial da própria distro. Um **repositório** é basicamente um servidor onde o software está armazenado, ao qual pedimos para instalar um certo pacote. Atualizar ou remover software também é feito através do **repositório**.

As distros baseadas em **Arch** têm ainda acesso ao **AUR (Arch User Repository)**, que é um repositório criado e mantido por utilizadores, que contém muitas vezes programas que não se encontram nos repositórios oficiais.

Finalmente, existe o **Flatpak/Flathub**, que é um repositório que funciona em qualquer distro, pois o seu software é distribuído num contentor que inclui o programa, bem como todas as bibliotecas e dependências necessárias para o executar.

## Outras Informações Úteis
- Esta documentação presume que o utlizador tenha um conhecimento básico sobre computadores, instalação de sistemas operativos (Windows ou MacOS) assim como formas de aceder à BIOS duma máquina.
- O `"~"` (til) representa o caminho da pasta `/home/NomeDoUtilizador/`
  - Exemplo: `~/` é igual a `/home/NomeDoUtilizador/`
- No terminal, `sudo` significa (Super User Do) e serve para executar comandos com privilégios de administrador.
