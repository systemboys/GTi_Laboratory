# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi") / Instalação de pacotes

[![Linux Terminal](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Instala%C3%A7%C3%A3o%20de%20de%20pacotes/images/Linux_terminal.jpg?raw=true "Linux Terminal")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Instala%C3%A7%C3%A3o%20de%20de%20pacotes/images/Linux_terminal.jpg?raw=true "Linux Terminal")

- [Erro de PATH após instalação de pacote .deb no Linux](#erro-de-path-ap%C3%B3s-instala%C3%A7%C3%A3o-de-pacote-deb-no-linux "Erro de PATH após instalação de pacote .deb no Linux")

---

## Erro de PATH após instalação de pacote .deb no Linux

Erro ao instalar um seguinte programa no Debian 10:

[![Erro ao instalar programa](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Instala%C3%A7%C3%A3o%20de%20de%20pacotes/images/Erro_PATH_do_root.png?raw=true "Erro ao instalar programa")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Instala%C3%A7%C3%A3o%20de%20de%20pacotes/images/Erro_PATH_do_root.png?raw=true "Erro ao instalar programa")

O erro "E: Sub-process /usr/bin/dpkg returned an error code (1)" é geralmente um erro genérico que ocorre durante a instalação ou atualização de pacotes em sistemas operacionais baseados em Debian, como Ubuntu e Debian. Esse erro pode ser causado por uma série de problemas, como dependências quebradas, problemas de conflito entre pacotes ou problemas com o próprio pacote que está sendo instalado. Para resolver esse erro, é necessário identificar a causa específica do problema e corrigi-lo adequadamente.

Com editor de sua preferência edite o arquivo `./etc/profile`.

```bash
sudo nano /etc/profile
```

[![Terminal Profile](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Instala%C3%A7%C3%A3o%20de%20de%20pacotes/images/Terminal_etc_profile.png?raw=true "Terminal Profile")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Instala%C3%A7%C3%A3o%20de%20de%20pacotes/images/Terminal_etc_profile.png?raw=true "Terminal Profile")

Observe que haverá uma condição com valor verdadeiro ou falso:

```bash
if [ "$(id -u)" -eq 0 ]; then
  PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
else
  PATH="/usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games"
fi
```

Altere a linha no `else` da condição, adicionando um `/sbin` como no exemplo abaixo:

```bash
PATH="/usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games/sbin"
```

Após modificar salve o arquivo e saia, você voltará para o terminal. Obs.: Se for no `nano`, execute os comandos:

| Comando | Descrição |
| :------------: | :------------ |
| Ctrl + O | Gravar alterações no arquivo |
| Ctrl + X | Sair do arquivo e voltar para o terminal |

Após editar, salvar e sair do arquivo, execute o seguinte comando:

```bash
source /etc/profile
```

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#erro-de-path-ap%C3%B3s-instala%C3%A7%C3%A3o-de-pacote-deb-no-linux "Subir para o topo")

Reinicie o PC, ou simplemente de um export.

---