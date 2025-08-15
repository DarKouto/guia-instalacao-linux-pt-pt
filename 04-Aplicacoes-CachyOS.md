# Aplicações CachyOS

Está finalmente na hora de explicar quais sãos as aplicações pré-instaladas no CachyOS, e quais algumas aplicações essenciais recomendo instalar.

## 1. Aplicações Pré-Instaladas e o seu Propósito
- **ARK**: é um compressor de ficheiros, semelhante ao WinZIP ou WinRAR, 100% compatível com ficheiros deste tipo.
- **Kate**: editor de texto simples, ideal para tirar notas, semelhante ao **Bloco de Notas** ou **Notepad++**
- **GwenView**: visualizador de imagens, também permite rodar, recortar e inverter imagens, assim como ver vídeos.
- **Firefox**: é o browser que vem instalado por defeito. Recuso-me a acreditar que não saibas o que é o Firefox.

## 2. Aplicações a Instalar dos Repositórios Oficiais
Existem duas formas de instalar aplicações dos repositórios oficiais do CachyOS:
1. Usar a **Konsole** (Terminal) com o gestor de pacotes do Arch chamado **pacman**, exemplo: `sudo pacman -S nome-do-pacote-a-instalar`
2. Ir ao **Iniciar** e procurar o **Octopi** que é um ambiente gráfico que ajuda a pesquisar, instalar ou remover pacotes dos repositórios oficiais.

Qual a melhor abordagem? Depende. Eis a minha opinião:
- Para instalar uma única aplicação, o **Octopi** é mais fácil e intuitivo:
  - Pesquisas pela aplicação que queres instalar
  - Clicas com o botão direito no nome do pacote e escolhes **+ Instalar**
  - Clicas no **"Visto"** que aparece no canto superior esquerdo
- Para instalar várias aplicações de uma só vez, usar o **Terminal** é melhor, pois com um único comando consegues instalar tudo ao mesmo tempo.

Cá fica o comando que instala as aplicações que considero essenciais:

**NOTA:** para colar texto no terminal, **NÃO** podes fazer CTRL+C, em vez disso, clica no meio da roda do rato ou fazes **CTRL+SHIFT+V**
```bash
sudo pacman -S brave-bin discord dolphin-plugins flatpak gnome-calculator kio-admin kolourpaint libreoffice-still-pt onlyoffice-bin protonup-qt qbittorrent vlc vlc-plugins-all yay zsh
```

Com este comando instalámos algumas biblitecas importantes, assim como as seguintes aplicações:
- **Brave Browser:** Um browser baseado no Google Chrome mas com melhores funcionalidades e privacidade.
- **Discord:** De certeza que sabes o que é Discord.
- **Gnome-Calculator:** Uma calculadora simples, considero-a melhor do que a KCalc que vem pré-instalada no KDE Plasma.
- **KolourPaint:** Um programa semelhante ao MS Paint.
- **LibreOffice:** Um conjunto de programas semelhantes ao MS Office
- **OnlyOffice:** Outro conjunto de programas semelhantes ao MS Offica (usa aquele que achares melhor)
- **ProtonUP-QT:** Um GUI que serve para instalar versões do Proton (mais info no capítulo de jogos)
- **VLC:** Um reprodutor de vídeo avançado. Certamente também já conheces o VLC.

## 3. Aplicações a Instalar do AUR
Para instalar aplicações do AUR tem mesmo que se usar o **Terminal**, com um "helper" chamado **yay**, que instalamos no comando anterior. Copia o seguinte comando para o teu **Terminal**:
```bash
yay -S discover-overlay pcloud-drive stacer-bin ttf-ms-win10-auto
```
Com este comando instalámos as seguintes aplicações:
- **Discover-Overlay:** uma forma de conseguirmos usar a funcionalidade overlay no Discord, ainda não disponível na app nativa para Linux.
- **pCloud-Drive:** uma Cloud alternativa ao Google Drive, OneDrive, Dropbox, etc.
- **Stacer-Bin:** um programa que ajuda a limpar ficheiros temporários e de cache, semelhante ao CCleaner no Windows, mas muito melhor.
- **TTF-MS-Win10-Auto:** são os principais tipos de letra do Windows. Necessário para ver documentos .doc ou .docx no formato correcto.

### 3.1 Para instalar qualquer outro tipo de letra:
- Procurar na internet e transferir os ficheiros .ttf
- Ir ao **Iniciar** e procurar por **Gestão de Tipos de Letra**
- Selecionar **Instalar de um Ficheiro** e procurar os ficheiros .ttf transferidos

## 4. Aplicações Flatpak/Flathub
Para instalar Flatpaks, também temos que usar o Terminal, mas apenas precisamos de ir ao site https://flathub.org/, procurar a aplicação desejada, clicar na setinha ao lado do botão Install e copiar o código que lá está para o nosso Terminal.

Em todo o caso, deixo aqui um comando com as aplicações essenciais em formato Flatpak:
```bash
flatpak install spotify vesktop warehouse
```
Com este comando instalámos as seguintes aplicações:
- **Spotify:** até a minha avó sabe o que é o Spotify...
- **Vesktop:** é um Discord alternativo, que usa a versão do browser numa app. Usar só quando o Discord oficial está com algum problema.
- **Warehouse:** é um programa que nos permite navegar a estrutura de pastas do Flapak, apenas necessário em casos específicos.
