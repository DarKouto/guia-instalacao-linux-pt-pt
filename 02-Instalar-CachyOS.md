# Instalação do Sistema Operativo CachyOS Linux

**NOTA:** Este guia irá instalar o CachyOS num sistema que já tenha Windows, ou seja, irás ficar com 2 sistemas operativos a funcionar, e quando ligares o computador ele pergunta-te se queres arrancar para Linux ou para Windows, chama-se a isto **Dual-Boot**. Isto é o ideal, porque quem está a começar não tem se comprometer a usar apenas Linux. Caso queiras ignorar este passo, a instalação é ainda mais fácil, e essa informação estará disponível nessa parte.

## Requisitos:
- Internet
- Pen Drive USB (min. 4GB)
- Um computador (óbvio)

## Passos a Seguir
### 1. Transferir a imagem .iso do CachyOS
Este ficheiro é o Sistema Operativo propriamente dito.
- Vai a [https://cachyos.org/download](https://cachyos.org/download) e escolhe a Desktop Edtion. Qualquer método de Download é viável, mas eu costumo usar o Direct. Guarda o ficheiro no teu computador.

### 2. Transferir e instalar balenaEtcher
Este programa serve para injectar a imagem .iso do CachyOS na tua Pen Drive, existem outros, mas este é o mais simples de usar na minha opinião.
- Vai a [https://etcher.balena.io/](https://etcher.balena.io/) e clica no botão Download Etcher, seleciona o teu sistema operativo, transfere e instala o ficheiro.

### 3. Colocar a imagem .iso do CachyOS na Pen Drive com balenaEtcher
- **ATENÇÃO: Este passo irá apagar todos os dados que da tua Pen, por isso certifica-te que tens um backup**
- Conecta a tua Pen Drive ao PC, certifica-te que está detectada
- Abre o programa balenaEtcher que instalaste
- Clicas em **"Flash From File"** e selecionas o ficheiro .iso que transferiste do site do CachyOS
- Clicas em **"Select Target"**" e escolhes a tua Pen Drive
- Clicas em **"Flash"** e esperas que o processo termime.
- Reinicia o PC, mas mantém sempre a PEN ligada.

### 4. Configurar a BIOS
- **NOTA:** Este processo não é igual em todas as máquinas, pois todas as motherboards têm uma BIOS diferente
- Reinicia o computador e entra na **BIOS** (regra geral é ir carregando de forma intermitente na tecla DEL ou F12 assim que ligas o computador)
- Dentro da BIOS, procura pelas definições de **Fast Boot** e/ou **Secure Boot** e **desactiva-as**. Caso contrário o CachyOS pode não arrancar e ter outros problemas.
- Ainda dentro da BIOS, procura a definção de **Boot Order** ou **Boot Priority** e certifica-te que a Pen USB está em primeiro lugar. (Caso a tua BIOS tenha um selector de Boot no arraque, podes ignorar este passo)
- **Certifica-te que gravas as alterações ao sair da BIOS!**

### 5. Arrancar a partir da PEN no Live ISO CachyOS
- Se tudo correU bem, o teu PC irá agora arrancar através da PEN Drive.
- Irá aparecer um menu com várias opções, com o teclado usa as **Setas** para navegar e **Enter** para selecionar:
  - Se **NÃO** tiveres uma placa gráfica **Nvidia**, escolhes: **CachyOS**
  - Se **TIVERES** uma placa gráfica **Nvidia**, escolhes: **CachyOS with Nvidia Driver**
- Agora é só esperar que o processo acabe, e ficas a usar o CachyOS num formato Live USB. Isto permite-te experimentar o sistema todo sem qualquer compromisso de instalação.

### 6. Instalação do CachyOS
