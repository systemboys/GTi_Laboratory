# [Laboratório GTi](../../README.md#laborat%C3%B3rio-gti "Laboratório GTi")

## Monitoramento de sistema

[![Monitoramento Linux](./images/monitoramento_linux.jpeg?raw=true "Monitoramento Linux")](./images/monitoramento_linux.jpeg?raw=true "Monitoramento Linux")

### *Sumário*

- [Sensores de Hardware do Linux](#sensores-de-hardware-do-linux "Sensores de Hardware do Linux")
- [Instalar o BashTOP no Debian Linux](#instalar-o-bashtop-no-debian-linux "Instalar o BashTOP no Debian Linux")
- [Monitoramento e Execução Contínua do Bashtop](#monitoramento-e-execu%C3%A7%C3%A3o-cont%C3%ADnua-do-bashtop "Monitoramento e Execução Contínua do Bashtop")
- [🔄 Script para executar Bashtop em loop e reiniciar apenas em falha](#-script-para-executar-bashtop-em-loop-e-reiniciar-apenas-em-falha "Script para executar Bashtop em loop e reiniciar apenas em falha")
- [Instalar o utilitário de monitoramento HTOP](#instalar-o-utilit%C3%A1rio-de-monitoramento-htop "Instalar o utilitário de monitoramento HTOP")

---

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Sensores de Hardware do Linux

Sim, é possível verificar a temperatura do processador utilizando o Terminal Linux. Você pode usar o comando "sensors" para obter informações sobre a temperatura do processador.

```bash
sensors
```

Este comando exibirá as informações de temperatura do processador, incluindo a temperatura atual e máxima. Certifique-se de ter o pacote "lm-sensors" instalado em seu sistema antes de executar o comando.

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

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

[![BashTOP](./images/BashTOP.png?raw=true "BashTOP")](./images/BashTOP.png?raw=true "BashTOP")

O BashTOP deve iniciar e começar a exibir informações sobre o uso de CPU, memória e outros recursos do sistema.

Lembre-se de que, como o BashTOP é uma ferramenta de terceiros, ele pode não estar disponível nos repositórios oficiais do Debian. Portanto, ao instalá-lo dessa maneira, você está confiando no código fornecido no repositório do GitHub. Sempre verifique a fonte e a confiabilidade das ferramentas que você instala no seu sistema.

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Monitoramento e Execução Contínua do Bashtop

Esse script em Bash cria um loop infinito que verifica se o processo chamado "bashtop" está em execução. Se não estiver em execução, ele inicia o programa "bashtop". O comando `pgrep -f bashtop` busca por processos que correspondam ao nome "bashtop", e se não encontrar nenhum, o comando `bashtop` é executado para iniciar o programa.

O `sleep 1` faz com que o script espere 1 segundo antes de verificar novamente se o processo "bashtop" está em execução. Isso cria um loop contínuo que garante que o programa "bashtop" esteja sempre em execução.

> ( i ) Para ShellScript (.sh).

```bash
while true; do
  pgrep -f bashtop >/dev/null || bashtop
  sleep 1
done
```
> ( i ) Em uma linha no Terminal.

```bash
while true; do pgrep -f bashtop >/dev/null || bashtop; sleep 1; done
```

Esse script vai rodar infinitamente (while true) e  lançar o bashtop se ele não estiver rodando. Você pode salvar esse  arquivo em qualquer lugar que você quiser e executá-lo com o comando:

```bash
./keepalivescript.sh
```

Você também pode agendar esse script para ser  executado automaticamente na inicialização do sistema, usando o cron ou  outro gerenciador de tarefas. Para isso, você precisa editar o seu  crontab com o comando:

```bash
crontab -e
```

E adicionar uma linha usando a expressão @reboot, que vai executar o seu código uma vez na inicialização:

```bash
@reboot ./keepalivescript.sh
```

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## 🔄 Script para executar Bashtop em loop e reiniciar apenas em falha

Este script executa o Bashtop em loop infinito, reiniciando o computador **apenas se o Bashtop falhar**. Inclui configuração para reinício sem senha no sudo, garantindo automação completa em ambientes de monitoramento ou kiosks.

ShellScript:

```sh
#!/bin/bash

while true; do
  # Executa o bashtop
  bashtop
  STATUS=$?

  # Se bashtop falhar, reinicia
  if [ $STATUS -ne 0 ]; then
    echo "⚠️ Bashtop falhou com status $STATUS. Reiniciando o sistema..."
    sudo reboot
  fi

  # Pausa antes de reiniciar o loop
  sleep 1
done
```

Segue o **comando em uma única linha**, direto, formal e pronto para seu Codex ou execução imediata em terminal:

```bash
while true; do bashtop; STATUS=$?; if [ $STATUS -ne 0 ]; then echo "⚠️ Bashtop falhou com status $STATUS. Reiniciando o sistema..."; sudo reboot; fi; sleep 1; done
```

### ⚠️ **Explicação executiva**

* Tudo em **uma única linha** para shell scripts inline, cron jobs, containers, ou quick tests.
* Mantém **exatamente a mesma lógica** do script estruturado.
* Ideal para pipelines CI/CD de kiosks, scripts de provisionamento ou uso direto em shells remotos.

Comando em uma única linha para execução direta no terminal:

```bash
echo 'seu_usuario ALL=(ALL) NOPASSWD:/sbin/reboot' | sudo tee -a /etc/sudoers
```

Explicação:

Este script cria um loop que executa o `bashtop` continuamente. Caso o `bashtop` retorne um status diferente de 0 (indicando falha ou encerramento anormal), o sistema será reiniciado com uma mensagem clara ⚠️ para logs ou stdout. O comando em uma linha adiciona a permissão ao `sudoers` para que o comando `sudo reboot` seja executado **sem solicitar senha**, permitindo reinício automatizado sem intervenção manual.

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

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

[![HTop](./images/htop.png?raw=true "HTop")](./images/htop.png?raw=true "HTop")

O "htop" deve ser iniciado e exibirá uma interface interativa que mostra uma visão detalhada do uso de recursos do sistema.

Lembre-se de que o "htop" é uma ferramenta amplamente reconhecida e confiável. Ele é distribuído pelos repositórios oficiais do Debian e é uma escolha popular para monitoramento de sistema.

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---