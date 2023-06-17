# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi") / Processos em execução

# Sumário

- [Barra de tarefas (`taskbar`), Eliminar processo ativo](#system-tray-icon "Barra de tarefas (`taskbar`), Eliminar processo ativo")
- [Tarefas em execução (top)](# "Tarefas em execução (top)")

---

### System Tray Icon

[Marcos Aurélio]
Quando o ícone do Skype não sai após um erro no software, o que fazer para eliminar o ícone forçadamente?

[Resposta]
Se o ícone do Skype não desaparecer da área de notificação após um erro no software e você não conseguir fechá-lo normalmente, pode ser necessário encerrar o processo do Skype manualmente para remover o ícone. Aqui estão alguns passos que você pode seguir para eliminar o ícone do Skype forçadamente:

- Abra o terminal (pressionando Ctrl + Alt + T).
- Digite o seguinte comando para listar todos os processos em execução:
```bash
ps -A
```

[![Processos em execução](https://github.com/systemboys/GTi_Laboratory/raw/main/Debian%20Linux%20e%20derivados/Processos%20em%20execu%C3%A7%C3%A3o/images/ps_-A.png "Processos em execução")](https://github.com/systemboys/GTi_Laboratory/raw/main/Debian%20Linux%20e%20derivados/Processos%20em%20execu%C3%A7%C3%A3o/images/ps_-A.png "Processos em execução")

- Procure pelo processo do Skype na lista. Geralmente, o processo do Skype é chamado de skype ou skypeforlinux.
- Anote o número do PID (Process ID) do processo do Skype.
- Digite o seguinte comando para encerrar o processo do Skype:
```bash
kill PID
```

> Substitua "PID" pelo número do PID que você anotou no passo anterior.

- O ícone do Skype deve desaparecer da área de notificação após o processo ser encerrado.

Se o ícone do Skype ainda não desaparecer da área de notificação após encerrar o processo, você pode tentar reiniciar a interface gráfica do usuário (GUI) usando o seguinte comando:

```bash
sudo systemctl restart display-manager
```

Esse comando irá reiniciar a GUI do sistema e, com sorte, removerá o ícone do Skype. Lembre-se de que, ao reiniciar a GUI, você será desconectado da sua sessão atual e todas as janelas abertas serão fechadas.

Você pode usar o operador "&&" para executar vários comandos "kill PID" em uma única linha. Nesse caso, os comandos serão executados em sequência, e cada um só será executado se o comando anterior for executado com sucesso.

Por exemplo, para finalizar os processos com PID 1234, 5678 e 9012 em uma única linha, você pode executar o seguinte comando:

```bash
kill 1234 && kill 5678 && kill 9012
```

Este comando executará o primeiro comando "kill 1234" e, se ele for executado com sucesso (ou seja, se o processo com o PID 1234 for finalizado), o segundo comando "kill 5678" será executado, e assim por diante. Se um dos comandos falhar, os comandos subsequentes não serão executados.

Para listar os processos em ordem alfabética crescente (A a Z) com base na coluna CMD usando o comando `ps -A`, você pode usar o seguinte comando:

```bash
ps -A --sort=cmd
```

Este comando adiciona a opção `--sort=cmd` para classificar os processos com base no nome do comando (CMD) em ordem alfabética crescente.

Se você quiser classificar os processos em ordem decrescente (Z a A), basta adicionar o sinal de menos (-) antes da opção de classificação, como no seguinte comando:

```bash
ps -A --sort=-cmd
```

Este comando classifica os processos com base no nome do comando (CMD) em ordem alfabética decrescente.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--processos-em-execu%C3%A7%C3%A3o "Subir para o topo")

---

## Tarefas em execução (top)

O comando "top" pode ser combinado com outros comandos no terminal Linux usando a funcionalidade de redirecionamento de saída. Por exemplo, você pode usar o comando "top -n 1" para executar o "top" uma única vez e redirecionar sua saída para outro comando ou arquivo.

Aqui estão alguns exemplos de combinações de comandos com o "top":

1. Redirecionar a saída do "top" para um arquivo:

   ```bash
   top -n 1 > arquivo.txt
   ```

2. Filtrar informações específicas do "top" usando o comando "grep":

   ```bash
   top -n 1 | grep "nome_do_processo"
   ```

3. Contar o número de processos em execução usando o comando "wc":

   ```bash
   top -n 1 | wc -l
   ```

Esses são apenas alguns exemplos básicos, mas você pode combinar o comando "top" com vários outros comandos do Linux para realizar diferentes tarefas e obter informações específicas sobre os processos em execução no sistema.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--processos-em-execu%C3%A7%C3%A3o "Subir para o topo")

---
