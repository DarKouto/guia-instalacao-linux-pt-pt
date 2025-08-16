<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/01-Notas-Iniciais.md">[01 - Notas Iniciais]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/03-Configurar-CachyOS.md">[03 - Configurar CachyOS]</a>
</div>

# Instalação do Sistema Operativo CachyOS Linux

**NOTA:** Este guia irá instalar o **CachyOS** num sistema que já tenha Windows. Assim, irás ficar com dois sistemas operativos a funcionar, e no arranque do computador podes escolher se queres arrancar para **Linux** ou para **Windows**, num processo que se chama **Dual-Boot**. Esta opção é ideal para quem está a começar e não se quer comprometer a usar apenas Linux. Caso queiras ignorar este passo, a instalação será ainda mais simples.

## Requisitos
- Internet
- Pen Drive USB (mínimo 4 GB)
- Um computador

## Passos a Seguir
### 1. Transferir a imagem .iso do CachyOS
Este ficheiro é o Sistema Operativo propriamente dito.
- Vai a [https://cachyos.org/download](https://cachyos.org/download) e escolhe a **Desktop Edition**. Qualquer método de Download é viável, mas eu costumo usar o Direct. Guarda o ficheiro no teu computador.

### 2. Transferir e instalar o balenaEtcher
Este programa serve para "gravar" a imagem .iso do **CachyOS** na tua Pen Drive. Existem outros, mas este é o mais simples de usar na minha opinião.
- Vai a [https://etcher.balena.io/](https://etcher.balena.io/), seleciona o teu sistema operativo, transfere e instala o ficheiro.

### 3. Gravar a imagem .iso na Pen Drive com balenaEtcher
**ATENÇÃO:** Este passo irá apagar todos os dados que tens na tua **Pen Drive**, por isso certifica-te de que tens um backup.
- Conecta a tua Pen Drive ao PC e verifica se a mesma é detetada.
- Abre o programa **balenaEtcher**.
- Clica em **"Flash From File"** e seleciona o ficheiro `.iso` que transferiste do site do **CachyOS**.
- Clica em **"Select Target"** e escolhe a tua Pen Drive.
- Clica em **"Flash"** e espera que o processo termine.
- **Reinicia o PC, mas mantém a Pen sempre ligada.**

### 4. Configurar a BIOS
**NOTA:** Este processo não é igual em todas as máquinas, pois as BIOS das motherboards são todas diferentes.
- Reinicia o computador e entra na **BIOS** (regra geral é carregar de forma intermitente na tecla **DEL** ou **F12** assim que ligas o computador).
- Dentro da **BIOS**, procura as definições de **Fast Boot** e **Secure Boot** e desativa-as. Caso contrário, o **CachyOS** pode não arrancar ou ter outros problemas.
- Ainda dentro da **BIOS**, procura por **Boot Order** ou **Boot Priority** e certifica-te de que a tua **Pen Drive USB** está em primeiro lugar. (Caso a tua **BIOS** tenha um seletor de arranque, podes ignorar este passo).
- **Certifica-te de que gravas as alterações ao sair da BIOS!**

### 5. Arrancar a partir da Pen no Live ISO do CachyOS
- Se tudo correu bem, o teu PC irá agora arrancar através da **Pen Drive**.
- Irá aparecer um menu com várias opções, escolher a primeira que diz **CachyOS** com enter
- Agora é só esperar que o processo termine.

### 6. Instalação do CachyOS
- Agora o **CachyOS** está oficialmente a correr em fomato **Live USB**. Isto permite-te experimentar todo o sistema  sem qualquer compromisso de instalação.
- Uma janela chamada **CachyOS Hello** estára aberta por defeito no arraque. Aqui há um botão em baixo e ao centro com o texto **Launch Installer**.
- **NOTA:** Antes de clicares, certifica-te de que tens a internet ligada, é possível que em alguns portáteis mais antigos o Wi-Fi não funcione de imediato, se isso acontecer tenta ligar um cabo ethernet.
- Ao clicares em **Launch Installer**, o CachyOS vai abrir um instalador gráfico chamado **Calamares**, e é aqui que vais proceder a toda a instalação:
  - Quando perguntar o **Bootloader** que queres, escolhes o **GRUB**, é o padrão, funciona bem e não há nada a apontar.
  - No separador **Location**, escolhes a tua localização e língua (com a internet ligada é automaticamente detectada)
  - No separador **Keyboard**, escolhes o esquema do teclado (com a internet ligada é automaticamente detectada)
    
  - No separador **Partitions**, escolhes em cima o Disco onde queres instalar o CachyOS (caso tenhas mais que um), e como o queres particionar:
    - Caso vás usar Dual-Boot (Recomendado para iniciantes), escolhes **Instalar Paralelamente**. Em baixo, clicas na partição **Actual** (colorida), na partição **Depois** usas o "slider" para definir o tamanho da partição do CachyOS
    - Caso tenhas um 2º Disco, ou queiras usar somente CachyOS, selecionas a opção **Apagar Disco**. E fazes seguinte. Fácil.
   
  - No separador **Desktop**, escolhes o ambiente gráfico (o Desktop Environment - DE). Por defeito aparece o **Plasma Desktop** também conhecido como **KDE Plasma**. Escolhe esse pois é o DE com o qual iremos trabalhar. E porque é de longe o melhor na minha opinião.
  - No separador **Packages**, escolhes pacotes de software adicionais. Por norma, apenas precisas de selecionar **Printing Support**, e **HP Printer/Scanner support**, caso tenhas ou vás usar uma impressora HP.
  - No separador **Users**, escolhes o teu nome de utilizador, password, e nome do PC.
    - No **Nome Completo** escreves o teu primeiro e último nome
    - No **Nome de Utilizador** escreves um username, tudo com letras minúsculas e sem espaços
    - No **Nome do Computador**: escreves o nome que queres dar à tua máquina, uma boa prática é chamares: `oteuusername-cachyos`
    - Em **Password**: escreves a tua password, tem que ter no mínimo 6 caracteres, e pode ser mudada à posterior.
    - Finalmente **Activas** a caixa que diz: **Usar a mesma password para conta de administrador**
  - O **Calamares** irá agora mostrar-te um sumário de todas as tuas opções de instalação. Verifica se está tudo correcto, e se estiver, avanças para a instalação.
  - Assim que o processo estiver concluído reinicia o PC.
  - Ao reiniciar, abre novamente a **BIOS** e no menu **Boot Priority** (ou semelhante), certifica-te que a 1ª opção é a partição do **CachyOS**. Grava as alterações e sai da BIOS.
  - **NOTA:** é possível (e normal) que nesta fase inicial não te apareça o menu de selecção de sistema operativo ao ligares o PC. Mas calma, já vamos tratar disso no próximo capítulo.
 
## Parabéns! Conseguiste instalar com sucesso o CachyOS 🐧
## Bem-vindo ao Linux 🐧

<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/01-Notas-Iniciais.md">[01 - Notas Iniciais]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/03-Configurar-CachyOS.md">[03 - Configurar CachyOS]</a>
</div>
