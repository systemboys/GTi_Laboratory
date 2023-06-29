# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi") / Assuntos relacionados à redes e Internet

[![Redes e Internet](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Assuntos%20relacionados%20%C3%A0%20redes%20e%20Internet/images/networks.png?raw=true "Redes e Internet")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Assuntos%20relacionados%20%C3%A0%20redes%20e%20Internet/images/networks.png?raw=true "Redes e Internet")

- [Entendendo o comando nslookup e a resolução de DNS no Linux (obtendo IP de domínios)](#entendendo-o-comando-nslookup-e-a-resolu%C3%A7%C3%A3o-de-dns-no-linux-obtendo-ip-de-dom%C3%ADnios "Entendendo o comando nslookup e a resolução de DNS no Linux (obtendo IP de domínios)")

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