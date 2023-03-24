# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi") / Usuários linux

# Sumário

- [Criar um `usuário Root`](#criar-um-usu%C3%A1rio-root "Criar um usuário Root")
- [Mudar a senha do `super usuário`](#mudar-a-senha-do-super-usu%C3%A1rio "Mudar a senha do super usuário")

---

## Criar um usuário "root"

No Linux, o usuário "root" já vem pré-instalado no sistema e é criado automaticamente durante a instalação do sistema operacional. No entanto, se você precisa criar um novo usuário com privilégios de superusuário, pode seguir os seguintes passos:

1. Faça login no sistema como um usuário com permissões de superusuário (por exemplo, o próprio "root").

2. Abra o terminal ou console de comandos.

3. Digite o seguinte comando para criar um novo usuário com o nome desejado (substitua "novo_usuario" pelo nome escolhido):

    ```bash
    sudo adduser novo_usuario
    ```

4. Em seguida, você será solicitado a definir uma senha para o novo usuário.

5. Agora, é necessário conceder ao novo usuário privilégios de superusuário. Para fazer isso, execute o seguinte comando para adicionar o novo usuário ao grupo "sudo":

    ```bash
    sudo usermod -aG sudo novo_usuario
    ```

6. Agora, o novo usuário pode executar comandos com privilégios de superusuário usando o comando "sudo". Por exemplo, para executar um comando como superusuário, o novo usuário pode digitar:

    ```bash
    sudo comando_a_ser_executado
    ```

> Lembre-se de que é importante limitar o acesso do usuário root sempre que possível e evitar usá-lo para tarefas rotineiras. Em vez disso, use um usuário comum com privilégios limitados para tarefas diárias e execute comandos como superusuário apenas quando necessário.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--usu%C3%A1rios-linux "Subir para o topo")

---

## Mudar a senha do super usuário

Para mudar a senha do superusuário "root" no Linux, você pode seguir os seguintes passos:

1. Faça login no sistema como o usuário "root" usando a senha atual.

2. Abra o terminal ou console de comandos.

3. Digite o seguinte comando para alterar a senha do superusuário:

    ```bash
    passwd
    ```

    Ou 

    ```bash
    passwd root
    ```

    > Esse último exemplo, é indicando o usuário!

4. Você será solicitado a digitar a nova senha duas vezes para confirmar. Digite a nova senha e pressione "Enter".

5. Depois de digitar a nova senha, o sistema confirmará que a senha foi alterada com sucesso.

6. Agora, a nova senha será necessária para fazer login como o superusuário "root" no futuro.

> Lembre-se de escolher uma senha forte e complexa para aumentar a segurança do sistema. Uma senha forte deve conter uma combinação de letras maiúsculas e minúsculas, números e caracteres especiais e ter pelo menos 8 caracteres de comprimento. Evite usar senhas fáceis de adivinhar, como datas de nascimento, nomes comuns ou palavras do dicionário.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--usu%C3%A1rios-linux "Subir para o topo")

---

Vogais
á = a (agudo)
ã = a (til)
à = a (case)
é = e (agudo)
ê = e (circunflexo)
í = i (agudo)
ó = o (agudo)
õ = o (til)
ú = u (agudo)

Letras consoantes
ç = c (cedilha)
