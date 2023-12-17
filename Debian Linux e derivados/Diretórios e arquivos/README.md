# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi")

## Diretórios e arquivos

[![Diretórios e arquivos](https://github.com/systemboys/GTi_Laboratory/raw/main/Debian%20Linux%20e%20derivados/Diret%C3%B3rios%20e%20arquivos/images/desktop_zero_feature_tiny.jpg "Diretórios e arquivos")](http://link.com "Diretórios e arquivos")

> Comandos e Gerenciamento de Arquivos no Terminal Linux

### *Sumário*

> Comandos básicos para Linux

- [Renomear um diretório via terminal Linux](#renomear-um-diret%C3%B3rio-via-terminal-linux "Renomear um diretório via terminal Linux")
- [Como Copiar Arquivos e Diretórios Usando o Terminal Linux](#como-copiar-arquivos-e-diret%C3%B3rios-usando-o-terminal-linux "Como Copiar Arquivos e Diretórios Usando o Terminal Linux")
    - [Como Copiar Arquivos e Pastas com Indicador de Progresso no Linux usando o Rsync](#como-copiar-arquivos-e-pastas-com-indicador-de-progresso-no-linux-usando-o-rsync "Como Copiar Arquivos e Pastas com Indicador de Progresso no Linux usando o Rsync")
    - [Explorando o Poder do Rsync: Parâmetros Essenciais para Sincronização e Cópia Eficientes de Arquivos no Linux](#explorando-o-poder-do-rsync-par%C3%A2metros-essenciais-para-sincroniza%C3%A7%C3%A3o-e-c%C3%B3pia-eficientes-de-arquivos-no-linux "Explorando o Poder do Rsync: Parâmetros Essenciais para Sincronização e Cópia Eficientes de Arquivos no Linux")
- [Mover diretório ou arquivo de um local para outro](#mover-diret%C3%B3rio-ou-arquivo-de-um-local-para-outro "Mover diretório ou arquivo de um local para outro")
- [Apagar um diretório com todos os seus subdiretórios e arquivos](#apagar-um-diret%C3%B3rio-com-todos-os-seus-subdiret%C3%B3rios-e-arquivos "Apagar um diretório com todos os seus subdiretórios e arquivos")
- [Apagar todos os arquivo de um diretório exceto um arquivo ou diretório filho](#apagar-todos-os-arquivo-de-um-diret%C3%B3rio-exceto-um-arquivo-ou-diret%C3%B3rio-filho "Apagar todos os arquivo de um diretório exceto um arquivo ou diretório filho")
- [Permissões a arquivos e diretórios](#permiss%C3%B5es-a-arquivos-e-diret%C3%B3rios "Permissões a arquivos e diretórios")
- [Concedendo Permissões 777 a Arquivos, Exceto um Diretório, ex.: .git no Linux](#concedendo-permiss%C3%B5es-777-a-arquivos-exceto-um-diret%C3%B3rio-ex-git-no-linux "Concedendo Permissões 777 a Arquivos, Exceto um Diretório, ex.: .git no Linux")
- [Listando Arquivos e Pastas Ocultos com o Comando ls no Linux](#listando-arquivos-e-pastas-ocultos-com-o-comando-ls-no-linux "Listando Arquivos e Pastas Ocultos com o Comando ls no Linux")
- [Comandos Básicos de Manipulação de Arquivos e Texto no Terminal Linux: Um Guia Detalhado](#comandos-b%C3%A1sicos-de-manipula%C3%A7%C3%A3o-de-arquivos-e-texto-no-terminal-linux-um-guia-detalhado "Comandos Básicos de Manipulação de Arquivos e Texto no Terminal Linux: Um Guia Detalhado")
- [PIPES, REDIRECIONAMENTOS, METACARACTERES e REGEX no Linux: Um Guia Detalhado](#pipes-redirecionamentos-metacaracteres-e-regex-no-linux-um-guia-detalhado "PIPES, REDIRECIONAMENTOS, METACARACTERES e REGEX no Linux: Um Guia Detalhado")

> Redes e Compartilhamento

- [Compartilhando um Diretório no Debian com o Linux Mint Usando o Samba](#compartilhando-um-diret%C3%B3rio-no-debian-com-o-linux-mint-usando-o-samba "Compartilhando um Diretório no Debian com o Linux Mint Usando o Samba")

> Compactadores

- [Guia Rápido: Como Extrair Arquivos ZIP Usando o Terminal no Linux](#guia-r%C3%A1pido-como-extrair-arquivos-zip-usando-o-terminal-no-linux "Guia Rápido: Como Extrair Arquivos ZIP Usando o Terminal no Linux")
- [Guia Rápido: Extraindo Arquivos .tar.xz via Terminal no Linux](#guia-r%C3%A1pido-extraindo-arquivos-tarxz-via-terminal-no-linux "Guia Rápido: Extraindo Arquivos .tar.xz via Terminal no Linux")

---

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

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

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Como Copiar Arquivos e Diretórios Usando o Terminal Linux

Você pode copiar arquivos de um local para outro usando o comando `cp` no terminal Linux. Aqui está a sintaxe básica:

```bash
cp origem destino
```

Substitua "origem" pelo caminho completo do arquivo ou diretório que você deseja copiar e "destino" pelo caminho para onde você deseja copiar os arquivos.

Aqui estão alguns exemplos:

1. Copiar um arquivo para um diretório:
```bash
cp arquivo.txt /caminho/do/destino/
```

2. Copiar um arquivo para o diretório atual:
```bash
cp arquivo.txt .
```

3. Copiar um arquivo com um novo nome:
```bash
cp arquivo.txt novo-arquivo.txt
```

4. Copiar um diretório inteiro com seu conteúdo:
```bash
cp -r diretorio_origem /caminho/do/destino/
```

O uso da opção `-r` é importante para copiar diretórios de maneira recursiva, ou seja, copiar todo o conteúdo dentro do diretório.

Lembre-se de que, se você estiver copiando arquivos para diretórios protegidos por permissões, como diretórios de sistema, pode ser necessário usar o comando `sudo` para executar a operação de cópia com privilégios de superusuário:

```bash
sudo cp arquivo.txt /diretorio/protegido/
```

Sempre tenha cuidado ao usar o comando `cp` para evitar sobrescrever acidentalmente arquivos existentes. É uma boa prática fazer backup ou ter certeza do que você está copiando e para onde está copiando.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Como Copiar Arquivos e Pastas com Indicador de Progresso no Linux usando o Rsync

Para copiar todo o conteúdo de um diretório para outro local via terminal no Linux e ver um indicador de progresso, você pode usar o comando `rsync` com a opção `--progress`. O `rsync` é uma ferramenta poderosa para sincronização e cópia de dados, e a opção `--progress` exibe um indicador de progresso durante a cópia.

Aqui está o comando que você pode usar:

```bash
rsync -av --progress /caminho/do/seu/diretorio/fonte/ /caminho/do/seu/diretorio/destino/
```

Neste comando:

- `/caminho/do/seu/diretorio/fonte/` é o caminho do diretório que você quer copiar.
- `/caminho/do/seu/diretorio/destino/` é o caminho do diretório para onde você quer copiar os arquivos.

O `-av` é para copiar recursivamente e exibir informações verbosas (indicador de andamento).

Certifique-se de substituir `/caminho/do/seu/diretorio/fonte/` pelo caminho real do diretório de origem e `/caminho/do/seu/diretorio/destino/` pelo caminho real do diretório de destino.

Isso copiará todos os arquivos e pastas do diretório de origem para o diretório de destino, exibindo um indicador de progresso no terminal.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Explorando o Poder do Rsync: Parâmetros Essenciais para Sincronização e Cópia Eficientes de Arquivos no Linux

O `rsync` é uma ferramenta poderosa para copiar e sincronizar arquivos e diretórios em sistemas Unix e Linux. Aqui está uma lista de alguns parâmetros comuns e suas descrições:

1. `-a` (ou `--archive`): Copia recursivamente, preserva permissões, propriedades, timestamps e links simbólicos. É equivalente a `-rlptgoD`.

2. `-v` (ou `--verbose`): Exibe informações verbosas sobre o progresso da transferência.

3. `-z` (ou `--compress`): Comprime os dados durante a transferência, o que pode economizar largura de banda, especialmente ao copiar através da rede.

4. `--delete`: Remove arquivos no destino que não existem mais no origem, tornando o destino uma cópia exata do origem.

5. `--exclude`: Permite excluir arquivos ou diretórios específicos da cópia, usando padrões de exclusão.

6. `--include`: Especifica quais arquivos ou diretórios incluir na cópia, quando usado em conjunto com `--exclude`.

7. `-n` (ou `--dry-run`): Simula a operação de cópia, exibindo o que seria copiado, mas não faz as alterações no destino.

8. `--progress`: Mostra um indicador de progresso durante a cópia, exibindo o percentual concluído.

9. `--bwlimit`: Define um limite de largura de banda para a transferência em KBytes por segundo.

10. `-P` (ou `--partial`): Mantém arquivos parcialmente transferidos em caso de interrupção, permitindo retomar a transferência posteriormente.

11. `-r` (ou `--recursive`): Copia diretórios e seu conteúdo recursivamente.

12. `-l` (ou `--links`): Copia links simbólicos como links simbólicos em vez de seguir o link e copiar o arquivo de destino.

13. `-t` (ou `--times`): Preserva os timestamps dos arquivos copiados.

14. `-o` (ou `--owner`): Preserva o proprietário dos arquivos copiados.

15. `-g` (ou `--group`): Preserva o grupo dos arquivos copiados.

16. `-D` (ou `--devices`): Copia dispositivos especiais.

17. `-H` (ou `--hard-links`): Preserva hard links entre arquivos.

18. `-c` (ou `--checksum`): Verifica a integridade dos arquivos usando checksums, em vez de depender apenas de timestamps e tamanhos de arquivo.

19. `--size-only`: Considera apenas diferenças de tamanho de arquivo ao decidir se um arquivo deve ser copiado.

20. `--ignore-errors`: Ignora erros não fatais, permitindo que o `rsync` continue copiando outros arquivos.

21. `-e` (ou `--rsh`): Especifica o shell remoto a ser usado para a transferência. Por padrão, usa o SSH.

22. `--daemon`: Inicia o `rsync` em modo daemon, permitindo a comunicação com outros sistemas.

Lembre-se de que o `rsync` é uma ferramenta flexível e pode ser usada de várias maneiras, combinando esses parâmetros de acordo com suas necessidades específicas. Certifique-se de ler a documentação do `rsync` (`man rsync`) para obter informações detalhadas sobre todos os parâmetros disponíveis e suas opções.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

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

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

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

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

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

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

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

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Concedendo Permissões 777 a Arquivos, Exceto um Diretório, ex.: .git no Linux

Você pode usar o comando `find` em combinação com o `chmod` para conceder permissões 777 a todos os arquivos, exceto aqueles dentro do diretório `.git`. Aqui está um exemplo de como fazer isso:

```bash
find . -type f -not -path "./.git/*" -exec chmod 777 {} \;
```

Este comando faz o seguinte:

- `find .`: Procura no diretório atual.
- `-type f`: Seleciona apenas os arquivos.
- `-not -path "./.git/*"`: Exclui todos os arquivos que estão dentro do diretório `.git`.
- `-exec chmod 777 {} \;`: Executa o comando `chmod 777` nos arquivos encontrados, concedendo permissões de leitura, escrita e execução.

Certifique-se de executar este comando no diretório raiz do seu repositório Git local. Isso dará permissões 777 a todos os arquivos, exceto aqueles dentro do diretório `.git`.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Listando Arquivos e Pastas Ocultos com o Comando ls no Linux

Para listar não apenas os itens visíveis, mas também os ocultos em um diretório usando o comando `ls` no Linux, você pode usar a opção `-a` ou `--all`. Essa opção faz com que o `ls` mostre todos os arquivos, incluindo os ocultos, que começam com um ponto `.`.

Aqui está como fazer:

```bash
ls -a
```

ou

```bash
ls --all
```

Quando você usar um desses comandos, o `ls` exibirá todos os itens, incluindo os ocultos, no diretório atual. Isso é útil para visualizar todos os arquivos e pastas, inclusive os que normalmente não são mostrados ao usar apenas o comando `ls`.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Comandos Básicos de Manipulação de Arquivos e Texto no Terminal Linux: Um Guia Detalhado

Esses são comandos bastante úteis no Linux. Vou explicar cada um deles com um exemplo:

1. **`cat`** - O comando `cat` é usado para mostrar o conteúdo de um arquivo.

   Exemplo: `cat arquivo.txt` - Isso exibirá o conteúdo do arquivo `arquivo.txt` no terminal.

2. **`head`** - O comando `head` é usado para mostrar as primeiras linhas de um arquivo.

   Exemplo: `head -n 10 arquivo.txt` - Isso exibirá as 10 primeiras linhas do arquivo `arquivo.txt`.

3. **`tail`** - O comando `tail` é usado para mostrar as últimas linhas de um arquivo.

   Exemplo: `tail -n 5 arquivo.txt` - Isso exibirá as últimas 5 linhas do arquivo `arquivo.txt`.

4. **`wc`** - O comando `wc` é usado para contar palavras, linhas e caracteres em um arquivo.

   Exemplo: `wc arquivo.txt` - Isso mostrará o número de linhas, palavras e caracteres no arquivo `arquivo.txt`.

5. **`nl`** - O comando `nl` é usado para numerar as linhas de um arquivo.

   Exemplo: `nl arquivo.txt` - Isso numerará as linhas do arquivo `arquivo.txt`.

6. **`grep`** - O comando `grep` é usado para pesquisar padrões em arquivos.

   Exemplo: `grep "palavra" arquivo.txt` - Isso mostrará todas as linhas em `arquivo.txt` que contêm a palavra "palavra".

7. **`sed`** - O comando `sed` é um editor de fluxo usado para realizar transformações em texto.

   Exemplo: `sed 's/velho/novo/g' arquivo.txt` - Isso substituirá todas as ocorrências de "velho" por "novo" no `arquivo.txt`.

8. **`awk`** - O comando `awk` é uma linguagem de programação para processamento de texto.

   Exemplo: `awk '{print $1}' arquivo.txt` - Isso imprimirá a primeira coluna de `arquivo.txt` para cada linha.

9. **`vim`** - O Vim é um editor de texto poderoso e altamente configurável.

   Exemplo: `vim arquivo.txt` - Isso abrirá o arquivo `arquivo.txt` no Vim para edição.

10. **`nano`** - O Nano é um editor de texto fácil de usar para o terminal.

   Exemplo: `nano novo_arquivo.txt` - Isso abrirá um novo arquivo chamado `novo_arquivo.txt` no Nano para edição.

Esses comandos são fundamentais para qualquer usuário do Linux que trabalhe com texto e arquivos de forma regular. Cada um tem suas próprias funcionalidades específicas, tornando-os muito versáteis em várias situações.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## PIPES, REDIRECIONAMENTOS, METACARACTERES e REGEX no Linux: Um Guia Detalhado

### Pipes (|):
Pipes são usados para direcionar a saída de um comando para a entrada de outro. Eles permitem que você combine vários comandos para criar operações mais complexas.

Exemplo:
```bash
ls -l | grep ".txt"
```
Neste exemplo, a saída do comando `ls -l` (que lista todos os arquivos no diretório com detalhes) é direcionada para o comando `grep ".txt"`, que filtra apenas os arquivos com extensão ".txt".

### Redirecionamentos (>, >>, <):
Redirecionamentos são usados para controlar a entrada e saída de comandos. `>` é usado para redirecionar a saída de um comando para um arquivo. `>>` é usado para adicionar a saída de um comando a um arquivo existente. `<` é usado para fornecer a entrada para um comando a partir de um arquivo.

Exemplo:
```bash
echo "Olá, Mundo!" > arquivo.txt
```
Neste exemplo, a frase "Olá, Mundo!" é escrita no arquivo `arquivo.txt`.

### Metacaracteres (*, ?, []):
Metacaracteres são caracteres especiais que têm significados especiais no contexto da linha de comando. `*` corresponde a zero ou mais caracteres. `?` corresponde a um único caractere. `[]` corresponde a qualquer caractere dentro dos colchetes.

Exemplo:
```bash
ls *.txt
```
Neste exemplo, `*.txt` corresponde a todos os arquivos com extensão ".txt" no diretório atual.

### Expressões Regulares (Regex):
Expressões Regulares são padrões utilizados para fazer correspondência de padrões em texto. São muito poderosas e flexíveis para encontrar, substituir ou manipular texto com base em padrões complexos.

Exemplo:
```bash
grep "^[A-Z].*ing$" arquivo.txt
```
Neste exemplo, a expressão regular `^[A-Z].*ing$` corresponde a linhas que começam com uma letra maiúscula e terminam com "ing" no arquivo `arquivo.txt`.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Compartilhando um Diretório no Debian com o Linux Mint Usando o Samba

Para compartilhar um diretório do Debian para que você possa acessá-lo a partir do Linux Mint, você pode configurar o servidor Samba. O Samba é uma implementação do protocolo SMB/CIFS que permite compartilhar arquivos e impressoras entre sistemas Linux e Windows na mesma rede.

Aqui está um guia passo a passo para configurar o compartilhamento de diretórios usando o Samba:

1. **Instalar o Samba**:

   No Debian, abra um terminal e execute os seguintes comandos para instalar o Samba:

   ```bash
   sudo apt update
   sudo apt install samba
   ```

2. **Configurar o Compartilhamento**:

   Edite o arquivo de configuração do Samba usando um editor de texto, como o `nano` ou o `vim`:

   ```bash
   sudo nano /etc/samba/smb.conf
   ```

   Dentro do arquivo, adicione as configurações do compartilhamento no final:

   ```plaintext
   [NomeCompartilhamento]
   path = /caminho/para/o/diretorio
   valid users = seu_usuario
   read only = no
   ```

   Substitua `NomeCompartilhamento` pelo nome que você deseja dar ao compartilhamento, `/caminho/para/o/diretorio` pelo caminho absoluto do diretório que você deseja compartilhar e `seu_usuario` pelo seu nome de usuário no Debian.

3. **Definir uma Senha para o Usuário Samba**:

   Execute o seguinte comando para definir uma senha para o usuário Samba (você precisará definir uma senha separada do seu usuário do sistema):

   ```bash
   sudo smbpasswd -a seu_usuario
   ```

4. **Reiniciar o Serviço Samba**:

   Após fazer as configurações, reinicie o serviço Samba:

   ```bash
   sudo systemctl restart smbd
   ```

5. **Acesso do Linux Mint**:

   No Linux Mint, você pode usar o gerenciador de arquivos Caja para acessar o compartilhamento. Abra o Caja e vá para `Rede -> Windows Network -> NomeDoComputador -> NomeCompartilhamento`. Ele pode solicitar suas credenciais Samba (o nome de usuário e senha definidos com `smbpasswd`).

Isso permitirá que você acesse o diretório compartilhado do Debian a partir do Linux Mint na mesma rede local.

Lembre-se de que as configurações de firewall e permissões de acesso podem afetar a capacidade de compartilhamento e acesso. Certifique-se de que o firewall permita o tráfego necessário (geralmente a porta 445 para o Samba) e que as permissões de compartilhamento e do diretório estejam configuradas corretamente.

> ( i ) Dica: Configurando um Compartilhamento Somente Leitura no Samba no Linux.

Se você deseja configurar um compartilhamento no Samba que seja somente leitura, ou seja, os usuários não podem modificar os arquivos, você pode ajustar as configurações da seguinte forma:

```bash
[NomeCompartilhamento]
path = /caminho/para/o/diretorio
valid users = seu_usuario
read only = yes
```

Note que a única mudança em relação à configuração anterior é definir `read only` como `yes`. Isso faz com que os usuários tenham apenas acesso de leitura ao compartilhamento, sem a permissão de modificar ou criar novos arquivos.

Ao usar essa configuração, os usuários que acessarem o compartilhamento apenas poderão visualizar o conteúdo, sem poder editar, mover ou excluir arquivos. Certifique-se de que as permissões de acesso aos arquivos no sistema de arquivos também estejam configuradas corretamente para evitar conflitos.

> ( i ) Configurar mais de um diretório para compartilhamento.

Sim, você pode configurar mais de um diretório para compartilhamento no Samba replicando as linhas de configuração para cada diretório que deseja compartilhar. Cada seção de configuração representa um compartilhamento separado. Por exemplo:

```bash
[Compartilhamento1]
path = /caminho/para/o/diretorio1
valid users = seu_usuario
read only = yes

[Compartilhamento2]
path = /caminho/para/o/diretorio2
valid users = seu_usuario
read only = no
```

Nesse exemplo, dois compartilhamentos diferentes, "Compartilhamento1" e "Compartilhamento2", são configurados. Você pode adicionar quantos compartilhamentos desejar seguindo esse padrão. Lembre-se de ajustar os valores de `path`, `valid users` e outras opções de acordo com suas necessidades.

Após fazer as alterações no arquivo de configuração do Samba, você precisará reiniciar o serviço para que as alterações entrem em vigor:

```bash
sudo service smbd restart
```

Certifique-se de também ajustar as permissões de acesso nos diretórios no sistema de arquivos para garantir que os usuários tenham as permissões apropriadas para os compartilhamentos.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

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

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Guia Rápido: Extraindo Arquivos .tar.xz via Terminal no Linux

Para extrair arquivos no formato ".tar.xz" via terminal, você pode usar o comando `tar`. No Linux, o `tar` é uma ferramenta amplamente utilizada para criar, manipular e extrair arquivos compactados. O formato ".tar.xz" combina o empacotamento de arquivos usando o comando `tar` com a compressão usando o algoritmo XZ.

Aqui está a sintaxe básica para extrair arquivos ".tar.xz":

```bash
tar -xvf nome-do-arquivo.tar.xz
```

- `-x`: Indica que você deseja extrair arquivos.
- `-v`: Exibe a saída detalhada, mostrando os arquivos sendo extraídos.
- `-f`: Indica que você está especificando o arquivo que deseja extrair.

Substitua "nome-do-arquivo.tar.xz" pelo nome real do arquivo que você deseja extrair.

Você também pode usar opções adicionais para especificar um diretório de destino para a extração ou para incluir/excluir arquivos específicos. Aqui estão alguns exemplos:

- Para extrair em um diretório específico:
  ```bash
  tar -xvf nome-do-arquivo.tar.xz -C /caminho/do/diretorio
  ```

- Para extrair apenas um arquivo específico:
  ```bash
  tar -xvf nome-do-arquivo.tar.xz arquivo-desejado.txt
  ```

Lembre-se de que o comando `tar` é bastante versátil e possui várias opções que você pode explorar usando o `man tar` no terminal ou consultando sua documentação online.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

