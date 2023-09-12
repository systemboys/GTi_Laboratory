# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi") / Assuntos relacionados à redes e Internet

[![Redes e Internet](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Assuntos%20relacionados%20%C3%A0%20redes%20e%20Internet/images/networks.png?raw=true "Redes e Internet")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Assuntos%20relacionados%20%C3%A0%20redes%20e%20Internet/images/networks.png?raw=true "Redes e Internet")

- [Entendendo o comando nslookup e a resolução de DNS no Linux (obtendo IP de domínios)](#entendendo-o-comando-nslookup-e-a-resolu%C3%A7%C3%A3o-de-dns-no-linux-obtendo-ip-de-dom%C3%ADnios "Entendendo o comando nslookup e a resolução de DNS no Linux (obtendo IP de domínios)")
- [Como Configurar um IP Estático via Terminal no Linux](#como-configurar-um-ip-est%C3%A1tico-via-terminal-no-linux "Como Configurar um IP Estático via Terminal no Linux")

---

## Entendendo o comando nslookup e a resolução de DNS no Linux (obtendo IP de domínios)

O comando "nslookup dominio_do_site.com" é usado para obter informações sobre um domínio específico, como o endereço IP associado a ele. No exemplo abaixo, o comando "nslookup facebook.com" foi executado.

[![Comando nslookup](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Assuntos%20relacionados%20%C3%A0%20redes%20e%20Internet/images/Terminal_comando_nslookup.png?raw=true "Comando nslookup")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Assuntos%20relacionados%20%C3%A0%20redes%20e%20Internet/images/Terminal_comando_nslookup.png?raw=true "Comando nslookup")

A resposta retornada mostra o servidor DNS usado para fazer a consulta (no caso, 10.0.0.1) e as informações relacionadas ao domínio "facebook.com". A resposta não é autoritativa, o que significa que não é proveniente do servidor DNS oficial do domínio.

Em seguida, são exibidos os registros de nome e endereço (IP) associados ao domínio. No exemplo, o "facebook.com" tem dois endereços associados: 157.240.216.35 (IPv4) e 2a03:2880:f159:82:face:b00c:0:25de (IPv6).

Essas informações são úteis para verificar a resolução de DNS de um domínio específico e obter os endereços IP associados a ele.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--assuntos-relacionados-%C3%A0-redes-e-internet "Subir para o topo")

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
[(&uarr;) Subir](#laborat%C3%B3rio-gti--assuntos-relacionados-%C3%A0-redes-e-internet "Subir para o topo")

---