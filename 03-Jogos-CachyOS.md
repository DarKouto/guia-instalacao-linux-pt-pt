# Jogos no CachyOS

---

## Gaming Linux
- O Gaming em Linux melhorou bastante desde que a Valve lançou o Steam Deck, que tem como sistema operativo o SteamOS (que é Linux).
- Para isso funcionar, a Valve desenvolveu uma "Camada de Compatibilidade" chamada **Proton** (uma espécie de tradutor Windows-Linux). Tem como base um software chamado WINE, que já existe há alguns anos e serve para suportar aplicações Windows em Linux, mas nos jogos sempre deixou algo a desejar.
- O Proton é necessário para todos os jogos, exceto os que têm uma versão nativa para Linux.
- Existem várias versões do Proton oficial e modificações como o **Proton-GE**.
- Regra geral, as melhores versões são o Proton-GE, Proton-CachyOS, Proton 10.0 e o Proton Experimental.
- Tanto o Proton-GE como o Proton-CachyOS contêm codecs para reproduzir cutscenes de alguns jogos. Algo que o Proton oficial da Valve não tem.
- No entanto, isto pode variar de jogo para jogo, há inclusivamente jogos que funcionam melhor com uma versão mais antiga do Proton.
  - **EXEMPLOS**:
    - O Dead Cells tem versão nativa (não precisa de Proton).
    - O Remnant: From The Ashes corre muito melhor com o Proton-GE.
    - O Wukong corre bem com o Proton Experimental (segundo relatos).
    - O WH40K só corre bem com o Proton 9.0.4.
    - O 20XX só abre se tiver uma versão do Proton oficial mais antiga (8.0).
- O ideal é testar o jogo com as várias versões, ou então procurar pelo jogo no site: [https://www.protondb.com/](https://www.protondb.com/) e ler os comentários do pessoal.

---

## Configuração de Jogos

### Game-Performance
- Na Steam usar `game-performance %command%`.
- Isto muda o power profile para performance, também pode ser feito manualmente.
- Para ativar nos outros launchers, ler o Wiki: [https://wiki.cachyos.org/configuration/gaming/#tab-panel-6](https://wiki.cachyos.org/configuration/gaming/#tab-panel-6).
- **NOTA**: não usar Feral GameMode, pois o CachyOS já tem Ananicy Cpp.

### MangoHud / GOVERLAY (MSI AFTERBURNER)
- Abrir Goverlay, mudar algumas definições e fazer Save, isto vai criar uma pasta de configuração (pode demorar, calma).
- Copiar o ficheiro **MangoHud.conf** (pCloud) para `/home/darkouto/.config/MangoHud/`.
- Para ter MangoHud escrever nas propriedades da Steam: `mangohud %command%`.
- Nos outros Launchers há opção de ativar sempre isto por defeito.
- Para Ligar/Desligar o Overlay, pressionar "Shift_Direito+F12".

### WINE
- `wine --version` (verificar a versão).
- Clicar 2x num ficheiro `.exe` para o instalar.
- Para Desinstalar programas, abrir Terminal e escrever:
  - `wine uninstaller`.
- A pasta de instalação está em `/home/darkouto/.wine`.
- Para usar MangoHud, abrir um Terminal na pasta do jogo e escrever por exemplo: `mangohud --dlsym wine SpaceMarine.exe`.
- Para instalar e jogar jogos `.exe`, é melhor usar o **Lutris**, pois torna tudo muito mais simples e com mais opções. Usar apenas Wine caso o Lutris não tenha suporte. Mais Info na parte LUTRIS.

### STEAM
- **USAR A VERSÃO RUNTIME**.
- **Definições**:
  - Compatibilidade > Usar Steam Play em todos os jogos com `proton-cachyos`.
  - Interface > Pág. Inicial: Biblicoteca > Desativar Aviso de Atualizações.
  - Downloads > Desativar pré-Shaders (apenas ativar caso o jogo corra mal).
- Instalar um jogo pequeno, ex: Half-Life.
- Ir às propriedades do jogo > Compatibilidade > Forçar > Selcionar Proton Experimental, e depois Proton 10.0 - Isto vai sacar e instalar estas versões, ficando também disponíveis nos outros launchers.
- Para Forçar a gráfica Dedicada na Steam, usar este comando nas propriedades:
  `__NV_PRIME_RENDER_OFFLOAD=1 __GLX_VENDOR_LIBRARY_NAME=nvidia __VK_LAYER_NV_optimus=NVIDIA_only %command%`.
- A pasta Steam está em: `~/.local/share/Steam/steamapps/` (JOGOS).
- E os saves estão em: `~/.local/share/Steam/steamapps/compatdata/` (PROCURAR DRIVE-C E PASTA APPDATA).
- `F12` Tira Screenshots.
- Para os ver ir a VER > Gravação de Jogos e Capturas.
- **Definições > Gravação de Jogos** > GRAVAR EM 2º PLANO.
  - Guardar os últimos "120" segundos como clipe > `ALT+S`.
  - Todos os Jogos > Duração: 5 Min > Alta Qualidade.
  - Pasta de Gravações > `/home/darkouto/Steam Records`.
  - Altura Máxima do Vídeo: 720p.
  - Gravar Som do Micro: Ativar.
  - (`LD_PRELOAD="" %command%` remove a possibilidade de gravar, usado no marvel rivals).

### Proton-GE / ProtonUp-QT / ProtonPlus
- O ProtonUp-QT é um GUI para instalar e gerir versões do Proton-GE.
- Selecionar a Steam, a versão Proton-GE desejada e instalar.
- Isto irá injetar essa versão do Proton-GE na Steam e nos outros Launchers.
- Basta sacar apenas Major Version mais recente, exemplo: 9-27 e a 10-04.
- No Heroic, convém ter sempre a versão 9 do Proton-GE, pois o comando xbox não funciona em alguns jogos com o GE-Proton-10-7.

### Proton-CachyOS
- Tem praticamente as mesmas funcionalidades que o Proton-GE, mas é atualizado automaticamente e tem algumas otimizações específicas para CachyOS.

### HEROIC (EPIC GAMES)
- Usar **FLATPAK** (não desinstalar a normal, porque quebra os Gaming Packages).
- Fazer Login na EPIC (para criar pasta config).
- Instalar as versões Flatpak do MangoHud:
  - `flatpak install org.freedesktop.Platform.VulkanLayer.MangoHud`
  - (instalar para USER, e ambas as versões 23 e 24).
- Abrir o Warehouse > HEROIC > Open User Data > `/config/MangoHud/` e colar o ficheiro **MangoHud.conf** da pasta pCloud (se a pasta MangoHud não existir, é só criar).
- **Settings > Game Defaults** > Wine > Version > Proton-GE-MAISRECENTE.
- **Settings > Game Defaults** > Other > Ativar Dedicated GPU e MangoHud.
- **Settings > Advanced** > Instalar EOS Overlay (para dar achievements).
- Nas Definições de cada jogo (depois de instalado) verificar se GameMode, Dedicated GPU, MangoHud e outras opções estão ativadas.
- Para colocar argumentos (exemplo língua em inglês), ir às defs de jogo, Advanced > Game Arguments > `-culture=en`.
- Os Saves que seriam da pasta AppData no Windows estão localizados em:
  `/home/darkouto/Games/Heroic/Prefixes/default/`.
- Aqui terá uma pasta com o nome do jogo, abrir essa pasta e ir a `/pfx/drive_c/users/steamuser/`.
- Depois depende do jogo, pode estar em AppData, Documentos, Saved Games, etc.
- Para usar Proton-CachyOS na versão Flapak do Heroic, usar o ProtonUp-QT para o injetar na app "Heroic Proton Flatpak" em vez de na Steam.
- Para adicionar os jogos semanais grátis, ir ao site da EPIC num browser.

### LUTRIS (Todos Outros Launchers e jogos .EXE)
- Hamburger > Prefs > Opções Globais >
  - Ativar GPU Dedicada, FPS Counter (MangoHud).
  - Desativar Feral GameMode (o CachyOS já tem Ananicy Cpp).
- Para Instalar Battle.net ir a: [https://lutris.net/games/battlenet/](https://lutris.net/games/battlenet/) e seguir a instruções. Exemplo: só fazer login no fim de tudo.
- Para funcionar usar Proton ou GE-Proton 10.
- Para Instalar jogos `.exe`, ir ao ícone do "+" (canto superior esquerdo) e selecionar "Install Windows Game from .exe" > Instalar com Wine normalmente.
- Botão Direito nos Launchers/Jogos > Browse Files (para ver pasta de jogo).
- Botão Direito nos Launchers/Jogos > Configure > Aqui dá para mudar versões do Proton e outras configurações de jogo.

### Discover Overlay
- Abrir Config > Voice > Escolher: Right e Top.
- Voice Advanced > Padding Vertical e Horizontal: 12, Show Names Font: 11 > Remover Square Avantar > Avatar Size: 30.
- Opacity 0,8.

### Vesktop (Flatpak)
- É um Discord 3rd Party. Usar apenas se Discord oficial não abrir nesse dia.

### OBS Studio / SteelSeries Moments
- Fazer a Configuração automática, escolher 60 FPS.
- O Vídeo deverá estar a 10.000 kbps e o Audio a 160 kbps.
- Adicionar "Captura de Ecrã (PipeWire)", pois tem melhor desempenho, mas captura todo o ecrã.
- Para Iniciar Stream é sempre preciso ir ao YouTube no Browser:
  - [https://www.youtube.com/live_dashboard](https://www.youtube.com/live_dashboard).
  - Inserir o título, descrição e o jogo na info.
- Mais info na imagem "OBS Config" na pCloud.
- Ficheiro > Definições > Saída > AVANÇADO > Repetições > 90s.
- Atalhos > Pesquisar por Guardar > Guardar Repetições > `ALT+X` (porque o `ALT+S` fecha a janela).
- Para Funcionar é preciso ter o OBS Aberto e clicar em "Iniciar Mem Repetição".
- EM PRINCÍPIO NA STEAM FUNCIONARÁ MELHOR, MAS SÃO PRECISOS MAIS TESTES.
- TESTAR TAMBÉM O GPU RECORDER COM INSTANT REPLAY 2 MIN.

---

## Emuladores

### SONIC 3 AIR
- Sacar Versão Tar.Gz da página oficial, extrair os ficheiros.
- Copiar o ficheiro da ROM que está no pCloud (manter nome ficheiro).
- Executar o ficheiro `sonic3air_linux`.
- Os Saves e Mods estão em: `/home/darkouto/.local/share/Sonic3AIR/`.
- Ir a Display e escolher filtro HQ3x.
- Ir a Audio e sacar OST Remastered.

### PLAYSTATION 1 / DUCKSTATION
- Usar versão Flatpak: [https://flathub.org/apps/org.duckstation.DuckStation](https://flathub.org/apps/org.duckstation.DuckStation).
- Criar Pasta `PSX` no `home/darkouto/Games` e meter lá a pasta `BIOS` e `cdimages`, criar uma pasta para cada jogo. Usar preferencialmente as versões USA, pois correm a 60Hz, e a BIOS é a versão USA.
- Os ficheiros têm que estar em `.iso`, se forem `.bin` têm que ter o `.cue`.
- View > Ativar "Toolbar" e "Lock Toolbar".
- Settings > Graphics > Internal Resolution > Meter **1080p** ou **720p**.
- Ativar FORCE NTSC Timings para Jogos PAL (EU).
- Se o comando não funcionar automaticamente, ir a Settings > Controller e configurar manualmente, a vibração é no Large e Small Motor.
- FullScreen é clicar 2x com o rato na tela, e para tirar igual.
- Carregar no `ESC` abre um menu de Save/Load States, Fast Forward, etc.
- Se algum jogo der erro de LibCrypt, ir ao ficheiro `PlayStation - SBI.7z` e procurar o `NomeDoJogo.SBI`, colar na pasta de jogo, e mudar o nome do `.iso` para o mesmo do `.SBI`.
