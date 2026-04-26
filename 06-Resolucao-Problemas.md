<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/05-Jogos-CachyOS.md">[05 - Jogos CachyOS]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/07-Notas-Finais.md">[07 - Notas Finais]</a>
</div>
<hr>

# 🔨 Resolução de Problemas / Troubleshoot

Nesta área estão alguns dos problemas mais comuns que podem surgir, e a forma mais simples de os resolver.

## 🪟 Mostrar a Opção do Windows no Menu de Arranque (GRUB)
Caso o teu sistema Windows não apareça no menu de arranque **Grub**, é necessário fazer o seguinte:
- Vai ao **Menu Iniciar** e procura por **Konsole** (Terminal), copia os seguintes comandos para lá

**NOTA:** para colar texto na **Konsole**, **NÃO** podes fazer CTRL+C, em vez disso, clica no **botão direito do rato** e fazes colar, ou clicas **botão do meio do rato**, ou fazes **CTRL+SHIFT+V**
```bash
sudo os-prober
```
```bash
kate /etc/default/grub
```
- Este segundo comando vai abrir um ficheiro de texto no **Kate** (Bloco de Notas)
- Na parte final deste ficheiro, vais encontrar uma linha com o texto `#GRUB_DISABLE_OS_PROBER=false`, remove o símbolo `#` que aparece antes do texto.
- Grava o ficheiro e escreve a tua password quando pedir.
- **Finalmente** copia o seguinte comando para a **Konsole**:
```bash
sudo grub-mkconfig -o /boot/grub/grub.cfg
```
- **Reinicia o PC**. Agora já podes escolher qual o sistema operativo que queres usar quando o PC arranca.

<hr>

## 🪟 Aceder ao Disco Windows (NTFS) no CachyOS
Por vezes, o CachyOS não consegue abrir o Disco do Windows caso esteja no formato NTFS (que é o mais comum), caso isso aconteça:
- Vai ao **Menu Iniciar** e procura por **Konsole** (Terminal), copia os seguintes comandos para lá

**NOTA:** para colar texto na **Konsole**, **NÃO** podes fazer CTRL+C, em vez disso, clica no **botão direito do rato** e fazes colar, ou clicas **botão do meio do rato**, ou fazes **CTRL+SHIFT+V**
```bash
sudo pacman -S ntfs-3g
```
```bash
sudo bash -c 'echo "blacklist ntfs3" > /etc/modprobe.d/disable-ntfs3.conf'
```
- Reinicia o PC.

<hr>

## 📸 Snapshots / BTRFS Assistant
Sempre que instalas programas, atualizas o sistema ou mudas uma configuração importante, o CachyOS cria automaticamente um Snapshot/Ponto de Restauro, é como se fosse um *Save Point* de um jogo. Isto é útil caso surja algum problema que quebre o sistema.
Na improvável eventualidade de surgir algum problema fazes o seguinte:
- No Menu de Arranque (**GRUB**) seleciona a opção **CachyOS Snapshots**.
- Escolhe um Snapshot com uma data anterior a esse problema.

O sistema irá agora reiniciar com as configurações desse **Snapshot** numa espécie de "Modo de Segurança". Se estiver tudo OK, é preciso agora definir esse ponto como o arranque normal/oficial, para finalizar o processo:
 - Vai ao **Menu Iniciar** e procura por **BTRFS Assistant**
 - Escolhe o separador **Snapper**
 - Seleciona o separador **Browse/Restore**
 - Seleciona o mesmo Snapshot que selecionaste no **GRUB**
 - Clica no botão **Restore**. (opcional: escolhe um nome para esse backup)
 - Reinicia o PC.
<img src="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/imagens/btrfs-assistant.jpg" width=700>

<hr>

## 🔐 Remover Erro db.lock do pacman
Caso tenhas que usar os **SnapShots** ou aconteça algum erro durante a instalação de um programa ou atualização do sistema, o pacman cria uma salvaguarda chamada "db.lock" que bloqueia todo o gestor de pacotes. Para resolver esse problema segues os seguintes passos:
- Vai a Iniciar e procura por **Shelly**
- Clica em **Settings**
- Clica no botão **Remove db.lock**

<hr>
<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/05-Jogos-CachyOS.md">[05 - Jogos CachyOS]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/07-Notas-Finais.md">[07 - Notas Finais]</a>
</div>
