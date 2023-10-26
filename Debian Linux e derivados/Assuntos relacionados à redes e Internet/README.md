# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi")

## Assuntos relacionados à redes e Internet

[![Redes e Internet](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Assuntos%20relacionados%20%C3%A0%20redes%20e%20Internet/images/networks.png?raw=true "Redes e Internet")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Assuntos%20relacionados%20%C3%A0%20redes%20e%20Internet/images/networks.png?raw=true "Redes e Internet")

### *Sumário*

- [Entendendo o comando nslookup e a resolução de DNS no Linux (obtendo IP de domínios)](#entendendo-o-comando-nslookup-e-a-resolu%C3%A7%C3%A3o-de-dns-no-linux-obtendo-ip-de-dom%C3%ADnios "Entendendo o comando nslookup e a resolução de DNS no Linux (obtendo IP de domínios)")
- [Como Configurar um IP Estático via Terminal no Linux](#como-configurar-um-ip-est%C3%A1tico-via-terminal-no-linux "Como Configurar um IP Estático via Terminal no Linux")
- [Configurando Temporariamente uma Rede no Linux via Terminal](#configurando-temporariamente-uma-rede-no-linux-via-terminal "Configurando Temporariamente uma Rede no Linux via Terminal")
- [Dominando as Configurações de Rede no Linux: Um Guia Abrangente para Iniciantes](#dominando-as-configura%C3%A7%C3%B5es-de-rede-no-linux-um-guia-abrangente-para-iniciantes "Dominando as Configurações de Rede no Linux: Um Guia Abrangente para Iniciantes")

---

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Entendendo o comando nslookup e a resolução de DNS no Linux (obtendo IP de domínios)

O comando "nslookup dominio_do_site.com" é usado para obter informações sobre um domínio específico, como o endereço IP associado a ele. No exemplo abaixo, o comando "nslookup facebook.com" foi executado.

[![Comando nslookup](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Assuntos%20relacionados%20%C3%A0%20redes%20e%20Internet/images/Terminal_comando_nslookup.png?raw=true "Comando nslookup")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Assuntos%20relacionados%20%C3%A0%20redes%20e%20Internet/images/Terminal_comando_nslookup.png?raw=true "Comando nslookup")

A resposta retornada mostra o servidor DNS usado para fazer a consulta (no caso, 10.0.0.1) e as informações relacionadas ao domínio "facebook.com". A resposta não é autoritativa, o que significa que não é proveniente do servidor DNS oficial do domínio.

Em seguida, são exibidos os registros de nome e endereço (IP) associados ao domínio. No exemplo, o "facebook.com" tem dois endereços associados: 157.240.216.35 (IPv4) e 2a03:2880:f159:82:face:b00c:0:25de (IPv6).

Essas informações são úteis para verificar a resolução de DNS de um domínio específico e obter os endereços IP associados a ele.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Como Configurar um IP Estático via Terminal no Linux

Configurar um IP estático via terminal no Linux envolve a edição do arquivo de configuração da interface de rede. Vou fornecer instruções gerais para configurar um IP estático no Linux usando o utilitário de linha de comando `ip`. Lembre-se de substituir "interface" pelo nome da sua interface de rede, como "eth0" ou "enp0s3", e "seu_ip", "seu_gateway" e "sua_mascara" pelos valores apropriados da sua rede.

**Passo 1: Verifique o nome da sua interface de rede**

Você pode verificar o nome da sua interface de rede usando o comando `ip a` ou `ifconfig`. Procure por algo como "eth0" ou "enp0s3". Anote o nome da interface que deseja configurar.

**Passo 2: Edite o arquivo de configuração da interface**

Abra o arquivo de configuração da interface de rede usando um editor de texto, como o Nano:

```bash
sudo nano /etc/network/interfaces
```

**Passo 3: Configure a interface**

Adicione as seguintes linhas ao arquivo, substituindo "interface", "seu_ip", "seu_gateway" e "sua_mascara" pelos valores apropriados:

```plaintext
auto interface
iface interface inet static
    address seu_ip
    netmask sua_mascara
    gateway seu_gateway
```

**Passo 4: Reinicie o serviço de rede**

Para que as alterações entrem em vigor, reinicie o serviço de rede:

```bash
sudo systemctl restart networking
```

**Passo 5: Verifique a configuração**

Você pode verificar a configuração da interface usando o comando `ip a`:

```bash
ip a show interface
```

Substitua "interface" pelo nome da sua interface de rede. Certifique-se de que as configurações estejam corretas.

Depois de seguir essas etapas, sua interface de rede deve estar configurada com o IP estático especificado. Certifique-se de ter anotado todos os valores corretamente, pois incorreções podem causar problemas na conectividade de rede.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Configurando Temporariamente uma Rede no Linux via Terminal

Sim, é possível configurar temporariamente uma rede no Linux via terminal usando o utilitário `ip` ou comandos específicos, como `ifconfig` e `route`. Essa configuração será efêmera e não persistirá após reiniciar o sistema. Aqui estão alguns exemplos de como fazer isso:

**Configurando um IP temporário com `ip` (exemplo para a interface eth0):**

```bash
sudo ip addr add seu_ip/24 dev eth0
sudo ip link set eth0 up
sudo ip route add default via seu_gateway
```

Substitua "seu_ip", "eth0", "seu_gateway" e "24" pelos valores apropriados.

**Configurando um IP temporário com `ifconfig` (exemplo para a interface eth0):**

```bash
sudo ifconfig eth0 seu_ip netmask sua_mascara up
sudo route add default gw seu_gateway
```

Substitua "seu_ip", "eth0", "sua_mascara" e "seu_gateway" pelos valores apropriados.

Essas configurações serão válidas até o próximo reinício do sistema. Se você deseja tornar a configuração permanente, siga as instruções fornecidas na resposta anterior para configurar um IP estático.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Dominando as Configurações de Rede no Linux: Um Guia Abrangente para Iniciantes

> Tutorial para alterar configurações de rede através do Terminal Linux:

---

**Alterando Configurações de Rede no Linux: Um Guia Passo a Passo**

O Linux oferece a flexibilidade de gerenciar suas configurações de rede diretamente pelo terminal. Este guia passo a passo ajudará você a modificar configurações como IP, máscara de sub-rede, gateway e servidores DNS.

**1º Passo: Identificar e Interromper Interfaces de Rede**

Antes de alterar qualquer configuração, é crucial identificar as interfaces de rede instaladas. Você pode fazer isso usando o comando `ifconfig`. Por exemplo:

```bash
ifconfig
```

Identifique sua interface (por exemplo, `eth0` para Ethernet) e interrompa sua instância:

```bash
sudo ifconfig eth0 down
```

**2º Passo: Configurar IP, Máscara de Sub-rede e Gateway**

Configure o IP e a máscara de sub-rede para a interface desejada (substitua `eth0` pelo nome da sua interface, `192.168.14.35` pelo IP desejado e `255.255.255.0` pela máscara de sub-rede):

```bash
sudo ifconfig eth0 192.168.14.35 netmask 255.255.255.0 up
```

Adicione o gateway (substitua `192.168.14.1` pelo IP do seu gateway):

```bash
sudo route add default gw 192.168.14.1 eth0
```

**3º Passo: Configurar Servidores DNS**

Edite o arquivo `/etc/resolv.conf` para configurar seus servidores DNS. Use um editor de texto como `nano`:

```bash
sudo nano /etc/resolv.conf
```

Adicione suas configurações DNS:

```plaintext
nameserver 192.168.14.1
nameserver 192.168.1.1
```

Pressione `Ctrl + O` para salvar e `Ctrl + X` para sair no Nano.

---

> Este tutorial oferece uma visão clara e concisa do processo de modificação das configurações de rede no Linux, permitindo que você ajuste sua conexão de acordo com suas necessidades.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---