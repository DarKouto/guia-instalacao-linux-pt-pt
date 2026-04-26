<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/03-Configurar-CachyOS.md">[03 - Configurar CachyOS]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/05-Jogos-CachyOS.md">[05 - Jogos CachyOS]</a>
</div>
<hr>

# Aplicações CachyOS
Existem várias fontes das quais podemos instalar software no CachyOS, podes pensar nelas como sendo uma espécie **App Store** ou **Play Store**. As 3 principais são:
1. **Repositórios Oficiais** do CachyOS
2. **AUR** (Arch User Repository)
3. **Flatpak/Flathub**

Os **repositórios oficiais** contêm os programas testados e aprovados para o CachyOS. Deves usar esta opção sempre que possível, pois é a mais indicada.

As distros baseadas em **Arch Linux** têm ainda acesso ao **AUR (Arch User Repository)**, que é um repositório criado e mantido por utilizadores. Uma excelente opção para encontrar programas que não se encontram nos repositórios oficiais.

Existe ainda o **Flatpak/Flathub**, que é um repositório que funciona em qualquer distro, pois o seu software é distribuído num "contentor". **Podes e deves** usar o Flatpak, mas apenas quando o programa que procuras não exista nem nos repositórios oficiais nem no AUR, pois os "contetores" Flatpak ocupam mais espaço em disco.

**NOTA**: Na eventualidade de precisares de uma app específica que não esteja disponível nestas 3 fontes, terás que ser tu próprio a investigar como a instalar (AppImage, Build From Source, .DEB, etc), ou se há um software alternativo. Faz parte do processo, é a luta.

## 🎒 Aplicações Pré-Instaladas
Estas aplicações já vêm instaladas por defeito no CachyOS com KDE Plasma. Cá ficam as essenciais:
- **ARK**: é um compressor de ficheiros, semelhante ao WinZIP ou WinRAR, 100% compatível com ficheiros deste tipo.
- **Firefox**: é o browser/navegador da Mozilla.
- **GwenView**: visualizador e editor imagens, também permite ver vídeos.
- **Kate**: editor de texto semelhante ao **Bloco de Notas** ou **Notepad++**
- **Konsole**: é o emulador de **Terminal**. Existem outros mas este é o mais simples e o que vamos usar.
- **Monitor de Sistema:** semelhante ao **Gestor de Tarefas** do Windows.

## 🐚 Shelly

Para instalar aplicações podes usar o **Shelly** que é um ambiente gráfico que permite pesquisar programas nos repositórios. Também existe a possiblidade de usar a **Konsole**/**Terminal**, com um comando do género: ```sudo pacman -S audacious```. No entanto o **Shelly** é mais simples e intuitivo para quem se está a iniciar no mundo Linux.

### Configurar Shelly
- Vai a **Iniciar** e procura **Shelly**
- Na Configuração Inicial faz o seguinte:
  - Activa **AUR**
  - Activa **Flatpak**
  - Desactiva **Tray Icon**

<img src="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/imagens/shelly1.jpg" width=750>

### Instalar Aplicações
- Seleciona o separador **"Install"** do lado esquerdo: isto vai procurar nos **repositórios oficiais**
- Pesquisa o pacote que queres instalar. Ex: audacious
- Clica no **"Visto"** > Clica em **Instalar**
- Para desinstalares, selecionas o separador **"Manage"** e segues o mesmo processo.
- Para instalares algo do **AUR** ou **Flatpak**, apenas tens que selecionar o respectivo separador, que está bem identificado.
  
<img src="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/imagens/shelly2.jpg" width=700>

## 💽 Aplicações dos Repositórios Oficiais
Ficam aqui algumas aplicações essenciais. Como são várias aplicações de uma só vez, é mais rápido usar a **Konsole**, visto que já te deixei aqui o comando completo, só precisas de copiar e colar. Podes usar o **Shelly** se preferires, mas tens que selecionar os pacotes um a um.

**NOTA:** para colar texto no **Konsole**, **NÃO** podes fazer CTRL+C, em vez disso, clica no **botão direito do rato** e fazes colar, ou clicas **botão do meio do rato**, ou fazes **CTRL+SHIFT+V**

```bash
sudo pacman -S brave-bin discord dolphin-plugins flatpak gnome-calculator kio-admin kolourpaint libreoffice-still-pt onlyoffice-bin openrgb protonup-qt qbittorrent sane-airscan skanpage stacer vesktop vlc vlc-plugins-all yay zsh
```

Com este comando instalámos as seguintes aplicações (assimo como algumas dependências importantes):
- **Brave:** Um browser baseado no Chromium mas com melhores funcionalidades e privacidade.
- **Discord:** A aplicação oficial do Discord, famosa plataforma de chat.
- **Gnome Calculator:** Uma calculadora simples, considero-a melhor do que a KCalc que vem pré-instalada no KDE Plasma.
- **KolourPaint:** Um programa semelhante ao MS Paint.
- **LibreOffice:** Um conjunto de programas semelhantes ao MS Office
- **OnlyOffice:** Outro conjunto de programas semelhantes ao MS Office (usa aquele que achares melhor)
- **OpenRGB:** Um programa que controla o RGB e efeitos dos teus dispostivos
- **ProtonUP-QT:** Um GUI que serve para instalar versões do Proton (mais info no capítulo de jogos)
- **qBitTorrent:** Um cliente de BitTorrent
- **Skanpage:** Programa do KDE para usar o Scanner (caso tenhas um)
- **Stacer:** Um programa que ajuda a limpar ficheiros temporários e de cache, semelhante ao CCleaner no Windows, mas muito melhor.
- **Vesktop:** É o Discord mas numa aplicação alternativa, com algumas funcionalidades extra.
- **VLC:** Um reprodutor de áudio e vídeo. Certamente também já conheces o VLC.

## ⌨️ Aplicações do AUR

Copia o seguinte comando para a tua **Konsole**:
```bash
yay -S ani-cli pcloud-drive visual-studio-code-bin
```
Com este comando instalámos as seguintes aplicações:
- **Ani-Cli:** uma forma de pesquisar e ver Anime Master Race directamente no Terminal, basta escreveres `ani-cli` e seguires a instruções.
- **pCloud Drive:** uma Cloud alternativa ao Google Drive, OneDrive, Dropbox, etc.
- **Visual Studio Code:** o famoso IDE, ferramenta de programação, versão oficial.

Para mais informações vai a https://aur.archlinux.org

## 📦 Aplicações do Flatpak/Flathub

Copia o seguinte comando para a tua **Konsole**:
```bash
flatpak install spotify tuxguitar
```
Com este comando instalámos as seguintes aplicações:
- **Spotify:** até a minha avó sabe o que é o Spotify...
- **TuxGuitar:** é um clone do famoso Guitar Pro, 100% compatível com ficheiros .gp3, 4, 5 e 6.

Para mais informação vai a https://flathub.org/

## ⭐ Aplicações Predefinidas
Para selecionares as aplicações predefinidas para cada tarefa ou tipo de ficheiro, vai a **Iniciar** e procura por **Default Applications**. Aqui podes configurar tudo conforme as tuas preferências.

## 🔠 Tipos de Letra / Fonts:
Os sistemas Linux não têm os tipos de letra / fonts típicas da Microsoft e MacOS. Existem formas "oficiais" de as instalar, mas requerem algum trabalho extra. Como tal decidi facilitar-te a vida e criei 2 ficheiros que contêm as principais fonts que praticamente toda a gente usa. 
- Faz o download dos seguintes ficheiros:
  - [Fonts Linux 1](https://raw.githubusercontent.com/darkouto/guia-instalacao-linux-pt-pt/main/fonts/fonts-linux-1.tar.gz)
  - [Fonts Linux 2](https://raw.githubusercontent.com/darkouto/guia-instalacao-linux-pt-pt/main/fonts/fonts-linux-2.tar.gz)
- Abre os ficheiros e extrai as pastas que lá estão comprimidas.
- Vai ao **Iniciar** e procura por **Gestão dos Tipos de Letra**.
- Seleciona **Instalar de um Ficheiro** e seleciona os ficheiros .ttf extraídos.
- Quando perguntar onde queres instalar, escolhe **Sistema**.

<img src="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/imagens/fonts.jpg">

**NOTA**: Qualquer outra font que precises, procura na internet pelos os ficheiros .ttf, descarrega-os, e torna a instalar através da **Gestão dos Tipos de Letra**.

## 🔄 Atualizar Sistema / Cachy-Update
É recomendado que atualizes o teu sistema com regularidade (uma vez por semana pelo menos). Ao atualizares um sistema Linux, ele faz tudo de uma só vez: atualiza o Sistema Operativo, as Aplicações e os Drivers.
- Clica no **Cachy Update**, que é o **ícone do CachyOS** que aparece no canto inferior direito (junto ao relógio). Agora é só seguir as instruções que aparecem no terminal.
- **NOTA**: se aparecer uma "parede de texto" referente a pacotes do AUR, basta clicar na tecla **Q** do teclado para continuar.
<img src="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/imagens/cachy-update.jpg">

<hr>
<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/03-Configurar-CachyOS.md">[03 - Configurar CachyOS]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/05-Jogos-CachyOS.md">[05 - Jogos CachyOS]</a>
</div>
