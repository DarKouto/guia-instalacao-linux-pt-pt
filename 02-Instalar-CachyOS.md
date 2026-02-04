<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/01-Notas-Iniciais.md">[01 - Notas Iniciais]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/03-Configurar-CachyOS.md">[03 - Configurar CachyOS]</a>
</div>
<hr>

# Instalação do Sistema Operativo CachyOS Linux

**NOTA:** Este guia irá instalar o **CachyOS** num sistema que já tenha Windows. Assim, irás ficar com dois sistemas operativos a funcionar, e no arranque do computador podes escolher se queres arrancar para **Linux** ou para **Windows**, num processo que se chama **Dual-Boot**. Esta opção é ideal para quem está a começar e não se quer comprometer a usar apenas Linux. Caso queiras ignorar este passo, a instalação será ainda mais simples.

## Passos a Seguir
### 1. Transferir a imagem .iso do CachyOS
Este ficheiro é o Sistema Operativo propriamente dito.
- Vai a [https://cachyos.org/download](https://cachyos.org/download) e escolhe a **Desktop Edition**. Qualquer método de Download é viável, mas eu costumo usar o Direct. Guarda o ficheiro no teu computador.

### 2. "Gravar" a imagem .iso numa Pen Drive USB
Se já instalaste sistemas operativos, certamente já estarás familizarizado com este processo. Precisas de um programa para "gravar" a imagem .iso do **CachyOS** na tua Pen Drive. Escolhe aquele que preferires, mas os mais populares são:
- **balena Etcher** [https://etcher.balena.io/](https://etcher.balena.io/)
- **Ventoy** [https://www.ventoy.net/](https://www.ventoy.net/)
- **Rufus** [https://rufus.ie/](https://rufus.ie/)

Após este processo estar concluído, reinicia o PC com a Pen Drive conectada.

### 3. Configurar a BIOS
**NOTA:** Este processo não é igual em todas as máquinas, pois as BIOS das motherboards são todas diferentes.
- Reinicia o computador e entra na **BIOS** (regra geral é preciso carregar na tecla **DEL** ou **F12**).
- Dentro da **BIOS**, procura as definições de **Fast Boot**/**Secure Boot** ou semelhantes e desativa-as. Geralmente as Distros de Linux têm problemas com Secure Boots.
- Ainda dentro da **BIOS**, procura por **Boot Order**/**Boot Priority** ou semelhantes e certifica-te de que a tua **Pen Drive USB** está em primeiro lugar. (Caso a tua **BIOS** tenha um seletor de arranque, podes ignorar este passo).
- **Certifica-te de que gravas as alterações ao sair da BIOS!**

### 4. Arrancar a partir da Pen no Live ISO do CachyOS
- Se tudo correu bem, o teu PC irá agora arrancar através da **Pen Drive**.
- Irá aparecer um menu com várias opções, escolhe a primeira que diz **CachyOS** com a tecla ENTER.
- Agora é só esperar que o processo termine.

### 5. Instalação do CachyOS
- Agora o **CachyOS** está oficialmente a correr em fomato **Live USB**. Isto permite-te experimentar todo o sistema sem qualquer compromisso de instalação.
- Uma janela chamada **CachyOS Hello** estará aberta por defeito, clica no botão **Launch Installer**.
- Vai-te aparecer um instalador gráfico chamado **Calamares**, e é aqui que vais proceder a toda a instalação.
**NOTA:** Antes de iniciares a instalação, certifica-te de que tens a internet ligada, é possível que em alguns portáteis mais antigos o Wi-Fi não funcione de imediato, se isso acontecer tenta ligar um cabo Ethernet, que o **CachyOS** consegue logo instalar driver do Wi-Fi.

Eis o que escolher em cada um dos separadores:
- **Bootloader**: escolhes o **GRUB**, é o padrão, funciona bem e não há nada a apontar.
- **Location**: escolhes a tua localização e língua (com a internet ligada é automaticamente detectada)
- **Keyboard**: escolhes o esquema do teclado (caso tenhas um teclado noutra língua)
- **Partitions**, escolhes em cima o Disco onde queres instalar o CachyOS (caso tenhas mais que um), e como o queres particionar:
  - Caso vás usar Dual-Boot (Recomendado para iniciantes), escolhes **Instalar Paralelamente**. Em baixo, clicas na partição **Actual** (colorida), na partição **Depois** usas o "slider" para definir o tamanho da partição do CachyOS
    - Caso tenhas um 2º Disco, ou queiras usar somente CachyOS, selecionas a opção **Apagar Disco**. E fazes seguinte. Fácil.

- **Desktop**: escolhe **Plasma Desktop**, também conhecido como **KDE Plasma**. É o DE com o qual iremos trabalhar neste guia. E porque é o melhor na minha opinião.
- **Packages**: por norma, apenas precisas de selecionar **Printing Support** (caso tenhas impressora) e também **HP Printer/Scanner support** (caso o fabricante seja a **HP**).
- **Users**: escolhes o teu nome de utilizador, password, e nome do PC.
    - **Nome Completo** escreves o teu primeiro e último nome. Ou só o primeiro. Como preferires.
    - **Nome de Utilizador** escreves o teu *username*, tudo com **letras minúsculas** e **sem espaços**.
    - **Nome do Computador**: escreves o nome que queres dar à tua máquina, uma boa prática é chamares: `oteuusername-cachyos`
    - **Password**: escreves a tua password, tem que ter no mínimo 6 caracteres, e pode ser mudada à posterior.
    - Finalmente **Activas** a caixa que diz: **Usar a mesma password para conta de administrador**
- O **Calamares** irá agora mostrar-te um sumário de todas as tuas opções de instalação. Verifica se está tudo correcto, e se estiver, avanças para a instalação.
- Assim que o processo estiver concluído reinicia o PC.
- Ao reiniciar, abre novamente a **BIOS** e no menu **Boot Priority** (ou semelhante), certifica-te que a 1ª opção é a partição do **CachyOS**. Grava as alterações e sai da BIOS.

**NOTA:** é possível que nesta fase inicial não te apareça a opção para selecionar o Windows no **GRUB** assim que ligas o PC. É normal, já vamos resolver disso no próximo capítulo.
 
<div align="center">
  <h1>
    Parabéns! Conseguiste instalar com sucesso o CachyOS 🐧<br>Bem-vindo ao Linux 🐧
  </h1>
</div>

<hr>
<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/01-Notas-Iniciais.md">[01 - Notas Iniciais]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/03-Configurar-CachyOS.md">[03 - Configurar CachyOS]</a>
</div>
