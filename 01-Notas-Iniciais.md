##########################
####  NOTAS INICIAIS  ####
##########################

 - CachyOS Linux é baseado em Arch Linux e é uma Rolling Release, ou seja,
   está constantemente a receber updates.
 - É basicamente um Arch Linux em esteróides, que tem um instalador gráfico
   e um Kernel customizado para gaming e performance, que é considerado um dos
   melhores Kernels da actualidade.

 - O gestor de pacotes é o pacman. Exemplos:
   - sudo pacman -S htop cmatrix
   - sudo pacman -R neofetch
   - sudo pacman -Syu
   - -S é Sync/Instalar, -R é Remove, -Syu é System Update

 - Outro gestor de pacotes melhor é o YAY, que não requer sudo, e também gere
   e instala pacotes do AUR (Arch User Repository). Exemplos:
   - yay -S stacer-bin
   - yay -R neofetch
   - Para actualizar o sistema basta escrever: yay

 - Usar Ventoy para colocar a .iso na PEN > Desactivar Secure Boot >
   Escolher Partição GPT (PC's Recentes) ou MBR (PC's Antigos) >
   No final, basta colar a .iso na Partição chamada "VENTOY"
 - Ao arrancar pela PEN, escolher a opção que diz NVIDIA
 - Na LIVE USB, ligar a NET, e só depois iniciar a instalação.
 - Escolher GRUB como Bootloader, e instalar Firefox e Printing Support.
   (em teoria agora na instalção dá para selecionar shell do terminal, se
   der escolher a ZSH)

 - A primeira coisa a fazer em qualquer Linux após a instalação é actualizar
   o sistema e reiniciar. No CachyOS já deve estar actualizado pois faz isso
   durante a instalação inicial.

------------------------------------------------
------------------------------------------------
------------------------------------------------
------------------------------------------------
------------------------------------------------

                 .88888888:.
                88888888.88888.
              .8888888888888888.
              888888888888888888
              88' _`88'_  `88888
              88 88 88 88  88888
              88_88_::_88_:88888
              88:::,::,:::::8888
              88`:::::::::'`8888
             .88  `::::'    8:88.
            8888            `8:888.
          .8888'             `888888.
         .8888:..  .::.  ...:'8888888:.
        .8888.'     :'     `'::`88:88888
       .8888        '         `.888:8888.
      888:8         .           888:88888
    .888:88        .:           888:88888:
    8888888.       ::           88:888888
    `.::.888.      ::          .88888888
   .::::::.888.    ::         :::`8888'.:.
  ::::::::::.888   '         .::::::::::::
  ::::::::::::.8    '      .:8::::::::::::.
 .::::::::::::::.        .:888:::::::::::::
 :::::::::::::::88:.__..:88888:::::::::::'
  `'.:::::::::::88888888888.88:::::::::'
        `':::_:' -- '' -'-' `':_::::'`

------------------------------------------------
------------------------------------------------
------------------------------------------------
------------------------------------------------
------------------------------------------------

#######################
#### TROUBLESHOOT  ####
#######################

LED DO TECLADO (GIBABYTE)
 - No Windows > Gigabyte Control Center > Teclado
 - Escolher opção desejada e Desactivar "Animação Inicial"
 - Assim fica sempre na opção ideal sem ter que iniciar o Windows

ÍCONE DAS PASTAS ERRADO:
 - Conf. Sitema > Default Applications > Associação de Ficheiros >
   inode > directory > ESCOLHER stock_folder

7ZIP / P7ZIP
 - Caso o ARK não abra ficheiros é preciso usar o p7zip
 - Abrir um terminal onde está o ficheiro e escrever: 7z x nomedf.zip

BLACK SCREEN NO LOGIN
 - CTRL + ALT + F3 (abre terminal)
 - startplasma-wayland

FORÇAR ESVAZIAR RECICLAGEM
 - sudo rm -rf ~/.local/share/Trash/*


#######################
####  OUTRAS INFOS ####
#######################

DIVERSOS:
 - CTRL+H Revela ficheiros e pastas ocultos
 - Super+ESC abre o Monitor de Sistema
 - F4 numa pasta no Dolphin abre um terminal lá
 - No terminal usar a roda do rato para colar, CTRL+C termina o processo
 - clear no Terminal limpa tudo, ou então CTRL+L
 - sudo significa (Super User Do)
 - sudo -i dá acesso root (ainda mais forte que admin)
 - O "~" (til) significa "/home/NomeDoUtilizador/"
 - Usar ./ significa: na pasta onde estou, fazer X
 - Para saber o Local IP escrever:
   - ip a
 - Para saber se estou a usar PulseAudio ou Pipewire escrever:
   - pactl info | grep "Server Name"

MONTAR IMAGENS .ISO / DAEMON TOOLS
 - É preciso ter o dolphin-plugins instalado
 - Reiniciar o Dolphin
 - Botão direito do rato na .iso e escolher "Montar Imagem"

FORMATAR PEN:
 - Abrir discos (gnome-disk-utility) > Selecionar PEN e Partição
 - Clicar no Ícone do Play > Formatar Partição
 - Escolher Nome do Volume e formato de ficheiros
 - NÃO ACTIVAR APAGAR, isso é só para formatações completas!

MUDAR ENTRE NVIDIA OPEN / PROPRIETARY BLOB-MODULE
 - Para verificar o que está instalado basta abrir o fastfetch (custom)
   e ler o que diz à frente de nvidia
 - Existem 2 pacotes no Octopi, e cada um corresponde a uma versão:
     - linux-cachyos-nvidia (PROPRIETARY)
     - linux-cachyos-nvidia-open (Open)
 - Para mudar, basta selecionar o que não está instalado.
 - Ele pede para abrir um novo terminal e remover a versão actual, aceitar.

ABRIR/INSTALAR FICHEIROS .RUN
 - Abrir um terminal na pasta do ficheiro
 - chmod +x NomeDoFicheiro.run
 - sudo LANG=C ./NomeDoFicheiro.run

CRIAR SHELL SCRIPTS (COMANDOS TERMINAL)
 - Novo Ficheiro Vazio, gravar com extensão .sh
 - Propriedades do ficheiro, tornar executável
 - Abrir com Kate e escrever no ínicio:
     #!/bin/fish
 - Em baixo escreve-se os comandos do Terminal. Caso a shell não seja o fish
   mudar o nome para bash ou zsh

INSTALAR FICHEIROS .DEB EM DISTROS ARCH BASED (DEBTAP):
 - yay -S debtap
 - sudo debtap -u
   (para actualizar base de dados)
 - Abrir um terminal na pasta do ficheiro .deb e escrever:
   - sudo debtap NomeDoFicheiro.deb
   - sudo pacman -U nomedoNOVOficheiro.pkg.tar.zst

MUDAR HOSTNAME (NOME DO PC)
 - hostnamectl
   (verifica o nome actual)
 - sudo hostnamectl set-hostname NEW_NAME
   (muda para NEW_NAME)
 - Abrir /etc/hosts
   (mudar o nome antigo para o novo, gravar)
 - REINICIAR

VER INFO GRÁFICA:
 - glxinfo | grep -i vendor
   (verifica gráfica activa)
 - nvidia-smi
   (verificar driver gráfica)

VERIFICAR SWAP
 - swapon

DESACTIVAR COMPOSIÇÃO DE JANELAS (só X11):
 - A Composição/Efeitos das janelas são muito bonitos, mas podem afectar
   o desempenho de algums jogos mais "pesados" no Linux.
 - SHIFT+ALT+F12 Activa/Desactiva o Compositor Manualmente.
   Costuma verificar-se um ganho médio de 10 FPS com o compositor desligado.
