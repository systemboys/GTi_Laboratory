# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi") / Monitoramento de sistema

[![Imagem 1](https://site.com/img/exemplo.png "Imagem 1")](http://link.com "Imagem 1")

- [Instalar o BashTOP no Debian Linux](#instalar-o-bashtop-no-debian-linux "Instalar o BashTOP no Debian Linux")

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

[![BashTOP](https://site.com/img/exemplo.png "BashTOP")](http://link.com "BashTOP")

O BashTOP deve iniciar e começar a exibir informações sobre o uso de CPU, memória e outros recursos do sistema.

Lembre-se de que, como o BashTOP é uma ferramenta de terceiros, ele pode não estar disponível nos repositórios oficiais do Debian. Portanto, ao instalá-lo dessa maneira, você está confiando no código fornecido no repositório do GitHub. Sempre verifique a fonte e a confiabilidade das ferramentas que você instala no seu sistema.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#assunto "Subir para o topo")

---