# [Laboratório GTi](../../README.md#laborat%C3%B3rio-gti "Laboratório GTi")

## Configurações e Soluções para Ambientes Linux

[![Ambientes Linux](./images/Linux_environments.png?raw=true "Ambientes Linux")](./images/Linux_environments.png?raw=true "Ambientes Linux")

### *Sumário*

- [Como Instalar o Ambiente de Desktop Cinnamon via Terminal no Linux](#como-instalar-o-ambiente-de-desktop-cinnamon-via-terminal-no-linux "Como Instalar o Ambiente de Desktop Cinnamon via Terminal no Linux")
  - [Restauração do Ambiente Cinnamon no Debian](# "Restauração do Ambiente Cinnamon no Debian")
- [Como Desinstalar o Ambiente GNOME e Manter Apenas o Cinnamon no Linux](#como-desinstalar-o-ambiente-gnome-e-manter-apenas-o-cinnamon-no-linux "Como Desinstalar o Ambiente GNOME e Manter Apenas o Cinnamon no Linux")
- [Como Solucionar o Problema 'Falha ao Iniciar a Sessão' ao Criar um Novo Usuário no Linux](#como-solucionar-o-problema-falha-ao-iniciar-a-sess%C3%A3o-ao-criar-um-novo-usu%C3%A1rio-no-linux "Como Solucionar o Problema 'Falha ao Iniciar a Sessão' ao Criar um Novo Usuário no Linux")
- [Configurando Atalhos nos Cantos no Debian](#configurando-atalhos-nos-cantos-no-debian "Configurando Atalhos nos Cantos no Debian")

---

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Como Instalar o Ambiente de Desktop Cinnamon via Terminal no Linux

Para instalar o ambiente de desktop Cinnamon via terminal em distribuições Linux baseadas no Debian, como o Debian ou o Ubuntu, você pode usar o seguinte comando:

```bash
sudo apt-get install cinnamon-desktop-environment
```

Este comando instalará o ambiente de desktop Cinnamon e suas dependências. Lembre-se de que você precisará ter privilégios de superusuário (sudo) para executar o comando.

Depois que a instalação estiver concluída, você pode fazer logout da sua sessão atual ou reiniciar o sistema e, na tela de login, selecionar "Cinnamon" como ambiente de desktop antes de fazer login novamente.

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

### 🛠️ **Restauração do Ambiente Cinnamon no Debian**

**Problema identificado:**

* Área de trabalho do Cinnamon sem barra de tarefas;
* Ícones sem imagens;
* Ambiente gráfico incompleto após login;
* Terminal é o único funcionando.

#### ✅ **Diagnóstico inicial**

Verifique o ambiente atual:

```bash
echo $XDG_CURRENT_DESKTOP
```

#### 🔄 **Tentativa de restaurar sessão (usuário normal)**

```bash
cinnamon --replace
```

Se der erro de *session bus*, ignore e continue com os passos abaixo.

#### ♻️ **Reinstalação completa do Cinnamon**

```bash
sudo apt update
sudo apt install --reinstall cinnamon
```

#### 🧹 **Verificar e corrigir pacotes quebrados**

```bash
sudo apt install -f
```

#### 🔁 **Reinicie o sistema**

```bash
sudo reboot
```

#### ✅ **Resultado esperado**

* Área de trabalho com barra inferior restaurada;
* Ícones visuais normalizados;
* Softwares abrindo corretamente.

**Observações finais:**

* Não execute `cinnamon --replace` como root — use com o usuário normal.
* Se for necessário rodar via terminal gráfico direto:

  ```bash
  DISPLAY=:0 cinnamon --replace
  ```

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Como Desinstalar o Ambiente GNOME e Manter Apenas o Cinnamon no Linux

Para desinstalar o ambiente GNOME e manter apenas o Cinnamon (ou qualquer outro ambiente de desktop) que você instalou, você pode seguir os passos abaixo. Lembre-se de que, ao fazer isso, você pode remover aplicativos e configurações associadas ao GNOME, portanto, faça um backup dos seus dados importantes antes de prosseguir.

1. **Verifique a sessão atual**: Certifique-se de estar atualmente usando o ambiente Cinnamon ou outro ambiente de desktop que você deseja manter. Você não pode desinstalar um ambiente de desktop enquanto estiver usando-o.

2. **Abra um terminal**: Pressione `Ctrl + Alt + T` para abrir um terminal.

3. **Desinstale o GNOME**: Use o comando `apt-get` para desinstalar o ambiente GNOME. Lembre-se de que isso pode variar um pouco dependendo da versão do GNOME que você está usando (por exemplo, GNOME Shell, GNOME 3, etc.). Execute o comando correspondente:

   Para desinstalar o GNOME Shell (ambiente GNOME padrão no Ubuntu 18.04 e posterior):

   ```bash
   sudo apt-get remove gnome-shell
   ```

   Para desinstalar o GNOME 3 (ambiente GNOME nas versões mais antigas do Ubuntu):

   ```bash
   sudo apt-get remove gnome
   ```

4. **Limpe os pacotes desnecessários**: Para remover quaisquer pacotes residuais e suas dependências, execute o seguinte comando:

   ```bash
   sudo apt-get autoremove
   ```

5. **Defina um novo gerenciador de janelas (opcional)**: Se o GNOME era o seu gerenciador de janelas padrão e você deseja configurar o Cinnamon como o gerenciador de janelas padrão, use o comando a seguir para configurar o Cinnamon como gerenciador de sessão padrão:

   ```bash
   sudo dpkg-reconfigure gdm3   # Use gdm3 se estiver usando o GNOME Shell como gerenciador de janelas
   ```

   Selecione o Cinnamon na lista de gerenciadores de sessão disponíveis.

6. **Reinicie o sistema**: Para aplicar as alterações, reinicie o sistema:

   ```bash
   sudo reboot
   ```

Após reiniciar, você deve estar usando apenas o ambiente de desktop Cinnamon, com o ambiente GNOME removido. Certifique-se de verificar se tudo está funcionando conforme o esperado antes de prosseguir, pois a desinstalação de ambientes de desktop pode ter efeitos inesperados em alguns casos.

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Como Solucionar o Problema 'Falha ao Iniciar a Sessão' ao Criar um Novo Usuário no Linux

A mensagem "Falha ao iniciar a sessão" pode ser causada por várias razões no Linux. Vamos verificar algumas soluções comuns para resolver esse problema:

1. **Verifique o Nome de Usuário e Senha**: Certifique-se de que você está inserindo o nome de usuário e senha corretos ao fazer login. Preste atenção a maiúsculas e minúsculas, pois o Linux faz distinção entre elas.

2. **Verifique o Diretório Pessoal**: Certifique-se de que o diretório pessoal do usuário foi criado corretamente. O comando `adduser` normalmente cria o diretório pessoal, mas é bom verificar se ele existe:

   ```bash
   ls /home
   ```

   Você deve ver uma pasta com o nome do novo usuário.

3. **Verifique as Permissões**: Verifique se o diretório pessoal do usuário possui as permissões corretas. O diretório deve pertencer ao usuário e ao grupo do usuário. Você pode ajustar as permissões com o seguinte comando (substitua "usuario" pelo nome do seu usuário):

   ```bash
   sudo chown -R usuario:usuario /home/usuario
   ```

4. **Verifique o Shell**: Verifique se o shell padrão do usuário está configurado corretamente. Você pode verificar isso editando o arquivo `/etc/passwd`:

   ```bash
   sudo nano /etc/passwd
   ```

   Certifique-se de que a linha que corresponde ao seu usuário tenha o shell correto. O shell padrão é geralmente `/bin/bash`.

5. **Espaço em Disco Insuficiente**: Verifique se há espaço em disco suficiente no sistema. A falta de espaço em disco pode impedir o login de qualquer usuário.

6. **Arquivos de Configuração Corrompidos**: Se o problema persistir, os arquivos de configuração do usuário podem estar corrompidos. Você pode tentar criar um novo usuário e ver se o problema persiste:

   ```bash
   sudo adduser novo_usuario
   ```

   Em seguida, tente fazer login com o novo usuário para ver se o problema ocorre com ele.

Se nenhum desses passos resolver o problema, é possível que haja um problema mais complexo na configuração do sistema. Nesse caso, pode ser necessário investigar mais a fundo ou pedir ajuda de alguém com mais experiência em Linux.

---

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Configurando Atalhos nos Cantos no Debian

1. Abra o menu de aplicativos do Debian e procure por **Configurações do sistema**.
2. Clique em **Configurações do sistema** para abrir a janela principal.

![Configurações do sistema](./images/Corner_shortcuts_in_System_Settings.png "Janela principal de Configurações do sistema no Debian")

3. Dentro das **Configurações do sistema**, selecione **Atalhos nos cantos**.
4. Na janela de **Atalhos nos cantos**, ative um dos cantos ligando o interruptor correspondente.

![Configuração dos Atalhos nos cantos](./images/Shortcuts_in_the_corners.png "Janela de configuração dos atalhos nos cantos")

5. No menu suspenso, selecione **“Mostrar todas as janelas”**.
6. Para outro canto, ative a opção **“Exibir todos os espaços de trabalho”**.
7. Se desejar, ajuste o **Atraso de ativação (ms)**.
8. Pronto! Seus atalhos nos cantos estão configurados.

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

[#configurando-atalhos-nos-cantos-no-debian "Configurando Atalhos nos Cantos no Debian"]: 