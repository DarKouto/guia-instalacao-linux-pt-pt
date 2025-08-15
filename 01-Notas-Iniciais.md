# Notas Iniciais

## O que é um Sistema Operativo Linux
- Tecnicamente falando, o **Linux** não é bem um sistema operativo, mas sim um **Kernel** (núcleo), que é o que faz a ponte entre o software e o hardware duma máquina. Foi desenvolvido por **Linus Torvalds** em 1991, e continua a ser actualizado e mantindo aos dias de hoje. Tem a particularidade de ser totalmente **Open Source** (código aberto)
- Aquilo a que chamámos um sistema operativo **Linux**, é na verdade uma combinação de várias coisas:
  - O Kernel Linux
  - As utilidades **GNU** (desenvolvidas por **Richard Stallman**)
  - O ambiente gráfico (**Desktop Environment**)
- É comum encontrar quem defenda que o termo mais correcto seria **GNU/Linux**. No entanto, por convenção social e simplicidade, acabou-se por chamar simplesmente **Linux** ao sistema operativo.

## Distribuições de Linux (Distros)
- Uma **Distro Linux**, de forma muito simplificada, é um sistema operativo completo que conta com o Kernel Linux, utilidades GNU, pacotes de software, um ambiente gráfico (exemplos: KDE Plasma ou Gnome) e outras ferramentas.
- À primeira vista parecem existir centenas de **Distros Linux**, mas na verdade, a maior parte delas são adaptações e modificações de outras distribuições maiores. Como tal, considero existirem 3 grandes **Distros**:
  1. **Debian**: é muito estável, mas apenas recebe actualizações de 2 em 2 anos.
  2. **Arch**: é muito leve e personalizável, está constantemente a ser actualizada, modelo Rolling Release.
  3. **Fedora**: é um meio termo entre o Debian e o Arch, recebe grandes actualizções de 6 em 6 meses.
- A distribuição que uso e que esta documentação aborda é o **CachyOS**, que é um "fork" do **Arch Linux**, e que conta com algumas melhorias e adições, como por exemplo um instalador gráfico, um kernel personalizado para performance e gaming, um conjunto de software pré-instalado, etc.

## Instalar Software em Linux
- A forma mais comum de instalar programas e aplicações em Linux é usar o **repositório** de software oficial da própria distro.
- Um **repositório** é basicamente um servidor onde o software está armazenado, ao qual pedimos para instalar um certo e determinado pacote.
- Actualizar ou remover software também é feito através do **repositório**.
- As distros baseadas em Arch têm ainda acesso ao **AUR (Arch User Repository)**, que é um repositório criado e mantindo por utilizadores, que contém muitas vezes programas não encontrados nos repositórios oficiais.
- Finalmente, existe o **Flatpak/Flathub**, que é um repositório que funciona em qualquer distro, pois o seu software é distribuído num contentor que contém o programa/app em si, assim como todas as librarias e depenências necessárias para o executar.

## Outras Informações
- Esta documentção presume que o utlizador tenha já um conhecimento básico sobre computadores, instalação de sistemas operativos (Windows ou MacOS) assim como formas de aceder à BIOS duma máquina.
- O `"~"` (til) represente o caminho da pasta `/home/NomeDoUtilizador/`.
- No terminal, `sudo`: Significa (Super User Do).
- A Shell do terminal que iremos usar é a ZSH. Se o utilizador não for programador, isto é irrelevante. Se for programador, recuso-me a aceitar que não saiba porque escolhi a ZSH.
