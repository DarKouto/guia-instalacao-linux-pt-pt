<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/04-Aplicacoes-CachyOS.md">[04 - Aplicacções CachyOS]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/06-Notas-Finais.md">[06 - Notas Finais]</a>
</div>
<hr>

# Jogos no CachyOS

O Gaming em Linux melhorou de forma muito significativa nos últimos anos, ao ponto de que actualmente é possível jogar *quase* 100% dos jogos disponíveis para Windows. Esta melhoria deve-se muito à **Valve** e ao lançamento do seu **Steam Deck**, que tem como sistema operativo o **SteamOS** (que é Linux). Para isso funcionar, a Valve desenvolveu uma *Camada de Compatibilidade* chamada **Proton**, que **NÃO É UM EMULADOR**, mas sim uma espécie de tradutor Windows-Linux. O **Proton** tem como base um software chamado **WINE**, que já existe há alguns anos e serve para suportar aplicações Windows em Linux.

O **Proton** é necessário para todos os jogos, exceto aqueles que têm uma versão nativa para Linux. As 3 versões do Proton que iremos usar são:
- O **Proton** oficial da Valve (que vamos instalar/actualizar através da Steam)
- O **GE-Proton** desenvolvido pelo **GloriousEggRoll** (que vamos instalar/actualizar através do ProtonUP-QT)
- O **Proton-CachyOS** desenvolvido pela equipa do CachyOS (já vem pré-instalado e é actualizado automaticamente ao actualizarmos o sistema)

**NOTA**: O **GE-Proton** e o **Proton-CachyOS** são modificações ao Proton oficial, que contam com algumas melhorias, como por exemplo a inclusão de **codecs de vídeo** proprietários que permitem ver as *cutscenes* de alguns jogos. Regra geral, usar estas versões é melhor que usar a versão original, mas nem sempre é o caso. A sua eficiência varia de jogo para jogo, como vamos ver nos seguintes exemplos:
- O *Dead Cells* tem versão nativa (não precisa de Proton).
- O *Remnant: From The Ashes* corre muito melhor com o **Proton-GE**.
- O *WH40K: Space Marine 2* só corre bem com o **Proton 9.0.4** (oficial).
- O **20XX** só abre com uma versão do **Proton** oficial mais mais antiga, como 8.0 ou inferior.

Para sabermos qual a melhor versão a usar, vamos ao site [https://www.protondb.com/](https://www.protondb.com/). Aqui encontramos os jogos, com relatos de utilizadores que indicam qual a versão Proton que utilizaram, e se foi necessário algum comando de lançamento. Atenção que isto não é a Verdade Universal, mas sim um guia de orientação que nos poupa muito trabalho em testes.

## 1. Instalar Gaming Packages
Vai a **Iniciar** e procura por **CachyOS Hello**
- Vai a **Apps/Tweaks**
- Clica em **Install Gaming Packages**

O CachyOS vai agora instalar-te todos os Launchers (Steam, Heroic, Lutris), assim como outros utilitários, librarias e dependências necessárias para jogares sem qualquer problema.

## 2. Steam
Se és Gamer certamente conheces a **Steam**, este é o nosso Launcher principal e aquele que usamos para instalar o **Proton** oficial da Valve.
- Vai a **Iniciar** e procura por **Steam (Runtime)** (não abras a versão Steam (Native) pois é mais pesada e desnecessária)
- Entra com a tua conta, e faz as tuas configurações habituais, como farias no Windows
- Vai a **Definições** e depois **Compatibilidade**
- Irás reparar que por defeito já aparece o **proton-cachyos** selecionado
- Clica nesse menu *dropdown* e seleciona as seguintes versões (de cada vez que selecionas uma versão, a Steam irá transferir e instalar essa versão, ficando também disponíveis nos outros Launchers):
  - Proton Experimental
  - Proton 10.0-*nr-mais-recente*
  - Proton 9.0.4
  - Proton 8.0-5
- Agora instala um jogo qualquer. Após conclusão, clicas com o **botão direito do rato** no jogo e vais a **Propriedades**:
  - No separador **Geral**, nas **Opções de Arranque** recomendo escrever: `game-performance mangohud %command%`
    - **game-performace** é um *daemon/serviço* que automaticamente coloca o teu PC em modo de Performance assim que abres um jogo, e que retorna ao normal assim que o fechas.
    - **MangoHud** é um overlay que conta os FPS, carga de CPU, GPU, Ram, etc. Semelhante ao **MSI Afterburner**. Podes fechar este overlay com **SHIFT+F12**
  - No separador **Compatibilidade**, podes activar a opção **Forçar uso de ferramenta específica** e isso permite-te selecionar a versão do **Proton** que queres usar. Se nada fizeres, a Steam automaticamente assume e aplica o **proton-cachyos**
 
## 3. ProtonUP-QT
O **ProtonUP-QT** é um ambiente gráfico que serve para instalar o **GE-Proton** (assim como outras modificações) nos nossos Launchers.
- Vai a **Iniciar** e procura **ProtonUP-QT**
- Clicas em **Adicionar Versão**
- Na **Ferramenta** escolhes **GE-Proton**
- Na **Versão** escolhes:
  - GE-Proton-10-*nr-mais-recente*, e clicas **Instalar**, e esperas que termine.
  - GE-Proton-9-27, e clicas **Instalar**, e esperas que termine.
  - Recomendo instalar a versão 10 e 9, pois alguns jogos ainda funcionam melhor com a versão 9.
- Isto vai injetar estas versões do **GE-Proton** na Steam e nos outros Launchers. Agora já o podes usar em qualquer jogo.
- Recomendo que abras este programa de vez em quando para verificares se há novas versões do Proton-GE, ou então segue o GloriousEggRoll em https://github.com/GloriousEggroll/proton-ge-custom/releases
- Ao instalares uma nova versão do **GE-Proton-10**, podes remover a antiga. Exemplo: se instalares o **Proton-GE-10-12** podes remover o Proton-GE-10-11 e inferiores.

## 4. Heroic Games Launcher (EPIC e GOG)
O **Heroic Games Launcher** é o Launcher preferencial para jogos da EPIC Games Store e GOG.
- Vai a **Iniciar** e procura por **Heroic**
- Vai ao separador **Stores**, e faz login com as tuas credenciais Epic e GOG
- Agora os teus jogos aparecem todos no separador **Library**
- Para instalar um jogo, basta clicar nele, e fazer **Install**, isto abre uma janela com várias definições:
  - Clica no *dropdown* com o texto **Show Wine Settings**
  - Aqui poderás selecionar a versão **Proton** que pretendes usar
- Após instalado, podes explorar outras definições de cada jogo, como comandos de lançamento.

### 4.1 Heroic Games Launcher (Flatpak)
Em alguns PC's, a versão oficial do **Heroic** pode ter alguns problemas de estabilidade. Caso isso suceda, temos que instalar a sua versão **Flatpak**, assim como a versão **Flatpak** do **MangoHud**.
- Abre o **Terminal** e escreve:
```bash
flatpak install com.heroicgameslauncher.hgl
```
```bash
flatpak install org.freedesktop.Platform.VulkanLayer.MangoHud
```
- Quando te perguntar que versão do MangoHud queres instalar, escolhe a 23 e a 24. Talvez tenhas que correr este comando 2 vezes para instalar as 2 versões.
De resto, o funcionamento da versão Flatpak é igual à versão normal.

## 5. Lutris (Todos os outros Launchers)
O Lutris serve para todos os outros Launchers, como a Battle.net, EA Games, Ubisoft, etc. Também permite instalar jogos locais.
- Vai a **Iniciar** e procura por **Lutris**
- Vai ao menu **Hamburger** (as 3 linhas horizontais no canto superior esquerdo) e clica em **Preferences**
- No separador **Global Options**
  - Activa **Advanced** na parte de cima
  - Activa **FPS Counter/MangoHud**
  - Desactiva **Feral GameMode** (o CachyOS tem o Ananicy Cpp que faz o mesmo efeito)
- Para instalar qualquer Launcher, basta clicar no seu ícone que aparece no separador esquerdo.
- Agora os teus Launchers e jogos aparecem no separador **Windows**
- Clica com o botão direito do rato no Launcher/Jogo instalado e escolhe **Configure**
  - No separador **Runner Options** onde diz **Wine Options** podes escolher a versão do Proton.

## 5.1 Battle.net no Lutris
O processo para instalar a **Battle.net** é ligeiramente diferente dos outros Launchers: 
- Vai ao site https://lutris.net/games/battlenet/ e clica no botão **Install**
- **Aceita** o pedido do teu browser para abrir a ligação no Lutris, e segue as intruções que te aparecem no ecrã:
  - Exemplo: da primeira vez que aparece a janela para fazer login, não faças nada, apenas fecha a janela.

**NOTA**: Para a Battle.net fucionar é necessário usar uma **versão 10 ou superior** do Proton, GE-Proton ou proton-cachyos.

<hr>
<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/04-Aplicacoes-CachyOS.md">[04 - Aplicacções CachyOS]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/06-Notas-Finais.md">[06 - Notas Finais]</a>
</div>
