# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi") / Dicas e Truques

[![Dicas e Truques](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Dicas%20e%20Truques/images/Comandos-basicos-do-Linux-para-iniciantes.jpg?raw=true "Dicas e Truques")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Dicas%20e%20Truques/images/Comandos-basicos-do-Linux-para-iniciantes.jpg?raw=true "Dicas e Truques")

- [Resolvendo Problemas de Resolução em uma Máquina Virtual Debian no Hyper-V](#resolvendo-problemas-de-resolu%C3%A7%C3%A3o-em-uma-m%C3%A1quina-virtual-debian-no-hyper-v "Resolvendo Problemas de Resolução em uma Máquina Virtual Debian no Hyper-V")
- [Como Limpar o Histórico de Comandos no Terminal Linux](#como-limpar-o-hist%C3%B3rico-de-comandos-no-terminal-linux "Como Limpar o Histórico de Comandos no Terminal Linux")
- [Como Desligar ou Reiniciar o Linux via Terminal: Comandos Úteis](#como-desligar-ou-reiniciar-o-linux-via-terminal-comandos-%C3%BAteis "Como Desligar ou Reiniciar o Linux via Terminal: Comandos Úteis")
- [Entendendo a Mensagem 'Do you want to continue? [Y/n]' em Instalações de Pacotes no Linux](#entendendo-a-mensagem-do-you-want-to-continue-yn-em-instala%C3%A7%C3%B5es-de-pacotes-no-linux "Entendendo a Mensagem 'Do you want to continue? [Y/n]' em Instalações de Pacotes no Linux")

---

## Resolvendo Problemas de Resolução em uma Máquina Virtual Debian no Hyper-V

Aqui está uma instrução adaptada para uma máquina virtual Debian no Hyper-V:

Resolvendo o Problema de Resolução em uma Máquina Virtual Debian no Hyper-V:

1. Inicie sua máquina virtual Debian no Hyper-V.

2. Abra um terminal.

3. Navegue até o diretório `/etc/default/`. Você pode fazer isso digitando o seguinte comando:

   ```bash
   cd /etc/default/
   ```

4. Abra o arquivo de configuração do GRUB com um editor de texto. Você pode usar o editor de texto Nano, por exemplo:

   ```bash
   sudo nano grub
   ```

   [![Nano - Grub](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Dicas%20e%20Truques/images/nano_etc_default_grub.png?raw=true "Nano - Grub")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Dicas%20e%20Truques/images/nano_etc_default_grub.png?raw=true "Nano - Grub")

5. No arquivo de configuração do GRUB, encontre as linhas que começam com `GRUB_CMDLINE_LINUX_DEFAULT` e `GRUB_CMDLINE_LINUX`. Adicione a resolução ideal para a sua tela ao final dessas linhas. Por exemplo, se a resolução desejada for 1366x768, as linhas devem ser assim:

   ```plaintext
   GRUB_CMDLINE_LINUX_DEFAULT="quiet splash video=hyperv_fb:1366x768"
   GRUB_CMDLINE_LINUX="video=hyperv_fb:1366x768"
   ```

   [![Grub](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Dicas%20e%20Truques/images/nano_etc_default_grub_code.png?raw=true "Grub")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Dicas%20e%20Truques/images/nano_etc_default_grub_code.png?raw=true "Grub")

6. Salve as alterações no arquivo e saia do editor de texto.

7. Atualize o GRUB para aplicar as alterações digitando o seguinte comando:

   ```bash
   sudo update-grub
   ```

8. Reinicie a máquina virtual Debian:

   ```bash
   sudo reboot
   ```

Após a reinicialização da máquina virtual Debian, você deve ter a resolução configurada corretamente. Se necessário, ajuste a resolução da tela nas configurações do ambiente gráfico do Debian para corresponder à configuração feita no GRUB.

[![Configurações do sistema](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Dicas%20e%20Truques/images/System_settings-layout.png?raw=true "Configurações do sistema")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Dicas%20e%20Truques/images/System_settings-layout.png?raw=true "Configurações do sistema")

Essas etapas devem ajudá-lo a resolver problemas de resolução em uma máquina virtual Debian no Hyper-V.

[![Desktop do Debian Linux](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Dicas%20e%20Truques/images/desktop_debian.png?raw=true "Desktop do Debian Linux")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Dicas%20e%20Truques/images/desktop_debian.png?raw=true "Desktop do Debian Linux")

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--dicas-e-truques "Subir para o topo")

---

## Como Limpar o Histórico de Comandos no Terminal Linux

Para apagar o histórico de comandos digitados no terminal Linux, você pode usar o comando `history` seguido pelo comando `history -c`. Isso irá limpar todo o histórico de comandos. 

Aqui estão os passos:

1. Abra um terminal.

2. Digite o seguinte comando para exibir seu histórico de comandos:

   ```bash
   history
   ```

   Isso mostrará uma lista numerada de todos os comandos que você digitou anteriormente.

3. Para apagar todo o histórico de comandos, digite o seguinte comando:

   ```bash
   history -c
   ```

   Isso irá limpar o histórico.

4. Para garantir que o histórico seja salvo vazio, você pode digitar o comando `history -w`. Isso salvará o histórico vazio no arquivo de histórico.

Agora, seu histórico de comandos estará vazio. Lembre-se de que isso apagará permanentemente o histórico de comandos, portanto, certifique-se de que é isso que deseja fazer. Se você deseja evitar que comandos futuros sejam registrados no histórico, pode configurar o shell para ignorar o histórico com um comando específico ou ajustar as configurações de histórico em seu arquivo de perfil, como o `~/.bashrc` para o Bash shell.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--dicas-e-truques "Subir para o topo")

---

## Como Desligar ou Reiniciar o Linux via Terminal: Comandos Úteis

Você pode desligar o Linux via terminal usando vários comandos, mas os principais comandos são:

1. **shutdown:** O comando `shutdown` permite que você desligue ou reinicie o sistema. Aqui estão alguns exemplos:

   - Para desligar imediatamente: `sudo shutdown -h now`
   - Para reiniciar imediatamente: `sudo shutdown -r now`
   - Para agendar um desligamento em 10 minutos: `sudo shutdown -h +10`
   - Para cancelar um desligamento agendado: `sudo shutdown -c`

2. **poweroff:** Este é um comando simples para desligar o sistema imediatamente:

   ```bash
   sudo poweroff
   ```

3. **halt:** Outro comando para desligar o sistema:

   ```bash
   sudo halt
   ```

4. **reboot:** Para reiniciar o sistema imediatamente:

   ```bash
   sudo reboot
   ```

5. **init:** Você também pode usar o comando `init` para alterar o nível de execução do sistema. Por exemplo, para desligar:

   ```bash
   sudo init 0
   ```

   Para reiniciar:

   ```bash
   sudo init 6
   ```

6. **systemctl:** Se você estiver usando um sistema com o systemd (como muitas distribuições modernas), pode usar o `systemctl` para desligar ou reiniciar:

   - Para desligar: `sudo systemctl poweroff`
   - Para reiniciar: `sudo systemctl reboot`

Lembre-se de usar o `sudo` antes desses comandos para executá-los com privilégios de superusuário, pois o desligamento do sistema geralmente requer permissões elevadas. Certifique-se de salvar o trabalho antes de desligar ou reiniciar o sistema para evitar perda de dados.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--dicas-e-truques "Subir para o topo")

---

## Entendendo a Mensagem 'Do you want to continue? [Y/n]' em Instalações de Pacotes no Linux

Claro, vou explicar essa mensagem "Do you want to continue? [Y/n]" que você frequentemente encontra ao instalar pacotes no Linux via terminal. 

A mensagem "Do you want to continue? [Y/n]" é uma solicitação de confirmação que aparece durante a instalação ou atualização de pacotes no sistema Linux. Ela é projetada para que o usuário confirme se deseja prosseguir com a ação que está prestes a ser executada.

- **O "Y" maiúsculo:** O "Y" maiúsculo é a opção padrão e é usado para indicar uma resposta afirmativa. Se você pressionar "Enter" sem digitar nada, a ação será confirmada automaticamente como "Sim" (Y). Isso é útil para agilizar o processo de instalação quando você deseja aceitar a configuração padrão.

- **O "n" minúsculo:** O "n" minúsculo é a opção para negação ou rejeição. Se você não deseja prosseguir com a ação, pode pressionar "n" e depois "Enter" para recusar a instalação ou atualização. 

Essa abordagem de ter a opção padrão como "Sim" (Y) é uma convenção para tornar o processo mais eficiente, especialmente quando os usuários geralmente querem prosseguir com a instalação. No entanto, a inclusão da opção "n" permite que os usuários cancelem a ação facilmente, caso desejem.

Em resumo, essa mensagem visa tornar as operações no terminal mais seguras e eficientes, permitindo que os usuários confirmem ou cancelem a ação de forma rápida e simples.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--dicas-e-truques "Subir para o topo")

---