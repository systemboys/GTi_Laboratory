# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi")

## Usuários linux

### *Sumário*

> Gerenciando Usuários no Linux
- [Criar um `usuário Root`](#criar-um-usu%C3%A1rio-root "Criar um usuário Root")
- [Concedendo Privilégios de Superusuário a um Usuário no Linux usando o Grupo sudo](#concedendo-privil%C3%A9gios-de-superusu%C3%A1rio-a-um-usu%C3%A1rio-no-linux-usando-o-grupo-sudo "Concedendo Privilégios de Superusuário a um Usuário no Linux usando o Grupo sudo")
- [Removendo Usuários via Terminal](#removendo-usu%C3%A1rios-via-terminal "Removendo Usuários via Terminal")
- [Editando Configurações de Usuários no Linux com o Comando usermod](#editando-configura%C3%A7%C3%B5es-de-usu%C3%A1rios-no-linux-com-o-comando-usermod "Editando Configurações de Usuários no Linux com o Comando usermod")
- [Mudar a senha do `super usuário`](#mudar-a-senha-do-super-usu%C3%A1rio "Mudar a senha do super usuário")
   - [Redefinindo Senha do Usuário Root e Executando um Script em uma Linha de Comando](# "Redefinindo Senha do Usuário Root e Executando um Script em uma Linha de Comando")

---

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

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

Lembre-se de que é importante limitar o acesso do usuário root sempre que possível e evitar usá-lo para tarefas rotineiras. Em vez disso, use um usuário comum com privilégios limitados para tarefas diárias e execute comandos como superusuário apenas quando necessário.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Concedendo Privilégios de Superusuário a um Usuário no Linux usando o Grupo sudo

Para conceder a um usuário a capacidade de executar comandos com privilégios de superusuário no Linux, você pode adicionar esse usuário ao grupo `sudo`. O grupo `sudo` é geralmente configurado para permitir que os membros executem comandos com `sudo`, o que lhes concede temporariamente privilégios de superusuário.

Aqui estão os passos para adicionar um usuário ao grupo `sudo` e conceder-lhe privilégios de superusuário:

1. Abra um terminal.

2. Execute o seguinte comando para adicionar o usuário ao grupo `sudo`, substituindo `name_user` pelo nome do usuário que você deseja conceder privilégios de superusuário:

   ```bash
   sudo usermod -aG sudo name_user
   ```

   O parâmetro `-aG` significa "adicionar ao grupo", e `sudo` é o nome do grupo que concede privilégios de superusuário.

3. Após adicionar o usuário ao grupo `sudo`, você pode testar os privilégios de superusuário executando um comando com `sudo`. Por exemplo, para atualizar o índice de pacotes do sistema, você pode usar o seguinte comando:

   ```bash
   sudo apt update
   ```

   Você será solicitado a inserir a senha do seu usuário para confirmar a ação.

A partir deste ponto, o usuário `name_user` terá a capacidade de executar comandos com privilégios de superusuário usando `sudo`. Isso elimina a necessidade de usar `su` para trocar para o superusuário, mas ainda exigirá a autenticação com a senha do próprio usuário ao usar `sudo`. Certifique-se de usar esses privilégios com responsabilidade, pois comandos errados podem afetar o sistema.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Removendo Usuários via Terminal

Para remover um usuário via terminal no Linux, você pode usar o comando `sudo deluser nome_usuario`. No entanto, esse comando remove o usuário, mas não exclui os arquivos pessoais associados a esse usuário. Se você deseja excluir completamente o usuário e seus arquivos, pode usar `sudo deluser --remove-home nome_usuario`.

Portanto, você tem duas opções, dependendo se deseja manter ou excluir os arquivos do usuário:

1. Para remover o usuário, mas manter seus arquivos pessoais (casa), use:

   ```bash
   sudo deluser nome_usuario
   ```

2. Para remover o usuário e todos os seus arquivos pessoais, use:

   ```bash
   sudo deluser --remove-home nome_usuario
   ```

Certifique-se de substituir "nome_usuario" pelo nome real do usuário que você deseja remover. Lembre-se de que você precisará ter privilégios de administrador (sudo) para executar esses comandos. Certifique-se de fazer isso com cuidado, pois a remoção de um usuário é uma ação irreversível e seus arquivos serão perdidos.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Editando Configurações de Usuários no Linux com o Comando usermod

Para editar as configurações de um usuário no Linux, como alterar informações de conta, senha, grupos e outros detalhes, você pode usar o comando `sudo usermod`. Aqui estão alguns exemplos de como você pode usar o `usermod` para editar as configurações de um usuário:

1. **Alterar o Nome Completo do Usuário:**
   
   ```bash
   sudo usermod -c "Novo Nome Completo" nome_usuario
   ```

2. **Mudar o Diretório Home do Usuário:**
   
   ```bash
   sudo usermod -d /novo/caminho/para/diretorio nome_usuario
   ```

3. **Adicionar o Usuário a um Grupo:**
   
   ```bash
   sudo usermod -aG nome_do_grupo nome_usuario
   ```

4. **Mudar a Senha do Usuário:**
   
   ```bash
   sudo passwd nome_usuario
   ```

Lembre-se de substituir "nome_usuario" pelo nome real do usuário e os valores relevantes nas outras opções.

Importante: Tome cuidado ao usar esses comandos, pois eles podem afetar a configuração do usuário e até mesmo o acesso ao sistema. Certifique-se de verificar a documentação relevante (`man usermod`) ou use a opção `-h` para obter ajuda com um comando específico.

A edição de usuários geralmente requer privilégios de administrador (sudo), pois envolve alterações nas configurações do sistema. Certifique-se de que está fazendo alterações com cuidado e de acordo com as necessidades do sistema.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

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
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Redefinindo Senha do Usuário Root e Executando um Script em uma Linha de Comando

Sim, você pode fazer isso em uma única linha de comando usando uma tubulação de comandos no terminal. A sintaxe seria a seguinte:

```bash
echo "nova_senha" | sudo passwd root && echo "nova_senha" | su -c './arquivo.sh' root
```

Neste comando:

- `echo "nova_senha" | sudo passwd root` redefine a senha do usuário root.
- `echo "nova_senha" | su -c './arquivo.sh' root` tentará fazer login como root usando a nova senha e, se bem-sucedido, executará o arquivo shell script `arquivo.sh`.

Lembre-se de substituir `"nova_senha"` pela senha desejada.

No entanto, este método de fornecer senhas diretamente no terminal pode ser inseguro, pois deixa as senhas visíveis no histórico do terminal e em processos em execução. Em ambientes de produção ou em sistemas críticos, é altamente recomendável utilizar métodos mais seguros para gerenciar senhas e autenticações, como o uso de chaves SSH e políticas de segurança adequadas.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

