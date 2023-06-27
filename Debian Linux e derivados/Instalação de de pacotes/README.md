# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi") / Instalação de pacotes

[![Linux Terminal](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Instala%C3%A7%C3%A3o%20de%20de%20pacotes/images/Linux_terminal.jpg?raw=true "Linux Terminal")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Instala%C3%A7%C3%A3o%20de%20de%20pacotes/images/Linux_terminal.jpg?raw=true "Linux Terminal")

- [Erro de PATH após instalação de pacote .deb no Linux](#erro-de-path-ap%C3%B3s-instala%C3%A7%C3%A3o-de-pacote-deb-no-linux "Erro de PATH após instalação de pacote .deb no Linux")
- [Instalar o Google Earth via terminal](#instalar-o-google-earth-via-terminal "Instalar o Google Earth via terminal")
- [Instalar o Oracle Virtual Box no Debian Linux](#instalar-o-oracle-virtual-box-no-debian-linux "Instalar o Oracle Virtual Box no Debian Linux")
- [Instalação e Desinstalação de Programas no Linux via Terminal](#instala%C3%A7%C3%A3o-e-desinstala%C3%A7%C3%A3o-de-programas-no-linux-via-terminal "Instalação e Desinstalação de Programas no Linux via Terminal")
   - [Identificar programa para removê-lo via comando no terminal Linux](# "Identificar programa para removê-lo via comando no terminal Linux")

---

## Erro de PATH após instalação de pacote .deb no Linux

Erro ao instalar um seguinte programa no Debian 10:

```bash
dpkg -i your_installation_package.deb
```

[![Erro ao instalar programa](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Instala%C3%A7%C3%A3o%20de%20de%20pacotes/images/Erro_PATH_do_root.png?raw=true "Erro ao instalar programa")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Instala%C3%A7%C3%A3o%20de%20de%20pacotes/images/Erro_PATH_do_root.png?raw=true "Erro ao instalar programa")

O erro "E: Sub-process /usr/bin/dpkg returned an error code (1)" é geralmente um erro genérico que ocorre durante a instalação ou atualização de pacotes em sistemas operacionais baseados em Debian, como Ubuntu e Debian. Esse erro pode ser causado por uma série de problemas, como dependências quebradas, problemas de conflito entre pacotes ou problemas com o próprio pacote que está sendo instalado. Para resolver esse erro, é necessário identificar a causa específica do problema e corrigi-lo adequadamente.

Com editor de sua preferência edite o arquivo `./etc/profile`.

```bash
sudo nano /etc/profile
```

[![Terminal Profile](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Instala%C3%A7%C3%A3o%20de%20de%20pacotes/images/Terminal_etc_profile.png?raw=true "Terminal Profile")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Instala%C3%A7%C3%A3o%20de%20de%20pacotes/images/Terminal_etc_profile.png?raw=true "Terminal Profile")

Observe que haverá uma condição com valor verdadeiro ou falso:

```bash
if [ "$(id -u)" -eq 0 ]; then
  PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
else
  PATH="/usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games"
fi
```

Altere a linha no `else` da condição, adicionando um `/sbin` como no exemplo abaixo:

```bash
PATH="/usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games/sbin"
```

Após modificar salve o arquivo e saia, você voltará para o terminal. Obs.: Se for no `nano`, execute os comandos:

| Comando | Descrição |
| :------------: | :------------ |
| Ctrl + O | Gravar alterações no arquivo |
| Ctrl + X | Sair do arquivo e voltar para o terminal |

Após editar, salvar e sair do arquivo, execute o seguinte comando:

```bash
source /etc/profile
```

Feito este processo, seu linux irá instalar normalmente o pacote através do `dpkg -i your_installation_package.deb`.

> ( ! ) Obs.: Em uma instalação futura, se houver o mesmo problema, faça o mesmo procedimento reomovendo o `/sbin`. No caso, algumas instalações exigirão o "sbin" e outras não.

Uma solução definitiva para o erro de `PATH` após a instalação de um pacote `.deb` é adicionar o caminho correto ao arquivo `/etc/environment`, que é lido pelo sistema no momento do login. Para fazer isso, você pode seguir estes passos:

1. Abra o arquivo `/etc/environment` em um editor de texto com privilégios de administrador:

   ```bash
   sudo nano /etc/environment
   ```

2. Adicione o caminho correto à variável `PATH`. Por exemplo, se o caminho correto for `/usr/local/bin`, adicione esta linha:

   ```bash
   PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/usr/local/bin"
   ```

3. Salve e feche o arquivo.

4. Recarregue o arquivo `/etc/environment` para que as alterações tenham efeito:

   ```bash
   source /etc/environment
   ```

Depois de seguir estes passos, o caminho correto deve estar configurado corretamente e o erro de `PATH` não deve mais ocorrer.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--instala%C3%A7%C3%A3o-de-pacotes "Subir para o topo")

---

## Instalar o Google Earth via terminal

O Google Earth não está disponível nos repositórios oficiais do Debian, mas você pode baixar e instalar o pacote .deb do Google Earth diretamente do site oficial. 

Siga as etapas abaixo para instalar o Google Earth no Debian Linux via terminal:

1. Abra um terminal.

2. Baixe o pacote .deb mais recente do Google Earth usando o comando `wget`. Certifique-se de escolher a versão correta para o seu sistema operacional (32 bits ou 64 bits):

   - Para sistemas de 32 bits:

     ```bash
     wget https://dl.google.com/dl/earth/client/current/google-earth-stable_current_i386.deb
     ```

   - Para sistemas de 64 bits:

     ```bash
     wget https://dl.google.com/dl/earth/client/current/google-earth-stable_current_amd64.deb
     ```

3. Após o download, instale o pacote .deb usando o comando `dpkg`:

   ```bash
   sudo dpkg -i google-earth-stable_current_*.deb
   ```

4. Se ocorrerem dependências ausentes durante a instalação, execute o seguinte comando para corrigir e instalar as dependências necessárias:

   ```bash
   sudo apt install -f
   ```

5. Após a instalação, você pode iniciar o Google Earth digitando `google-earth-pro` no terminal ou procurando-o no menu de aplicativos.

Lembre-se de ter privilégios administrativos para executar os comandos com `sudo`. Certifique-se também de baixar a versão correta do Google Earth para o seu sistema operacional (32 bits ou 64 bits) e de atualizar os comandos acima com o nome do arquivo .deb baixado, se necessário.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--instala%C3%A7%C3%A3o-de-pacotes "Subir para o topo")

---

## Instalar o Oracle Virtual Box no Debian Linux

Para instalar o Oracle VirtualBox no Debian Linux, você pode seguir as seguintes etapas:

1. Abra um terminal.

2. Adicione o repositório do VirtualBox ao seu sistema executando o seguinte comando:

```bash
sudo sh -c 'echo "deb [arch=amd64] https://download.virtualbox.org/virtualbox/debian $(lsb_release -sc) contrib" >> /etc/apt/sources.list.d/virtualbox.list'
```

3. Baixe e importe a chave GPG do VirtualBox para verificar a autenticidade dos pacotes:

```bash
wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add -
```

4. Atualize a lista de pacotes disponíveis:

```bash
sudo apt update
```

5. Instale o VirtualBox:

```bash
sudo apt install virtualbox-6.1
```

6. Após a instalação, você pode executar o VirtualBox a partir do menu de aplicativos ou digitando o comando `virtualbox` no terminal.

Certifique-se de ter privilégios administrativos para executar os comandos com `sudo`. Além disso, verifique a versão mais recente do VirtualBox no site oficial (https://www.virtualbox.org) para garantir que você está instalando a versão correta.

Observação: Se você estiver usando uma versão diferente do Debian, substitua `$(lsb_release -sc)` pelo código do seu sistema, como "buster" para o Debian 10.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--instala%C3%A7%C3%A3o-de-pacotes "Subir para o topo")

---

## Instalação e Desinstalação de Programas no Linux via Terminal

Exemplo 1: Instalando o TigerVNC
1. Abra o terminal em seu sistema.
2. Execute o seguinte comando para instalar o TigerVNC:
   ```bash
   sudo apt install tigervnc-scraping-server
   ```
3. Aguarde até que o processo de instalação seja concluído.

Exemplo 2: Desinstalando o TigerVNC
1. Abra o terminal em seu sistema.
2. Execute o seguinte comando para desinstalar o TigerVNC:
   ```bash
   sudo apt remove tigervnc-scraping-server
   ```
3. Aguarde até que o processo de desinstalação seja concluído.

Exemplo 3: Instalando o RealVNC Viewer
1. Abra o terminal em seu sistema.
2. Execute o seguinte comando para instalar o RealVNC Viewer:
   ```bash
   sudo dpkg -i realvnc-vnc-viewer.deb
   ```
   (substitua "realvnc-vnc-viewer.deb" pelo nome do pacote .deb que você baixou)
3. Aguarde até que o processo de instalação seja concluído.

Exemplo 4: Desinstalando o RealVNC Viewer
1. Abra o terminal em seu sistema.
2. Execute o seguinte comando para desinstalar o RealVNC Viewer:
   ```bash
   sudo dpkg -r realvnc-vnc-viewer
   ```
3. Aguarde até que o processo de desinstalação seja concluído.

Certifique-se de adaptar os comandos de instalação e desinstalação de acordo com o programa que você está instalando ou removendo.

Ao seguir esses exemplos, você poderá fazer a instalação e desinstalação de programas no Linux via terminal.

Lembre-se de verificar a documentação oficial do programa e fazer backup de dados importantes antes de realizar qualquer alteração em seu sistema.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--instala%C3%A7%C3%A3o-de-pacotes "Subir para o topo")

---

## Identificar programa para removê-lo via comando no terminal Linux

Sim, existe outra forma de identificar o programa para removê-lo via comando no terminal Linux. Você pode usar o comando `dpkg --list` para listar todos os pacotes instalados no sistema. Em seguida, você pode filtrar a saída usando o comando `grep` e fornecer um trecho do nome do programa que você deseja desinstalar.

Por exemplo, se você lembrar que o programa possui a palavra "editor" no nome, você pode executar o seguinte comando:

```bash
dpkg --list | grep editor
```

Isso mostrará uma lista dos pacotes instalados que contêm a palavra "editor" no nome. A partir daí, você pode identificar o pacote específico que deseja desinstalar e usar o comando `apt remove` seguido do nome do pacote para removê-lo.

Tenha cuidado ao desinstalar pacotes usando esse método, pois é importante identificar corretamente o pacote que você deseja remover para evitar a remoção de pacotes indesejados.

Título para anotação: Identificando e removendo programas no Linux usando o comando dpkg.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--instala%C3%A7%C3%A3o-de-pacotes "Subir para o topo")

---