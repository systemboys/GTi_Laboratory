# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi") / Monitoramento de sistema

[![Monitoramento Linux](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Monitoramento%20de%20sistemas/images/monitoramento_linux.jpeg?raw=true "Monitoramento Linux")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Monitoramento%20de%20sistemas/images/monitoramento_linux.jpeg?raw=true "Monitoramento Linux")

- [Instalar o BashTOP no Debian Linux](#instalar-o-bashtop-no-debian-linux "Instalar o BashTOP no Debian Linux")
- [Instalar o utilitário de monitoramento HTOP](# "Instalar o utilitário de monitoramento HTOP")

---

## Instalar o BashTOP no Debian Linux

O "BashTOP" é uma ferramenta de monitoramento de sistema baseada em Bash, que exibe informações sobre o uso de recursos do sistema de uma maneira semelhante ao "top". Para instalá-lo no Debian Linux, siga os passos abaixo:

1. Abra um terminal. Você pode fazer isso pressionando `Ctrl` + `Alt` + `T` ao mesmo tempo.

2. Certifique-se de que seu sistema esteja atualizado executando o seguinte comando:

```bash
sudo apt update && sudo apt upgrade
```

3. Instale as dependências necessárias, como o Git (caso você ainda não tenha instalado):

```bash
sudo apt install git
```

4. Clone o repositório do BashTOP do GitHub:

```bash
git clone https://github.com/aristocratos/bashtop.git
```

5. Entre no diretório do BashTOP que foi criado após o clone:

```bash
cd bashtop
```

6. Instale o BashTOP usando o comando "make":

```bash
sudo make install
```

7. Agora você pode executar o BashTOP simplesmente digitando `bashtop` no terminal:

```bash
bashtop
```

[![BashTOP](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Monitoramento%20de%20sistemas/images/BashTOP.png?raw=true "BashTOP")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Monitoramento%20de%20sistemas/images/BashTOP.png?raw=true "BashTOP")

O BashTOP deve iniciar e começar a exibir informações sobre o uso de CPU, memória e outros recursos do sistema.

Lembre-se de que, como o BashTOP é uma ferramenta de terceiros, ele pode não estar disponível nos repositórios oficiais do Debian. Portanto, ao instalá-lo dessa maneira, você está confiando no código fornecido no repositório do GitHub. Sempre verifique a fonte e a confiabilidade das ferramentas que você instala no seu sistema.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--monitoramento-de-sistema "Subir para o topo")

---

## Instalar o utilitário de monitoramento HTOP

O "htop" é um utilitário de monitoramento de sistema interativo que exibe informações detalhadas sobre o uso de recursos do sistema, como CPU, memória e processos. Ele é uma alternativa avançada e aprimorada para o comando "top". Para instalá-lo no Debian Linux, siga estas etapas:

1. Abra um terminal. Você pode fazer isso pressionando `Ctrl` + `Alt` + `T` ao mesmo tempo.

2. Certifique-se de que seu sistema esteja atualizado executando o seguinte comando:

```bash
sudo apt update && sudo apt upgrade
```

3. Instale o "htop" usando o gerenciador de pacotes APT:

```bash
sudo apt install htop
```

4. Após a instalação, você pode executar o "htop" simplesmente digitando `htop` no terminal:

```bash
htop
```

O "htop" deve ser iniciado e exibirá uma interface interativa que mostra uma visão detalhada do uso de recursos do sistema.

Lembre-se de que o "htop" é uma ferramenta amplamente reconhecida e confiável. Ele é distribuído pelos repositórios oficiais do Debian e é uma escolha popular para monitoramento de sistema.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--monitoramento-de-sistema "Subir para o topo")

---