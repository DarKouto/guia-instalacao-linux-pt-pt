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
- O **Proton** oficial da Valve
- O **GE-Proton** desenvolvido pelo **GloriousEggRoll**
- O **Proton-CachyOS** desenvolvido pela equipa do CachyOS, e que já vem pré-instalado nesta distro.

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

O CachyOS vai agora instalar-te todos os Launchers (Steam, Heroic, Lutris), assim como outras librarias e dependências necessárias para jogares sem qualquer problema.

## 2. Steam
Se és Gamer certamente conheces a **Steam**, este é o nosso Launcher principal e aquele que usamos para instalar o **Proton** oficial da Valve.
- Vai a **Iniciar** e procura por **Steam (Runtime)** (não abras a versão Steam (Native) pois é mais pesada e desnecessária)
- Entra com a tua conta, e faz as tuas configurações habituais, como farias no Windows
- Vai a **Definições** e depois **Compatibilidade**
- Irás reparar que por defeito já aparece o **proton-cachyos** selecionado
- Clica nesse menu *dropdown* e seleciona as seguintes versões, uma de cada vez:
  - Proton Experimental
  - Proton 10.0-xxx
  - Proton 9.0.4
  - Proton 8.0-5
- De cada vez que selecionas uma versão, a Steam irá transferir e instalar essa versão.


<hr>
<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/04-Aplicacoes-CachyOS.md">[04 - Aplicacções CachyOS]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/06-Notas-Finais.md">[06 - Notas Finais]</a>
</div>
