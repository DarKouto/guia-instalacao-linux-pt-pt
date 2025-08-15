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
- **ATENÇÃO: Usar este processo irá apagar todos os dados que estejam previamente na tua Pen, por isso certifica-te que tens um backup**
- Conecta a tua Pen Drive ao PC, certifica-te que está detectada
- Abre o programa balenaEtcher que instalaste
- Clicas em **"Flash From File"** e selecionas o ficheiro .iso que transferiste do site do CachyOS
- Clicas em **"Select Target"**" e escolhes a tua Pen Drive
- Clicas em **"Flash"** e esperas que o processo termime.

### 4. Entrar na BIOS
- **NOTA:** Este processo não é igual em todas as máquinas, pois todas as motherboards têm uma BIOS diferente
- Reinicia o computador, e entra na BIOS. , mas regra geral é ir carregando de forma intermitente na tecla DEL ou F12 assim que ligas o computador.
- Assim que estiveres na BIOS, procura
