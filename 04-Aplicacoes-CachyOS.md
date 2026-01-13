<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/03-Configurar-CachyOS.md">[03 - Configurar CachyOS]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/05-Jogos-CachyOS.md">[05 - Jogos CachyOS]</a>
</div>
<hr>

# Aplicações CachyOS
Existem várias formas de instalar software no CachyOS, mas as principais são:
1. **Repositórios Oficiais** do CachyOS
2. **AUR** (Arch User Repository)
3. **Flatpak/Flathub**

Um **repositório** é basicamente um servidor onde o software está armazenado, ao qual pedimos para instalar um certo pacote, podes pensar nisso como se fosse uma **App Store** ou **Play Store**. Atualizar ou remover software também é feito através do **repositório**.

As distros baseadas em **Arch Linux** têm ainda acesso ao **AUR (Arch User Repository)**, que é um repositório criado e mantido por utilizadores, que contém software que por vezes não se encontra nos repositórios oficiais.

Finalmente, existe o **Flatpak/Flathub**, que é um repositório que funciona em qualquer distro, pois o seu software é distribuído num contentor que inclui o programa e as dependências necessárias para o executar.

**NOTA**: Qualquer aplicação que não esteja disponível nestas 3 fontes, terás que ser tu próprio a investigar como a instalar, ou se há um software alternativo. Faz parte do processo, é a luta.

## 1. Aplicações Pré-Instaladas e o seu Propósito
- **ARK**: é um compressor de ficheiros, semelhante ao WinZIP ou WinRAR, 100% compatível com ficheiros deste tipo.
- **Firefox**: é o browser/navegador que vem instalado por defeito.
- **GwenView**: visualizador e editor imagens, também permite ver vídeos.
- **Kate**: editor de texto semelhante ao **Bloco de Notas** ou **Notepad++**
- **Monitor de Sistema:** semelhante ao **Gestor de Tarefas** do Windows. Para abrir carrega em **Super+Esc** (chama-se **Super** à tecla Windows)

## 2. Aplicações a Instalar dos Repositórios Oficiais

Existem 2 formas de instalar aplicações dos repositórios oficiais:

### 1. Octopi (Ambiente Gráfico)
- Vai a **Iniciar** e procura **Octopi**
- Pesquisa pela aplicação que queres instalar
- Clica com o botão direito no nome do pacote e escolhes "**+ Instalar**"
- Clica no **"Visto"** que aparece no canto superior esquerdo
- Para remover uma aplicação o processo é o mesmo, mas selecionas **Remover**

### 2. Konsole (Terminal)
- Vai a **Iniciar** e procura **Konsole**
- Usa o gestor de pacotes do **Arch Linux** chamado **pacman**
  - Exemplo: `sudo pacman -S nome-do-pacote-a-instalar`

Qual a melhor abordagem? Depende:
- Para instalar **uma única aplicação** o **Octopi** é melhor, pois é mais fácil e intuitivo.
- Para instalar **várias aplicações** de uma só vez, a **Konsole** é melhor, pois com um único comando consegues instalar tudo ao mesmo tempo.

### Aplicações Essenciais

Ficam aqui algumas aplicações que considero essenciais. Como são várias aplicações de uma só vez, o melhor é usar a **Konsole**, copia este comando para o teu Terminal.

**NOTA:** para colar texto na **Konsole**, **NÃO** podes fazer CTRL+C, em vez disso, clica no **botão do meio do rato** ou fazes **CTRL+SHIFT+V**

```bash
sudo pacman -S brave-bin discord dolphin-plugins flatpak gnome-calculator kio-admin kolourpaint libreoffice-still-pt onlyoffice-bin openrgb protonup-qt qbittorrent stacer vesktop vlc vlc-plugins-all yay zsh
```

Com este comando instalámos as seguintes aplicações (assimo como algumas dependências importantes):
- **Brave Browser:** Um browser baseado no Chromium mas com melhores funcionalidades e privacidade.
- **Discord:** A aplicação oficial do Discord, famosa plataforma de chat.
- **Gnome-Calculator:** Uma calculadora simples, considero-a melhor do que a KCalc que vem pré-instalada no KDE Plasma.
- **KolourPaint:** Um programa semelhante ao MS Paint.
- **LibreOffice:** Um conjunto de programas semelhantes ao MS Office
- **OnlyOffice:** Outro conjunto de programas semelhantes ao MS Office (usa aquele que achares melhor)
- **OpenRGB:** Um programa que controla o RGB e efeitos dos teus dispostivos
- **ProtonUP-QT:** Um GUI que serve para instalar versões do Proton (mais info no capítulo de jogos)
- **qBitTorrent:** Um cliente de BitTorrent
- **Stacer:** Um programa que ajuda a limpar ficheiros temporários e de cache, semelhante ao CCleaner no Windows, mas muito melhor.
- **Vesktop:** É o Discord mas numa aplicação alternativa, com algumas funcionalidades extra.
- **VLC:** Um reprodutor de áudio e vídeo. Certamente também já conheces o VLC.

## 3. Aplicações a Instalar do AUR
Para instalar aplicações do AUR, tens mesmo que se usar a **Konsole**, com um "helper" chamado **yay**, que instalamos no comando anterior. Podes pesquisar por pacotes em https://aur.archlinux.org/

Cá ficam algumas apps essenciais, copia o seguinte comando para a tua **Konsole**:
```bash
yay -S discover-overlay pcloud-drive ttf-ms-win10-auto
```
Com este comando instalámos as seguintes aplicações:
- **Discover Overlay:** permite usar a funcionalidade overlay no Discord, que ainda não está disponível na app nativa para Linux.
- **pCloud Drive:** uma Cloud alternativa ao Google Drive, OneDrive, Dropbox, etc.
- **TTF-MS-Win10-Auto:** são os principais tipos de letra do Windows (ex: Arial, Verdana, Times New Roman)

**NOTA**: Ultimamente o pacote ttf-ms-win10-auto tem dado alguns problemas na instalação, caso te aconteça, ignora o pacote, e instalas os tipos de letra manualmente.

### 3.1 Para instalar qualquer outro tipo de letra:
- Procura na internet e transfere os ficheiros .ttf
- Vai ao **Iniciar** e procura por **Gestão de Tipos de Letra**
- Seleciona **Instalar de um Ficheiro** e procura os ficheiros .ttf transferidos

## 4. Aplicações Flatpak/Flathub
Para instalar Flatpaks, também temos que usar a **Konsole**, mas apenas precisamos de ir ao site https://flathub.org/, procurar a aplicação desejada, clicar na setinha ao lado do botão Install e copiar o código que lá está para a **Konsole**.

Em todo o caso, deixo aqui um comando com as aplicações essenciais em formato Flatpak:
```bash
flatpak install spotify tuxguitar 
```
Com este comando instalámos as seguintes aplicações:
- **Spotify:** até a minha avó sabe o que é o Spotify...
- **TuxGuitar:** é um clone do famoso Guitar Pro, 100% compatível com ficheiros .gp3, 4, 5 e 6.

## 5. Aplicações Predefinidas
Para selecionares as aplicações predefinidas para cada tarefa ou tipo de ficheiro, vai a **Iniciar** e procura por **Default Applications**. Aqui podes configurar tudo conforme as tuas preferências.

## 6. Atualizar Sistema e Aplicações
Contrariamente ao Windows que te obriga a atualizar quer queiras quer não, e nos piores momentos possíveis, o Linux não te obriga a rigorosamente a nada. Dito isto, podes e **deves** atualizar o teu sistema com regularidade (uma vez por semana pelo menos).

Há duas formas para **atulizar o sistema**, escolhe o método que preferires:
1. Clicar no **ícone do CachyOS** que aparece no canto inferior direito (junto ao relógio), esse é o **Cachy Updater** que se ativou no ínicio da configuração. Depois é só seguir as instruções que aparecem no terminal. **NOTA**: quando aparecer a "parede de texto" referente a pacotes do AUR, basta clicar na tecla **Q** do teclado para continuar.
2. Ir a **Iniciar**, procurar por **Konsole** (Terminal) e escrever:
```bash
yay
flatpak update
```
- O *yay* atualiza as aplicações dos **Repositórios Oficiais** e do **AUR**, e também atualiza o sistema.
- O *flatpak update* atualiza as aplicações **Flatpak**

<hr>
<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/03-Configurar-CachyOS.md">[03 - Configurar CachyOS]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/05-Jogos-CachyOS.md">[05 - Jogos CachyOS]</a>
</div>
