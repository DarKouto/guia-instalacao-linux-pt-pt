<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/02-Instalar-CachyOS.md">[02 - Instalar CachyOS]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/04-Aplicacoes-CachyOS.md">[04 - Aplicações CachyOS]</a>
</div>
---

# Configurar CachyOS e KDE Plasma

Agora que já temos o sistema operativo totalmente instalado e a funcionar, vamos proceder a algumas configurações simples e essenciais que melhoram a experiência.

**NOTA:** No KDE Plasma, o **Menu Iniciar** chama-se **Lançador de Aplicações**. No entanto, por uma questão de facilidade e hábito, vamos continuar a chamá-lo **Menu Iniciar** ao longo deste guia.

## 1. Janela CachyOS Hello
Esta janela abre automaticamente assim que entras no sistema.
- **Desativa** a opção **Launch at Start** (no canto inferior direito).
- Clica em **Apps/Tweaks**.
  - **Ativa** as opções **Ananicy Cpp** e **Bluetooth** (devem estar ativadas por defeito).
  - Clica no botão **Rank Mirrors** e espera que o processo termine. Isto serve para selecionar o servidor mais rápido para instalares software e atualizares o sistema.
- Fecha a janela.

## 2. Mudar o Tema Global
Isto é uma preferência pessoal, pois considero o tema oficial do CachyOS demasiado escuro.
- Vai ao **Menu Iniciar** e procura por **Tema Global** (**Global Theme**).
- Escolhe **Brisa ao Anoitecer**.
- **Ativa** as opções **Configuração da Aparência** e **Disposição da Área de Trabalho e das Janelas**.
- **Reinicia o PC** para que todas as alterações sejam aplicadas corretamente.

## 3. Desativar o KWallet
O **KWallet** é um gestor de passwords cuja utilidade é discutível para a maioria dos utilizadores. Além disso, a sua janela está sempre a aparecer, por isso é melhor desativá-lo.
- Vai ao **Menu Iniciar** e procura por **Carteira KDE** (**Wallet**), e faz estes 2 passos **pela ordem descrita**:
  1. **Desativa** o visto da opção **inferior**, clica em **Aplicar**
  2. **Desativa** o visto da opção **superior**, clica em **Aplicar**
- Fecha a janela. O KWallet já não te chateia mais.

## 4. Configurar o Dolphin (Gestor de Ficheiros)
O **Dolphin** é o gestor de ficheiros do KDE Plasma, semelhante ao **Explorador de Ficheiros** no Windows, mas muito mais poderoso. Vamos fazer uma ligeira configuração para melhorar a experiência.
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

## 5. Outras Configurações e Informações Úteis
- Vai ao **Menu Iniciar** e clica no teu nome, que aparece no canto superior esquerdo, isto abre o menu de **Conta de Utilizador**, aqui podes modificar a tua password, assim como a foto de perfil
- Vai ao **Menu Iniciar** e procura **Configuração do Sistema**, isto é semelhante ao **Painel de Controlo/Definições** do Windows, mas mais uma vez, muito mais poderoso. Aqui podes modificar as definições de Teclado, Rato, Som, Energia, etc ao teu gosto. Investiga e testa à vontade.
- Para adicionar um programa favorito (atalho) ao **Menu Iniciar** ou ao **Painel**, procuras o programa no **Iniciar**, clicas com o botão direito e escolhes **Adicionar aos Favoritos** (para Iniciar) ou **Fixar no Gestor de Tarefas** (para o Painel)
- Carregar na tecla **PrintScreen** abre automaticamente um programa chamado **Spectacle** que te permite fazer e editar capturas de ecrã rapidamente.

## 6. Aceder ao Disco Windows (NTFS)
Por vezes, o CachyOS não consegue abrir o Disco do Windows caso esteja no formato NTFS (que é o mais comum), caso isso aconteça:
- Vai ao **Menu Iniciar** e procura por **Konsole** (**Terminal**), copia os seguintes comandos para lá
- **NOTA:** para colar texto no terminal, **NÃO** podes fazer CTRL+C, em vez disso, clica no meio da roda do rato ou fazes **CTRL+SHIFT+V**
```bash
sudo pacman -S ntfs-3g
```
```bash
sudo bash -c 'echo "blacklist ntfs3" > /etc/modprobe.d/disable-ntfs3.conf'
```
- **Reinicia o PC.** Agora já podes aceder e ver o conteúdo dos discos NTFS do Windows.

## 7. Ativar o Menu de Seleção de SO no Arranque (Grub)
Caso o teu sistema operativo Windows não apareça no menu de arranque **Grub**, é necessário fazer o seguinte:

**NOTA:** Este é o passo mais complexo, mas se seguires o guia, nada tens a temer. **Tranquilo!**
- Vai ao **Menu Iniciar** e procura por **Konsole** (**Terminal**), copia os seguintes comandos para lá
- **NOTA:** para colar texto no terminal, **NÃO** podes fazer CTRL+C, em vez disso, clica no meio da roda do rato ou fazes **CTRL+SHIFT+V**
```bash
sudo os-prober
```
```bash
sudo nano /etc/default/grub
```
- Este segundo comando vai abrir um ficheiro de texto. Usa as setas do teclado para navegares para o fim da página.
- Quando encontrares a linha que diz `#GRUB_DISABLE_OS_PROBER=false`, remove o símbolo `#` que aparece antes do texto.
- Carrega em **CTRL+O** para gravar o ficheiro, **Enter** para confirmar e em **CTRL+X** para fechar e voltar ao terminal.
- **Finalmente** copia o seguinte código para o terminal:
```bash
sudo grub-mkconfig -o /boot/grub/grub.cfg
```
- **Reinicia o PC**. Agora já podes escolher qual o sistema operativo que queres usar quando o PC arranca. Viste? Não custou nada.
- "O Terminal é nosso amigo" - Linus Torvalds, provavelmente.
---
<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/02-Instalar-CachyOS.md">[02 - Instalar CachyOS]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/04-Aplicacoes-CachyOS.md">[04 - Aplicações CachyOS]</a>
</div>
