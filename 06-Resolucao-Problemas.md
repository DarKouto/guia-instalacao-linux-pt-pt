<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/05-Jogos-CachyOS.md">[05 - Jogos CachyOS]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/07-Notas-Finais.md">[07 - Notas Finais]</a>
</div>
<hr>

# 🔨 Resolução de Problemas / Troubleshoot

## 🪟 Aceder ao Disco Windows (NTFS)
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
<img src="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/imagens/btrfs.jpg" width=600>

<hr>
<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/05-Jogos-CachyOS.md">[05 - Jogos CachyOS]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/07-Notas-Finais.md">[07 - Notas Finais]</a>
</div>
