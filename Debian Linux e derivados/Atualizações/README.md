# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi") / Atualizações

[![Atualizações](https://github.com/systemboys/GTi_Laboratory/raw/main/Debian%20Linux%20e%20derivados/Atualiza%C3%A7%C3%B5es/images/Upgrade_button.jpg "Atualizações")](https://github.com/systemboys/GTi_Laboratory/raw/main/Debian%20Linux%20e%20derivados/Atualiza%C3%A7%C3%B5es/images/Upgrade_button.jpg "Atualizações")

- [Alguns erros](#alguns-erros-durante-a-atualiza%C3%A7%C3%A3o-de-pacotes "Alguns erros")

---

## Alguns erros durante a atualização de pacotes

> O que quer dizer o seguinte erro no terminal Linux após o comando "apt update"?

```bash
W: Skipping acquire of configured file 'contrib/source/Sources' as repository 'https://download.virtualbox.org/virtualbox/debian buster InRelease' does not seem to provide it (sources.list entry misspelt?)
E: The repository 'https://download.virtualbox.org/virtualbox/debian <mydist> Release' does not have a Release file.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.
```

Esse erro indica que há um problema com o repositório VirtualBox no arquivo `/etc/apt/sources.list`. Especificamente, há um problema com a entrada de linha do arquivo que se refere ao repositório VirtualBox.

A mensagem de erro indica que a entrada da linha do arquivo para o diretório de origem do repositório VirtualBox (contrib/source/Sources) está faltando ou foi mal escrita. Além disso, a mensagem de erro também informa que o repositório não possui um arquivo Release, o que torna o processo de atualização inseguro e, portanto, é desabilitado por padrão.

Para corrigir esse problema, você pode editar o arquivo `/etc/apt/sources.list` e corrigir a entrada do repositório VirtualBox ou removê-la completamente. Para fazer isso, você pode seguir as etapas abaixo:

1. Abra o arquivo `/etc/apt/sources.list` com um editor de texto de sua preferência, como o nano:

```bash
sudo nano /etc/apt/sources.list
```

2. Procure a linha que se refere ao repositório VirtualBox e corrija-a, se houver um erro de digitação, ou remova-a completamente. Para remover a linha, basta comentá-la adicionando um "#" no início da linha. A linha deve ficar assim:

```bash
# deb https://download.virtualbox.org/virtualbox/debian buster contrib
```

3. Salve e feche o arquivo.

4. Execute o comando `sudo apt update` novamente para atualizar a lista de pacotes disponíveis.

Com esses passos, você deve conseguir resolver o erro e atualizar seu sistema sem problemas.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--atualiza%C3%A7%C3%B5es "Subir para o topo")

---