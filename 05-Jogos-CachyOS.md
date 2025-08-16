<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/04-Aplicacoes-CachyOS.md">[04 - Aplicacções CachyOS]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/06-Notas-Finais.md">[06 - Notas Finais]</a>
</div>
<hr>

# Jogos no CachyOS

O Gaming em Linux melhorou de forma muito significativa nos últimos anos, ao ponto de que actualmente é possível jogar *quase* 100% dos jogos disponíveis para Windows. Esta melhoria deve-se muito à **Valve** e ao lançamento do seu **Steam Deck**, que tem como sistema operativo o **SteamOS** (que é Linux). Para isso funcionar, a Valve desenvolveu uma *Camada de Compatibilidade* chamada **Proton**, que **NÃO É UM EMULADOR**, mas sim uma espécie de tradutor Windows-Linux. O **Proton** tem como base um software chamado **WINE**, que já existe há alguns anos e serve para suportar aplicações Windows em Linux.

O Proton é necessário para todos os jogos, exceto aqueles que têm uma versão nativa para Linux.
Existem várias versões do Proton oficial da Valve e modificações como o **Proton-GE** ou o **Proton-CachyOS**.
- Regra geral, as melhores versões são o Proton-GE, Proton-CachyOS, Proton 10.0 e o Proton Experimental.
- Tanto o Proton-GE como o Proton-CachyOS contêm codecs para reproduzir cutscenes de alguns jogos. Algo que o Proton oficial da Valve não tem.
- No entanto, isto pode variar de jogo para jogo, há inclusivamente jogos que funcionam melhor com uma versão mais antiga do Proton.
  - **EXEMPLOS**:
    - O Dead Cells tem versão nativa (não precisa de Proton).
    - O Remnant: From The Ashes corre muito melhor com o Proton-GE.
    - O Wukong corre bem com o Proton Experimental (segundo relatos).
    - O WH40K só corre bem com o Proton 9.0.4.
    - O 20XX só abre se tiver uma versão do Proton oficial mais antiga (8.0).
- O ideal é testar o jogo com as várias versões, ou então procurar pelo jogo no site: [https://www.protondb.com/](https://www.protondb.com/) e ler os comentários do pessoal.

## Configuração de Jogos

### Game-Performance
- Na Steam usar `game-performance %command%`.
- Isto muda o power profile para performance, também pode ser feito manualmente.

<hr>
<div align="left">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/04-Aplicacoes-CachyOS.md">[04 - Aplicacções CachyOS]</a>
</div>
<div align="right">
  <a href="https://github.com/DarKouto/guia-instalacao-linux-pt-pt/blob/main/06-Notas-Finais.md">[06 - Notas Finais]</a>
</div>
