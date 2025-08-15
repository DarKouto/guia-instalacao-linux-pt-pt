# Notas Iniciais

## O que é um Sistema Operativo Linux
- Tecnicamente falando, o Linux não é bem um sistema operativo, mas sim um Kernel (núcleo). O Kernel é o que faz a ponte entre o software e o hardware numa máquina. Foi desenvolvido por Linus Torvalds em 1991, e continua a ser actualizado e mantindo aos dias de hoje. Tem a particularidade de ser totalmente Open-Source (código aberto)
- Aquilo que chamámos um sistema operativo Linux, é na verdade uma combinação de várias coisas:
  - O Kernel Linux
  - As utilidades GNU (desenvolvidas por Richard Stallman)
  - O ambiente gráfico (Desktop Environment)
- Como tal é comum encontrar quem defenda que o termo mais correcto seria GNU/Linux. No entanto, por convenção social e simplicidade, acabou-se por chamar simplesmente Linux ao sistema operativo.

## Distribuições de Linux (Distros)
- Uma Distro de Linux, de forma muito simplificada. é um sistema operativo completo que conta com o Kernel Linux, utilidades GNU, pacotes de software e um ambiente gráfico (exemplos: KDE Plasma ou Gnome).
- À primeira vista parecem existir centenas de Distros Linux, mas na verdade, a maior parte delas são adaptações e modificações de outras distribuições. Como tal, considero existirem 3 grandes distribuições de Linux:
  1. Debian: é muito estável, mas apenas recebe actualizações de 2 em 2 anos.
  2. Arch: é muito leve e personalizável, que está constantemente a ser actualizada, modelo Rolling Release.
  3. Fedora: é um meio termo entre o Debian e o Arch, recebe grandes actualizções de 6 em 6 meses.
- A distribuição que uso que esta documentação aborda é o CachyOS, que é um fork do Arch Linux, que conta com algumas melhorias e adiçõe, como por exemplo um instalador gráfico, um kernel personalizado para performance e gaming, um conjunto de software pré-instalado, etc.

### Gestor de Pacotes `pacman`
- `sudo pacman -S htop cmatrix`: Instala pacotes.
- `sudo pacman -R neofetch`: Remove pacotes.
- `sudo pacman -Syu`: Atualiza o sistema.
- **-S** é Sync/Instalar, **-R** é Remove, **-Syu** é System Update.

### Gestor de Pacotes `YAY`
- Outro gestor de pacotes melhor é o **YAY**, que não requer sudo, e também gere e instala pacotes do AUR (Arch User Repository).
- `yay -S stacer-bin`: Instala pacotes do AUR.
- `yay -R neofetch`: Remove pacotes.
- Para atualizar o sistema basta escrever: `yay`.

### Instalação
- Usar Ventoy para colocar a .iso na PEN > Desativar Secure Boot > Escolher Partição GPT (PC's Recentes) ou MBR (PC's Antigos) > No final, basta colar a .iso na Partição chamada "VENTOY".
- Ao arrancar pela PEN, escolher a opção que diz NVIDIA.
- Na LIVE USB, ligar a NET, e só depois iniciar a instalação.
- Escolher GRUB como Bootloader, e instalar Firefox e Printing Support. (em teoria agora na instalação dá para selecionar shell do terminal, se der escolher a ZSH).
- A primeira coisa a fazer em qualquer Linux após a instalação é atualizar o sistema e reiniciar. No CachyOS já deve estar atualizado pois faz isso durante a instalação inicial.

---

## Troubleshooting

- **LED DO TECLADO (GIGABYTE):**
  - No Windows > Gigabyte Control Center > Teclado.
  - Escolher opção desejada e Desativar "Animação Inicial".
  - Assim fica sempre na opção ideal sem ter que iniciar o Windows.

- **ÍCONE DAS PASTAS ERRADO:**
  - Conf. Sistema > Default Applications > Associação de Ficheiros > inode > directory > ESCOLHER stock_folder.

- **7ZIP / P7ZIP:**
  - Caso o ARK não abra ficheiros é preciso usar o p7zip.
  - Abrir um terminal onde está o ficheiro e escrever: `7z x nomedf.zip`.

- **BLACK SCREEN NO LOGIN:**
  - `CTRL + ALT + F3` (abre terminal).
  - `startplasma-wayland`.

- **FORÇAR ESVAZIAR RECICLAGEM:**
  - `sudo rm -rf ~/.local/share/Trash/*`.

---

## Outras Informações

### Diversos
- `CTRL+H`: Revela ficheiros e pastas ocultos.
- `Super+ESC`: Abre o Monitor de Sistema.
- `F4`: Numa pasta no Dolphin abre um terminal lá.
- No terminal: usar a roda do rato para colar, `CTRL+C` termina o processo.
- `clear` no Terminal limpa tudo, ou então `CTRL+L`.
- `sudo`: Significa (Super User Do).
- `sudo -i`: Dá acesso root (ainda mais forte que admin).
- O `"~"` (til) significa `/home/NomeDoUtilizador/`.
- Usar `./` significa: na pasta onde estou, fazer X.
- Para saber o Local IP escrever: `ip a`.
- Para saber se estou a usar PulseAudio ou Pipewire escrever: `pactl info | grep "Server Name"`.

### Montar Imagens `.iso` / Daemon Tools
- É preciso ter o `dolphin-plugins` instalado.
- Reiniciar o Dolphin.
- Botão direito do rato na `.iso` e escolher "Montar Imagem".

### Formatar PEN
- Abrir discos (`gnome-disk-utility`) > Selecionar PEN e Partição.
- Clicar no Ícone do Play > Formatar Partição.
- Escolher Nome do Volume e formato de ficheiros.
- **NÃO ACTIVAR APAGAR**, isso é só para formatações completas!

### Mudar entre NVIDIA `open` / `proprietary` BLOB-MODULE
- Para verificar o que está instalado basta abrir o fastfetch (custom) e ler o que diz à frente de nvidia.
- Existem 2 pacotes no Octopi, e cada um corresponde a uma versão:
  - `linux-cachyos-nvidia` (PROPRIETARY)
  - `linux-cachyos-nvidia-open` (Open)
- Para mudar, basta selecionar o que não está instalado.
- Ele pede para abrir um novo terminal e remover a versão atual, aceitar.

### Abrir/Instalar Ficheiros `.run`
- Abrir um terminal na pasta do ficheiro.
- `chmod +x NomeDoFicheiro.run`.
- `sudo LANG=C ./NomeDoFicheiro.run`.

### Criar Shell Scripts (Comandos Terminal)
- Novo Ficheiro Vazio, gravar com extensão `.sh`.
- Propriedades do ficheiro, tornar executável.
- Abrir com Kate e escrever no início: `#!/bin/fish`.
- Em baixo escreve-se os comandos do Terminal. Caso a shell não seja o fish mudar o nome para bash ou zsh.

### Instalar Ficheiros `.deb` em distros Arch based (DEBTAP)
- `yay -S debtap`.
- `sudo debtap -u` (para atualizar base de dados).
- Abrir um terminal na pasta do ficheiro `.deb` e escrever:
  - `sudo debtap NomeDoFicheiro.deb`.
  - `sudo pacman -U nomedoNOVOficheiro.pkg.tar.zst`.

### Mudar Hostname (Nome do PC)
- `hostnamectl` (verifica o nome atual).
- `sudo hostnamectl set-hostname NEW_NAME` (muda para NEW_NAME).
- Abrir `/etc/hosts` (mudar o nome antigo para o novo, gravar).
- **REINICIAR**.

### Ver Info Gráfica
- `glxinfo | grep -i vendor` (verifica gráfica ativa).
- `nvidia-smi` (verificar driver gráfica).

### Verificar SWAP
- `swapon`.

### Desativar Composição de Janelas (só X11)
- A Composição/Efeitos das janelas são muito bonitos, mas podem afetar o desempenho de alguns jogos mais "pesados" no Linux.
- `SHIFT+ALT+F12` ativa/desativa o Compositor Manualmente.
- Costuma verificar-se um ganho médio de 10 FPS com o compositor desligado.
