# [Laboratório GTi](../../README.md#laborat%C3%B3rio-gti "Laboratório GTi")

## Monitoramento de sistema

[![Monitoramento Linux](./images/monitoramento_linux.jpeg?raw=true "Monitoramento Linux")](./images/monitoramento_linux.jpeg?raw=true "Monitoramento Linux")

### *Sumário*

- [Sensores de Hardware do Linux](#sensores-de-hardware-do-linux "Sensores de Hardware do Linux")
- [Instalar o BashTOP no Debian Linux](#instalar-o-bashtop-no-debian-linux "Instalar o BashTOP no Debian Linux")
- [Monitoramento e Execução Contínua do Bashtop](#monitoramento-e-execu%C3%A7%C3%A3o-cont%C3%ADnua-do-bashtop "Monitoramento e Execução Contínua do Bashtop")
- [🔄 Monitoramento Automático da CPU com Reinicialização](#-monitoramento-autom%C3%A1tico-da-cpu-com-reinicializa%C3%A7%C3%A3o "Monitoramento Automático da CPU com Reinicialização")
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

## 🔄 Monitoramento Automático da CPU com Reinicialização

### 📌 **Descrição**

Este script Shell monitora o uso de **todos os núcleos do processador** em tempo real.
Se **todos** atingirem 100% de uso simultaneamente, o sistema é reiniciado automaticamente.
Enquanto monitora, exibe um **spinner animado** e mostra o status de carga de cada núcleo com **bolinhas coloridas**:

* 🟢 Verde: uso até 49%
* 🟠 Laranja: uso entre 50% e 75%
* 🔴 Vermelho: uso de 76% pra cima

### ⚙️ **Pré-requisitos**

* Sistema Linux com **bash**
* **sysstat** instalado (`mpstat`)

```bash
sudo apt update
sudo apt install sysstat
```

* Permissão para reiniciar sem senha:

```bash
sudo visudo
```

Adicione:

```
seu_usuario ALL=(ALL) NOPASSWD: /sbin/reboot
```

### 🗂️ **Arquivo: `monitor_cpu_reboot.sh`**

```bash
#!/bin/bash

INTERVAL=1
SPINNER="/-\|"
SPINNER_INDEX=0

while true; do
    ALL_CORES_100=true

    clear

    echo "==================================================="
    echo "               MONITORAMENTO DA CPU"
    echo "---------------------------------------------------"
    echo "                  ⚠️  Atenção!"
    echo "Seu computador poderá reiniciar a qualquer momento!"
    echo "==================================================="

    printf "Monitorando CPU... [%c]\n" "${SPINNER:SPINNER_INDEX++:1}"
    ((SPINNER_INDEX == ${#SPINNER})) && SPINNER_INDEX=0

    CPU_USAGES=$(mpstat -P ALL 1 1 | grep -E "^[0-9]" | awk '{print 100 - $12}')

    CORE_INDEX=1
    for usage in $CPU_USAGES; do
        usage_int=$(printf "%.0f" "$usage")

        if [ "$usage_int" -le 49 ]; then
            STATUS="🟢"
        elif [ "$usage_int" -le 75 ]; then
            STATUS="🟠"
        else
            STATUS="🔴"
        fi

        echo "Núcleo $CORE_INDEX: $STATUS $usage_int%"

        if [ "$usage_int" -lt 100 ]; then
            ALL_CORES_100=false
        fi

        ((CORE_INDEX++))
    done

    echo "---------------------------------------------------"

    if [ "$ALL_CORES_100" = true ]; then
        echo "⚠️  Todos os núcleos atingiram 100%."
        echo "⏳  Reiniciando o sistema... 🖥️"
        sudo reboot
        exit 0
    fi

    sleep $INTERVAL
done
```

### ▶️ **Como executar**

1️⃣ Dê permissão:

```bash
chmod +x monitor_cpu_reboot.sh
```

2️⃣ Rode no terminal:

```bash
./monitor_cpu_reboot.sh
```

3️⃣ Para rodar em segundo plano:

```bash
./monitor_cpu_reboot.sh &
```

4️⃣ Para parar:

```bash
ps aux | grep monitor_cpu_reboot.sh
kill PID
```

### 🚦 **Uso recomendado**

* Use somente em cenários de emergência enquanto espera manutenção de hardware.
* Monitore logs, pois reinícios forçados podem gerar perda de dados.
* Mantenha backup atualizado.

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