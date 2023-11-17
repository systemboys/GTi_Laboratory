# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi")

## Prompt de Comandos e o PowerShell

![Terminal Windows](https://github.com/systemboys/GTi_Laboratory/blob/main/Microsoft%20Windows/Prompt%20de%20Comandos%20e%20o%20PowerShell/images/WINDOWS-TERMINAL.png?raw=true "Terminal Windows")

### *Sumário*

> **_Prompt de comandos_** do Windows

- [Menu de Instalação de Programas no Prompt de Comando do Windows](#menu-de-instala%C3%A7%C3%A3o-de-programas-no-prompt-de-comando-do-windows "Menu de Instalação de Programas no Prompt de Comando do Windows")
- [Como Corrigir a Exibição de Caracteres Especiais no Prompt de Comando do Windows](#como-corrigir-a-exibi%C3%A7%C3%A3o-de-caracteres-especiais-no-prompt-de-comando-do-windows "Como Corrigir a Exibição de Caracteres Especiais no Prompt de Comando do Windows")
- [Menu Interativo de Instalação - Com uso de setas direcionais](#menu-interativo-de-instala%C3%A7%C3%A3o---com-uso-de-setas-direcionais "Menu Interativo de Instalação - Com uso de setas direcionais")
- [Exibição da Data e Hora Atual - Script Batch](#exibi%C3%A7%C3%A3o-da-data-e-hora-atual---script-batch "Exibição da Data e Hora Atual - Script Batch")
- [Como Extrair a Versão do Histórico em Scripts Batch do Windows: Dicas Úteis para Gerenciar Seus Projetos](#como-extrair-a-vers%C3%A3o-do-hist%C3%B3rico-em-scripts-batch-do-windows-dicas-%C3%BAteis-para-gerenciar-seus-projetos "Como Extrair a Versão do Histórico em Scripts Batch do Windows: Dicas Úteis para Gerenciar Seus Projetos")
- [Guia Essencial de Comandos e Variáveis de Ambiente no Windows](#guia-essencial-de-comandos-e-vari%C3%A1veis-de-ambiente-no-windows "Guia Essencial de Comandos e Variáveis de Ambiente no Windows")

> Microsoft **_PowerShell_**

- [Ativar a execução de scripts no PowerShell](#ativar-a-execu%C3%A7%C3%A3o-de-scripts-no-powershell "Ativar a execução de scripts no PowerShell")
- [Função que executa um menu interativo com PowerShell](#fun%C3%A7%C3%A3o-que-executa-um-menu-interativo-com-powershell "Função que executa um menu interativo com PowerShell")
- [Verificar a existência de um diretório ou de um arquivo com arquivo PowerShell (.ps1)](#verificar-a-exist%C3%AAncia-de-um-diret%C3%B3rio-ou-de-um-arquivo-com-arquivo-powershell-ps1 "Verificar a existência de um diretório ou de um arquivo com arquivo PowerShell (.ps1)")
- [Script de Instalação Silenciosa de Software (verificação por chave de registro)](#script-de-instala%C3%A7%C3%A3o-silenciosa-de-software-verifica%C3%A7%C3%A3o-por-chave-de-registro "Script de Instalação Silenciosa de Software (verificação por chave de registro)")
- [Arquivo (.ps1) para instalação de pacotes](#arquivo-ps1-para-instala%C3%A7%C3%A3o-de-pacotes "Arquivo (.ps1) para instalação de pacotes")
- [Execução Interativa de Comandos no PowerShell: Como Permitir que os Usuários Execute Comandos Personalizados](#execu%C3%A7%C3%A3o-interativa-de-comandos-no-powershell-como-permitir-que-os-usu%C3%A1rios-execute-comandos-personalizados "Execução Interativa de Comandos no PowerShell: Como Permitir que os Usuários Execute Comandos Personalizados")
- [Executando Comandos Remotos com PowerShell: Desvendando IRM e IEX](#executando-comandos-remotos-com-powershell-desvendando-irm-e-iex "Executando Comandos Remotos com PowerShell: Desvendando IRM e IEX")
- [Execução Remota de Script PowerShell via Domínio](#execu%C3%A7%C3%A3o-remota-de-script-powershell-via-dom%C3%ADnio "Execução Remota de Script PowerShell via Domínio")
- [Como Abrir Links no Navegador Padrão via PowerShell](#como-abrir-links-no-navegador-padr%C3%A3o-via-powershell "Como Abrir Links no Navegador Padrão via PowerShell")
- [Guia Rápido do PowerShell: Obtendo Diretórios-Chave através de Variáveis de Ambiente no Windows](#guia-r%C3%A1pido-do-powershell-obtendo-diret%C3%B3rios-chave-atrav%C3%A9s-de-vari%C3%A1veis-de-ambiente-no-windows "Guia Rápido do PowerShell: Obtendo Diretórios-Chave através de Variáveis de Ambiente no Windows")
- [Script PowerShell: Obtendo Caminhos dos Principais Diretórios do Perfil do Usuário no Windows](#script-powershell-obtendo-caminhos-dos-principais-diret%C3%B3rios-do-perfil-do-usu%C3%A1rio-no-windows "Script PowerShell: Obtendo Caminhos dos Principais Diretórios do Perfil do Usuário no Windows")
- [Script PowerShell: Abrir File Explorer e Selecionar Arquivo em um Diretório Específico](#script-powershell-abrir-file-explorer-e-selecionar-arquivo-em-um-diret%C3%B3rio-espec%C3%ADfico "Script PowerShell: Abrir File Explorer e Selecionar Arquivo em um Diretório Específico")
- [Executar as atualizações do Windows a partir de um script PowerShell](#executar-as-atualiza%C3%A7%C3%B5es-do-windows-a-partir-de-um-script-powershell "Executar as atualizações do Windows a partir de um script PowerShell")
- [Exportando e importando variáveis em arquivos PowerShell](#exportando-e-importando-vari%C3%A1veis-em-arquivos-powershell "Exportando e importando variáveis em arquivos PowerShell")
- [Exportação e Importação, Compartilhando Funções entre Scripts PowerShell](#exporta%C3%A7%C3%A3o-e-importa%C3%A7%C3%A3o-compartilhando-fun%C3%A7%C3%B5es-entre-scripts-powershell "Exportação e Importação, Compartilhando Funções entre Scripts PowerShell")
- [Passando Argumentos em Scripts PowerShell: Entre arquivos (.ps1)](#passando-argumentos-em-scripts-powershell-entre-arquivos-ps1 "Passando Argumentos em Scripts PowerShell: Entre arquivos (.ps1)")
- [Alterar a cor de fundo do PowerShell](#alterar-a-cor-de-fundo-do-powershell "Alterar a cor de fundo do PowerShell")
- [Ajustando a Janela do PowerShell: Alterando a Largura e a Altura da Janela](#ajustando-a-janela-do-powershell-alterando-a-largura-e-a-altura-da-janela "Ajustando a Janela do PowerShell: Alterando a Largura e a Altura da Janela")
- [Função de Correção de Codificação para Exibição de Texto no PowerShell (UTF8)](#fun%C3%A7%C3%A3o-de-corre%C3%A7%C3%A3o-de-codifica%C3%A7%C3%A3o-para-exibi%C3%A7%C3%A3o-de-texto-no-powershell-utf8 "Função de Correção de Codificação para Exibição de Texto no PowerShell (UTF8)")

---

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Menu de Instalação de Programas no Prompt de Comando do Windows

Para criar um menu no Prompt de Comandos ou PowerShell do Windows que permite ao usuário baixar e instalar programas, você pode usar scripts em lote (batch scripts) para simplificar esse processo. Abaixo, vou mostrar um exemplo de como criar um menu simples para baixar e instalar o WinRAR usando um script em lote. Certifique-se de que o usuário execute o script com privilégios administrativos, pois a instalação de programas normalmente requer direitos de administrador. 

Aqui está um exemplo de script em lote:

```batch
@echo off

:: Menu.bat - Executa o menu com várias linhas de comandos
:: para instalação de softwares para Windows
::
:: URL: ?
:: Autor: Marcos Aurélio R. da Silva "systemboys@hotmail.com"
:: Manutenção: Marcos Aurélio R. da Silva "systemboys@hotmail.com"
::
:: ---------------------------------------------------------------
:: Este programa tem a finadade de agilizar na instalação de softwares
:: para Windows durante a formatação e/ou manutenção de computadores.
:: ---------------------------------------------------------------
:: Histórico:
:: v1.0 2023-09-30 às 19h00, Marcos Aurélio:
::   - Versão inicial, menu de instalações de programas para Windows.
::
:: Licença: GPL.

chcp 65001
title Menu de Instalação

:menu
mode 98,35
color A
cls
echo ╭───────────────────────────────────────╮
echo │          SELECIONE UMA OPÇAO          │
echo ╰───────────────────────────────────────╯
echo.
echo ╭─────────────[Utilitários]─────────────╮
echo │ 1 │ Baixar e Instalar WinRAR          │
echo │ 2 │ Sair                              │
echo ╰───────────────────────────────────────╯

set /p option=Digite o número da opção desejada: 

if "%option%"=="q" (
    cls
    echo Saindo...
    exit
) else if "%option%"=="1" (
    cls
    mode 98,20
    echo Baixando WinRAR...
    bitsadmin /transfer "DownloadWinRAR" "https://exemplo.com/winrar.exe" "%CD%\winrar.exe"
    echo.
    echo Instalando WinRAR...
    start /wait "" "%CD%\winrar.exe"
    del /f /a "%CD%\winrar.exe"
    echo.
    echo ╭───────────────────────────────╮
    echo │ WinRAR instalado com sucesso! │
    echo ╰───────────────────────────────╯
    pause
) else if "%option%"=="2" (
    cls
    echo Você escolheu a Opção 2.
    @REM Aqui você coloca suas linhas de comandos...
    pause
    goto menu
) else (
    cls
    echo Opção inválida! Tente novamente.
    pause
)
goto menu
```

Neste exemplo:

1. O script exibe um menu com duas opções: baixar e instalar o WinRAR ou sair.

2. Quando o usuário seleciona a opção 1, o script usa o comando `bitsadmin` para baixar o arquivo de instalação do WinRAR de um URL fictício (substitua `https://exemplo.com/winrar.exe` pelo URL real). O arquivo é baixado para o diretório onde o script está localizado.

3. Em seguida, o script inicia a instalação do WinRAR usando o comando `start /wait`. O `/wait` faz com que o script aguarde até que a instalação seja concluída.

4. Após a instalação, uma mensagem de sucesso é exibida e o usuário pode pressionar qualquer tecla para continuar.

5. Se o usuário selecionar a opção 2, o script sai.

Observe que este é apenas um exemplo simples e você pode personalizá-lo para suas necessidades específicas. Certifique-se de que o URL de download seja válido e que você tenha os arquivos de instalação corretos para outros programas que deseja incluir no menu. Além disso, considere adicionar tratamento de erros e melhorias de usabilidade, dependendo da complexidade do seu menu de instalação.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Como Corrigir a Exibição de Caracteres Especiais no Prompt de Comando do Windows

O problema que você está enfrentando com caracteres incorretos (como "├º" e "├║") ao usar o comando "echo" no arquivo .bat é devido à codificação do terminal. Para corrigir isso, você pode configurar a codificação do terminal para UTF-8, que é mais compatível com caracteres especiais.

Para fazer isso, siga estas etapas:

1. Abra o Prompt de Comando.

2. Execute o comando a seguir para alterar a codificação do terminal para UTF-8:

```batch
chcp 65001
```

Isso define a codificação do terminal para UTF-8.

3. Agora, execute seu arquivo .bat novamente. A linha "echo Selecione uma opção:" deve ser exibida corretamente.

Lembre-se de que, ao usar UTF-8, você deve garantir que seu arquivo .bat e quaisquer outros arquivos de texto estejam salvos com codificação UTF-8 para que os caracteres especiais sejam exibidos corretamente.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Menu Interativo de Instalação - Com uso de setas direcionais

direcionais

Entendi, você deseja que após executar uma funcionalidade relacionada a uma opção do menu, o script retorne ao menu em vez de sair do Prompt de Comandos. Aqui está o script modificado para atender a esse requisito:

```batch
<# : Batch portion
@echo off & setlocal enabledelayedexpansion

:: Menu.bat - Executa o menu com várias linhas de comandos
:: para instalação de softwares para Windows
::
:: URL: ?
:: Autor: Marcos Aurélio R. da Silva "systemboys@hotmail.com"
:: Manutenção: Marcos Aurélio R. da Silva "systemboys@hotmail.com"
::
:: ---------------------------------------------------------------
:: Este programa tem a finadade de agilizar na instalação de softwares
:: para Windows durante a formatação e/ou manutenção de computadores.
:: ---------------------------------------------------------------
:: Histórico:
:: v1.0 2023-10-28 às 16h40, Marcos Aurélio:
::   - Versão inicial, menu de instalações de programas para Windows.
::
:: Licença: GPL.

chcp 65001 > nul

:: Obter o ano atual
for /f "tokens=2 delims==" %%I in ('"wmic os get localdatetime /value"') do set datetime=%%I
set "ano=%datetime:~0,4%"

:: Subtrair o ano atual por 2008
set /a resultado=ano-2008

:: Mensagem de entrada do Menu com o resultado
echo © %ano% - GLOBAL TEC Informática ® - A %resultado% no mercado de Informática.
echo www.gti1.com.br - gti.inf@hotmail.com - systemboys@hotmail.com

:: Opções do Menu
set "menu[0]=Sair"
set "menu[1]=Opção 1"
set "menu[2]=Opção 2"
set "menu[3]=Opção 3"
set "menu[4]=Opção 4"
set "menu[5]=Opção 5"

set "default=0"

:menu
powershell -noprofile "iex (gc \"%~f0\" | out-string)"
if %ERRORLEVEL% equ 0 (
    echo Você escolheu Sair.
    pause
    goto :EOF
)

if %ERRORLEVEL% equ 1 (
    echo Você selecionou a Opção 1.

    @REM  Your commands here...

    pause
    goto menu
)

if %ERRORLEVEL% equ 2 (
    echo Você selecionou a Opção 2.

    @REM  Your commands here...

    pause
    goto menu
)

if %ERRORLEVEL% equ 3 (
    echo Você selecionou a Opção 3.

    @REM  Your commands here...

    pause
    goto menu
)

if %ERRORLEVEL% equ 4 (
    echo Você selecionou a Opção 4.

    @REM  Your commands here...

    pause
    goto menu
)

if %ERRORLEVEL% equ 5 (
    echo Você selecionou a Opção 5.

    @REM  Your commands here...

    pause
    goto menu
)

goto :EOF
: end batch / begin PowerShell hybrid chimera #>

$menutitle = "=== Menu GTi_Support ==="
$menuprompt = "Use as teclas direcionais. Pressione Enter para selecionar."

$maxlen = $menuprompt.length + 6
$menu = gci env: | ?{ $_.Name -match "^menu\[\d+\]$" } | %{
    $_.Value.trim()
    $len = $_.Value.trim().Length + 6
    if ($len -gt $maxlen) { $maxlen = $len }
}
[int]$selection = $env:default
$h = $Host.UI.RawUI.WindowSize.Height
$w = $Host.UI.RawUI.WindowSize.Width
$xpos = [math]::floor(($w - ($maxlen + 5)) / 2)
$ypos = [math]::floor(($h - ($menu.Length + 4)) / 3)

$offY = [console]::WindowTop;
$rect = New-Object Management.Automation.Host.Rectangle `
    0,$offY,($w - 1),($offY+$ypos+$menu.length+4)
$buffer = $Host.UI.RawUI.GetBufferContents($rect)

function destroy {
    $coords = New-Object Management.Automation.Host.Coordinates 0,$offY
    $Host.UI.RawUI.SetBufferContents($coords,$buffer)
}

function getKey {
    while (-not ((37..40 + 13 + 48..(47 + $menu.length)) -contains $x)) {
        $x = $Host.UI.RawUI.ReadKey('NoEcho,IncludeKeyDown').VirtualKeyCode
    }
    $x
}

# http://goo.gl/IAmdR6
function WriteTo-Pos ([string]$str, [int]$x = 0, [int]$y = 0,
    [string]$bgc = [console]::BackgroundColor, [string]$fgc = [Console]::ForegroundColor) {
    if($x -ge 0 -and $y -ge 0 -and $x -le [Console]::WindowWidth -and
        $y -le [Console]::WindowHeight) {
        $saveY = [console]::CursorTop
        $offY = [console]::WindowTop       
        [console]::setcursorposition($x,$offY+$y)
        Write-Host $str -b $bgc -f $fgc -nonewline
        [console]::setcursorposition(0,$saveY)
    }
}

function center([string]$what) {
    $what = "    $what  "
    $lpad = " " * [math]::max([math]::floor(($maxlen - $what.length) / 2), 0)
    $rpad = " " * [math]::max(($maxlen - $what.length - $lpad.length), 0)
    WriteTo-Pos "$lpad   $what   $rpad" $xpos $line blue yellow
}

function menu {
    $line = $ypos
    center $menutitle
    $line++
    center " "
    $line++

    for ($i=0; $item = $menu[$i]; $i++) {
        # write-host $xpad -nonewline
        $rtpad = " " * ($maxlen - $item.length)
        if ($i -eq $selection) {
            WriteTo-Pos "  > $item <$rtpad" $xpos ($line++) yellow blue
        } else {
            WriteTo-Pos " $i`: $item  $rtpad" $xpos ($line++) blue yellow
        }
    }
    center " "
    $line++
    center $menuprompt
    1
}

while (menu) {

    [int]$key = getKey

    switch ($key) {

        37 {}   # left or up
        38 { if ($selection) { $selection-- }; break }

        39 {}   # right or down
        40 { if ($selection -lt ($menu.length - 1)) { $selection++ }; break }

        # number or enter
        default { if ($key -gt 13) {$selection = $key - 48}; destroy; exit($selection) }
    }
}
```

Neste script modificado, após executar uma opção do menu (exceto "Sair"), o script retornará ao menu em vez de sair do Prompt de Comandos. Você pode adicionar a lógica de cada opção do menu no local correspondente no script.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Exibição da Data e Hora Atual - Script Batch

Certamente! Você pode obter a data atual dentro de um script batch no Windows usando variáveis de ambiente e a função `echo`. Aqui está um exemplo de como você pode fazer isso:

```batch
@echo off
setlocal enabledelayedexpansion

:: Obter a data atual
for /f "tokens=2 delims==" %%I in ('"wmic os get localdatetime /value"') do set datetime=%%I
set "ano=%datetime:~0,4%"
set "mes=%datetime:~4,2%"
set "dia=%datetime:~6,2%"
set "hora=%datetime:~8,2%"
set "minuto=%datetime:~10,2%"
set "segundo=%datetime:~12,2%"

:: Exibir a data atual
echo Data Atual: %dia%/%mes%/%ano% %hora%:%minuto%:%segundo%

endlocal
```

Neste exemplo, o script usa o comando `wmic os get localdatetime` para obter a data e a hora atuais. Em seguida, ele processa a saída para extrair o ano, o mês, o dia, a hora, o minuto e o segundo. Esses valores são armazenados em variáveis (`ano`, `mes`, `dia`, `hora`, `minuto` e `segundo`) e, em seguida, são usados no comando `echo` para exibir a data atual no formato desejado.

Por favor, note que o formato da data e da hora pode variar com base nas configurações regionais do sistema. O exemplo acima assume o formato "dd/mm/aaaa hh:mm:ss". Você pode ajustar o formato conforme necessário para atender aos seus requisitos específicos.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Como Extrair a Versão do Histórico em Scripts Batch do Windows: Dicas Úteis para Gerenciar Seus Projetos

Para extrair a versão do histórico do script Batch do Windows, você pode usar um comando `for` para percorrer o conteúdo do próprio script e encontrar a última versão mencionada no histórico. Aqui está um exemplo de como fazer isso:

```batch
@echo off
setlocal enabledelayedexpansion

:: Obtém o número da última versão do histórico do script
for /f "tokens=2 delims= " %%a in ('findstr /r /c:":: v[0-9]*\.[0-9]*\.[0-9]*" "%~f0"') do (
    set "lastVersion=%%a"
)

echo QuickWindows !lastVersion!
```

Neste exemplo, o comando `findstr` é usado para encontrar linhas que correspondem ao padrão do histórico (`:: v[0-9]*\.[0-9]*\.[0-9]*`). O comando `for /f` é usado para extrair a segunda parte da linha, que representa a versão (`%%a`). A variável `lastVersion` é então definida com o valor da versão encontrada.

Lembre-se de substituir `"QuickWindows"` pelo nome do seu script, se necessário. Este script Batch fornecerá a última versão do histórico do seu arquivo Batch.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Guia Essencial de Comandos e Variáveis de Ambiente no Windows

Aqui estão alguns dos principais diretórios do Windows e as variáveis de ambiente correspondentes para acessá-los:

1. **C:\ (Unidade do Sistema):**
   ```
   echo %SystemDrive%
   ```

2. **Arquivos de Programas (Program Files):**
   - Para sistemas de 64 bits:
     ```
     echo %ProgramFiles%
     ```
   - Para sistemas de 32 bits em sistemas de 64 bits:
     ```
     echo %ProgramFiles(x86)%
     ```

3. **Diretório do Usuário:**
   ```
   echo %UserProfile%
   ```

4. **System32:**
   ```
   echo %SystemRoot%\System32
   ```

5. **Pasta Temporária do Windows:**
   ```
   echo %Temp%
   ```

6. **Pasta Documentos do Usuário:**
   ```
   echo %UserProfile%\Documents
   ```

7. **Área de Trabalho do Usuário:**
   ```
   echo %UserProfile%\Desktop
   ```

8. **Meus Documentos:**
   ```
   echo %UserProfile%\My Documents
   ```

9. **Downloads:**
   ```
   echo %UserProfile%\Downloads
   ```

10. **Configurações de Aplicativos Locais:**
    ```
    echo %LocalAppData%
    ```

Lembre-se de que essas variáveis de ambiente podem variar de acordo com a versão e configuração do Windows. Você pode usar essas variáveis em scripts ou no Prompt de Comandos para acessar esses diretórios.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Ativar a execução de scripts no PowerShell

Para ativar a execução de scripts no sistema, você precisa alterar a política de execução de scripts do PowerShell. A mensagem de erro que você recebeu sugere que a execução de scripts foi desabilitada no sistema. Para habilitá-la, siga as etapas abaixo:

1. Abra o PowerShell como administrador. Para fazer isso, clique com o botão direito do mouse no ícone do PowerShell e selecione “Executar como administrador”.
2. Digite o seguinte comando e pressione Enter: `Set-ExecutionPolicy RemoteSigned`
3. Se você receber uma mensagem de confirmação, digite A e pressione Enter.
4. Agora, tente executar o script novamente.

O comando `Set-ExecutionPolicy RemoteSigned` permite a execução de scripts locais não assinados e scripts assinados baixados da Internet.


[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Função que executa um menu interativo com PowerShell

Aqui está um script em PowerShell que exibe um menu em uma função:

```powershell
# Define a função do menu
function Show-Menu {
    param (
        [string]$Title = 'Menu',
        [string[]]$MenuItems = @(
            'Exit...',
            'Windows Updates',
            'Software Update',
            'Windows and Software Updates'
        )
    )

    # Limpa a tela
    Clear-Host

    # Exibe o título do menu
    Write-Host "`n$Title`n" -ForegroundColor Cyan

    # Exibe as opções do menu
    for ($i = 0; $i -lt $MenuItems.Length; $i++) {
        Write-Host "$i | $($MenuItems[$i])"
    }

    # Lê a entrada do usuário
    $choice = Read-Host "`nEscolha uma opção"

    # Executa a opção escolhida
    switch ($choice) {
        '0' {
            return
        }
        '1' {
            Install-Module PSWindowsUpdate -Force
            Get-WindowsUpdate -AcceptAll -Install
        }
        '2' {
            winget upgrade --all
        }
        '3' {
            Install-Module PSWindowsUpdate -Force
            Get-WindowsUpdate -AcceptAll -Install
            winget upgrade --all
        }
        default {
            Write-Host 'Invalid option' -ForegroundColor Red
        }
    }

    # Pausa o script
    Pause
}

# Chama a função do menu
Show-Menu
```

Este script define uma função Show-Menu que exibe um menu com quatro opções, conforme solicitado. A função usa um loop for para exibir as opções do menu e um comando switch para executar a opção escolhida pelo usuário. As opções 1, 2 e 3 executam os comandos que você forneceu em seu pedido.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Verificar a existência de um diretório ou de um arquivo com arquivo PowerShell (.ps1)

Este script em `PowerShell` verifica a existência de um diretório:

```powershell
# Check if the directory exists
$programFiles = [Environment]::GetEnvironmentVariable("ProgramFiles(x86)")
$directory = "$programFiles\AnyDesk"

if (Test-Path $directory) {
    Write-Host "The directory $directory exists."
} else {
    Write-Host "The directory $directory does not exist."
}
# End of verification
```

Modificação para verificar a existência de um arquivo:

```powershell
# Check if the file exists
$programFiles = [Environment]::GetEnvironmentVariable("ProgramFiles(x86)")
$filePath = "$programFiles\AnyDesk\AnyDesk.exe"

if (Test-Path $filePath) {
    Write-Host "The file exists."
} else {
    Write-Host "The file does not exist."
}
# End of verification
```

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Script de Instalação Silenciosa de Software (verificação por chave de registro)

> **_( ! )_** No exemplo, o software testado é o ***Google Earth Pro***!

```powershell
$installed = Get-ItemProperty HKLM:\Software\Microsoft\Windows\CurrentVersion\Uninstall\* | Where-Object {$_.DisplayName -eq "Google Earth Pro"}
if ($installed -eq $null) {
    $temporaryDirectory = $env:TEMP
    $url = "https://dl.google.com/earth/client/advanced/current/GoogleEarthProWin.exe"
    $output = "$temporaryDirectory\GoogleEarthProWin.exe"
    Invoke-WebRequest -Uri $url -OutFile $output
    Start-Process -FilePath $output -ArgumentList "/S /v/qn"
    Remove-Item $output
} else {
    Write-Host "Google Earth Pro já está instalado."
}
```

Este script em PowerShell verifica se o software "Google Earth Pro" está instalado no sistema. Se o software não estiver instalado, o script realiza o download do instalador do Google Earth Pro a partir de uma URL específica, salva o instalador em um diretório temporário, e em seguida, inicia o processo de instalação silenciosa do software. A instalação silenciosa é realizada usando os argumentos "/S /v/qn" com o comando Start-Process. Após a instalação, o instalador baixado é removido para limpar o espaço temporário. Se o Google Earth Pro já estiver instalado, o script exibe uma mensagem indicando que o software já está presente no sistema.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Arquivo (.ps1) para instalação de pacotes

Escrever o `arquivo.ps1` para scripts de instalação:

```powershell
# Install_YourPackage.ps1 - Executa o script de instalação de YourPackage.
#
# URL: https://github.com/github_user/project_on_github.git
# Autor: Marcos Aurélio R. da Silva <systemboys@hotmail.com>
# Manutenção: Marcos Aurélio R. da Silva <systemboys@hotmail.com>
#
# ---------------------------------------------------------------
# Este programa tem a finalidade de facilitar na instalação de
# pacotes para Windows.
# ---------------------------------------------------------------
# Histórico:
# v0.0.1 2023-10-31 às 01h10, Marcos Aurélio:
#   - Versão inicial, Instalação de YourPackage.
#
# Licença: GPL.

# Se o YourPackage não estiver instalado, faz o download e instala
$programFiles = "$env:SystemDrive\Program Files"
$directory = "$programFiles\YourPackage"

if (Test-Path $directory) {
    Write-Host "YourPackage is installed!"
} else {
    Write-Host "YourPackage is not installed! Starting installation process."

    # Link do download e o diretório Temp
    $downloadUrl = "https://download.anydesk.com/YourPackage.exe"
    $downloadPath = "$env:temp\YourPackage.exe"
    
    # Faz o download do YourPackage
    Invoke-WebRequest -Uri $downloadUrl -OutFile $downloadPath
    
    # Instala o YourPackage
    Start-Process -FilePath $downloadPath -ArgumentList "/S" -Wait

    # Apagar o arquivo
    Remove-Item -Path $downloadPath -Force
}

Write-Host "Press any key to continue..."
$null = $Host.UI.RawUI.ReadKey("NoEcho,IncludeKeyDown")

```

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Execução Interativa de Comandos no PowerShell: Como Permitir que os Usuários Execute Comandos Personalizados

**Instrução:**

Este conjunto de comandos PowerShell permite que o usuário insira um comando e o execute imediatamente no PowerShell.

```powershell
$command = Read-Host "Enter a command to be executed in PowerShell"
Invoke-Expression $command

Write-Host "Press any key to continue..."
$null = $Host.UI.RawUI.ReadKey("NoEcho,IncludeKeyDown")
```

Primeiro, ele solicita ao usuário que digite um comando por meio do cmdlet `Read-Host`, armazenando a entrada na variável `$command`. Em seguida, o comando digitado é executado usando o `Invoke-Expression $command`. Após a execução do comando, o script exibe a mensagem "Pressione qualquer tecla para continuar..." e aguarda até que o usuário pressione uma tecla antes de continuar.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Executando Comandos Remotos com PowerShell: Desvendando IRM e IEX

`IRM` e `IEX` são abreviações para cmdlets do PowerShell (Windows PowerShell Web Cmdlets) e são usados para baixar e executar scripts da web, respectivamente.

- **IRM (`Invoke-RestMethod`):** O cmdlet `Invoke-RestMethod` é usado para fazer solicitações HTTP/S para um URI específico (Uniform Resource Identifier) e recuperar os dados de resposta. No contexto do comando `irm https://dominio.com/dir`, o `IRM` está baixando um script ou um arquivo de um local específico na web.

- **IEX (`Invoke-Expression`):** O cmdlet `Invoke-Expression` é usado para avaliar ou executar strings como comandos no PowerShell. No contexto do comando `irm https://dominio.com/dir | iex`, o `IEX` está sendo usado para executar imediatamente o conteúdo baixado pelo `IRM`. Isso é útil quando você deseja baixar um script da web e executá-lo diretamente no PowerShell sem salvá-lo como um arquivo separado.

Juntos, esses cmdlets são frequentemente usados em uma única linha de comando para baixar e executar scripts do PowerShell diretamente da web. No entanto, é importante ter cuidado ao usar esses comandos, pois eles podem executar código arbitrário do qual você não tem controle total, o que pode ser um risco de segurança se você estiver baixando e executando scripts de fontes não confiáveis.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Execução Remota de Script PowerShell via Domínio

Ação, onde um script em PowerShell é executado remotamente a partir de um domínio usando os parâmetros "irm ... | iex".

Neste exemplo, o script está hospedado em um domínio e o mesmo tem a função de instalar o Git no Windows caso não esteja instalado e clonar um repositório no GitHub.

> **_( i )_** Segue abaixo o script em `PowerShell`:

```powershell
# file.ps1 - Executa o script de ...
#
# Autor: Marcos Aurélio R. da Silva <systemboys@hotmail.com>
# Manutenção: Marcos Aurélio R. da Silva <systemboys@hotmail.com>
#
# ---------------------------------------------------------------
# Este programa tem a finalidade de ...
# ---------------------------------------------------------------
# Histórico:
# v0.0.1 2023-11-13 às 01h10, Marcos Aurélio:
#   - Versão inicial, execução do script ...
#
# Licença: GPL.

clear

# Ativar a execução de scripts no PowerShell
Set-ExecutionPolicy RemoteSigned

# Verifica se o pacote está instalado
Write-Host "Checking if Git exists on Windows..."
if (!(Get-Command git -ErrorAction SilentlyContinue)) {
    # Definição do arquivo
    $fileName="Git"
    $fileUrl="https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe"
    $outputFileName="Git_Setup.exe"

    Write-Host "$fileName does not exist on Windows! Downloading the installer..."

    # Baixa o instalador do pacote
    Invoke-WebRequest -Uri $fileUrl -OutFile "$env:TEMP\$outputFileName"

    Write-Host "Running the $fileName installer..."

    # Instala o pacote
    Start-Process -FilePath "$env:TEMP\$outputFileName" -Wait

    Write-Host "Deleting the $fileName installer..."

    # Remove o instalador do pacote
    Remove-Item "$env:TEMP\$outputFileName"

    # Fechar a janela do Windows PowerShell
    Write-Host "After installing Git, Windows PowerShell must be restarted!"
    Write-Host "Type the same command again or press the up directional arrow key."
    Write-Host
    Write-Host "Press any key to continue..."
    $null = $Host.UI.RawUI.ReadKey("NoEcho,IncludeKeyDown")
    exit
}

# Check if the directory exists
Write-Host "Check if QuickWindows exists, if so, delete it to clone it again..."
$programFiles = $env:TEMP
$directory = "$programFiles\QuickWindows"

# Verifica se o diretório existe antes de excluí-lo
if (Test-Path $directory) {
    Write-Host "The directory $directory exists."
    Remove-Item -Path $directory -Recurse -Force
} else {
    Write-Host "The directory $directory does not exist."
}

# Clonando o QuickWindows do repositório GitHub
Write-Host "Clonando o QuickWindows..."
cd $env:TEMP ; git clone https://github.com/systemboys/QuickWindows.git ; cd .\QuickWindows\ ; .\QuickWindows.cmd
```

> **_( i )_** Hospedagem do `arquivo.ps1` e sua execução:

```tex
https://domain.com/
    └─ /dir/
        └─ file.ps1
```

> **_( i )_** Executar com o **_Microsoft PowerShell_** o seguinte comando:

```powershell
irm https://domain.com/dir/file.ps1 | iex
```

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Como Abrir Links no Navegador Padrão via PowerShell

É possível abrir um link no navegador padrão usando o PowerShell. Você pode fazer isso usando o cmdlet `Start-Process`. Aqui está um exemplo:

```powershell
Start-Process "https://www.microsoft.com/pt-br/edge"
```

Esse comando abrirá o link no navegador padrão configurado no sistema operacional.

Se você quiser abrir o link em um navegador específico, você pode usar o parâmetro `-FilePath` e fornecer o caminho do executável do navegador. Por exemplo, para abrir o link no Microsoft Edge, você poderia fazer algo assim:

```powershell
Start-Process "msedge.exe" -ArgumentList "https://www.microsoft.com/pt-br/edge"
```

Lembre-se de que o caminho para o executável pode variar dependendo da instalação do navegador no seu sistema. No exemplo acima, `msedge.exe` é o executável do Microsoft Edge, mas para outros navegadores, você precisaria fornecer o caminho apropriado.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Guia Rápido do PowerShell: Obtendo Diretórios-Chave através de Variáveis de Ambiente no Windows

Para obter variáveis de ambiente específicas no PowerShell, você pode usar a variável `$env`. Aqui estão exemplos para obter as variáveis de ambiente relacionadas aos diretórios mencionados:

1. **C:\ (Unidade do Sistema):**
   ```powershell
   $env:SystemDrive
   ```

2. **C:\Arquivos de programas:**
   ```powershell
   $env:ProgramFiles
   ```

3. **C:\Arquivos de programas (x86) (para programas de 32 bits em sistemas de 64 bits):**
   ```powershell
   $env:ProgramFiles(x86)
   ```

4. **C:\Windows:**
   ```powershell
   $env:Windir
   ```

Esses comandos retornarão os caminhos associados às variáveis de ambiente correspondentes. Lembre-se de que, em sistemas de 64 bits, `$env:ProgramFiles` geralmente aponta para a pasta "Program Files" para aplicativos de 64 bits, e `$env:ProgramFiles(x86)` aponta para a pasta "Program Files (x86)" para aplicativos de 32 bits.

Experimente esses comandos no PowerShell para ver os resultados específicos em seu sistema.

Se você deseja definir variáveis no PowerShell para armazenar esses caminhos, você pode fazer algo assim:

```powershell
# Defina variáveis para os diretórios-chave
$SystemDrive = $env:SystemDrive
$ProgramFiles = $env:ProgramFiles
$ProgramFilesx86 = $env:ProgramFiles(x86)
$WindowsDirectory = $env:Windir
```

Agora, as variáveis `$SystemDrive`, `$ProgramFiles`, `$ProgramFilesx86`, e `$WindowsDirectory` contêm os caminhos correspondentes aos diretórios-chave. Você pode usar essas variáveis em seus scripts ou comandos PowerShell conforme necessário.

Por exemplo, para exibir o conteúdo da pasta "Program Files", você poderia fazer algo assim:

```powershell
Get-ChildItem -Path $ProgramFiles
```

Lembre-se de que, ao definir variáveis, é boa prática usar nomes descritivos para que o código seja mais legível.

> **_( i )_** Exemplo de definição e exibição.

Certamente, aqui está um bloco de código PowerShell que define as variáveis de ambiente mencionadas e exibe seus valores:

```powershell
# Definindo as variáveis de ambiente
$systemRoot = $env:SystemRoot
$systemDrive = $env:SystemDrive
$programFiles = $env:ProgramFiles
$programData = $env:ProgramData
$userProfile = $env:UserProfile
$temp = $env:Temp
$tmp = $env:Tmp
$commonProgramFiles = $env:CommonProgramFiles

# Exibindo os valores
Write-Host "SystemRoot: $systemRoot"
Write-Host "SystemDrive: $systemDrive"
Write-Host "ProgramFiles: $programFiles"
Write-Host "ProgramData: $programData"
Write-Host "UserProfile: $userProfile"
Write-Host "Temp: $temp"
Write-Host "Tmp: $tmp"
Write-Host "CommonProgramFiles: $commonProgramFiles"
```

Este script define cada variável de ambiente e, em seguida, usa o cmdlet `Write-Host` para exibir os valores correspondentes. Você pode executar este script em um ambiente PowerShell para ver os diretórios associados a cada variável de ambiente no seu sistema. Certifique-se de estar executando o PowerShell com privilégios suficientes, dependendo das operações que o script pode realizar.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Script PowerShell: Obtendo Caminhos dos Principais Diretórios do Perfil do Usuário no Windows

Você pode usar o cmdlet `Get-Item` para obter informações sobre diretórios específicos do perfil do usuário no Windows. Aqui está um exemplo de script PowerShell que lista alguns dos diretórios principais do perfil do usuário, como Área de Trabalho, Documentos, Downloads, etc.:

```powershell
# Obter o perfil do usuário
$userProfile = [System.IO.Path]::Combine($env:SystemDrive, $env:HomePath)

# Obter caminhos para diretórios principais
$desktopPath = [System.IO.Path]::Combine($userProfile, 'Desktop')
$documentsPath = [System.IO.Path]::Combine($userProfile, 'Documents')
$downloadsPath = [System.IO.Path]::Combine($userProfile, 'Downloads')
$picturesPath = [System.IO.Path]::Combine($userProfile, 'Pictures')
$musicPath = [System.IO.Path]::Combine($userProfile, 'Music')
$videosPath = [System.IO.Path]::Combine($userProfile, 'Videos')

# Exibir os caminhos dos diretórios
Write-Output "Desktop: $desktopPath"
Write-Output "Documents: $documentsPath"
Write-Output "Downloads: $downloadsPath"
Write-Output "Pictures: $picturesPath"
Write-Output "Music: $musicPath"
Write-Output "Videos: $videosPath"
```

Este script cria caminhos para os diretórios principais do perfil do usuário e os exibe no console. Você pode adicionar ou remover caminhos conforme necessário para atender às suas necessidades específicas. Execute este script no PowerShell para ver os caminhos dos diretórios no seu sistema.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Script PowerShell: Abrir File Explorer e Selecionar Arquivo em um Diretório Específico

Sim, é possível abrir o File Explorer do Windows em um diretório específico e selecionar um arquivo usando o PowerShell. Para isso, você pode usar o cmdlet `Start-Process` e fornecer o caminho do diretório desejado. Aqui está um exemplo de script que faz isso:

```powershell
# Caminho do diretório desejado
$diretorio = "C:\Caminho\Para\Seu\Diretorio"

# Arquivo que deseja ser selecionado
$arquivoSelecionado = "Exemplo.txt"

# Caminho completo do arquivo
$caminhoCompleto = Join-Path -Path $diretorio -ChildPath $arquivoSelecionado

# Abrir o File Explorer no diretório e selecionar o arquivo
Start-Process explorer.exe -ArgumentList "/select, $caminhoCompleto"
```

Substitua `$diretorio` pelo caminho do diretório desejado e `$arquivoSelecionado` pelo nome do arquivo que você deseja selecionar. O script utiliza o comando `/select` para abrir o File Explorer e selecionar o arquivo especificado.

Execute esse script no PowerShell para abrir o File Explorer no diretório desejado e selecionar o arquivo especificado.

> Executar um determinado arquivo.

Abrir e selecionar um arquivo no File Explorer via PowerShell não implica automaticamente em executar esse arquivo. O File Explorer é uma ferramenta de navegação e gerenciamento de arquivos, e não é projetado para executar automaticamente arquivos selecionados.

Para executar um arquivo específico, você precisará usar um comando ou processo específico relacionado ao tipo de arquivo que está tentando abrir. Por exemplo:

- **Executar um arquivo executável (por exemplo, um programa):**
  ```powershell
  Start-Process -FilePath "C:\Caminho\Para\Seu\Programa.exe"
  ```

- **Abrir um documento usando o aplicativo padrão associado:**
  ```powershell
  Start-Process "C:\Caminho\Para\Seu\Documento.txt"
  ```

Lembre-se de que a capacidade de execução depende do tipo de arquivo e da configuração do sistema. Alguns arquivos podem exigir privilégios de administrador ou outros requisitos específicos.

Se você deseja abrir e executar automaticamente um arquivo específico, você precisa fornecer mais informações sobre o tipo de arquivo e o comportamento desejado para que eu possa oferecer uma orientação mais precisa.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Executar as atualizações do Windows a partir de um script PowerShell

Sim, é possível executar as atualizações do Windows a partir de um script PowerShell. Você pode usar o cmdlet `Get-WindowsUpdate` para verificar e instalar atualizações do Windows. Para executar o  script como administrador sem precisar digitar a senha, você pode criar  um atalho para o script no desktop, clicar com o botão direito do mouse  no atalho e selecionar “Propriedades”. Em seguida, clique em “Avançado” e marque a caixa “Executar como administrador”.

```powershell
Install-Module PSWindowsUpdate -Force
Get-WindowsUpdate -AcceptAll -Install -AutoReboot
```

Este script usa o cmdlet `Install-Module` para instalar o módulo `PSWindowsUpdate` e, em seguida, usa o cmdlet `Get-WindowsUpdate` para verificar e instalar todas as atualizações disponíveis do Windows. O parâmetro `-AcceptAll` é usado para aceitar todas as atualizações sem solicitar confirmação, o parâmetro `-Install` é usado para instalar as atualizações e o parâmetro `-AutoReboot` é usado para reiniciar automaticamente o sistema após a instalação das atualizações.

Não há problema em remover o parâmetro `-AutoReboot` do cmdlet `Get-WindowsUpdate`. Isso impedirá que o sistema seja reiniciado automaticamente após a  instalação das atualizações. No entanto, você precisará reiniciar o  sistema manualmente para que as atualizações entrem em vigor.

Se você quiser executar outro comando após a instalação das atualizações, pode adicioná-lo ao script PowerShell após o cmdlet `Get-WindowsUpdate`. Por exemplo, se você quiser executar o comando `winget upgrade --all` após a instalação das atualizações, pode usar o seguinte código:

```powershell
Install-Module PSWindowsUpdate -Force
Get-WindowsUpdate -AcceptAll -Install
winget upgrade --all
```

Este script usa o cmdlet `Get-WindowsUpdate` para verificar e instalar todas as atualizações disponíveis do Windows. Em seguida, ele executa o comando `winget upgrade --all` para atualizar todos os aplicativos instalados usando o Gerenciador de Pacotes do Windows.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Exportando e importando variáveis em arquivos PowerShell

Você pode exportar várias variáveis de um arquivo PowerShell e importá-las em outro arquivo. Você pode usar o cmdlet `Export-ModuleMember` para exportar as variáveis do arquivo1.ps1 e, em seguida, usar o cmdlet `Import-Module` para importá-las no arquivo2.ps1. Aqui está um exemplo de como fazer isso:

1. No arquivo1.ps1, defina as variáveis que você deseja exportar:

```powershell
$variable_a = "text1"
$variable_b = "text2"
$variable_c = "text3"
Export-ModuleMember -Variable variable_a, variable_b, variable_c
```

1. No arquivo2.ps1, importe as variáveis e exiba seus valores:

```powershell
Import-Module .\arquivo1.ps1
Write-Host $variable_a
Write-Host $variable_b
Write-Host $variable_c
```

Isso deve imprimir o valor das variáveis no console.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Exportação e Importação, Compartilhando Funções entre Scripts PowerShell

Para importar as funções de um arquivo para outro em PowerShell, você pode usar o comando `dot sourcing`. O `dot sourcing` é um método no PowerShell que permite que você chame funções definidas  em um script, em outro script. Aqui está como você pode fazer isso:

Exemplo de funções:

```powershell
# Program functions
function commandExecution_0() {
    clear
    exit
}
function commandExecution_1() {
    Write-Host "Running commands for $selection"
    # Start of commands here...
    # Command 1...
    # Command 2...
    # Command 3...
    Write-Host " >>> ok f1 <<< "
    # End of commands here...
    Read-Host -Prompt "Commands executed successfully, press Enter to return!"
    & .\MyScripts.ps1
}
function commandExecution_2() {
    Write-Host "Running commands for $selection"
    # Start of commands here...
    # Command 1...
    # Command 2...
    # Command 3...
    Write-Host " >>> ok f2 <<< "
    # End of commands here...
    Read-Host -Prompt "Commands executed successfully, press Enter to return!"
    & .\MyScripts.ps1
}
function commandExecution_3() {
    Write-Host "Running commands for $selection"
    # Start of commands here...
    # Command 1...
    # Command 2...
    # Command 3...
    Write-Host " >>> ok f3 <<< "
    # End of commands here...
    Read-Host -Prompt "Commands executed successfully, press Enter to return!"
    & .\MyScripts.ps1
}
```

1. Primeiro, certifique-se de que o arquivo `myFunctions.ps1` está no mesmo diretório que o seu script `myScript.ps1`. Se não estiver, você precisará fornecer o caminho completo para o arquivo `myFunctions.ps1`.
2. No início do seu script `myScript.ps1`, adicione o seguinte comando para importar as funções do arquivo `myFunctions.ps1`:

```powershell
. .\myFunctions.ps1
```

Agora, todas as funções definidas em `myFunctions.ps1` estão disponíveis para uso em `myScript.ps1`.

Por favor, note que há um espaço entre os dois pontos. O primeiro ponto é o operador de `dot sourcing` e o segundo ponto é parte do caminho do arquivo. Se o seu arquivo `myFunctions.ps1` estiver em um diretório diferente, você precisará ajustar o caminho do arquivo de acordo. Por exemplo, se `myFunctions.ps1` estiver em um subdiretório chamado `scripts`, você usaria:

```powershell
. .\scripts\myFunctions.ps1
```

Você pode usar a função Invoke-Command para executar a função desejada. Aqui está um exemplo de como você pode fazer isso:

```powershell
Invoke-Command -ScriptBlock (Get-Command "commandExecution_$ID").ScriptBlock
```

Substitua `$ID` pala referência da função a qual deseja executar caso esteja dentro de uma estrutura de controle. Caso contrário, se não tiver estrutura de controle, basta substituir o nome da função para a desejada `commandExecution_1`.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Passando Argumentos em Scripts PowerShell: Entre arquivos (.ps1)

O código PowerShell para executar um arquivo .ps1 com um argumento seria o seguinte:

```powershell
$argumento = $args[0]
& ".\file1.ps1" $argumento
```

Neste código, a variável `$argumento` armazena o valor do primeiro argumento passado para o script. Em seguida, o comando `&` é usado para executar o arquivo `.ps1`, passando o valor do argumento como parâmetro. Dentro do outro arquivo `file2.ps1`, você pode exibir o argumento usando a variável `$args[0]`.

> **_( i )_** Para passar mais de um argumentos, basta incrementar um após o outro:

O código em Powershell para executar dois arquivos .ps1 com argumentos seria o seguinte:

**_file1.ps1_**
```powershell
# Executa o primeiro file1.ps1 com os argumentos 1 e 2
& ".\file2.ps1" 1 2
```

**_file2.ps1_**
```powershell
# Dentro do arquivo file2.ps1, você pode acessar os argumentos usando o objeto $args
# Exibe os argumentos passados para o arquivo
Write-Host "Argumento 1: $($args[0])"
Write-Host "Argumento 2: $($args[1])"
```

Certifique-se de substituir `.\file2.ps1` pelo caminho correto do primeiro arquivo.ps1 que você deseja executar. Os argumentos passados para o arquivo podem ser acessados usando o objeto `$args`, onde `$args[0]` representa o primeiro argumento e `$args[1]` representa o segundo argumento.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Alterar a cor de fundo do PowerShell

Para alterar a cor de fundo do PowerShell para preto, você pode seguir as seguintes etapas:

1. Abra o PowerShell.
2. Clique com o botão direito do mouse na barra superior da janela do PowerShell e selecione “Propriedades”.
3. Clique na guia “Cores”.
4. Selecione “Preto” na lista suspensa “Cor de fundo”.
5. Clique em “OK” para salvar as alterações.

Se você quiser definir a cor de fundo do PowerShell para preto  permanentemente, você pode adicionar o seguinte código ao seu arquivo de perfil do PowerShell:

```
$Host.UI.RawUI.BackgroundColor = "Black"
$Host.UI.RawUI.ForegroundColor = "White"
```

Isso definirá a cor de fundo como preto e a cor do  texto como branco sempre que você abrir o PowerShell. Para obter uma  lista de todas as cores disponíveis no PowerShell, você pode usar o  seguinte comando:

```
[Enum]::GetValues([System.ConsoleColor])
```

Isso  retornará uma lista de todas as cores disponíveis no PowerShell,  incluindo preto, azul, verde, ciano, vermelho, magenta, amarelo, cinza e  branco.

```powershell
Black
DarkBlue
DarkGreen
DarkCyan
DarkRed
DarkMagenta
DarkYellow
Gray
DarkGray
Blue
Green
Cyan
Red
Magenta
Yellow
White
```

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Ajustando a Janela do PowerShell: Alterando a Largura e a Altura da Janela

Sim, é possível alterar a largura e a altura da janela do Windows PowerShell usando um script. Aqui está um exemplo de como você pode fazer isso:

```powershell
# Cria uma nova instância do objeto System.Management.Automation.Host.Size
$size = New-Object System.Management.Automation.Host.Size(120, 30)

# Atribui o novo tamanho à janela do PowerShell
$host.UI.RawUI.WindowSize = $size
```

Neste exemplo, a largura da janela é definida como 120 e a altura como 30. Você pode alterar esses valores de acordo com suas necessidades. Este script deve ser executado no início do seu arquivo .ps1 para definir o tamanho da janela antes de executar o restante do script.

Por favor, note que este script só funcionará quando executado diretamente no Windows PowerShell. Se você estiver executando o script através de um atalho ou de outra interface de linha de comando, o tamanho da janela pode não ser alterado. Além disso, o Windows pode ter limitações sobre o quão grande a janela do PowerShell pode ser, dependendo da configuração do seu sistema.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Função de Correção de Codificação para Exibição de Texto no PowerShell (UTF8)

Você pode criar uma função para lidar com essa correção de codificação e exibição da string. Aqui está um exemplo de como você pode fazer isso:

```powershell
function ShowEncodedString($text) {
    $encodedText = [System.Text.Encoding]::UTF8.GetString([System.Text.Encoding]::Default.GetBytes($text))
    return $encodedText
}

$footer = " (C) $currentYear GLOBAL TEC Informática"

# Exibindo o texto corrigido
Write-Host (ShowEncodedString $footer)
```

Neste exemplo, a função `ShowEncodedString` recebe uma string como argumento, corrige a codificação e retorna o texto corrigido. Depois, ao chamar `Write-Host`, utiliza-se a função `ShowEncodedString` para exibir a string corrigida.

Você pode ajustar a função `ShowEncodedString` conforme necessário para incluir outras correções ou manipulações na string antes de exibi-la.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---