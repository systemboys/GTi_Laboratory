# [Laboratório GTi](../../README.md#laborat%C3%B3rio-gti "Laboratório GTi")

## Segurança de Rede no Debian Linux

[![Firewall Linux](./images/managed-firewalls.png?raw=true "Firewall Linux")](./images/managed-firewalls.png?raw=true "Firewall Linux")

### *Sumário*

- [Verificarndo porta com NMap](#verificarndo-porta-com-nmap "Verificarndo porta com NMap")
- [Verificar status de todas as portas em um host](#verificar-status-de-todas-as-portas-em-um-host "Verificar status de todas as portas em um host")
- [Instalar utilitário "ufw" (Uncomplicated Firewall) no Debian Linux](#instalar-utilit%C3%A1rio-ufw-uncomplicated-firewall-no-debian-linux "Instalar utilitário 'ufw' (Uncomplicated Firewall) no Debian Linux")
- [🛡️ Instruções para Instalação e Uso do ClamAV no Debian](# "Instruções para Instalação e Uso do ClamAV no Debian")
- [Firewall UFW (abrir ou fechar portas)](#firewall-ufw-abrir-ou-fechar-portas "Firewall UFW (abrir ou fechar portas)")

---

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Verificarndo porta com NMap

Para verificar se a porta 22 (SSH) está aberta em um determinado endereço IP, você pode usar uma ferramenta como o `nmap`. No seu computador local (Debian Linux), siga os passos abaixo:

1. Instale o `nmap` se ainda não estiver instalado. Você pode usar o seguinte comando para instalar:

   ```bash
   sudo apt-get install nmap
   ```

2. Depois que o `nmap` estiver instalado, execute o seguinte comando para verificar a porta 22 no endereço IP da sua máquina na Linode:

   ```bash
   sudo nmap -p 22 50.116.40.116
   ```

   Substitua "50.116.40.116" pelo seu endereço IP da Linode.

3. O `nmap` exibirá a saída mostrando o estado da porta 22. Se a porta estiver aberta, você verá algo como:

   ```bash
   PORT   STATE SERVICE
   22/tcp open  ssh
   ```

   Se a porta estiver fechada, a saída será diferente.

Isso irá verificar se a porta 22 está aberta na máquina da Linode. Se a porta estiver fechada ou se você estiver enfrentando problemas de conexão, verifique suas configurações de firewall e rede na máquina da Linode.

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Verificar status de todas as portas em um host

Para verificar o status de todas as portas em um host usando o Nmap, você pode executar o seguinte comando:

```bash
sudo nmap -p- <endereço_IP>
```

Substitua `<endereço_IP>` pelo endereço IP do host que você deseja verificar.

Esse comando usará a opção `-p-` para especificar que todas as portas devem ser verificadas. O `sudo` é usado para garantir que você tenha permissões de administrador para executar o comando.

Após a execução do comando, o Nmap irá verificar todas as portas no host e exibirá o status de cada porta, indicando se está aberta, fechada ou filtrada.

Lembre-se de que verificar todas as portas em um host pode levar algum tempo, dependendo do número de portas a serem verificadas.

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Instalar utilitário "ufw" (Uncomplicated Firewall) no Debian Linux

Para instalar o utilitário "ufw" (Uncomplicated Firewall) no Debian Linux, você pode seguir os passos abaixo:

1. Conecte-se à sua máquina Debian Linux via SSH ou abra um terminal local.

2. Execute o seguinte comando para atualizar a lista de pacotes disponíveis:
   ```bash
   sudo apt update
   ```

3. Em seguida, execute o comando a seguir para instalar o "ufw":
   ```bash
   sudo apt install ufw
   ```

4. Durante a instalação, você será solicitado a confirmar a ação digitando "Y" ou "S" e pressionando Enter.

Após a conclusão da instalação, você poderá utilizar o "ufw" para configurar o firewall no seu sistema Debian Linux. Lembre-se de consultar a documentação ou recursos adicionais para aprender a usar o "ufw" corretamente e configurar as regras de firewall de acordo com suas necessidades.

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## 🛡️ Instruções para Instalação e Uso do ClamAV no Debian

Este guia orienta sobre como instalar o antivírus **ClamAV** no Debian e executar uma varredura completa em uma pasta específica (como um pendrive com **Ventoy**).

### ✅ Etapa 1: Acessar como superusuário (root)

```bash
su
```

Digite a senha de root quando solicitado.

### 📦 Etapa 2: Instalar o ClamAV

Execute o comando:

```bash
sudo apt-get install clamav
```

Confirme a instalação pressionando `S` quando for solicitado para continuar.

### 🔄 Etapa 3: Atualizar base de dados de vírus (opcional, mas recomendado)

```bash
sudo freshclam
```

> *Obs.: Se o serviço estiver rodando em segundo plano, talvez precise pará-lo para atualizar manualmente.*

### 🧼 Etapa 4: Executar varredura em uma pasta

No exemplo abaixo, é feita a varredura recursiva da pasta `/media/marcos/Ventoy`:

```bash
clamscan -r /media/marcos/Ventoy
```

### 📊 Exemplo de resultado da varredura

```text
/media/marcos/Ventoy/Win10.iso: OK
/media/marcos/Ventoy/debian.iso: OK
...

----------- SCAN SUMMARY -----------
Known viruses: 8706641
Engine version: 1.0.7
Scanned directories: 7
Scanned files: 176
Infected files: 0
Data scanned: 0.72 MB
Time: 51.948 sec (0 m 51 s)
```

### 🧠 Observações

* O `clamscan` apenas verifica, **não remove** os arquivos infectados.
* Para ações automáticas como mover arquivos infectados, use flags como `--move` ou `--remove`.
* A varredura pode demorar, dependendo do tamanho e quantidade de arquivos.

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Firewall UFW (abrir ou fechar portas)

Para abrir ou fechar portas em um sistema Debian Linux, você pode usar o utilitário UFW (Uncomplicated Firewall) da seguinte maneira:

1. Verifique se o UFW está instalado. Caso não esteja, você pode instalá-lo executando o seguinte comando:
   ```bash
   sudo apt-get install ufw
   ```

2. Após a instalação, você pode verificar o status atual do UFW executando o comando:
   ```
   sudo ufw status
   ```

3. Por padrão, o UFW geralmente bloqueia todas as conexões de entrada e permite todas as conexões de saída. Para abrir uma porta específica, você pode executar o seguinte comando, substituindo `<número_da_porta>` pelo número da porta que deseja abrir:
   ```bash
   sudo ufw allow <número_da_porta>
   ```

4. Para fechar uma porta, você pode usar o comando:
   ```bash
   sudo ufw deny <número_da_porta>
   ```

5. Após adicionar ou remover regras, você deve habilitar o UFW para que as alterações entrem em vigor. Use o comando:
   ```bash
   sudo ufw enable
   ```

6. Você pode verificar as regras configuradas pelo UFW a qualquer momento com o comando:
   ```bash
   sudo ufw status
   ```

Lembre-se de substituir `<número_da_porta>` pelo número da porta que deseja abrir ou fechar.

Certifique-se de configurar suas regras de firewall com cuidado e considere os riscos de segurança ao abrir portas em seu sistema.

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---