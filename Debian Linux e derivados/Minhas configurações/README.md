# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi") / Minhas configurações

[![Programação](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Minhas%20configura%C3%A7%C3%B5es/images/programacao.png?raw=true "Programação")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Minhas%20configura%C3%A7%C3%B5es/images/programacao.png?raw=true "Programação")

- [Marcos Aurélio Rocha da Silva (programação)](#marcos-aur%C3%A9lio-rocha-da-silva-programa%C3%A7%C3%A3o "Marcos Aurélio Rocha da Silva (programação)")

> Instalação do Linux

- [Como Instalar o Debian Linux em uma Partição Específica sem Afetar Outras Partições](#como-instalar-o-debian-linux-em-uma-parti%C3%A7%C3%A3o-espec%C3%ADfica-sem-afetar-outras-parti%C3%A7%C3%B5es "Como Instalar o Debian Linux em uma Partição Específica sem Afetar Outras Partições")

> Outras instações e configurações

- [Instalações e configurações](#instala%C3%A7%C3%B5es-e-configura%C3%A7%C3%B5es "Instalações e configurações")
- [Nativos e outros](#nativos-e-outros "Nativos e outros")
- [Algumas ferramentas úteis](#algumas-ferramentas-%C3%BAteis "Algumas ferramentas úteis")
- [Internet](#internet "Internet")
- [Desenvolvimento](#desenvolvimento "Desenvolvimento")

---
# Marcos Aurélio Rocha da Silva (programação)

> O conteúdo abaixo, são as configurações do meu computador o qual utilizo para fazer meus trabalhos, meus projetos e meu companheiro de gerra. Nessas configurações, estou utilizando o `Debian Linux` com o ambiente `Cinnamon`, adotei como minha principal interface de usuário...

## Como Instalar o Debian Linux em uma Partição Específica sem Afetar Outras Partições

Você pode instalar o Debian Linux em uma partição específica do seu disco rígido (HDD) sem afetar as outras partições. Aqui estão os passos gerais que você pode seguir:

**Nota:** Antes de começar, é sempre uma boa prática fazer backup dos dados importantes nas partições existentes, pois qualquer operação de instalação de sistema operacional envolve riscos.

1. **Baixe a Imagem do Debian:** Primeiro, você precisa baixar a imagem ISO do Debian da versão que deseja instalar. Você pode obtê-la no site oficial do Debian.

2. **Crie um Pendrive de Instalação:** Grave a imagem ISO em um pendrive USB usando um programa como o Etcher ou o Rufus. Isso criará um pendrive de instalação inicializável.

3. **Inicie a Instalação:** Insira o pendrive de instalação no seu computador e inicie a partir dele. Você pode precisar alterar a ordem de inicialização no BIOS ou na UEFI para inicializar a partir do pendrive.

4. **Escolha a Partição:** Durante o processo de instalação, você será solicitado a escolher a partição onde deseja instalar o Debian. Selecione a partição desejada e siga as instruções na tela.

5. **Instalação Padrão ou Personalizada:** Você terá a opção de escolher uma instalação padrão ou personalizada. Se você deseja instalar apenas o sistema base do Debian, escolha a opção personalizada e selecione os pacotes que deseja instalar. Certifique-se de não formatar ou alterar as outras partições durante este processo.

6. **Configure o GRUB:** Durante a instalação, você será perguntado se deseja instalar o GRUB (carregador de inicialização). Se você tiver outros sistemas operacionais instalados no disco rígido e quiser iniciar o Debian a partir do GRUB, escolha a opção de instalação do GRUB. Caso contrário, você pode optar por não instalar o GRUB e configurar o carregador de inicialização posteriormente.

7. **Conclua a Instalação:** Continue seguindo as instruções na tela para concluir a instalação do Debian na partição selecionada.

8. **Configure o GRUB (Opcional):** Se você optou por não instalar o GRUB durante a instalação, precisará configurá-lo manualmente para incluir o Debian. Isso envolve a edição do arquivo de configuração do GRUB e a atualização do GRUB.

Após concluir essas etapas, o Debian Linux estará instalado na partição desejada do seu disco rígido, e as outras partições devem permanecer intactas. Certifique-se de fazer backup dos dados importantes e tome cuidado ao selecionar a partição durante a instalação para evitar a formatação acidental de outras partições.

## Instalações e configurações

> ( ! ) Essa configuração corresponde às preferências de `Marcos Aurélio`.

## Nativos e outros

| Software | Copyright | Instalação e/ou Configurações |
| :--: | :--: | ---- |
| Configuração da data na área de notificação | Nativo | Clique inverso na data / Configurar... / Ativar "Exibir números da semana no calendário" e "Usar um formato de data personalizado", formato da data: `%A, %e de %B de %Y, %H:%M:%S`. [![Data e hora do sistema](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Minhas%20configura%C3%A7%C3%B5es/images/Data_e_hora_do_sistema.png?raw=true "Data e hora do sistema")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Minhas%20configura%C3%A7%C3%B5es/images/Data_e_hora_do_sistema.png?raw=true "Data e hora do sistema") |
| Captura de tela | Nativo | Adicionar ao painel. |
| Monitor do sistema | Nativo | Adicionar ao painel. |
| Editor de texto | Nativo | Preferêncis: Esquema de cores (Olívio) \| Adicionar ao painel. |
| Typora | [Typora](https://typora.io/ "Download") | Temas: Night \| Adicionar à área de trabalho. |

Botões do Painel na barra inferior.

[![Botões do painel](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Minhas%20configura%C3%A7%C3%B5es/images/panel_buttons.png?raw=true "Botões do painel")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Minhas%20configura%C3%A7%C3%B5es/images/panel_buttons.png?raw=true "Botões do painel")

> ( ! ) Acima estão os botões por ordem na barra inferior!

## Algumas ferramentas úteis

| Software | Copyright | Instalação e/ou Configurações |
| :--: | :--: | ---- |
| GParted | Copyright © 2004-2006 Bart Hakvoort \| Copyright © 2008-2021 Curtis Gedak \| Copyright © 2011-2021 Mike Fleetwood | `apt update && apt install gparted` |
| Virtual Box | [Oracle](https://www.oracle.com/ "Oracle - Cloud Applications and Cloud Platform") |  |

## Internet

| Software | Copyright | Instalação e/ou Configurações |
| :--: | :--: | ---- |
| AnyDesk | [AnyDesk Software GmbH](https://anydesk.com/pt "Download") | Adicionar à área de trabalho. |
| Mozilla Firefox | [mozilla.org](https://www.mozilla.org/pt-BR/firefox/new/ "Download") | Logar à conta Mizilla. |
| Firefox Developer Edition | [mozilla.org](https://www.mozilla.org/pt-BR/firefox/developer/ "Download") | Mover o diretório descompactado para `/opt` \| Adicionar à área de trabalho. |
| Google Chrome | Google Inc | Adicionar à área de trabalho. Logar à conta Google. |
| Google Earth Pro | Google Inc |  |
| Tor Project | [Trademark](https://www.torproject.org/ "Download") | Mover o diretório descompactado para `/opt` \|Adicionar à área de trabalho. |
| Opera | [Opera Norway](https://www.opera.com/pt-br "Download") | Adicionar à área de trabalho. |
| Microsoft Edge | [Microsoft](https://www.microsoft.com/pt-br/edge "Download") | Adicionar à área de trabalho. |
| Skype | [Microsoft](http://www.skype.com/pt-br "Download") | Adicionar à área de trabalho. |
| Discrod | [Discord Inc](https://discord.com/ "Download") | Adicionar à área de trabalho. \|  Adicionar à área de trabalho. |
| FileZilla | [filezilla-project.org](https://filezilla-project.org/download.php?type=client "Download") | Instalação via terminal: `apt install filezilla` e `apt --fix-broken install`. \|  Adicionar à área de trabalho. |
| Steam | [Valve Corporation](https://store.steampowered.com/?l=portuguese "Download") | Adicionar à área de trabalho. |
| Remmina | [Antenore Gatta](https://remmina.org/ "Antenore Gatta") | Instalação via terminal: `sudo apt-get install remmina` |

## Desenvolvimento

|      Software      |                          Copyright                           | Instalação e/ou Configurações                               |
| :----------------: | :----------------------------------------------------------: | ----------------------------------------------------------- |
| Visual Studio Code |    [Microsoft](https://code.visualstudio.com/ "Download")    | Adicionar à área de trabalho. \| ????                       |
|      Insomnia      |    [Kong Inc](https://insomnia.rest/download "Download")     | Adicionar à área de trabalho.                               |
|     Beekeeper      | [Bookeeper Studio Inc](https://www.beekeeperstudio.io/get "Download") | ( ! ) Falta instalar, é um arquivo AppImage!                |
|        Git         | [Software Freedom Conservancy](https://git-scm.com/ "Download") | Terminal: `apt update && apt install git && git --version`. |

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--minhas-configura%C3%A7%C3%B5es "Subir para o topo")

---