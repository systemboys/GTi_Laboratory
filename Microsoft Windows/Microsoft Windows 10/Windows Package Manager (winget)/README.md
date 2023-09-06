# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi") / Windows Package Manager

[![Windows Package Manager](https://github.com/systemboys/GTi_Laboratory/blob/main/Microsoft%20Windows/Microsoft%20Windows%2010/Windows%20Package%20Manager%20(winget)/images/winget.jpg?raw=true "Windows Package Manager")](https://github.com/systemboys/GTi_Laboratory/blob/main/Microsoft%20Windows/Microsoft%20Windows%2010/Windows%20Package%20Manager%20(winget)/images/winget.jpg?raw=true "Windows Package Manager")

- [Dicas para Utilizar o Windows Package Manager (winget)](#dicas-para-utilizar-o-windows-package-manager-winget "Dicas para Utilizar o Windows Package Manager (winget)")
- [Como Instalar Manualmente o Windows Package Manager (winget) em Versões Antigas do Windows](#como-instalar-manualmente-o-windows-package-manager-winget-em-vers%C3%B5es-antigas-do-windows "Como Instalar Manualmente o Windows Package Manager (winget) em Versões Antigas do Windows")

---

## Dicas para Utilizar o Windows Package Manager (winget)

Claro, aqui estão algumas orientações básicas para usar o Windows Package Manager (winget):

1. **Instalação do Windows Package Manager:**
   O Windows Package Manager (winget) geralmente já está incluído nas versões mais recentes do Windows. Se não estiver, você pode instalá-lo manualmente seguindo as instruções no site oficial da Microsoft.

2. **Abrir o Prompt de Comando:**
   Abra o Prompt de Comando ou o PowerShell. Você pode fazer isso pressionando as teclas Win + X e escolhendo "Prompt de Comando" ou "Windows PowerShell".

3. **Comandos Básicos:**
   - Para listar todos os aplicativos disponíveis para instalação, você pode usar o comando:
     ```bash
     winget list
     ```
   - Para instalar um aplicativo, você pode usar o comando:
     ```bash
     winget install NomeDoAplicativo
     ```
   - Para desinstalar um aplicativo, use:
     ```bash
     winget uninstall NomeDoAplicativo
     ```
   - Para buscar um aplicativo específico, utilize:
     ```bash
     winget search NomeOuPalavraChave
     ```

4. **Atualizações:**
   - Para verificar atualizações para todos os aplicativos instalados:
     ```bash
     winget upgrade
     ```
   - Para atualizar todas as atualizações disponíveis
     ```bash
     winget upgrade --all
     ```
   - Para atualizar um aplicativo específico:
     ```bash
     winget upgrade NomeDoAplicativo
     ```

5. **Informações Detalhadas:**
   - Para obter informações detalhadas sobre um aplicativo:
     ```bash
     winget show NomeDoAplicativo
     ```

6. **Listar Todos os Comandos:**
   - Para ver todos os comandos disponíveis:
     ```bash
     winget --help
     ```

[![WinGet Upgrade List](https://github.com/systemboys/GTi_Laboratory/blob/main/Microsoft%20Windows/Microsoft%20Windows%2010/Windows%20Package%20Manager%20(winget)/images/listar.png?raw=true "WinGet Upgrade List")](https://github.com/systemboys/GTi_Laboratory/blob/main/Microsoft%20Windows/Microsoft%20Windows%2010/Windows%20Package%20Manager%20(winget)/images/listar.png?raw=true "WinGet Upgrade List")

[![WinGet Upgrade All](https://github.com/systemboys/GTi_Laboratory/blob/main/Microsoft%20Windows/Microsoft%20Windows%2010/Windows%20Package%20Manager%20(winget)/images/update_all.PNG?raw=true "WinGet Upgrade All")](https://github.com/systemboys/GTi_Laboratory/blob/main/Microsoft%20Windows/Microsoft%20Windows%2010/Windows%20Package%20Manager%20(winget)/images/update_all.PNG?raw=true "WinGet Upgrade All")

Lembre-se de que você pode precisar executar o Prompt de Comando ou o PowerShell como administrador para usar alguns comandos, especialmente os de instalação e desinstalação.

Certifique-se de consultar a documentação oficial do Windows Package Manager (winget) da Microsoft para obter informações mais detalhadas e atualizadas sobre como usar esse recurso.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--windows-package-manager "Subir para o topo")

---

## Como Instalar Manualmente o Windows Package Manager (winget) em Versões Antigas do Windows

Para instalar manualmente o Windows Package Manager (winget) em versões mais antigas do Windows que não o têm pré-instalado, siga estas etapas:

1. **Verifique a Versão do Windows:** Primeiro, verifique se o seu sistema atende aos requisitos mínimos para o uso do winget. Ele é compatível com o Windows 10 versão 1809 (build 10.0.17763) ou posterior.

2. **Baixe a Ferramenta de Instalação:** A Microsoft fornece um instalador de código aberto chamado "App Installer" que você pode usar para instalar o winget manualmente. Você pode baixá-lo no GitHub da Microsoft.

3. **Instalação:** Após baixar o instalador, execute-o. Ele irá instalar o winget e fazer as configurações necessárias no seu sistema.

4. **Verificação da Instalação:** Para verificar se a instalação foi bem-sucedida, abra o Prompt de Comando (cmd.exe) e digite o seguinte comando:

   ```bash
   winget --version
   ```

   Isso deve exibir a versão do Windows Package Manager que foi instalada.

5. **Uso do winget:** Agora você pode usar o winget para instalar, desinstalar e gerenciar aplicativos da Microsoft Store ou outros programas suportados pelo winget.

Lembre-se de que a instalação manual pode não estar disponível em todas as versões mais antigas do Windows e pode exigir a execução de comandos com privilégios de administrador. Certifique-se de seguir as etapas com cuidado e de acordo com os requisitos do seu sistema.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#laborat%C3%B3rio-gti--windows-package-manager "Subir para o topo")

---