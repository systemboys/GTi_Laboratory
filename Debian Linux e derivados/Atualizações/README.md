# [Laboratório GTi](../../README.md#laborat%C3%B3rio-gti "Laboratório GTi")

## Atualizações

[![Atualizações](./images/Upgrade_button.jpg "Atualizações")](./images/Upgrade_button.jpg "Atualizações")

### *Sumário*

- [Atualizar o kernel do Linux](#atualizar-o-kernel-do-linux "Atualizar o kernel do Linux")
- [Alguns erros](#alguns-erros-durante-a-atualiza%C3%A7%C3%A3o-de-pacotes "Alguns erros")

---

## Atualizar o kernel do Linux

Para atualizar o kernel do Linux, você precisará seguir algumas etapas, mas antes de prosseguir, é importante lembrar que a atualização do kernel pode ser um procedimento avançado e potencialmente arriscado. Se não for feito corretamente, pode levar a problemas de incompatibilidade com hardware ou software. Portanto, recomendo fazer um backup completo do seu sistema antes de prosseguir.

Aqui estão os passos gerais para atualizar o kernel no Debian ou em distribuições Linux baseadas no Debian:

1. Verifique a versão atual do kernel:
Antes de atualizar, verifique a versão do kernel atual em execução no seu sistema usando o seguinte comando:

```bash
uname -r
```

2. Verifique as atualizações disponíveis:
Atualmente, os kernels são geralmente gerenciados pelo sistema de gerenciamento de pacotes da sua distribuição. Use os seguintes comandos para atualizar a lista de pacotes disponíveis e verificar se há atualizações do kernel:

```bash
sudo apt update
sudo apt list --upgradable
```

Isso mostrará uma lista de pacotes, incluindo pacotes relacionados ao kernel que estão disponíveis para atualização.

3. Atualize o kernel:
Para atualizar o kernel, use o seguinte comando no Debian ou em distribuições baseadas no Debian:

```bash
sudo apt upgrade
```

Ou, para atualizar apenas o kernel e seus pacotes relacionados:

```bash
sudo apt install linux-image-amd64 linux-headers-amd64
```

Substitua "amd64" pela arquitetura correspondente do seu sistema (por exemplo, i386, arm64, etc.).

4. Reinicie o sistema:
Após a atualização do kernel, será necessário reiniciar o sistema para que a nova versão do kernel seja carregada.

5. Verifique a nova versão do kernel:
Após reiniciar, verifique se a nova versão do kernel foi instalada corretamente usando novamente o comando:

```bash
uname -r
```

Se a nova versão do kernel for exibida, a atualização foi bem-sucedida.

Lembre-se de que, se você estiver usando um gerenciador de inicialização como o GRUB, ele pode listar várias versões do kernel durante a inicialização. Se por algum motivo a nova versão do kernel não funcionar corretamente, você poderá selecionar a versão anterior do kernel na lista do GRUB e inicializar com ela.

Novamente, reforço a importância de fazer backup dos seus dados antes de qualquer procedimento de atualização do kernel. Se você não estiver confortável com essas etapas, é melhor buscar assistência de alguém mais experiente ou evitar atualizar o kernel. O kernel existente do Debian é geralmente estável e seguro, a menos que você precise especificamente de uma nova funcionalidade ou correção fornecida em uma versão mais recente.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Alguns erros durante a atualização de pacotes

> O que quer dizer o seguinte erro no terminal Linux após o comando "apt update"?

```bash
W: Skipping acquire of configured file 'contrib/source/Sources' as repository 'https://download.virtualbox.org/virtualbox/debian buster InRelease' does not seem to provide it (sources.list entry misspelt?)
E: The repository 'https://download.virtualbox.org/virtualbox/debian <mydist> Release' does not have a Release file.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.
```

[![Terminal após o comando apt update](./images/apt_update.png "Terminal após o comando apt update")](./images/apt_update.png "Terminal após o comando apt update")

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
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---