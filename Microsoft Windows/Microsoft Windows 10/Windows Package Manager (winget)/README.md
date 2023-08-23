# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi") / Windows Package Manager

[![Windows Package Manager](https://github.com/systemboys/GTi_Laboratory/blob/main/Microsoft%20Windows/Microsoft%20Windows%2010/Windows%20Package%20Manager%20(winget)/images/winget.jpg?raw=true "Windows Package Manager")](https://github.com/systemboys/GTi_Laboratory/blob/main/Microsoft%20Windows/Microsoft%20Windows%2010/Windows%20Package%20Manager%20(winget)/images/winget.jpg?raw=true "Windows Package Manager")

- [Dicas para Utilizar o Windows Package Manager (winget)](#dicas-para-utilizar-o-windows-package-manager-winget "Dicas para Utilizar o Windows Package Manager (winget)")

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