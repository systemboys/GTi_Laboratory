# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi") / Diretórios e arquivos

[![Diretórios e arquivos](https://github.com/systemboys/GTi_Laboratory/raw/main/Debian%20Linux%20e%20derivados/Diret%C3%B3rios%20e%20arquivos/images/desktop_zero_feature_tiny.jpg "Diretórios e arquivos")](http://link.com "Diretórios e arquivos")

- [Renomear um diretório via terminal Linux](#renomear-um-diret%C3%B3rio-via-terminal-linux "Renomear um diretório via terminal Linux")
- [Mover diretório ou arquivo de um local para outro](#mover-diret%C3%B3rio-ou-arquivo-de-um-local-para-outro "Mover diretório ou arquivo de um local para outro")
- [Apagar um diretório com todos os seus subdiretórios e arquivos](#apagar-um-diret%C3%B3rio-com-todos-os-seus-subdiret%C3%B3rios-e-arquivos "Apagar um diretório com todos os seus subdiretórios e arquivos")
- [Apagar todos os arquivo de um diretório exceto um arquivo ou diretório filho](#apagar-todos-os-arquivo-de-um-diret%C3%B3rio-exceto-um-arquivo-ou-diret%C3%B3rio-filho "Apagar todos os arquivo de um diretório exceto um arquivo ou diretório filho")
- [Permissões a arquivos e diretórios](#permiss%C3%B5es-a-arquivos-e-diret%C3%B3rios "Permissões a arquivos e diretórios")
> Compactadores
- [Guia Rápido: Como Extrair Arquivos ZIP Usando o Terminal no Linux](#guia-r%C3%A1pido-como-extrair-arquivos-zip-usando-o-terminal-no-linux "Guia Rápido: Como Extrair Arquivos ZIP Usando o Terminal no Linux")

---

## Renomear um diretório via terminal Linux

Para renomear um diretório via terminal no Linux, você pode usar o comando `mv` (move). O `mv` também é usado para renomear diretórios, além de mover arquivos ou diretórios para um novo local. Aqui está o formato do comando:

```bash
mv nome_atual novo_nome
```

Substitua "nome_atual" pelo nome atual do diretório que você deseja renomear e "novo_nome" pelo novo nome que você deseja atribuir ao diretório.

Por exemplo, se você quiser renomear o diretório "antigo_nome" para "novo_nome", o comando seria:

```bash
mv antigo_nome novo_nome
```

Certifique-se de estar no diretório correto ou fornecer o caminho completo para o diretório, caso esteja em um local diferente. Além disso, verifique se você tem permissões suficientes para renomear o diretório.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao SumÃ¡rio") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--diret%C3%B3rios-e-arquivos "Subir para o topo")

---

## Mover diretório ou arquivo de um local para outro

Para mover um diretório de um local para outro no Linux via terminal, você também pode usar o comando `mv` (move). O `mv` é usado tanto para renomear diretórios quanto para movê-los para um novo local. O formato do comando é o seguinte:

```bash
mv nome_do_diretorio caminho_destino
```

Substitua "nome_do_diretorio" pelo nome do diretório que você deseja mover e "caminho_destino" pelo novo local de destino para o diretório.

Por exemplo, se você deseja mover o diretório "meu_diretorio" para a pasta "novo_destino", você pode usar o seguinte comando:

```bash
mv meu_diretorio novo_destino/
```

Certifique-se de fornecer o caminho correto para o diretório de destino. Se você estiver movendo o diretório para um local diferente, forneça o caminho completo do destino.

Além disso, verifique se você tem as permissões adequadas para realizar a operação de movimentação.

Para mover arquivos de um local para outro no Linux via terminal, você também pode usar o comando `mv` (move). O `mv` é usado tanto para renomear arquivos quanto para movê-los para um novo local. O formato do comando é o seguinte:

```bash
mv nome_do_arquivo caminho_destino
```

Substitua "nome_do_arquivo" pelo nome do arquivo que você deseja mover e "caminho_destino" pelo novo local de destino para o arquivo.

Por exemplo, se você deseja mover o arquivo "meu_arquivo.txt" para a pasta "novo_destino", você pode usar o seguinte comando:

```bash
mv meu_arquivo.txt novo_destino/
```

Certifique-se de fornecer o caminho correto para o local de destino. Se você estiver movendo o arquivo para um diretório diferente, forneça o caminho completo do destino.

Além disso, verifique se você tem as permissões adequadas para realizar a operação de movimentação.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao SumÃ¡rio") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--diret%C3%B3rios-e-arquivos "Subir para o topo")

---

## Apagar um diretório com todos os seus subdiretórios e arquivos

Para apagar um diretório com todos os seus subdiretórios e arquivos no Linux via terminal, você pode usar o comando "rm" com a opção "-r" para remover diretórios recursivamente. Os seguintes passos irão guiá-lo através do processo:

1. Abra o terminal ou console de comandos.

2. Navegue até o diretório que você deseja remover. Para fazer isso, use o comando "cd" seguido do caminho completo para o diretório. Por exemplo:

    ```bash
    cd /caminho/para/o/diretorio
    ```

3. Certifique-se de estar no diretório correto digitando "ls" para listar o conteúdo do diretório.

4. Use o comando "rm" com a opção "-r" e o nome do diretório para removê-lo recursivamente. Por exemplo:

    ```bash
    sudo rm -r nome_do_diretorio
    ```

    > ( ! ) Com o parâmetro `-f` o comando força a remoção sem pedir confirmação!

    ```bash
    sudo rm -rf nome_do_diretorio
    ```

5. Confirme a exclusão do diretório e de todos os seus arquivos e subdiretórios digitando "y" e pressionando "Enter" quando solicitado.

6. Aguarde enquanto o sistema exclui o diretório e seu conteúdo. Dependendo do tamanho do diretório, isso pode levar alguns minutos.

Lembre-se de ter cuidado ao usar o comando "rm" com a opção "-r", pois ele pode excluir arquivos importantes e não é possível recuperá-los. Certifique-se de que você esteja excluindo o diretório correto e que não haja arquivos importantes dentro dele antes de executar o comando.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao SumÃ¡rio") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--diret%C3%B3rios-e-arquivos "Subir para o topo")

---

## Apagar todos os arquivo de um diretório exceto um arquivo ou diretório filho

Para apagar todos os arquivos de um diretório, exceto um arquivo ou diretório filho específico no Linux via terminal, você pode usar o comando "find" com a opção "-not" e a opção "-name" para localizar todos os arquivos que não correspondem ao arquivo ou diretório que você deseja preservar, e então usar o comando "rm" para removê-los. Os seguintes passos irão guiá-lo através do processo:

1. Abra o terminal ou console de comandos.

2. Navegue até o diretório que contém os arquivos que você deseja remover, exceto o arquivo ou diretório filho específico. Por exemplo:

    ```bash
    cd /caminho/para/o/diretorio
    ```

3. Use o comando "find" com a opção "-not" e a opção "-name" para localizar todos os arquivos que não correspondem ao arquivo ou diretório que você deseja preservar. Por exemplo, para preservar o arquivo "arquivo_a_ser_preservado.txt", use o seguinte comando:

    ```bash
    sudo find . -not -name 'arquivo_a_ser_preservado.txt' -delete
    ```

    Este comando irá excluir todos os arquivos no diretório atual, exceto o arquivo "arquivo_a_ser_preservado.txt".

4. Aguarde enquanto o sistema exclui todos os arquivos no diretório, exceto o arquivo ou diretório filho que você deseja preservar.

Lembre-se de que este comando é muito poderoso e pode causar a exclusão acidental de arquivos importantes se não for usado com cuidado. Certifique-se de revisar cuidadosamente o comando antes de executá-lo e garantir que você esteja preservando o arquivo ou diretório filho desejado.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao SumÃ¡rio") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--diret%C3%B3rios-e-arquivos "Subir para o topo")

---

## Permissões a arquivos e diretórios

Para dar permissões a arquivos e diretórios no Linux via terminal, você pode usar o comando "chmod" (change mode). As permissões são definidas para três tipos de usuários: proprietário do arquivo, grupo e outros. Existem três tipos de permissões: leitura (r), escrita (w) e execução (x). Os seguintes passos irão guiá-lo através do processo:

1. Abra o terminal ou console de comandos.

2. Navegue até o arquivo ou diretório para o qual você deseja definir permissões. Por exemplo, para definir permissões para um arquivo chamado "arquivo.txt", use o seguinte comando:

    ```bash
    cd /caminho/para/o/arquivo
    ```

3. Use o comando "chmod" para definir as permissões. A sintaxe do comando é a seguinte:

    ```bash
    chmod [permissões] nome_do_arquivo
    ```

    > Ou com a opção `-R` para dar permissões a um diretório com todos os seus itens como subdiretórios e arquivos `recursivamente`.

    ```bash
    chmod -R [permissões] diretório/arquivo
    ```

Onde "[permissões]" são as permissões que você deseja definir para o arquivo ou diretório, e "nome_do_arquivo" é o nome do arquivo ou diretório que você deseja definir as permissões.

4. Defina as permissões usando os seguintes valores:

    ```bash
    r = permissão de leitura
    w = permissão de escrita
    x = permissão de execução
    ```

    Os valores são usados em conjunto para definir permissões para o proprietário do arquivo, o grupo e outros usuários. Para definir permissões para o proprietário, use "u" (user), para o grupo, use "g" (group) e para outros usuários, use "o" (others). Para definir as permissões para todos os usuários, use "a" (all). Por exemplo, para dar permissão de leitura, escrita e execução para o proprietário, permissão de leitura apenas para o grupo e permissão de execução apenas para outros usuários, use o seguinte comando:

    ```bash
    chmod u=rwx,g=r,o=x arquivo.txt
    ```

5. Confirme que as permissões foram definidas corretamente usando o comando "ls -l" para listar o arquivo ou diretório e suas permissões.

Lembre-se de que as permissões de arquivos e diretórios são uma parte importante da segurança do sistema, por isso é importante usar com cuidado e conceder apenas as permissões necessárias.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao SumÃ¡rio") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--diret%C3%B3rios-e-arquivos "Subir para o topo")

---

## Guia Rápido: Como Extrair Arquivos ZIP Usando o Terminal no Linux

Para extrair um arquivo ZIP via terminal, você pode usar o comando `unzip`. Aqui está a sintaxe básica:

```bash
unzip nome-do-arquivo.zip
```

Substitua "nome-do-arquivo.zip" pelo nome real do arquivo ZIP que você deseja extrair. Se o arquivo ZIP estiver em um diretório diferente do diretório atual do terminal, você precisará fornecer o caminho completo para o arquivo.

Por exemplo, se o arquivo ZIP estiver em sua pasta pessoal:

```bash
unzip ~/nome-do-arquivo.zip
```

Se o arquivo ZIP contiver diretórios e você quiser extrair tudo para o diretório atual, use o seguinte comando:

```bash
unzip nome-do-arquivo.zip -d .
```

Isso extrairá o conteúdo do arquivo ZIP para o diretório em que você está no momento.

Se você quiser extrair o conteúdo para um diretório específico, substitua `.` pelo caminho para o diretório de destino:

```bash
unzip nome-do-arquivo.zip -d /caminho/do/diretorio
```

Lembre-se de que o comando `unzip` precisa estar disponível no seu sistema. Se ele não estiver instalado, você pode instalá-lo usando o seguinte comando (no Debian ou Ubuntu):

```bash
sudo apt install unzip
```

Após a instalação do `unzip`, você poderá usá-lo para extrair arquivos ZIP como mencionado anteriormente.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao SumÃ¡rio") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--diret%C3%B3rios-e-arquivos "Subir para o topo")

---

