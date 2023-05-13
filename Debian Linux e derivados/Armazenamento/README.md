# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi") / Armazenamento

[![Imagem 1](https://site.com/img/exemplo.png "Imagem 1")](http://link.com "Imagem 1")

- [Como formatar e criar partições em um SSD no Linux via terminal](#como-formatar-e-criar-partições-em-um-ssd-no-linux-via-terminal "Como formatar e criar partições em um SSD no Linux via terminal")

---

## Como formatar e criar partições em um SSD no Linux via terminal

Para formatar e criar partições em um SSD no Linux via terminal, você pode seguir estes passos:

1. Abra o terminal no seu sistema Linux.

2. Digite o seguinte comando para iniciar o utilitário de particionamento:

   ```bash
   sudo fdisk /dev/sdb
   ```

   Substitua `/dev/sdb` pelo caminho correto do seu SSD, caso seja diferente.

3. No prompt do `fdisk`, digite `n` para criar uma nova partição.

4. Escolha o tipo de partição que deseja criar. Para uma partição primária, digite `p`. Se desejar criar uma partição estendida, digite `e`.

5. Escolha o número da partição. Para a primeira partição, digite `1`.

6. Em seguida, especifique o primeiro setor da partição. Pressione Enter para usar o valor padrão e usar todo o espaço disponível.

7. Especifique o último setor da partição. Pressione Enter para usar o valor padrão e usar todo o espaço disponível.

8. Agora que a partição foi criada, você pode definir o tipo de sistema de arquivos para ela. Digite o comando `t` e selecione o código correspondente ao sistema de arquivos desejado. Por exemplo, para usar o sistema de arquivos ext4, você pode digitar `83`.

9. Depois de definir o tipo de sistema de arquivos, digite `w` para gravar as alterações na tabela de partições e sair do utilitário `fdisk`.

10. Agora, você pode formatar a partição com o sistema de arquivos desejado. Por exemplo, se você escolheu o sistema de arquivos ext4, pode usar o seguinte comando para formatar a partição:

    ```bash
    sudo mkfs.ext4 /dev/sdb1
    ```

    Certifique-se de substituir `/dev/sdb1` pelo caminho correto da partição que você criou.

Após seguir esses passos, a partição do SSD será criada e formatada com o sistema de arquivos escolhido. Você pode montar a partição em um diretório de sua escolha para começar a usá-la.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--armazenamento "Subir para o topo")

---