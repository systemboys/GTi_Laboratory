# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi") / VM VirtualBox

[![VM VirtualBox](https://github.com/systemboys/GTi_Laboratory/blob/main/Hardwares%20e%20Softwares/VM%20VirtualBox/images/VM_VirtualBox.png?raw=true "VM VirtualBox")](https://github.com/systemboys/GTi_Laboratory/blob/main/Hardwares%20e%20Softwares/VM%20VirtualBox/images/VM_VirtualBox.png?raw=true "VM VirtualBox")

- [Configurando resolução da área de trabalho em uma máquina virtual no VirtualBox](#configurando-resolu%C3%A7%C3%A3o-da-%C3%A1rea-de-trabalho-em-uma-m%C3%A1quina-virtual-no-virtualbox "Configurando resolução da área de trabalho em uma máquina virtual no VirtualBox")

---

## Configurando resolução da área de trabalho em uma máquina virtual no VirtualBox

Para que a máquina virtual utilize as configurações de resolução do host no VirtualBox, você precisa instalar os "Adicionais para Convidado" (Guest Additions) dentro da máquina virtual. Siga os passos abaixo:

1. Inicie a máquina virtual no VirtualBox.

    [![Máquina Virtual iniciada](https://github.com/systemboys/GTi_Laboratory/blob/main/Hardwares%20e%20Softwares/VM%20VirtualBox/images/Virtual_Machine_started.png?raw=true "Máquina Virtual iniciada")](https://github.com/systemboys/GTi_Laboratory/blob/main/Hardwares%20e%20Softwares/VM%20VirtualBox/images/Virtual_Machine_started.png?raw=true "Máquina Virtual iniciada")

2. No menu da janela da máquina virtual, clique em "Dispositivos" e selecione "Inserir imagem dos Adicionais para Convidado" (Insert Guest Additions CD Image). Isso irá montar o CD dos Adicionais para Convidado dentro da máquina virtual.

    [![Unidade de CD (?:) VirtualBox Guest Additions](https://github.com/systemboys/GTi_Laboratory/blob/main/Hardwares%20e%20Softwares/VM%20VirtualBox/images/Insert_Guest_Additions_CD_Image.png?raw=true "Unidade de CD (?:) VirtualBox Guest Additions")](https://github.com/systemboys/GTi_Laboratory/blob/main/Hardwares%20e%20Softwares/VM%20VirtualBox/images/Insert_Guest_Additions_CD_Image.png?raw=true "Unidade de CD (?:) VirtualBox Gues Additions")

3. Acesse a máquina virtual e abra o Explorador de Arquivos.
4. Navegue até o CD montado que contém os Adicionais para Convidado.

    [![Arquivos do VirtualBox Guest](https://github.com/systemboys/GTi_Laboratory/blob/main/Hardwares%20e%20Softwares/VM%20VirtualBox/images/Insert_Guest_Additions_CD_Image_files.png?raw=true "Arquivos do VirtualBox Guest")](https://github.com/systemboys/GTi_Laboratory/blob/main/Hardwares%20e%20Softwares/VM%20VirtualBox/images/Insert_Guest_Additions_CD_Image_files.png?raw=true "Arquivos do VirtualBox Guest")

5. Execute o arquivo VBoxWindowsAdditions.exe e siga as instruções de instalação.

    [![Instalando Guest Additions](https://github.com/systemboys/GTi_Laboratory/blob/main/Hardwares%20e%20Softwares/VM%20VirtualBox/images/VBoxWindowsAdditions.png?raw=true "Instalando Guest Additions")](https://github.com/systemboys/GTi_Laboratory/blob/main/Hardwares%20e%20Softwares/VM%20VirtualBox/images/VBoxWindowsAdditions.png?raw=true "Instalando Guest Additions")

6. Reinicie a máquina virtual após a instalação dos Adicionais para Convidado.

    [![Reiniciando a VM](https://github.com/systemboys/GTi_Laboratory/blob/main/Hardwares%20e%20Softwares/VM%20VirtualBox/images/Restarting_virtual_machine.png?raw=true "Reiniciando a VM")](https://github.com/systemboys/GTi_Laboratory/blob/main/Hardwares%20e%20Softwares/VM%20VirtualBox/images/Restarting_virtual_machine.png?raw=true "Reiniciando a VM")

Após reiniciar a máquina virtual, você deverá conseguir ajustar a resolução da área de trabalho de acordo com as configurações disponíveis no host. Basta acessar as configurações de exibição no Windows 10 dentro da máquina virtual e selecionar a resolução desejada.

Lembrando que é importante ter os drivers de vídeo corretos instalados no host para que as opções de resolução sejam adequadamente disponibilizadas na máquina virtual.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--vm-virtualbox "Subir para o topo")

---