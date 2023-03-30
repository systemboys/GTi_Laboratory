# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi") / Diretórios e arquivos

[![Diretórios e arquivos](https://github.com/systemboys/GTi_Laboratory/raw/main/Debian%20Linux%20e%20derivados/Diret%C3%B3rios%20e%20arquivos/images/desktop_zero_feature_tiny.jpg "Diretórios e arquivos")](http://link.com "Diretórios e arquivos")

- [Apagar um diretório com todos os seus subdiretórios e arquivos](#apagar-um-diret%C3%B3rio-com-todos-os-seus-subdiret%C3%B3rios-e-arquivos "Apagar um diretório com todos os seus subdiretórios e arquivos")
- [Apagar todos os arquivo de um diretório exceto um arquivo ou diretório filho](#apagar-todos-os-arquivo-de-um-diret%C3%B3rio-exceto-um-arquivo-ou-diret%C3%B3rio-filho "Apagar todos os arquivo de um diretório exceto um arquivo ou diretório filho")

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

