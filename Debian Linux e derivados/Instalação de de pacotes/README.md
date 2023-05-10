# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi") / Instalação de pacotes

[![Imagem 1](https://site.com/img/exemplo.png "Imagem 1")](http://link.com "Imagem 1")

- [Erro de PATH após instalação de pacote .deb no Linux](#erro-ao-instalar-um-programa-no-debian-10 "Erro de PATH após instalação de pacote .deb no Linux")

---

## Erro de PATH após instalação de pacote .deb no Linux

Erro ao instalar um seguinte programa no Debian 10:

[![Erro ao instalar programa](https://plus.diolinux.com.br/uploads/default/optimized/2X/7/70f1a67449a44d1639b36cea19eb21a4d52d7053_2_690x387.png "Erro ao instalar programa")](https://plus.diolinux.com.br/uploads/default/optimized/2X/7/70f1a67449a44d1639b36cea19eb21a4d52d7053_2_690x387.png "Erro ao instalar programa")

O erro "E: Sub-process /usr/bin/dpkg returned an error code (1)" é geralmente um erro genérico que ocorre durante a instalação ou atualização de pacotes em sistemas operacionais baseados em Debian, como Ubuntu e Debian. Esse erro pode ser causado por uma série de problemas, como dependências quebradas, problemas de conflito entre pacotes ou problemas com o próprio pacote que está sendo instalado. Para resolver esse erro, é necessário identificar a causa específica do problema e corrigi-lo adequadamente.

Com editor de sua preferência edite o arquivo `./etc/profile`.

```bash
sudo nano /etc/profile
```

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

Após modificar salve o arquivo e saida. Obs.: Se for no `nano`, execute os comandos:

| Comando | Descrição |
| :------------: | :------------ |
| Ctrl + O | Gravar alterações no arquivo |
| Ctrl + X | Sair do arquivo e voltar para o terminal |

Após editar, salvar e sair do arquivo, execute o seguinte comando:

```bash
source /etc/profile
```

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#assunto "Subir para o topo")

Reinicie o PC, ou simplemente de um export.

---