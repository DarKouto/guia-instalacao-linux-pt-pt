<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/03-Configurar-CachyOS.md">[03 - Configurar CachyOS]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/05-Jogos-CachyOS.md">[05 - Jogos CachyOS]</a>
</div>
<hr>

# Aplicações CachyOS
Existem várias fontes das quais podemos instalar software no CachyOS, podes pensar nelas como sendo uma espécie **App Store** ou **Play Store**. As 3 principais, e a sua ordem preferencial é esta:
1. **Repositórios Oficiais** do CachyOS
2. **AUR** (Arch User Repository)
3. **Flatpak/Flathub**

Os **repositórios oficiais** contêm os programas testados e aprovados para o CachyOS.

As distros baseadas em **Arch Linux** têm ainda acesso ao **AUR (Arch User Repository)**, que é um repositório criado e mantido por utilizadores.

O **Flatpak/Flathub** é um repositório que funciona em qualquer distro, pois o seu software é distribuído num "contentor". **Podes e deves** usar Flatpaks, mas apenas quando o programa que procuras não exista nem nos repositórios oficiais nem no AUR, pois os "contetores" ocupam mais espaço em disco.

Além destas 3 formas, existe ainda o formato **AppImage**, que é um ficheiro executável com a aplicação a funcionar. Um pouco mais semelhante a um ficheiro .exe no Windows.

**NOTA**: Se precisares de alguma aplicação que não esteja disponível nestas 3 fontes ou em **AppImage**, terás que ser tu próprio a investigar como a instalar (Build From Source, ficheiros .TAR.GZ, ficheiros .DEB, etc), ou se há alguma aplicação alternativa que faça o mesmo efeito. Faz parte do processo, é a luta.

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
  - Activa **AppImage**
  - Desactiva **Recomendados** e **Ícone na Área de Notificação**

<img src="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/imagens/shelly01.jpg" width=650>

### Instalar Aplicações
1. Seleciona o separador **"Pacotes"** do lado esquerdo. Este refere-se aos **repositórios oficiais**.
2. Seleciona o separador **Instalar** em cima.
3. Pesquisa o pacote que queres instalar. Ex: piper
4. Clica no **"Visto"** para selecionar
5. Clica em **Instalar Selecionados**
- Para desinstalares, selecionas o separador **"Gerir"** em cima, e segues o mesmo processo.
- Para instalares algo do **AUR** ou **Flatpak**, apenas tens que selecionar o respectivo separador, que está bem identificado.
  
<img src="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/imagens/shelly02a.jpg" width=700>

## 💽 Aplicações dos Repositórios Oficiais
Ficam aqui algumas aplicações essenciais. Como são várias aplicações de uma só vez, é mais rápido usar a **Konsole**, visto que já te deixei aqui o comando completo, só precisas de copiar e colar. Podes usar o **Shelly** se preferires, mas tens que selecionar os pacotes um a um.

**NOTA:** para colar texto no **Konsole**, **NÃO** podes fazer CTRL+C, em vez disso, clica no **botão direito do rato** e fazes colar, ou clicas **botão do meio do rato**, ou fazes **CTRL+SHIFT+V**

```bash
sudo pacman -S brave-bin discord dolphin-plugins flatpak kdenlive kio-admin kolourpaint libreoffice-still-pt onlyoffice-bin openrgb protonup-qt qbittorrent sane-airscan skanpage stacer vesktop vlc vlc-plugins-all yay zsh
```

Com este comando instalámos as seguintes aplicações (assimo como algumas dependências importantes):
- **Brave:** Um browser baseado no Chromium, com mais privacidade e funcionalidades úteis.
- **Discord:** A aplicação oficial do Discord, famosa plataforma de chat.
- **Kdenlive:** Editor de vídeo avançado, semelhante a Sony Vegas ou Premiere.
- **KolourPaint:** Um programa semelhante ao MS Paint.
- **LibreOffice:** Um conjunto de programas semelhantes ao MS Office.
- **OnlyOffice:** Outro conjunto de programas semelhantes ao MS Office (usa aquele que achares melhor).
- **OpenRGB:** Um programa que controla o RGB e efeitos dos teus dispostivos.
- **ProtonUP-QT:** Um GUI que serve para instalar versões do Proton (mais info no capítulo de jogos).
- **qBitTorrent:** Um cliente de BitTorrent.
- **Skanpage:** Programa do KDE para usar o Scanner (caso tenhas um).
- **Stacer:** Um programa que ajuda a limpar ficheiros temporários e de cache, semelhante ao CCleaner.
- **Vesktop:** É o Discord mas numa aplicação alternativa, com algumas funcionalidades extra.
- **VLC:** Um reprodutor de áudio e vídeo. Certamente também já conheces o VLC.

## ⌨️ Aplicações do AUR
Copia o seguinte comando para a tua **Konsole**:
```bash
yay -S ani-cli lyra-music-bin pcloud-drive visual-studio-code-bin
```
Com este comando instalámos as seguintes aplicações:
- **Ani-Cli:** uma forma de pesquisar e ver Anime Master Race directamente no Terminal, basta escreveres `ani-cli` e seguires a instruções.
- **Lyra Music:** uma plataforma de streaming de música, rádio e podcasts. Semelhante ao Spotify mas com preços muito mais justos. E já agora, sou eu mesmo o mantedor oficial do pacote no AUR.
- **pCloud Drive:** uma Cloud alternativa ao Google Drive, OneDrive, Dropbox, etc.
- **Visual Studio Code:** o famoso IDE, ferramenta de programação, versão oficial.

Para mais informações vai a https://aur.archlinux.org

## 📦 Aplicações do Flatpak/Flathub
Copia o seguinte comando para a tua **Konsole**:
```bash
flatpak install chrome spotify tuxguitar
```
Com este comando instalámos as seguintes aplicações:
- **Google Chrome**: o famoso browser da Google. **NÃO RECOMENDO** ninguém usar este devorador de RAM. Mas sei que muita gente tem lá todas as suas contas e os dados, e não quer estar a ter o trabalho de migrar para outro browser, portanto cá fica.
- **TuxGuitar:** é um clone do famoso Guitar Pro, 100% compatível com ficheiros .gp3, 4, 5 e 6.

Para mais informação vai a https://flathub.org/

## ⚙️ Aplicações AppImage
Caso não encontres o que procuras nestes 3 repositórios, a próxima melhor alternativa é usares uma AppImage. Visita o site oficial do Software que procuras, ou algum site fidedigno, e verifica se existe uma versão **AppImage**, se existir descarrega o ficheiro.

Para instalares AppImages basta clicares 2x no ficheiro. Mas para ficar tudo integrado no sistema de uma forma mais correcta, segue os seguintes passos:
- Abre o **Shelly**
- Vai ao separador lateral **AppImage**
- Clica em **+ Instalar AppImage** 
- Escolhes o ficheiro que descarregaste.

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
Contrariamente ao Windows e MacOS, no Linux as actualizações não são automáticas, são manuais e ficam sempre ao encargo e responsabilidade do utilizador. Felizmente no CachyOS há uma forma muito simples de o fazeres:
- Clica no **Cachy Update** (é o **ícone do CachyOS** que aparece no canto inferior direito junto ao relógio)
- Segue as instruções que te aparecem no Terminal.
- Se aparecer uma "parede de texto" referente a pacotes do AUR, basta clicar na tecla **Q** do teclado para continuar.

É recomendado que atualizes o teu sistema com regularidade (uma vez por semana pelo menos, visto que o CachyOS/Arch é uma *rolling release*). Ao atualizares um sistema Linux, ele faz tudo de uma só vez: atualiza o Sistema Operativo, as Aplicações e os Drivers.

<img src="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/imagens/cachy-update.jpg">

**NOTA**: Caso te apareça uma aviso do género: "O pacote X **quebra** a dependência Y", **cancela a actualização** e tenta outra vez no dia seguinte (ou passadas umas horas), que o problema será resolvido internamente.

<hr>
<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/03-Configurar-CachyOS.md">[03 - Configurar CachyOS]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/05-Jogos-CachyOS.md">[05 - Jogos CachyOS]</a>
</div>
