# Configurar CachyOS, KDE Plasma e Instalar Aplicações Essenciais

Agora que já temos o sistema operativo totalmente instalado e a funcionar, vamos proceder a algumas configurações simples e essenciais que melhoraram a experiência.

**NOTA:** O **Menu Iniciar** no KDE Plasma chama-se **Lançador de Aplicações**, mas por uma questão de semelhança, facilidade e hábito, vamos chamar-lhe na mesma **Menu Iniciar**

## 1. CachyOS Hello
Esta janela abre assim que entras no sistema.
- **Desactiva** a opção que diz **Launch at Start** (no canto inferior direito)
- Clica no botão que diz **Apps/Tweaks**
  - Activa as opções **Ananicy Cpp** e **Bluetooth** (já devem estar activadas por defeito)
  - Clica no botão que diz **Rank Mirrors** e deixa o processo concluir. Isto serve para selecionar o servidor mais rápido para instalares software e actualizares o sitema
- Fecha a janela.

## 2. Mudar o Tema Global
- Vai a **Iniciar**, procura por **Tema Global** (Global Theme)
- Escolhe **Brisa ao Anoitecer**.
- Activa as opções **Configuração da Aparência** e **Disposição da Área de Trabalho e das Janelas**
- Reinicia o PC.
- Isto é um caso de preferência pessoal, porque considero o tema oficial do CachyOS demasiado escuro e pequeno. Mas podes escolher o que quiseres.

## 3. Desactivar KWallet
O KWallet é uma aplicação de gestão de passwords, cuja utilidade é no mínimo "discutível", além de ser chata e estar sempre a aparecer. O ideal é desactivar.
- Vai a **Iniciar**, procura por **Carteira KDE** (Wallet)
- Desactivar o visto de baixo, fazer aplicar, e depois desactivar o visto de cima.
- Fechar a janela.

## 4. Activar o Menu de Seleção de OS no Arraque (Grub)
Este é o passo mais complexo, mas só tens que fazer uma vez, tranquilo.
- Vai a **Iniciar** e procura por **Konsole** (Terminal)
- Escreve os seguintes comandos por ordem:
  - sudo os-prober
  - sudo nano /etc/default/grub
    - Isto vai abrir um ficheiro de texto. Usa as setas do teclado para navegares para o fim da página.
    - Quando encontrares o texto **GRUB_DISABLE_OS_PROBER=false** remove o símbolo "#" que aparece antes do texto.
    - Carrega em **CTRL+O** para gravar o ficheiro, **Enter** para confirmar e em **CTRL+X** para fechar esta janela.
    - Agora estás de volta ao Terminal.
  - sudo grub-mkconfig -o /boot/grub/grub.cfg
 - Reinincia o PC. E agora já pode escolher qual OS queres usar.
