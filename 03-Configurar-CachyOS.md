<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/02-Instalar-CachyOS.md">[02 - Instalar CachyOS]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/04-Aplicacoes-CachyOS.md">[04 - Aplicações CachyOS]</a>
</div>
<hr>

# Configurar CachyOS e KDE Plasma

Agora que já temos o sistema operativo totalmente instalado e a funcionar, vamos proceder a algumas configurações simples e essenciais que melhoram a experiência.

**NOTA:** No KDE Plasma, o **Menu Iniciar** chama-se **Lançador de Aplicações**. No entanto, por uma questão de facilidade e hábito, vamos continuar a chamá-lo **Menu Iniciar** ao longo deste guia.

## 1. Janela CachyOS Hello
Esta janela abre automaticamente assim que entras no sistema.
- **Desativa** a opção **Launch at Start** (no canto inferior direito).
- Clica em **Apps/Tweaks**.
  - **Ativa** as opções **Ananicy Cpp**, **Bluetooth** e **Cachy Update**
- Fecha a janela.

## 2. Mudar o Tema Global
Isto é uma preferência pessoal, pois considero o tema oficial do CachyOS demasiado escuro.
- Vai ao **Menu Iniciar** e procura por **Tema Global** (**Global Theme**).
- Escolhe **Brisa ao Anoitecer**.
- **Ativa** as opções **Configuração da Aparência** e **Disposição da Área de Trabalho e das Janelas**.
- **Reinicia o PC** para que todas as alterações sejam aplicadas corretamente.

## 3. Desativar o KWallet
O **KWallet** é um gestor de passwords cuja utilidade é no mínimo discutível. Como tal o melhor é desativá-lo.
- Vai ao **Menu Iniciar** e procura por **Carteira KDE** (**Wallet**), e faz estes 2 passos **pela ordem descrita**:
  1. **Desativa** o visto da opção **inferior**, clica em **Aplicar**
  2. **Desativa** o visto da opção **superior**, clica em **Aplicar**
- Fecha a janela. O KWallet já não te chateia mais.

## 4. Configurar o Dolphin (Gestor de Ficheiros)
O **Dolphin** é o gestor de ficheiros do KDE Plasma, semelhante ao **Explorador de Ficheiros** no Windows ou **Finder** no MacOS, mas muito mais poderoso. Vamos fazer uma ligeira configuração para melhorar a experiência.
- Vai ao **Menu Iniciar** e procura por **Dolphin** (caso não esteja já afixado no Painel)
- No Dolphin, clica no **Menu Hamburger** (as 3 linhas horizontais no canto superior esquerdo), procura **Configurar** e depois seleciona **Configure Dolphin**.
- Na parte lateral de **Interface**:
  - No separador **Folders e Tabs** -> **Mostrar no Arraque**: Seleciona a 2º opção: `/home/OTeuUserName`
  - No separador **Antevisões** tem uma opção em baixo chamada **Remote Storage** -> Seleciona 15MB. Isto serve para mostrar antevisões de ficheiros em armazenamento de rede.
  - No separador **Confirmações** activa a primeira opção que diz **Ao enviar ficheiros ou pastas para o Lixo**
  - No separador **Status & Location Bar** seleciona **Full Width** e activa a opção **Mostrar barra de Ampliação**
- Na parte lateral de **View**:
  - No separador **General** -> Display Style: Selecionar **Recordar o estilo de apresentação de cada pasta**

Fecha o Dolphin e torna a abrir, vais reparar que na parte de baixo tem um "slider" que permite aumentar a ampliação das pastas, assim como uma barra que demostra o espaço livre em disco. Outra excelente funcionalidade é a existência de Tabs/Separadores como num browser de internet, se clicares numa pasta com o botão do meio do rato, ele abre essa pasta numa nova tab.

## 5. Snapshots / BTRFS Assistant
Sempre que instalas programas, atualizas o sistema ou mudas uma configuração importante, o CachyOS cria automaticamente um Snapshot/Ponto de Restauro, é como se fosse um *Save Point* de um jogo. Isto é extremamente útil caso surja algum problema que quebre o sistema.
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

## 6. Outras Configurações e Informações Úteis
- Vai ao **Menu Iniciar** e clica no teu nome, que aparece no canto superior esquerdo, isto abre o menu de **Conta de Utilizador**, aqui podes modificar a tua password, assim como a foto de perfil
- Vai ao **Menu Iniciar** e procura **Configuração do Sistema**, isto é semelhante ao **Painel de Controlo/Definições** do Windows, mas mais uma vez, muito mais poderoso. Aqui podes modificar as definições de Teclado, Rato, Som, Energia, etc ao teu gosto. Investiga e testa à vontade.
- Para adicionar um programa favorito (atalho) ao **Menu Iniciar** ou ao **Painel**, procuras o programa no **Iniciar**, clicas com o botão direito e escolhes **Adicionar aos Favoritos** (para Iniciar) ou **Fixar no Gestor de Tarefas** (para o Painel)
- Carregar na tecla **PrintScreen** abre automaticamente um programa chamado **Spectacle** que te permite fazer e editar capturas de ecrã rapidamente.

## 7. Aceder ao Disco Windows (NTFS)
Por vezes, o CachyOS não consegue abrir o Disco do Windows caso esteja no formato NTFS (que é o mais comum), caso isso aconteça:
- Vai ao **Menu Iniciar** e procura por **Konsole** (Terminal), copia os seguintes comandos para lá

**NOTA:** para colar texto na **Konsole**, **NÃO** podes fazer CTRL+C, em vez disso, clica no **botão do meio do rato** ou fazes **CTRL+SHIFT+V**
```bash
sudo pacman -S ntfs-3g
```
```bash
sudo bash -c 'echo "blacklist ntfs3" > /etc/modprobe.d/disable-ntfs3.conf'
```
- Reinicia o PC.

## 8. Mostrar a Opção do Windows no Menu de Arranque (GRUB)
Caso o teu sistema Windows não apareça no menu de arranque **Grub**, é necessário fazer o seguinte:
- Vai ao **Menu Iniciar** e procura por **Konsole** (Terminal), copia os seguintes comandos para lá

**NOTA:** para colar texto na **Konsole**, **NÃO** podes fazer CTRL+C, em vez disso, clica no **botão do meio do rato** ou fazes **CTRL+SHIFT+V**
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
<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/02-Instalar-CachyOS.md">[02 - Instalar CachyOS]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/04-Aplicacoes-CachyOS.md">[04 - Aplicações CachyOS]</a>
</div>
