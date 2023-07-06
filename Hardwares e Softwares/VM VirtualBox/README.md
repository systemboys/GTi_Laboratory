# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi") / VM VirtualBox

[![Imagem 1](https://site.com/img/exemplo.png "Imagem 1")](http://link.com "Imagem 1")

- [Link 1](https://site.com#anchor-link-1 "Link 1")

---

## Configurando resolução da área de trabalho em uma máquina virtual no VirtualBox

Para que a máquina virtual utilize as configurações de resolução do host no VirtualBox, você precisa instalar os "Adicionais para Convidado" (Guest Additions) dentro da máquina virtual. Siga os passos abaixo:

1. Inicie a máquina virtual no VirtualBox.
2. No menu da janela da máquina virtual, clique em "Dispositivos" e selecione "Inserir imagem dos Adicionais para Convidado" (Insert Guest Additions CD Image). Isso irá montar o CD dos Adicionais para Convidado dentro da máquina virtual.
3. Acesse a máquina virtual e abra o Explorador de Arquivos.
4. Navegue até o CD montado que contém os Adicionais para Convidado.
5. Execute o arquivo VBoxWindowsAdditions.exe e siga as instruções de instalação.
6. Reinicie a máquina virtual após a instalação dos Adicionais para Convidado.

Após reiniciar a máquina virtual, você deverá conseguir ajustar a resolução da área de trabalho de acordo com as configurações disponíveis no host. Basta acessar as configurações de exibição no Windows 10 dentro da máquina virtual e selecionar a resolução desejada.

Lembrando que é importante ter os drivers de vídeo corretos instalados no host para que as opções de resolução sejam adequadamente disponibilizadas na máquina virtual.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#assunto "Subir para o topo")

---