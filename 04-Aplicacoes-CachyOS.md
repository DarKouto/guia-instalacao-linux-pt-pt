# Aplicações CachyOS

Está finalmente na hora de explicar quais sãos as aplicações pré-instaladas no CachyOS, e quais algumas aplicações essenciais recomendo instalar.

## Aplicações Pré-Instaladas e o seu Propósito
- **Kate**: editor de texto simples, ideal para tirar notas, semelhante ao **Bloco de Notas** ou **Notepad++**
- **GwenView**: visualizador de imagens, também permite rodar, recortar e inverter imagens, assim como ver vídeos.
- **Firefox**: é o browser que vem instalado por defeito. Recuso-me a acreditar que não saibas o que é o Firefox.

## Aplicações a Instalar dos Repositórios Oficiais
Existem duas formas de instalar aplicações dos repositórios oficiais do CachyOS:
1. Usar a **Konsole** (Terminal) com o gestor de pacotes do Arch chamado **pacman**, exemplo: `sudo pacman -S nome-do-pacote-a-instalar`
2. Ir ao **Iniciar** e procurar o **Octopi** que é um ambiente gráfico que ajuda a pesquisar, instalar ou remover pacotes dos repositórios oficiais.

Qual a melhor abordagem? Depende. Eis a minha opinião:
- Para instalar uma única aplicação, o **Octopi** é mais fácil e intuitivo, é simplesmente chegar lá, procurar, selecionar e instalar.
- Para instalar várias aplicações de uma só vez, usar o **Terminal** é melhor, pois com um único comando consegues instalar tudo ao mesmo tempo.

**NOTA:** para colar texto no terminal, **NÃO** podes fazer CTRL+C, em vez disso, clica no meio da roda do rato ou fazes **CTRL+SHIFT+V**
Cá fica o comando que instala as aplicações que considero essenciais:
```bash
sudo pacman -S brave-bin discord dolphin-plugins flatpak gnome-calculator kio-admin kolourpaint libreoffice-still-pt onlyoffice-bin protonup-qt qbittorrent vlc vlc-plugins-all yay zsh
```
