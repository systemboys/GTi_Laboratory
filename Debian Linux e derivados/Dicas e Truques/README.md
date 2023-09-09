# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi") / Dicas e Truques

[![Dicas e Truques](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Dicas%20e%20Truques/images/Comandos-basicos-do-Linux-para-iniciantes.jpg?raw=true "Dicas e Truques")](https://github.com/systemboys/GTi_Laboratory/blob/main/Debian%20Linux%20e%20derivados/Dicas%20e%20Truques/images/Comandos-basicos-do-Linux-para-iniciantes.jpg?raw=true "Dicas e Truques")

- [Configurando uma Resolução de Tela Personalizada no Debian Linux](#configurando-uma-resolu%C3%A7%C3%A3o-de-tela-personalizada-no-debian-linux "Configurando uma Resolução de Tela Personalizada no Debian Linux")

---

## Configurando uma Resolução de Tela Personalizada no Debian Linux

Se a resolução desejada de 1366x768 não está disponível nas opções de resolução na configuração do sistema, você pode tentar configurá-la manualmente editando o arquivo de configuração do Xorg. Aqui está um guia passo a passo sobre como fazer isso:

**Nota importante:** Certifique-se de fazer backup do arquivo de configuração do Xorg antes de fazer qualquer alteração. Isso permitirá que você restaure a configuração original, se algo der errado.

1. Abra um terminal.

2. Edite o arquivo de configuração do Xorg com um editor de texto. Você precisará de permissões de superusuário para fazer isso. Use o seguinte comando:

   ```bash
   sudo nano /etc/X11/xorg.conf
   ```

   Isso abrirá o arquivo de configuração do Xorg no editor de texto "nano".

3. Dentro do arquivo de configuração do Xorg, você precisará adicionar uma seção "Monitor" e uma seção "Screen" para a resolução desejada. Use o seguinte exemplo como referência:

   ```plaintext
   Section "Monitor"
       Identifier "Monitor0"
       Modeline "1366x768_60.00" 85.25 1366 1440 1576 1784 768 771 781 798 -hsync +vsync
       Option "PreferredMode" "1366x768_60.00"
   EndSection

   Section "Screen"
       Identifier "Screen0"
       Monitor "Monitor0"
       DefaultDepth 24
       SubSection "Display"
           Depth 24
           Modes "1366x768"
       EndSubSection
   ```

   Este exemplo configura uma resolução de 1366x768 a 60Hz. Você pode ajustar os valores conforme necessário para a resolução e a taxa de atualização desejadas.

4. Salve as alterações no arquivo pressionando `Ctrl + O`, confirme o nome do arquivo e pressione Enter. Em seguida, saia do editor de texto pressionando `Ctrl + X`.

5. Reinicie o seu sistema para aplicar as configurações:

   ```bash
   sudo reboot
   ```

Após reiniciar, sua resolução personalizada deve estar disponível nas configurações do sistema ou na configuração do monitor. Selecione-a e aplique-a como sua resolução preferida.

Lembre-se de que a edição incorreta do arquivo de configuração do Xorg pode causar problemas de exibição. Portanto, faça isso com cuidado e siga as etapas de backup para que você possa restaurar a configuração anterior, se necessário.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--dicas-e-truques "Subir para o topo")

---