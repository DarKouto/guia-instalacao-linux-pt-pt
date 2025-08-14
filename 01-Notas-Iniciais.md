# CachyOS: Notas e Configurações

---

## Notas Iniciais

- **CachyOS Linux** é baseado em Arch Linux e é uma Rolling Release (recebe updates constantemente). É basicamente um Arch Linux otimizado, com um instalador gráfico e um Kernel customizado para gaming e performance.

### Gestor de Pacotes `pacman`
- `sudo pacman -S htop cmatrix`: Sincroniza e instala pacotes.
- `sudo pacman -R neofetch`: Remove um pacote.
- `sudo pacman -Syu`: Atualiza o sistema.

### Gestor de Pacotes `yay`
- É uma alternativa mais completa que **não requer `sudo`** e também gere pacotes do **AUR** (Arch User Repository).
- `yay -S stacer-bin`: Instala pacotes do AUR.
- `yay -R neofetch`: Remove um pacote.
- `yay`: Atualiza o sistema.

### Instalação do CachyOS
- Usar o **Ventoy** para colocar a `.iso` numa PEN.
- Desativar o **Secure Boot**.
- Escolher a partição **GPT** (para PCs recentes) ou **MBR** (para PCs antigos).
- Na PEN, escolher a opção que diz **NVIDIA**.
- Na **Live USB**, ligar a Internet antes de iniciar a instalação.
- Escolher **GRUB** como Bootloader e instalar **Firefox** e **Printing Support**. Se a opção para a `shell` estiver disponível, escolher **ZSH**.
- Após a instalação, a primeira coisa a fazer é atualizar o sistema e reiniciar. O CachyOS faz isso na instalação.

---

## Troubleshooting

- **LED do Teclado (Gigabyte):**
  - No Windows, usar o Gigabyte Control Center > Teclado.
  - Desativar "Animação Inicial" para que a opção desejada fique sempre ativa.

- **Ícone das Pastas Errado:**
  - Configurações do Sistema > Aplicações Padrão > Associação de Ficheiros.
  - Em `inode > directory`, escolher `stock_folder`.

- **`7ZIP` / `P7ZIP`:**
  - Caso o ARK não abra ficheiros, é necessário o `p7zip`.
  - Abrir um terminal na pasta do ficheiro e usar: `7z x nomedoficheiro.zip`.

- **Black Screen no Login:**
  - Usar `CTRL + ALT + F3` para abrir o terminal.
  - Correr o comando `startplasma-wayland`.

- **Forçar Esvaziar Reciclagem:**
  - `sudo rm -rf ~/.local/share/Trash/*`

---

## Outras Informações Úteis

- `CTRL+H`: Revela ficheiros e pastas ocultos.
- `Super+ESC`: Abre o Monitor de Sistema.
- `F4`: Numa pasta no Dolphin, abre um terminal nessa localização.
- No terminal: usar a roda do rato para colar. `CTRL+C` termina o processo. `clear` ou `CTRL+L` limpa o terminal.
- `sudo`: Significa "Super User Do".
- `sudo -i`: Dá acesso root.
- `~` (til): Refere-se a `/home/NomeDoUtilizador/`.
- `./`: Executa um ficheiro na pasta atual.
- `ip a`: Para saber o IP local.
- `pactl info | grep "Server Name"`: Para saber se está a usar PulseAudio ou Pipewire.

### Montar Imagens `.iso`
- Instalar `dolphin-plugins`.
- Reiniciar o Dolphin.
- Clicar com o botão direito na `.iso` e escolher "Montar Imagem".

### Formatar PEN
- Usar o "Discos" (`gnome-disk-utility`).
- Selecionar a PEN e a Partição, clicar no ícone do play, e formatar a partição.
- **Não ativar "Apagar"**, que é para formatações completas.

### Mudar entre NVIDIA `open` / `proprietary`
- Para verificar o driver instalado: usar `fastfetch` ou `nvidia-smi`.
- Existem 2 pacotes no Octopi: `linux-cachyos-nvidia` (Proprietary) e `linux-cachyos-nvidia-open` (Open).
- Para mudar, basta instalar o que não está ativo. O sistema vai pedir para remover a versão atual.

### Instalar ficheiros `.run`
- Abrir um terminal na pasta do ficheiro.
- `chmod +x NomeDoFicheiro.run`
- `sudo LANG=C ./NomeDoFicheiro.run`

### Criar Shell Scripts
- Criar um novo ficheiro vazio com a extensão `.sh`.
- Tornar o ficheiro executável nas propriedades.
- Abrir o ficheiro e escrever no início: `#!/bin/fish` (ou `#!/bin/bash` / `#!/bin/zsh`).
- Por baixo, escrever os comandos.

### Instalar ficheiros `.deb` em distros Arch
- Instalar o `debtap`: `yay -S debtap`.
- Atualizar a base de dados: `sudo debtap -u`.
- Abrir um terminal na pasta do ficheiro `.deb` e correr:
  - `sudo debtap NomeDoFicheiro.deb`
  - `sudo pacman -U nomedonovoficheiro.pkg.tar.zst`

### Mudar Hostname (Nome do PC)
- `hostnamectl`: verifica o nome atual.
- `sudo hostnamectl set-hostname NOVO_NOME`: muda o nome.
- Abrir `/etc/hosts` e mudar o nome antigo para o novo.
- **Reiniciar**.

### Verificar Info Gráfica
- `glxinfo | grep -i vendor`: verifica a gráfica ativa.
- `nvidia-smi`: verifica o driver da gráfica.

### Verificar SWAP
- `swapon`

### Desativar Composição de Janelas (só X11)
- `SHIFT + ALT + F12`: ativa/desativa o compositor manualmente. Desligar o compositor pode dar um ganho de cerca de 10 FPS em jogos pesados.
