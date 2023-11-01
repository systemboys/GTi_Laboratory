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

- [Verificar a existência de um diretório ou de um arquivo com arquivo PowerShell (.ps1)](#verificar-a-exist%C3%AAncia-de-um-diret%C3%B3rio-ou-de-um-arquivo-com-arquivo-powershell-ps1 "Verificar a existência de um diretório ou de um arquivo com arquivo PowerShell (.ps1)")
- [Arquivo (.ps1) para instalação de pacotes](#arquivo-ps1-para-instala%C3%A7%C3%A3o-de-pacotes "Arquivo (.ps1) para instalação de pacotes")

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

---

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
$programFiles = [Environment]::GetEnvironmentVariable("ProgramFiles(x86)")
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
    $filePath = "C:\Path\to\YourPackage.exe"
    Remove-Item -Path $filePath -Force
}

Write-Host "Press any key to continue..."
$null = $Host.UI.RawUI.ReadKey("NoEcho,IncludeKeyDown")

```

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---