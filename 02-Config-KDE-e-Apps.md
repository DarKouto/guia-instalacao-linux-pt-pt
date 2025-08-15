# CachyOS: Configuração do KDE e Instalação de Aplicações

## Configuração do KDE

### KWALLET
- Abrir a aplicação da Carteira KDE e desativar os 2 vistos.
- (Remover o visto de baixo primeiro > Aplicar > só depois remover o de cima).

### Definições do Ecrã (WAYLAND)
- Botão direito > Display Configuration > **144hz**.
- **Escala**: 125% (Portáteis 1080p).
- **Color Profile**: ICC Profile (SÓ PARA GIGABYTE).
  - Selecionar Ficheiro **RGB-1.15G.icc** na pasta pCloud e Aplicar.
  - Isto coloca a Gamma em 1.15 mesmo em Wayland.
  - Neste momento estou a usar 1.15.

### Definições do Ecrã (X11)
- Botão direito > Display Configuration > **144hz**.
- **Escala**: 125% (Portáteis 1080p).
- **Gamma**: 1.10 (Gigabyte) (Requer instalação do `kgamma`).

### Tema Global
- Escolher **Breeze Twilight** (Brisa ao Anoitecer).
- Ativar os 2 vistos > Reiniciar.

### CachyOS Hello > Apps/Tweaks
- Ativar **Ananicy Cpp** e **Bluetooth**.
- Clicar em "Rank Mirrors".

### Configurar Ícones do Ambiente de Trabalho e Wallpaper
- Botão Direito do Rato > Desktop e Wallpaper.
- Escolher Wallpaper desejado.
- Ícones > Disposição > De Cima para Baixo.

### Superbar / Painel
- Botão direito > Show Panel Config > Desativar **Floating** > Height: **44**.
- Botão direito no Mostrar Ambiente de Trabalho > Alternativas > **Minimizar todas**.
- Botão direito > Configurar Gestor Por Ícones > Comportamento > Ao Carregar Numa Tarefa Agrupada > **Mostra Antevisões Pequenas**.

### Área de Notificação
- Clicar Notificações > Não incomodar > Até Cancelar Manualmente.
- Seta da Bandeja > Configurar > Elementos.
  - **Volume**, **Internet**, **Power**: Sempre Visíveis.
  - **Área de Transferência**: Sempre Escondida > Desativar os 2 Históricos.
  - **Notificações**: Desativada.

### Calendário
- Clicar no Calendário > Reduzir tamanho Horizontal.
- Nas configurações > Calendário > Primeiro dia da Semana > 2ª Feira.

### Iniciar / Menu
- Botão Direito no Iniciar > Editar Aplicações.
- Mover **KATE** de Desenvolvimento para Escritório.
- Remover: Educação, Desenvolvimento, Perdidos e Achados.

### Energia
- Conf. Sistema > Bloqueio de Ecrã > **Never**.
- Conf. Sistema > Bloqueio de Ecrã > Configure Appearance > Mudar imagem.
- Conf. Sistema > SDDM > Mudar imagem.
- Conf. Sistema > Poupança de Energia > Desativar as ações necessárias.

### Ficheiros Recentes
- Conf Sistema > F. Recentes > Desativar e Limpar Histórico.

### Pesquisa Plasma (INICIAR)
- Conf. Sistema > Pesquisa > Pesquisa Plasma > DESATIVAR: Favoritos, F.Recentes, File Search, Histórico Navegador, Janelas Abertas, Palavras-Chave, Páginas Navegador.

### Animações / Velocidade (SÓ CACHYOS)
- Conf. Sistema > Comportamento Geral > Velocidade da Animação.
- Contar 9 Pontos > Aplicar (o primeiro ponto é o 1, não o zero).

### Tipos de Letra (SÓ CACHYOS)
- Conf. Sistema > Text & Fonts > Tipos de Letra.
- Aumentar 1 ponto em alguns, para ficar: 11, 10, 9, 11, 11, 10.

### Teclado
- Conf. Sistema > Teclado > Taxa de Repetição > **40,00**.
- NumLock on Startup: **ON**.

### Volume no Teclado
- Conf. de Sistema > Teclado > Atalhos.
- Add New > Command/Script > No Final Adicionar atalho (Teclado).
  - **Mute**: `pactl -- set-sink-mute @DEFAULT_SINK@ toggle`.
  - **Volume Down**: `pactl -- set-sink-volume @DEFAULT_SINK@ -5%`.
  - **Volume Up**: `pactl -- set-sink-volume @DEFAULT_SINK@ +5%`.

### Rato
- Conf. Sistema > Rato > SELECIONAR O DISPOSITIVO CORRETO.
  - Desativar Aceleração (SÓ WAYLAND).
  - Velocidade Ponteiro: -0.10 (no Rival 110 a 1000dpi).
  - Velocidade Ponteiro: +0.10 (no Rival 3 a 800dpi).
  - Aumentar Velocidade deslocamento/roda (SÓ WAYLAND).
- Conf. Sistema > Rato por Toque > Desativar com rato conectado.
- Conf. Sistema > Rato > Extremos do Ecrã > Desativar.

### Som
- Conf. Sistema > Sound > Desligar Starship/Matisse.
- Rename Devices: Escrever "ASUS VG249Q1R" no monitor.

---

## Dolphin / File Manager

- Ampliação Portátil: **80px**.
- Ampliação Desktop: **96px**.
- Menu Hamburger > Configurar > Configure Dolphin.
  - **INTERFACE**:
    - Folders and Tabs > Arranque -> Escolher `home/darkouto`.
    - Antevisões > Remote > Files Below 15 MB > Show preview for Folders.
    - Confirmações > V no Enviar ficheiros para o lixo.
    - Status > Status Bar -> Full Width e Mostrar Ampliação.
  - **VIEW**: General > Recordar o estilo de cada pasta.
  - **MENU DE CONTEXTO**:
    - Remover: Atividades, Copiar p/ Localização, Marcas.
    - Ativar: Comandos Copiar/Mover Para.
  - **Reações do utilizador**: Verificar se está tudo desligado.

### Dolphin: Home Folder e Área de Trabalho
- Na Home Folder, apagar **Modelos** e **Público**.
- Arrastar **Lixo** para o Ambiente de Trabalho, criar também atalho para Dolphin e Terminal.
- Na Pasta Transferências > Hamburger > Mais > Ver > Tirar **MOSTRAR POR GRUPOS**.

### Dolphin: Pastas Pessoais
- Na pasta Home, arrastar **Docs**, **Imgs**, **Transf** e **Videos** para Acesso Rápido.
- Ir ao Disco "SNAKE 1TB" e Arrastar Docs, Imgs, Transf, etc, para a HOME.
- Escolher **CRIAR LIGAÇÃO** > Renomear para Documentos1 (por exemplo).
- Na Home Folder, apagar Docs, Imgs, Musica, Transf, e Videos originais.
- Remomear Documentos1 para Documentos e passam essas a ser as originais.

### Conta de Utilizador
- Iniciar > Clicar no User > Mudar Imagem e Password.

---

## Instalação de Aplicações

### Instalação de Apps Normais
- Abrir Terminal para instalar as seguintes apps:
  - `sudo pacman -S brave-bin cmatrix cpu-x discord dolphin-plugins flatpak ghostty gnome-calculator gnome-disk-utility htop keepassxc kio-admin kolourpaint libreoffice-still-pt librewolf-bin localsend ntfs-3g obs-studio obs-studio-browser openrgb protonup-qt qbittorrent vlc vlc-plugins-all xone-dkms-git xone-dongle-firmware yay youtube-music zsh`.

### Dependências para Discover Overlay
- `sudo pacman -S gtk-layer-shell libappindicator-gtk3 python-gobject`.

### Outras Opcionais
- `sudo pacman -S audacious audacity gparted ifuse onlyoffice-bin partitionmanager plasma-workspace-wallpapers plasma-x11-session yazi`.

### Remover
- `sudo pacman -R cachy-browser kwalletmanager micro cachyos-micro-settings`.

### Apps do AUR
- `yay -S discover-overlay pcloud-drive rivalcfg stacer-bin ttf-ms-win10-auto vlc-pause-click-plugin`.
  - (Instalar as restantes fonts (pCloud) em Gestão dos Tipos de Letra).
  - (`sudo pacman -Qm` revela todos os pacotes AUR instalados).

### CachyOS Hello - Apps/Tweaks
- Instalar **Gaming Packages** (Steam, Lutris, Goverlay, Heroic, etc.).
- Abrir o Heroic normal e mudar a cor, para não confundir com a versão FLATPAK que vai ser instalada a seguir (FLATPAK é a melhor versão deste launcher).

### Apps do Flatpak (https://flathub.org/)
- `flatpak install heroicgameslauncher spotify vesktop warehouse`.

---

## Configuração de Aplicações

### Konsole (Terminal)
- Colar o ficheiro **TokyoNightV2.colorscheme** (pCloud) em `~/.local/share/konsole/`.
- Hamburger > Configurar Barra de Ferramentas > Tirar os 2 Vistos.
- Abrir Config: Botão direito > Menu > Config > Config Konsole ou `CTRL+Shift+,`.
- **Perfis** > Novo:
  - **Geral**: Nome "Rice" > Perfil Por Omissão > Comando: `/bin/zsh`.
  - **Aparência**: TokyoNightV2 > MesloLGS Nerd Font > Tamanho 11 ou 12.
  - **Aparência** > Cursor > Escolher Traço-I e Ativar Intermitência.
  - **Rato** > Interação com Texto: Ativar "Copiar ao Selecionar" e "Desativar Texto como HTML".
  - **Rato** > Diversos: Ativar "Abrir Ficheiros/Ligações com click".
- Novas Tabs: `CTRL+SHIFT+T`.
- Pesquisar: `CTRL+SHIFT+F`.
- Limpar: `CTRL+L`.

### Fastfetch
- Para ter um tema diferente do fastfetch, colar o ficheiro **"config.jsonc"** (na pasta pCloud) para `~/.config/fastfetch`.

### ZSH Shell
- Por defeito o CachyOS usa a Fish Shell, que não segue o Standard POSIX, ou seja, alguns comandos para a programação são diferentes. Daí instalar a ZHS Shell e usá-la como default.
- Fazer a config na shell conforme as instruções.
- Para reconfigurar, escrever: `p10k configure`.
- Editar o ficheiro `~/.zshrc`.
  - Escrever `fastfetch` na 1ª linha.
  - E na última escrever: `alias git='LANG=en_US git'`.

### Alacritty (Outro Terminal)
- O Alacritty vem pré-instalado no CachyOS, não convém desinstalar, pois algumas das funcionalidades do Cachy Hello usam esse terminal.
- Copiar config (pCloud) para: `/home/darkouto/.config/alacritty/`.

### NumLock ligado no SDDM (Ecrã de Autenticação)
- Copiar o ficheiro **"kcminputrc"** (pCloud) para: `/var/lib/sddm/.config/`.
- (Requer `kio-admin` para abrir pasta como Administrador).

### Print Screen / Spectacle
- Carregar no PrintScreen > Configurar.
  - **Image Saving**: Escolher Área de Trabalho e Formato JPG.
  - **Video Saving**: Escolher Área de Trabalho e Formato MP4.
- Ativar: Sair após gravar.

### GnewView (Imagens)
- Hamburger > Configurar > Configurar GwenView.
  - **Geral**: Desativar Mostrar Vídeos.
  - **Vista de Imagem**: Roda do Rato: Ampliação > Animações: Nenhuma.
  - **Avançado**: Desativar Histórico de URL.

### OpenRGB
- Abrir OpenRGB, criar um perfil qualquer só para criar a pasta de config.
- Copiar o ficheiro **RedFix.orp** (pCloud) para `~/.config/OpenRGB`.
- Copiar o ficheiro **RedFix.sh** para GITs, e acrescentar ao arranque.
- A motherboard só tem 1 stripe de cor, vermelho static, aplica à board e ventoinha ASUS.
- O rato é breathing, vermelho.
- Em ambos fazer "Save to Device" e talvez não seja preciso carregar o ficheiro RedFix.

### LocalSend
- Mudar nome do Servidor para nome da máquina.
- Mudar pasta das descargas para `home/darkouto/LocalSend`.
- Nessa pasta usar o ícone da FOLDER-AppImage.
- Para funcionar entre PC's no CachyOS é preciso desativar a firewall:
  - `sudo ufw disable`.
  - (enviar ficheiros).
  - `sudo ufw enable`.

### VLC Media Player
- Ferramentas > Preferências > Mostrar Definições: Simples.
  - **Interface**: Continuar Reprod: Nunca > Guardar Items Recentes: Desativar.
  - **Legendas/OSD**: Mostrar Título: Desativar > Tipo de Letra: Arial.
  - **Entrada/Codecs**: Descod. Aceleração de Hardware: DESATIVAR.
- Ferramentas > Preferências > Mostrar Definições: TUDO.
  - "Negrito" > Ativar FORÇAR Negrito.
  - Recuo/Avanço Curto: 5 Segundos.
  - Interfaces de Controlo: `pause_click`.
  - Vídeo > Filtros: `pause_click`.
- `+` e `-` no NumPad ajusta a velocidade do vídeo.
- `G` e `H` ajusta o tempo das legendas.
- [https://subtitletools.com/subtitle-sync-shifter](https://subtitletools.com/subtitle-sync-shifter)

---

## Outras Configurações

### Caso o Disco Windows 10 / NTFS3 não abra
- Escrever no Terminal:
  `sudo bash -c 'echo "blacklist ntfs3" > /etc/modprobe.d/disable-ntfs3.conf'`.
- Reiniciar.

### Montar Discos Automaticamente
- Abrir `gnome-disk-utility` (Discos) > Selecionar a partição > Clicar no Play > Editar Montagem > Ativar 3 Vistos.

### Detetar Windows no GRUB
- No CachyOS por defeito não aparece a opção do Windows no Grub. Só aparece uma opção chamada UEFI FIRMWARE SETTINGS que abre a BIOS. Para ter a opção de Windows no Grub fazer o seguinte:
  - `sudo os-prober`: Isto procura os outros OS (e também verifica se o pacote está instalado).
  - Ir a `/etc/default/grub` > Tirar o comentário `#` de `GRUB_DISABLE_OS_PROBER=false`.
  - `sudo grub-mkconfig -o /boot/grub/grub.cfg`.

### Aumentar `vm.max_map_count` em Arch based
- Ir a: `/usr/lib/sysctl.d/10-arch.conf`.
- Meter o valor em `2147483642`.

### NVIDIA GSP Firmware
- Para verificar se está instalado ou não, escrever: `nvidia-smi -q`.
- E pesquisar (`CTRL+SHIFT+F`) por GSP. Se aparecer uma versão, está ativado, se aparecer N/A está desativado.
- Para desativar GSP na versão proprietary do driver nvidia, copiar o ficheiro **"nvidia-gsp.conf"** (pCloud) para `/etc/modprobe.d/nvidia-gsp.conf`.
  - (Lá tem o texto: `options nvidia NVreg_EnableGpuFirmware=0` onde **0** significa desativado, e **1** significa ativado).
- Escrever no terminal: `sudo mkinitcpio -P`.
- Reiniciar.

---

## Impressoras

### Em ambas é preciso instalar:
- `sudo pacman -S sane-airscan skanpage`.

### XEROX WORKCENTRE 6515
- Defs Impressora > Adicionar Impressora de Rede.
- Selecionar a que diz IPPS (nome mais comprido).
- A app de Scanner é o **SkanPage**.

### Scanner EPSON DS-730N
- Instalar Epson Scan (Flatpak): `flatpak install flathub net.epson.epsonscan2`.
- O Ip é: `192.168.1.73`.
- Nas Definições, no formato de ficheiro, escolher PDF e separar ficheiros.

---

### Cachy Hello - Apps/Tweaks
- Depois de tudo instalado clicar em **Remove Orphans** (remove dependências e pacotes desnecessários).
