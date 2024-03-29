# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi")
# Linode - Akamai Cloud Computing

[![Linode - Akamai Cloud Computing](https://github.com/systemboys/GTi_Laboratory/blob/main/Computa%C3%A7%C3%A3o%20em%20Nuvens/Linode%20-%20Akamai%20Cloud%20Computing/images/linode.png?raw=true "Linode - Akamai Cloud Computing")](https://github.com/systemboys/GTi_Laboratory/blob/main/Computa%C3%A7%C3%A3o%20em%20Nuvens/Linode%20-%20Akamai%20Cloud%20Computing/images/linode.png?raw=true "Linode - Akamai Cloud Computing")

### *Sumário*

- [Linode e Akamai: Explorando Duas Perspectivas Diferentes da Computação em Nuvem](#linode-e-akamai-explorando-duas-perspectivas-diferentes-da-computa%C3%A7%C3%A3o-em-nuvem "Linode e Akamai: Explorando Duas Perspectivas Diferentes da Computação em Nuvem")
- [Kali Linux Cloud Deploy na Linode](#kali-linux-cloud-deploy-na-linode "Kali Linux Cloud Deploy na Linode")
   - [Acessar o Kali Linux](#acessar-o-kali-linux "Acessar o Kali Linux")
   - [Alias (Apelido)](#alias-apelido "Alias (Apelido)")
   - [Como Conectar-se a uma VM Linode Usando o Visualizador TigerVNC e um Túnel SSH no Linux](#como-conectar-se-a-uma-vm-linode-usando-o-visualizador-tigervnc-e-um-t%C3%BAnel-ssh-no-linux "Como Conectar-se a uma VM Linode Usando o Visualizador TigerVNC e um Túnel SSH no Linux")
   - [Como Conectar-se a uma VM Linode Usando o Remmina e um Túnel SSH no Linux](#como-conectar-se-a-uma-vm-linode-usando-o-remmina-e-um-t%C3%BAnel-ssh-no-linux "Como Conectar-se a uma VM Linode Usando o Remmina e um Túnel SSH no Linux")
   - [Como Encerrar um Túnel SSH para uma Conexão VNC em um Servidor Remoto](#como-encerrar-um-t%C3%BAnel-ssh-para-uma-conex%C3%A3o-vnc-em-um-servidor-remoto "Como Encerrar um Túnel SSH para uma Conexão VNC em um Servidor Remoto")

---

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Linode e Akamai: Explorando Duas Perspectivas Diferentes da Computação em Nuvem

A "Linode" não é uma subsidiária da "Akamai" nem uma grande provedora de serviços de computação em nuvem. Na verdade, a "Linode" é uma empresa independente que oferece serviços de hospedagem na nuvem, principalmente conhecida por fornecer soluções de hospedagem de servidores virtuais privados (VPS) a preços competitivos.

Por outro lado, a "Akamai Technologies" é uma empresa global de serviços em nuvem que oferece uma ampla gama de serviços relacionados à entrega de conteúdo, segurança na web, otimização de desempenho e muito mais. A "Akamai" é conhecida por sua rede de distribuição de conteúdo (CDN) de alta velocidade e segurança.

Portanto, não há uma relação direta entre a "Linode" e a "Akamai" em termos de propriedade ou operações conjuntas. Ambas são empresas independentes que oferecem serviços relacionados à computação em nuvem, mas com foco em áreas diferentes.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Kali Linux Cloud Deploy na Linode

Tudo que você precisa para ter um Kali Linux na nuvem. Segue o passo a passo.

1. Acesso o site da [Linode](https://linode.com "Acesse o Linode.com") e crie uma conta.

2. Depois de logado, você estará no painel **Linode**, lá você deve procurar o link **Create Linode**, na **Aba** "Marketplace" você encontrará a opção do **Kali Linux** e depois de selecionar, role para baixo para fazer algumas configurações.

3. Na sessão **Kali Linux Options**, você dará criar um `usuário` e `senha` para o módulo `VNC` para acessar o Kali Linux com interface gráfica através de softwares VNC.

4. Em **Advanced Options**, deixe todas as opções em **Yes**, menos a opção "Disable root access over SSH", essa pode deixar marcada **No**. A menos que você queira desabilitar o acesso ao **Root** via **SSH**.

5. Mas a baixo, você deve escolher uma **Região**. Onde é definido em qual datacenter estará o Kali Linux.

6. Na sessão **Linode Plan**, em **Shared CPU** selecione a configuração de hardware que você precisa para o servidor.

7. Na sessão **Linode Label** informe um nome para seu servidor.

8. Na sessão **Root Password** defina uma senha de root para o servidor.

9. Por fim, para terminar de criar a VM, clique em **Create Linode** e aguarde o servidor ser provisionado.

   >  **( i )** Esse processo demorará alguns minutos e, você pode acompanhar clicando em **Launch LISH Console**, é um terminal no servidor Kali Linux onde você verá que ainda estará sendo realizado o processo de construção do Kali Linux.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

### Acessar o Kali Linux

Acessar o Kali Linux do servidor diretamente com interface gráfica XFCE. Criando um túnel via SSH para criar uma conexão VNC para o servidor.

```bash
ssh -L 61000:localhost:5901 -N -f username@123.231.132.133
```

> **( ! )** Informe a senha VNC que você criou!

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

### Alias (Apelido)

Criando um atalho para o comando SSH para acessar sua máquina via VNC.
No terminal, no diretório pessoa digite o seguinte comando como no exemplo abaixo:

```bash
marcos@10:~$ su
Senha: 
root@10:/home/marcos# nano .bashrc
```

> **( i )** No seu usuário `marcos@10:~$` foi digitado `su`, informado a senha do super usuário e depois o comando `nano .bashrc`.

O arquivo `.bashrc` será exibido e rolando um pouco para baixo, verá os "alias".

[![Alias no .BashRC](https://github.com/systemboys/GTi_Laboratory/blob/main/Computa%C3%A7%C3%A3o%20em%20Nuvens/Linode%20-%20Akamai%20Cloud%20Computing/images/Alias-BashRC.png?raw=true "Alias no .BashRC")](https://github.com/systemboys/GTi_Laboratory/blob/main/Computa%C3%A7%C3%A3o%20em%20Nuvens/Linode%20-%20Akamai%20Cloud%20Computing/images/Alias-BashRC.png?raw=true "Alias no .BashRC")

Como no exemplo na imagem, adicione a linha com o atalho:

```bash
# Meus atalhos customizados
alias kali-murdock='ssh -L 61000:localhost:5901 -N -f marcos@170.187.154.205'
```

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

### Como Conectar-se a uma VM Linode Usando o Visualizador TigerVNC e um Túnel SSH no Linux

Depois desse comando, o túnel estará rodando em background como um processo. A partir daí, precisa-se de um aplicativo VNC View para acessa o Kali Linux. Abaixo segue dois aplicativos que conseguem fazer a conexão via VNC.

[![Visualizador TigerVNC](https://github.com/systemboys/GTi_Laboratory/blob/main/Computa%C3%A7%C3%A3o%20em%20Nuvens/Linode%20-%20Akamai%20Cloud%20Computing/images/Visualizador_TigerVNC_logo.png?raw=true "Visualizador TigerVNC")](https://github.com/systemboys/GTi_Laboratory/blob/main/Computa%C3%A7%C3%A3o%20em%20Nuvens/Linode%20-%20Akamai%20Cloud%20Computing/images/Visualizador_TigerVNC_logo.png?raw=true "Visualizador TigerVNC")

[![Visualizador TigerVNC form](https://github.com/systemboys/GTi_Laboratory/blob/main/Computa%C3%A7%C3%A3o%20em%20Nuvens/Linode%20-%20Akamai%20Cloud%20Computing/images/Visualizador_TigerVNC_form.png?raw=true "Visualizador TigerVNC form")](https://github.com/systemboys/GTi_Laboratory/blob/main/Computa%C3%A7%C3%A3o%20em%20Nuvens/Linode%20-%20Akamai%20Cloud%20Computing/images/Visualizador_TigerVNC_form.png?raw=true "Visualizador TigerVNC form")

[![Visualizador TigerVNC Kali Linux](https://github.com/systemboys/GTi_Laboratory/blob/main/Computa%C3%A7%C3%A3o%20em%20Nuvens/Linode%20-%20Akamai%20Cloud%20Computing/images/Visualizador_TigerVNC_Kali_Linux.png?raw=true "Visualizador TigerVNC Kali Linux")](https://github.com/systemboys/GTi_Laboratory/blob/main/Computa%C3%A7%C3%A3o%20em%20Nuvens/Linode%20-%20Akamai%20Cloud%20Computing/images/Visualizador_TigerVNC_Kali_Linux.png?raw=true "Visualizador TigerVNC Kali Linux")

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

### Como Conectar-se a uma VM Linode Usando o Remmina e um Túnel SSH no Linux

Claro, aqui estão as instruções para se conectar a uma VM Linode usando o Remmina:

1. **Abra o Remmina**: Caso você tenha o aplicativo Remmina instalado em seu sistema, abra-o.

![Remmina](https://github.com/systemboys/GTi_Laboratory/blob/main/Computa%C3%A7%C3%A3o%20em%20Nuvens/Linode%20-%20Akamai%20Cloud%20Computing/images/Remmina_1.png?raw=true)

2. **Crie um Novo Perfil de Conexão**:
   - Com o Remmina aberto, clique no botão "Novo perfil de conexão" para configurar uma nova conexão.

![Novo Perfil de Conexão](https://github.com/systemboys/GTi_Laboratory/blob/main/Computa%C3%A7%C3%A3o%20em%20Nuvens/Linode%20-%20Akamai%20Cloud%20Computing/images/Remmina_2.png?raw=true)

3. **Configure os Detalhes da Conexão**:
   - Dentro das configurações do perfil de conexão, forneça os detalhes da sua conexão. Certifique-se de configurar os seguintes campos:
     - **Nome da Conexão**: Dê um nome para identificar essa conexão.
     - **Protocolo**: Selecione o protocolo apropriado para sua conexão (por exemplo, VNC).
     - **Servidor**: Insira "localhost" como o endereço do servidor, pois você criou um túnel SSH local.
     - **Porta**: Digite a porta que você especificou ao criar o túnel SSH (por exemplo, 61000).
     - **Nome de Usuário**: Insira seu nome de usuário SSH.
     - **Senha**: Se necessário, insira a senha associada à sua conta SSH.

4. **Salve o Perfil de Conexão**: Após configurar todos os detalhes, clique no botão "Salvar" para salvar o perfil de conexão.

5. **Inicie a Conexão**: Agora, você pode selecionar o perfil de conexão recém-criado na lista de conexões disponíveis e clicar no botão "Conectar" para iniciar a conexão com a sua VM Linode via o túnel SSH configurado.

![Kali Linux no Remmina](https://github.com/systemboys/GTi_Laboratory/blob/main/Computa%C3%A7%C3%A3o%20em%20Nuvens/Linode%20-%20Akamai%20Cloud%20Computing/images/Remmina_3.png?raw=true)

Lembre-se de que a segurança é fundamental. Certifique-se de usar senhas fortes e manter suas credenciais seguras.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

### Como Encerrar um Túnel SSH para uma Conexão VNC em um Servidor Remoto

Para fechar o túnel SSH que você criou para a conexão VNC, você pode seguir estas etapas:

1. Abra um terminal no seu sistema local (não no servidor remoto onde o Kali Linux está sendo executado).

2. Use o comando `ps aux | grep ssh` para listar os processos relacionados ao SSH e identificar o processo que está mantendo o túnel VNC ativo. Isso fornecerá uma lista de processos relacionados ao SSH, incluindo seus IDs de processo (PID).

3. Encontre o processo que corresponde ao túnel SSH que você deseja fechar. O processo relacionado ao túnel SSH geralmente terá informações sobre o servidor e a porta do túnel na linha de comando.

4. Use o comando `kill` para encerrar o processo. Substitua `PID` pelo número do PID do processo que você deseja encerrar. Por exemplo:

```bash
kill PID
```

Isso encerrará o túnel SSH e, consequentemente, a conexão VNC para o servidor remoto.

Lembre-se de substituir `PID` pelo número real do PID que corresponde ao seu túnel SSH. Certifique-se de encerrar apenas o processo relevante para evitar fechar outras conexões SSH que possam estar em execução no seu sistema local.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

