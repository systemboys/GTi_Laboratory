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
- [Passagem de Argumentos entre Arquivos: PowerShell e Batch (CMD)](#passagem-de-argumentos-entre-arquivos-powershell-e-batch-cmd "Passagem de Argumentos entre Arquivos: PowerShell e Batch (CMD)")
- [Compartilhando Variáveis e Funções entre Arquivos .CMD no Batch](#compartilhando-vari%C3%A1veis-e-fun%C3%A7%C3%B5es-entre-arquivos-cmd-no-batch "Compartilhando Variáveis e Funções entre Arquivos .CMD no Batch")

> Microsoft **_PowerShell_**

- [Atualizando o PowerShell no Windows: Um Guia Passo a Passo](#atualizando-o-powershell-no-windows-um-guia-passo-a-passo "Atualizando o PowerShell no Windows: Um Guia Passo a Passo")
- [Ativar a execução de scripts no PowerShell](#ativar-a-execu%C3%A7%C3%A3o-de-scripts-no-powershell "Ativar a execução de scripts no PowerShell")
- [Função que executa um menu interativo com PowerShell](#fun%C3%A7%C3%A3o-que-executa-um-menu-interativo-com-powershell "Função que executa um menu interativo com PowerShell")
- [Menu interativo com PowerShell, uma maneira organizada de organizar opções](#menu-interativo-com-powershell-uma-maneira-organizada-de-organizar-op%C3%A7%C3%B5es "Menu interativo com PowerShell, uma maneira organizada de organizar opções")
- [Verificar a existência de um diretório ou de um arquivo com arquivo PowerShell (.ps1)](#verificar-a-exist%C3%AAncia-de-um-diret%C3%B3rio-ou-de-um-arquivo-com-arquivo-powershell-ps1 "Verificar a existência de um diretório ou de um arquivo com arquivo PowerShell (.ps1)")
- [Verificando a existência de diretório ou arquivo em duas versões do Windows](#verificando-a-exist%C3%AAncia-de-diret%C3%B3rio-ou-arquivo-em-duas-vers%C3%B5es-do-windows "Verificando a existência de diretório ou arquivo em duas versões do Windows")
- [Executar arquivo chamado executável via linha de comando PowerShell](#executar-arquivo-chamado-execut%C3%A1vel-via-linha-de-comando-powershell "Executar arquivo chamado executável via linha de comando PowerShell")
- [Verificar para instalar ou executar arquivos executáveis](#verificar-para-instalar-ou-executar-arquivos-execut%C3%A1veis "Verificar para instalar ou executar arquivos executáveis")
- [Compressão de arquivos, PowerShell Backup Automático (.zip)](#compress%C3%A3o-de-arquivos-powershell-backup-autom%C3%A1tico-zip "Compressão de arquivos, PowerShell Backup Automático (.zip)")
- [Automatizando a Extração e Execução de Arquivos com PowerShell](#automatizando-a-extra%C3%A7%C3%A3o-e-execu%C3%A7%C3%A3o-de-arquivos-com-powershell "Automatizando a Extração e Execução de Arquivos com PowerShell")
- [Criar Atalho para Programa no Desktop usando PowerShell](#criar-atalho-para-programa-no-desktop-usando-powershell "Criar Atalho para Programa no Desktop usando PowerShell")
- [Criar Atalho para Programa no Desktop com ícone personalizado usando PowerShell](#criar-atalho-para-programa-no-desktop-usando-powershell "Criar Atalho para Programa no Desktop com ícone personalizado usando PowerShell")
- [Criar Atalho para Comando PowerShell no Desktop usando PowerShell](#criar-atalho-para-comando-powershell-no-desktop-usando-powershell "Criar Atalho para Comando PowerShell no Desktop usando PowerShell")
- [Criar Atalho para Comando PowerShell no Desktop com ícone personalizado usando PowerShell](#criar-atalho-para-comando-powershell-no-desktop-com-%C3%ADcone-personalizado-usando-powershell "Criar Atalho para Comando PowerShell no Desktop com ícone personalizado usando PowerShell")
- [Verificando versão do sistema operacional](#verificando-vers%C3%A3o-do-sistema-operacional "Verificando versão do sistema operacional")
- [Script de Instalação Silenciosa de Software (verificação por chave de registro)](#script-de-instala%C3%A7%C3%A3o-silenciosa-de-software-verifica%C3%A7%C3%A3o-por-chave-de-registro "Script de Instalação Silenciosa de Software (verificação por chave de registro)")
- [Arquivo (.ps1) para instalação de pacotes](#arquivo-ps1-para-instala%C3%A7%C3%A3o-de-pacotes "Arquivo (.ps1) para instalação de pacotes")
- [Execução Interativa de Comandos no PowerShell: Como Permitir que os Usuários Execute Comandos Personalizados](#execu%C3%A7%C3%A3o-interativa-de-comandos-no-powershell-como-permitir-que-os-usu%C3%A1rios-execute-comandos-personalizados "Execução Interativa de Comandos no PowerShell: Como Permitir que os Usuários Execute Comandos Personalizados")
- [Executar comandos do Prompt de comandos do Windows no Windows PowerShell](#executar-comandos-do-prompt-de-comandos-do-windows-no-windows-powershell "Executar comandos do Prompt de comandos do Windows no Windows PowerShell")
- [Script de Interação: Janela de Comando Interativa para Execução de Comandos](#script-de-intera%C3%A7%C3%A3o-janela-de-comando-interativa-para-execu%C3%A7%C3%A3o-de-comandos "Script de Interação: Janela de Comando Interativa para Execução de Comandos")
- [Executando Comandos Remotos com PowerShell: Desvendando IRM e IEX](#executando-comandos-remotos-com-powershell-desvendando-irm-e-iex "Executando Comandos Remotos com PowerShell: Desvendando IRM e IEX")
- [Execução Remota de Script PowerShell via Domínio](#execu%C3%A7%C3%A3o-remota-de-script-powershell-via-dom%C3%ADnio "Execução Remota de Script PowerShell via Domínio")
- [Entendendo o IRM e o Comando IEX: Proteção de Informações e Execução de Scripts](#entendendo-o-irm-e-o-comando-iex-prote%C3%A7%C3%A3o-de-informa%C3%A7%C3%B5es-e-execu%C3%A7%C3%A3o-de-scripts "Entendendo o IRM e o Comando IEX: Proteção de Informações e Execução de Scripts")
- [Como Abrir Links no Navegador Padrão via PowerShell](#como-abrir-links-no-navegador-padr%C3%A3o-via-powershell "Como Abrir Links no Navegador Padrão via PowerShell")
- [Fazer Windows PowerShell executar um comando após abrir novamente](#fazer-windows-powershell-executar-um-comando-ap%C3%B3s-abrir-novamente "Fazer Windows PowerShell executar um comando após abrir novamente")
- [Executar verificações de vírus e ameaças usando o Microsoft Defender Antivírus](#executar-verifica%C3%A7%C3%B5es-de-v%C3%ADrus-e-amea%C3%A7as-usando-o-microsoft-defender-antiv%C3%ADrus "Executar verificações de vírus e ameaças usando o Microsoft Defender Antivírus")
- [Guia Rápido do PowerShell: Obtendo Diretórios-Chave através de Variáveis de Ambiente no Windows](#guia-r%C3%A1pido-do-powershell-obtendo-diret%C3%B3rios-chave-atrav%C3%A9s-de-vari%C3%A1veis-de-ambiente-no-windows "Guia Rápido do PowerShell: Obtendo Diretórios-Chave através de Variáveis de Ambiente no Windows")
- [Script PowerShell: Obtendo Caminhos dos Principais Diretórios do Perfil do Usuário no Windows](#script-powershell-obtendo-caminhos-dos-principais-diret%C3%B3rios-do-perfil-do-usu%C3%A1rio-no-windows "Script PowerShell: Obtendo Caminhos dos Principais Diretórios do Perfil do Usuário no Windows")
- [Script PowerShell: Abrir File Explorer e Selecionar Arquivo em um Diretório Específico](#script-powershell-abrir-file-explorer-e-selecionar-arquivo-em-um-diret%C3%B3rio-espec%C3%ADfico "Script PowerShell: Abrir File Explorer e Selecionar Arquivo em um Diretório Específico")
- [Abrir Gerenciador de Arquivos do Windows em pastas de ambiente](#abrir-gerenciador-de-arquivos-do-windows-em-pastas-de-ambiente "Abrir Gerenciador de Arquivos do Windows em pastas de ambiente")
- [Script PowerShell: Abrir Gerenciador de Arquivos com Endereço Específico](#script-powershell-abrir-gerenciador-de-arquivos-com-endere%C3%A7o-espec%C3%ADfico "Script PowerShell: Abrir Gerenciador de Arquivos com Endereço Específico")
- [Executar as atualizações do Windows a partir de um script PowerShell](#executar-as-atualiza%C3%A7%C3%B5es-do-windows-a-partir-de-um-script-powershell "Executar as atualizações do Windows a partir de um script PowerShell")
- [Exportando e importando variáveis em arquivos PowerShell](#exportando-e-importando-vari%C3%A1veis-em-arquivos-powershell "Exportando e importando variáveis em arquivos PowerShell")
- [Exportação e Importação, Compartilhando Funções entre Scripts PowerShell](#exporta%C3%A7%C3%A3o-e-importa%C3%A7%C3%A3o-compartilhando-fun%C3%A7%C3%B5es-entre-scripts-powershell "Exportação e Importação, Compartilhando Funções entre Scripts PowerShell")
- [Passando Argumentos em Scripts PowerShell: Entre arquivos (.ps1)](#passando-argumentos-em-scripts-powershell-entre-arquivos-ps1 "Passando Argumentos em Scripts PowerShell: Entre arquivos (.ps1)")
- [Alterar a cor de fundo do PowerShell](#alterar-a-cor-de-fundo-do-powershell "Alterar a cor de fundo do PowerShell")
- [Ajustando a Janela do PowerShell: Alterando a Largura e a Altura da Janela](#ajustando-a-janela-do-powershell-alterando-a-largura-e-a-altura-da-janela "Ajustando a Janela do PowerShell: Alterando a Largura e a Altura da Janela")
- [Função de Correção de Codificação para Exibição de Texto no PowerShell (UTF8)](#fun%C3%A7%C3%A3o-de-corre%C3%A7%C3%A3o-de-codifica%C3%A7%C3%A3o-para-exibi%C3%A7%C3%A3o-de-texto-no-powershell-utf8 "Função de Correção de Codificação para Exibição de Texto no PowerShell (UTF8)")
- [Janela pop-up PowerShell com .NET Framework com mensagem com botões “Sim” e “Não”](#janela-pop-up-powershell-com-net-framework-com-mensagem-com-bot%C3%B5es-sim-e-n%C3%A3o "Janela pop-up PowerShell com .NET Framework com mensagem com botões 'Sim' e 'Não'")
- [Script PowerShell para Emitir Sequência de Beeps](#script-powershell-para-emitir-sequ%C3%AAncia-de-beeps "Script PowerShell para Emitir Sequência de Beeps")
- [Configuração Dinâmica de Rede no Windows via PowerShell / Habilitando DHCP e DNS Automático](#configura%C3%A7%C3%A3o-din%C3%A2mica-de-rede-no-windows-via-powershell--habilitando-dhcp-e-dns-autom%C3%A1tico "Configuração Dinâmica de Rede no Windows via PowerShell / Habilitando DHCP e DNS Automático")
- [Elevação de Privilégios e Execução Remota](#eleva%C3%A7%C3%A3o-de-privil%C3%A9gios-e-execu%C3%A7%C3%A3o-remota "Elevação de Privilégios e Execução Remota")
- [Obtendo Informações do Sistema com PowerShell: Processador, Memória e Detalhes Gerais](#obtendo-informa%C3%A7%C3%B5es-do-sistema-com-powershell-processador-mem%C3%B3ria-e-detalhes-gerais "Obtendo Informações do Sistema com PowerShell: Processador, Memória e Detalhes Gerais")
- [Script PowerShell: Apresentação Estilizada de Informações do Sistema em Quadros](#script-powershell-apresenta%C3%A7%C3%A3o-estilizada-de-informa%C3%A7%C3%B5es-do-sistema-em-quadros "Script PowerShell: Apresentação Estilizada de Informações do Sistema em Quadros")
- [Manipulando Espaços em PowerShell](#manipulando-espa%C3%A7os-em-powershell "Manipulando Espaços em PowerShell")
- [Verificação e Aplicação Dinâmica da Versão do PowerShell em Scripts CMD](#verifica%C3%A7%C3%A3o-e-aplica%C3%A7%C3%A3o-din%C3%A2mica-da-vers%C3%A3o-do-powershell-em-scripts-cmd "Verificação e Aplicação Dinâmica da Versão do PowerShell em Scripts CMD")
- [Modificando Informações do OEM no Registro do Windows Usando PowerShell](#modificando-informa%C3%A7%C3%B5es-do-oem-no-registro-do-windows-usando-powershell "Modificando Informações do OEM no Registro do Windows Usando PowerShell")
- [Execução Condicional de Recursos (Exemplo de execução de Rotinas)](#execu%C3%A7%C3%A3o-condicional-de-recursos-exemplo-de-execu%C3%A7%C3%A3o-de-rotinas "Execução Condicional de Recursos (Exemplo de execução de Rotinas)")

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

## Passagem de Argumentos entre Arquivos: PowerShell e Batch (CMD)

Em arquivos batch (.cmd ou .bat), passar argumentos entre eles é semelhante, mas usa uma sintaxe um pouco diferente do PowerShell. Aqui está um exemplo simples de como passar argumentos entre dois arquivos batch:

Suponha que você tenha `file1.cmd` e `file2.cmd`.

No `file1.cmd`, você pode chamar o `file2.cmd` e passar argumentos da seguinte maneira:

```batch
REM Chama file2.cmd e passa dois argumentos: "argumento1" e "argumento2"
file2.cmd argumento1 argumento2
```

No `file2.cmd`, você pode acessar esses argumentos usando `%1`, `%2`, etc., que representam o primeiro e o segundo argumentos passados, respectivamente:

```batch
@echo off
REM Exibe os argumentos passados para o arquivo file2.cmd
echo Argumento 1: %1
echo Argumento 2: %2
```

Assim como no PowerShell, você pode acessar os argumentos usando `%1` para o primeiro, `%2` para o segundo e assim por diante. Certifique-se de ajustar os comandos de acordo com o que você precisa realizar nos seus arquivos batch.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Compartilhando Variáveis e Funções entre Arquivos .CMD no Batch

Você pode importar as variáveis e funções de um arquivo `.cmd` para outro usando a declaração `call`. Se o arquivo que você deseja importar contém funções ou variáveis que precisam ser acessadas em outro script `.cmd`, você pode fazer da seguinte maneira:

**Passo 1: Criar um arquivo `.cmd` com variáveis e funções**

Vamos supor que você tem um arquivo chamado `functions.cmd` com variáveis e/ou funções que deseja importar para outro arquivo. Por exemplo, `functions.cmd` pode ter o seguinte conteúdo:

```batch
@echo off
REM Definindo variáveis
set variavelExemplo=123

REM Definindo uma função de exemplo
:exemploFuncao
echo Esta é uma função de exemplo
exit /b
```

**Passo 2: Importar as variáveis e funções em outro arquivo `.cmd`**

Para usar essas variáveis e funções em outro arquivo `.cmd`, você pode simplesmente chamar o arquivo `functions.cmd` usando `call`. Por exemplo, no arquivo em que você deseja usar essas variáveis e funções:

```batch
@echo off
REM Importando variáveis e funções de functions.cmd
call "caminho\para\functions.cmd"

REM Usando variáveis do arquivo importado
echo A variável de exemplo é %variavelExemplo%

REM Chamando a função do arquivo importado
call :exemploFuncao

REM Restante do código do arquivo atual...
```

Dessa forma, ao chamar `functions.cmd` com `call`, todas as variáveis e funções definidas nesse arquivo se tornarão disponíveis para uso no arquivo `.cmd` atual. Lembre-se de ajustar o caminho do arquivo conforme a estrutura do seu diretório.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Atualizando o PowerShell no Windows: Um Guia Passo a Passo

Existe um comando que você pode usar para instalar ou atualizar o PowerShell 7 através do PowerShell que você já tem no seu computador. Aqui está o comando:

```powershell
iex "& { $(irm https://aka.ms/install-powershell.ps1) } -UseMSI"
```

Este comando baixa o script de instalação do PowerShell 7 do site da Microsoft e executa o script para instalar o PowerShell 7.

No entanto, é importante notar que o PowerShell 7 é suportado nos seguintes sistemas operacionais Windows: Windows 10 e 11, Windows Server 2016, 2019 e 2022. Portanto, pode não ser compatível com o Windows 7.

Por favor, verifique a compatibilidade antes de tentar a instalação. Se você estiver usando o Windows 7, pode ser necessário atualizar seu sistema operacional para uma versão mais recente antes de poder instalar o PowerShell 7.

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

## Menu interativo com PowerShell, uma maneira organizada de organizar opções

A princípio, crie o arquivo principal.

***MenuInterativo.ps1***
```powershell
<#
MenuInterativo.ps1 - Executa o menu com opções personalizadas.

URL: https://github.com/systemboys/QuickWindows.git
Autor: Marcos Aurélio R. da Silva "systemboys@hotmail.com"
Manutenção: Marcos Aurélio R. da Silva "systemboys@hotmail.com"

---------------------------------------------------------------
Este programa tem a finalidade de disponibilizar opções personalizadas
para serem selecionadas com uso de setas direcionais.
---------------------------------------------------------------
Histórico:
v0.0.1 2023-11-19 às 23h01, Marcos Aurélio:
  - Versão inicial, começo do script...

Licença: GPL.
#>

# Get the name of the current script file
$currentFileName = $MyInvocation.MyCommand.Name

# Adjusting PowerShell window dimensions
$width = "120"
$height = "30"
$size = New-Object System.Management.Automation.Host.Size($width, $height)
$host.UI.RawUI.WindowSize = $size

# Colors
$Host.UI.RawUI.BackgroundColor = "Black" # Background
$Host.UI.RawUI.ForegroundColor = "Green" # Font

# Optoin Functions
. .\optionFunctions.ps1

# Globla Variables
. .\globalVariables.ps1

# Option Menu
. .\menuOptions.ps1

# Region FUNCTIONS

# Function used to simply revert console colors
function Reverse-Colors {
    $bColor = [System.Console]::BackgroundColor
    $fColor = [System.Console]::ForegroundColor
    [System.Console]::BackgroundColor = $fColor
    [System.Console]::ForegroundColor = $bColor    
}

# Main function showing the menu
function New-Menu {
    param(
        [parameter(Mandatory=$true)][System.Collections.Generic.List[string]]$menuItems, # Contains all menu items
        [string]$title       = $title,                                                   # The title for the menu
        [string]$hint        = $hint,                                                    # Hint to be displayed above menu entries
        [string]$footer      = $footer,                                                  # Menu footer
        [ValidateSet("green","yellow","red","black","white")]                            # You might add more colors allowed by console
        [string]$titleColor  = 'Yellow'                                                  # Color of the title
    )
    
    # Prepare variables with function wide scope
    $invalidChoice = $false                     # Initialize the flag indicating whether an ivalid key was pressed
    $selectIndex   = 0                          # Initialize the variable storing the selection index (by default the first entry)
    $outChar       = 'a'                        # Initialize the variable storing the Enter or Esc value

    # Prepare the cosnole
    [System.Console]::CursorVisible = $false    # Hide the cursor, we don't need it
    [Console]::Clear()                          # Clear everything before showing the menu

    # Main loop showing all the entries and handling the interaction with user
    # End the loop only when Enter or Escape is pressed
    while (([System.Int16]$inputChar.Key -ne [System.ConsoleKey]::Enter) -and ([System.Int16]$inputChar.Key -ne [System.ConsoleKey]::Escape)) {
        
        # Show title and hint
        [System.Console]::CursorTop = 0                     # Start from top and then overwrite all lines; it's used instead of Clear to avoid blinking
        $tempColor = [System.Console]::ForegroundColor      # Keep the default font color 
        [System.Console]::ForegroundColor = $titleColor     # Set the color for title according to value of parameter
        [System.Console]::WriteLine("$title`n")             # The title for the menu
        [System.Console]::ForegroundColor = $tempColor      # Revert back to default font color
        
        [System.Console]::WriteLine($hint)
        [System.Console]::WriteLine($header)
        # Show all entries
        for ($i = 0; $i -lt $menuItems.Count; $i++) {
            [System.Console]::Write("$leftSideEdge > [$i] ")                     # Add identity number to each entry, it's not highlighted for selection but it's in the same line
            if ($selectIndex -eq $i) {
                Reverse-Colors                                                   # In case this is the selected entry, reverse color just for it to make the selection visible
                [System.Console]::WriteLine($menuItems[$i] + "< $rightSideEdge")
                Reverse-Colors      
            } else {
                [System.Console]::WriteLine($menuItems[$i] + "< $rightSideEdge") # In case this is not-selected entry, just show it
            }
        }
        [System.Console]::WriteLine($footer)

        # In case of invalid key, show the message
        if ($invalidChoice) {
            [System.Console]::WriteLine("Invalid button! Try again...")
        } else {
            [System.Console]::Write([System.String]::new(' ',[System.Console]::WindowWidth)) # In case the valid key was used after invalid, clean-up this line
            [System.Console]::SetCursorPosition(0,[System.Console]::CursorTop)               # Set the cursor back to first column so it's properly back to 1st column, 1st row in next iteration of the loop
        }
        $invalidChoice = $false                                                              # Reset the invalid key flag

        # Read the key from user
        $inputChar=[System.Console]::ReadKey($true)

        # Try to convert it to number
        try {
            $number = [System.Int32]::Parse($inputChar.KeyChar)
        }
        catch{
            $number = -1                                                                     # In case it's not a valid number, set to always invalid -1
        }
        
        # Hanlde arrows
        if ([System.Int16]$inputChar.Key -eq [System.ConsoleKey]::DownArrow){
            if ($selectIndex -lt $menuItems.Count -1) {                                      # Avoid selection out of range
                $selectIndex++
            }
        } elseif ([System.Int16]$inputChar.Key -eq [System.ConsoleKey]::UpArrow){
            if ($selectIndex -gt 0){                                                         # Avoid selection out of range
                $selectIndex--
            }
        } elseif ($number -ge 0 -and $number -lt $menuItems.Count){                          # If it's valid number within the range
            # Handle double-digit numbers
            $timestamp = Get-Date       
            while (![System.Console]::KeyAvailable -and ((get-date) - $timestamp).TotalMilliseconds -lt 500){
                Start-Sleep -Milliseconds 250                                                # Give the user 500 miliseconds to type in the 2nd digit, check after 250 to improve responsivness
            }
            if ([System.Console]::KeyAvailable) {                                            # If user typed a key, read it in next line
                $secondChar = [System.Console]::ReadKey($true).KeyChar
                $fullChar   = "$($inputChar.KeyChar)$($secondChar)"                          # Join both keys
                try {
                    # Set selection
                    $number = [System.Int32]::Parse($fullChar)                               # Set the selection accordingly or raise flag for invalid key
                    if ($number -ge 0 -and $number -lt $menuItems.Count) {
                        $selectIndex   = $number
                    } else {
                        $invalidChoice = $true
                    }                
                }
                catch {
                    $invalidChoice = $true
                }
            } else {
                # Set selection
                $selectIndex = $number                                                       # Set selection for single digit number
            }
        } else {
            $invalidChoice = $true                                                           # Key not recognized, raise the flag
        }
        $outChar = $inputChar                                                                # Assign the key value to variable with scope outside the loop
    }

    # Hanlde the result, just show the selected entry if Enter was pressed; do nothing if Escape was pressed
    if ($outChar.Key -eq [System.ConsoleKey]::Enter) {
        [Console]::WriteLine(" You selected $($menuItems[$selectIndex])")
        Invoke-Command -ScriptBlock (Get-Command "menuOption_$selectIndex").ScriptBlock
    }
}

# Endregion FUNCTIONS

# Region MAIN SCRIPT

# Show the menu
do {
    New-Menu $menuItems
} while ($outChar.Key -ne [System.ConsoleKey]::Escape)

#endregion MAIN SCRIPT
```

Crie outro arquivo para colocar as opções do menu.

***menuOptions.ps1***
```powershell
<#
menuOptions.ps1 - Exporta as variáveis para outros arquivos.

Autor: Marcos Aurélio R. da Silva "systemboys@hotmail.com"
Manutenção: Marcos Aurélio R. da Silva "systemboys@hotmail.com"

---------------------------------------------------------------
Este programa tem a finalidade de exportar variáveis para outros arquivos.
---------------------------------------------------------------
Histórico:
v0.0.1 2023-11-19 às 23h01, Marcos Aurélio:
  - Versão inicial, variáveis globais.

Licença: GPL.
#>

# Populate menuItems with example entries
$menuItems = [System.Collections.Generic.List[string]]::new()
$menuItems.Add("..\Exit                                                     ")
$menuItems.Add("Option 1                                                    ")
$menuItems.Add("Option 2                                                    ")
$menuItems.Add("Option 3                                                    ")
```

Crie outro arquivo para colocar as variáveis globais, onde estão o layout do menu como informações, moldura etc.

***globalVariables.ps1***
```powershell
<#
globalVariables.ps1 - Exporta as variáveis para outros arquivos.

Autor: Marcos Aurélio R. da Silva "systemboys@hotmail.com"
Manutenção: Marcos Aurélio R. da Silva "systemboys@hotmail.com"

---------------------------------------------------------------
Este programa tem a finalidade de exportar variáveis para outros arquivos.
---------------------------------------------------------------
Histórico:
v0.0.1 2023-11-19 às 23h01, Marcos Aurélio:
  - Versão inicial, variáveis globais.

Licença: GPL.
#>

# Definition of variables
$currentYear = Get-Date -Format yyyy
$timeOnMarket = ($currentYear - 2008)

# Display
$title  = " QuickWindows v0.2.8"
$hint   = " (i) Use as setas ↓ e ↑ ou números, Enter ◄┘ Executa e ESC sai!`n"
$header = "                     ┌───────────────────────────┐
 ┌───────────────────┤░▒▓ QuackWindows | Home ▓▒░├───────────────────┐
┌┴───────────────────┘                           └───────────────────┴┐"
$leftSideEdge = "│"
# The menu options are posted here from the "menuOptions".ps1 file
$rightSideEdge = "│"
$footer = "└┬─────────────────────────────────────────────────────────────┬─┬─┬─┬┘
 │ (C) $currentYear GLOBAL TEC Informática (R) - GTi                     - ┼ ┤
 │ A $timeOnMarket anos no mercado de informática.                            - ┤
 │ A Tecnologia da Informção é o Futuro.                             ┤
 │ Website: https://gti1.com.br | Email: systemboys@hotmail.com    - ┤
 │ Author: Marcos Aurélio - Engenheiro de Software               - ┼ ┤
 └─────────────────────────────────────────────────────────────┴─┴─┴─┘"
```

Crie outro arquivo para colocar as funções que serão executadas após selecionar as opções.

***optionFunctions.ps1***
```powershell
<#
optionFunctions.ps1 - Exporta as variáveis para outros arquivos.

Autor: Marcos Aurélio R. da Silva "systemboys@hotmail.com"
Manutenção: Marcos Aurélio R. da Silva "systemboys@hotmail.com"

---------------------------------------------------------------
Este programa tem a finalidade de exportar variáveis para outros arquivos.
---------------------------------------------------------------
Histórico:
v0.0.1 2023-11-19 às 23h01, Marcos Aurélio:
  - Versão inicial, variáveis globais.

Licença: GPL.
#>

# Menu Option 0
function menuOption_0() {
    clear
    Write-Host "You have exited the menu..."
    exit
}

# Menu Option 1
function menuOption_1() {
    Write-Host " Function 1 executed successfully..."

    # Start your commands here
    # Command 1...
    # Command 2...
    # Command 3...
    # End your commands here

    # Press a key to continue...
    Write-Host " Press any key to continue..."
    $null = $Host.UI.RawUI.ReadKey("NoEcho,IncludeKeyDown")
}

# Menu Option 2
function menuOption_2() {
    Write-Host " Function 2 executed successfully..."

    # Start your commands here
    # Command 1...
    # Command 2...
    # Command 3...
    # End your commands here

    # Press a key to continue...
    Write-Host " Press any key to continue..."
    $null = $Host.UI.RawUI.ReadKey("NoEcho,IncludeKeyDown")
}

# Menu Option 3
function menuOption_3() {
    Write-Host " Function 3 executed successfully..."

    # Start your commands here
    # Command 1...
    # Command 2...
    # Command 3...
    # End your commands here

    # Press a key to continue...
    Write-Host " Press any key to continue..."
    $null = $Host.UI.RawUI.ReadKey("NoEcho,IncludeKeyDown")
}
```

A estrutura deve ficar da seguinte forma:

```te
/MenuInterativo/
├─ globalVariables.ps1
├─ menuOptions.ps1
├─ optionFunctions.ps1
└─ QuickWindows.ps1
```

Se quiser adicionar sessões para abrir em algumas opções, basta repetir o processo dentro de um subdiretório onde estão os arquivos `.ps1`. Obs.: Você pode usar nas sessões as mesmas variáveis do arquivo `globalVariables.ps1` para manter o mesmo cabeçalho e rodapé. No trecho que importa o arquivo das variáveis globais, use dois pontos para chegar até o arquivo `. ..\globalVariables.ps1`, mas observe que o primeiro ponto é da importação do arquivo.

No caso, a estrutura ficaria da seguinte forma:

```tex
/MenuInterativo/
├─ /nova_sessao/
│  ├─ menuOptions.ps1
│  ├─ optionFunctions.ps1
│  └─ QuickWindows.ps1
├─ globalVariables.ps1
├─ menuOptions.ps1
├─ optionFunctions.ps1
└─ QuickWindows.ps1
```

Observe que no diretório `/nova_sessao/` não existe o arquivo `globalVariables.ps1`, porque a nova sessão pode usar o arquivo que está fora do diretório `/nova_sessao`.

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

Para verificar se um diretório ou arquivo não existe, basta inverter a condição do `if`. Você pode usar o `Test-Path` com o operador `-not` para verificar se o diretório não existe. Aqui está o código de exemplo:

```powershell
# Verifica se o Git não está instalado
Write-Host "Checking if Git does not exist on Windows..."
# Se o Git não estiver instalado, faz o download e instala
$programFiles = "$env:SystemDrive\Program Files"
$directory = "$programFiles\Git"
if (-not (Test-Path $directory)) {
    # Command...
    Write-Host "The directory $directory does not exist."
} else {
    Write-Host "The directory $directory exists."
}
```

Agora, se o diretório não existir em $directory, o bloco de código dentro do if será executado.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Verificando a existência de diretório ou arquivo em duas versões do Windows

Você pode verificar se o Git está instalado no Windows 10 e 11 procurando por um executável específico do Git, como `git.exe`, em diferentes caminhos padrão de instalação. Aqui está um exemplo de como você pode fazer isso no PowerShell:

```powershell
# Verifica se o Git está instalado no Windows (versões 10 e 11)
Write-Host "Checking if Git is installed on Windows..."

# Verifica o caminho padrão de instalação no Windows 10 e 11
$gitPaths = @(
    "$env:ProgramFiles\Git\bin\git.exe",
    "$env:ProgramFiles(x86)\Git\bin\git.exe"
)

$gitInstalled = $false

foreach ($path in $gitPaths) {
    if (Test-Path $path) {
        Write-Host "Git found at $path"
        $gitInstalled = $true
        break
    }
}

if ($gitInstalled) {
    Write-Host "Git is installed."
} else {
    Write-Host "Git is not installed."
    # Comando para instalar o Git ou outra ação apropriada
}
```

Esse script procura pelo executável `git.exe` em locais padrão de instalação do Git no Windows 10 e 11. Se encontrar o `git.exe` em um desses locais, ele indicará que o Git está instalado. Caso contrário, ele informará que o Git não está instalado e você pode adicionar um comando ou ação apropriada para instalação ou tratamento adequado.

> ( ? ) E se eu desejar verificar apenas o diretório?

Sim, você pode adaptar o código para verificar a existência de um diretório em vez de um arquivo específico. Aqui está um exemplo de como verificar se um diretório específico, como o diretório de instalação do Git, existe no Windows 10 e 11:

```powershell
# Verifica se o diretório do Git está instalado no Windows (versões 10 e 11)
Write-Host "Checking if Git directory exists on Windows..."

# Caminhos padrão onde o Git pode estar instalado
$gitDirectories = @(
    "$env:ProgramFiles\Git",
    "$env:ProgramFiles(x86)\Git"
)

$gitInstalled = $false

foreach ($dir in $gitDirectories) {
    if (Test-Path $dir) {
        Write-Host "Git directory found at $dir"
        $gitInstalled = $true
        break
    }
}

if ($gitInstalled) {
    Write-Host "Git directory exists."
} else {
    Write-Host "Git directory does not exist."
    # Comando para instalar o Git ou outra ação apropriada
}
```

Neste caso, o script verifica a existência de diretórios específicos que podem conter a instalação do Git no Windows 10 e 11. Se encontrar o diretório em um dos caminhos especificados, indicará que o diretório do Git está presente. Caso contrário, informará que o diretório do Git não existe, e você pode adicionar um comando ou ação apropriada para lidar com essa situação.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Executar arquivo chamado executável via linha de comando PowerShell

Ok, eu entendo que você quer executar um arquivo chamado "`AnyDesk.exe`" que está localizado em "`C:\Program Files (x86)\AnyDesk`". Uma possível linha de comando para fazer isso em PowerShell é:

```powershell
Start-Process -FilePath "C:\Program Files (x86)\AnyDesk\AnyDesk.exe"
```

Esse comando usa o cmdlet `Start-Process` para iniciar um processo que executa o arquivo especificado pelo parâmetro `-FilePath`. Você pode testar esse comando em seu script e ver se funciona como você espera. Espero ter ajudado. blush: [Start-Process (Microsoft.PowerShell.Management) - PowerShell | Microsoft Docs]

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Verificar para instalar ou executar arquivos executáveis

O objetivo do script abaixo é verificar se um determinado software está instalado, caso esteja, ele ele informará através de uma popup que já está instalado e perguntará se deseja executá-lo, dando opção para o usuário responder com "Sim" ou "Não". Se o usuário responder com "Não", o script executará o "false" levando para a instalação do software.

```power
# Se o AnyDesk não estiver instalado, faz o download e instala
$programFiles = "$env:SystemDrive\Program Files (x86)"
$directory = "$programFiles\AnyDesk"

if (Test-Path $directory) {
    # Carrega a biblioteca do .NET Framework para criar a pop-up
    [System.Reflection.Assembly]::LoadWithPartialName('Microsoft.VisualBasic') | Out-Null

    # Define a mensagem, o título e os botões da pop-up
    $message = "AnyDesk is already installed, do you want to run it?"
    $title = "AnyDesk"
    $buttons = [Microsoft.VisualBasic.MsgBoxStyle]::YesNo

    # Mostra a pop-up ao usuário e guarda a resposta em uma variável
    $response = [Microsoft.VisualBasic.Interaction]::MsgBox($message, $buttons, $title)

    # Verifica se a resposta do usuário foi "Sim"
    if ($response -eq "Yes") {
        # Executa o AnyDesk
        Start-Process -FilePath "C:\Program Files (x86)\AnyDesk\AnyDesk.exe"
    }
    else {
        exit
    }
} else {
    Write-Host "AnyDesk is not installed! Starting installation process."
    Write-Host "File size: 5.27 MB"

    # Link do download e o diretório Temp
    $downloadUrl = "https://github.com/systemboys/_GTi_Support_/raw/main/Windows/Internet/RemoteAccess/AnyDesk.exe"
    $downloadPath = "$env:temp\AnyDesk.exe"
    
    # Faz o download do AnyDesk
    Invoke-WebRequest -Uri $downloadUrl -OutFile $downloadPath
    
    # Instala o AnyDesk
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

## Compressão de arquivos, PowerShell Backup Automático (.zip)

### Descrição
Este script em PowerShell permite a criação fácil de backups compactados em formato ZIP. O usuário é solicitado a fornecer o diretório a ser copiado e o local onde o arquivo ZIP resultante será salvo. O script utiliza a classe `ZipArchive` para criar um arquivo ZIP contendo todos os arquivos do diretório de origem. Além disso, uma barra de progresso é exibida para acompanhar o processo de compactação.

```powershell
# Solicita ao usuário o diretório a ser copiado
do {
    $sourceDirectory = Read-Host "Digite o caminho completo do diretório a ser copiado"
    if (-not $sourceDirectory) {
        Write-Host "Caminho inválido. Por favor, informe um caminho válido."
    }
    elseif (-not (Test-Path $sourceDirectory -PathType Container)) {
        Write-Host "O diretório de origem não existe. Verifique o caminho e tente novamente."
    }
} while (-not $sourceDirectory -or -not (Test-Path $sourceDirectory -PathType Container))

# Solicita ao usuário o caminho onde o arquivo ZIP será salvo
do {
    $destinationZip = Read-Host "Digite o caminho completo do local onde o arquivo ZIP será salvo"
    if (-not $destinationZip) {
        Write-Host "Caminho inválido. Por favor, informe um caminho válido."
    }
    elseif (-not (Test-Path $destinationZip -PathType Container)) {
        Write-Host "O diretório de destino não existe. Verifique o caminho e tente novamente."
    }
} while (-not $destinationZip -or -not (Test-Path $destinationZip -PathType Container))

# Obtém o nome base do diretório de origem e a data e hora atual para criar o nome do arquivo ZIP
$dateString = Get-Date -Format "yyyy-MM-dd HH-mm-ss"
$zipFileName = Join-Path $destinationZip ("$($sourceDirectory -split '\\|/' | Select-Object -Last 1) $dateString.zip")

# Cria uma instância de ZipArchive
$zipArchive = [System.IO.Compression.ZipFile]::Open($zipFileName, 'Create')

# Adiciona uma barra de progresso
Write-Progress -Activity "Comprimindo arquivos" -Status "Iniciando" -PercentComplete 0

# Utiliza a classe ZipArchive para criar o arquivo ZIP
$files = Get-ChildItem -Path $sourceDirectory -File -Recurse
$totalFiles = $files.Count
$currentFile = 0

foreach ($file in $files) {
    # Atualiza a barra de progresso
    $currentFile++
    $percentComplete = ($currentFile / $totalFiles) * 100
    Write-Progress -Activity "Comprimindo arquivos" -Status "Em andamento" -PercentComplete $percentComplete

    # Comprime o arquivo para o arquivo ZIP
    $entry = $zipArchive.CreateEntry($file.FullName -replace [regex]::Escape($sourceDirectory), 'Optimal')
    $stream = $entry.Open()
    $fileStream = [System.IO.File]::OpenRead($file.FullName)
    $fileStream.CopyTo($stream)
    $fileStream.Close()
    $stream.Close()
}

# Fecha o arquivo ZIP
$zipArchive.Dispose()

# Atualiza a barra de progresso para 100% e exibe a conclusão
Write-Progress -Activity "Comprimindo arquivos" -Status "Concluído" -PercentComplete 100
Write-Host "Backup concluído com sucesso. O arquivo ZIP está em: $zipFileName"
```

### Instruções de Uso
1. Execute o script em um ambiente PowerShell.
2. Digite o caminho completo do diretório a ser copiado quando solicitado.
3. Digite o caminho completo do local onde o arquivo ZIP será salvo.
4. Aguarde enquanto o script compacta os arquivos e exibe uma barra de progresso.
5. O arquivo ZIP resultante será salvo no local especificado, com um nome baseado no diretório de origem e na data/hora atual.

Lembre-se de verificar se possui as permissões adequadas para acessar os diretórios e se o módulo `ZipArchive` está disponível no ambiente onde o script será executado. Este script oferece uma solução rápida e eficiente para realizar backups compactados de seus dados importantes.

> ### Correções
> Caso o script anterior apresentar erros, eis aqui algumas modificações e correções!

```powershell
# Solicita ao usuário o diretório a ser copiado
do {
    $sourceDirectory = Read-Host "Enter the full path of the directory to be copied"
    if (-not $sourceDirectory) {
        Write-Host "Invalid path. Please provide a valid path."
    }
    elseif (-not (Test-Path $sourceDirectory -PathType Container)) {
        Write-Host "The source directory does not exist. Check the path and try again."
    }
} while (-not $sourceDirectory -or -not (Test-Path $sourceDirectory -PathType Container))

# Solicita ao usuário o caminho onde o arquivo ZIP será salvo
do {
    $destinationZip = Read-Host "Enter the full path to the location where the ZIP file will be saved"
    if (-not $destinationZip) {
        Write-Host "Invalid path. Please provide a valid path."
    }
    elseif (-not (Test-Path $destinationZip -PathType Container)) {
        Write-Host "The destination directory does not exist. Check the path and try again."
    }
} while (-not $destinationZip -or -not (Test-Path $destinationZip -PathType Container))

# Obtém o nome base do diretório de origem e a data e hora atual para criar o nome do arquivo ZIP
$dateString = Get-Date -Format "yyyy-MM-dd HH-mm-ss"
$zipFileName = Join-Path $destinationZip ("$($sourceDirectory -split '\\|/' | Select-Object -Last 1) $dateString.zip")

# Adiciona uma barra de progresso
Write-Progress -Activity "Compressing files" -Status "Starting" -PercentComplete 0

# Utiliza a classe ZipArchive para criar o arquivo ZIP
try {
    $zipArchive = [System.IO.Compression.ZipFile]::Open($zipFileName, 'Create')

    # Restante do código que usa $zipArchive para adicionar arquivos ao ZIP

    # Fecha o arquivo ZIP
    $zipArchive.Dispose()
}
catch {
    Write-Host "Error using System.IO.Compression.ZipFile: $_"
}

# Utiliza a classe ZipArchive para criar o arquivo ZIP
Write-Host "Creating ZIP archive: $zipFileName"
$files = Get-ChildItem -Path $sourceDirectory -File -Recurse

try {
    Compress-Archive -Path $files.FullName -DestinationPath $zipFileName -Force -CompressionLevel Optimal
    Write-Host "ZIP archive created successfully."
}
catch {
    Write-Host "Error creating ZIP archive: $_"
}

# Adiciona linhas vazias para espaçamento
Write-Host ""
Write-Host ""
Write-Host ""
Write-Host ""

# Atualiza a barra de progresso para 100% e exibe a conclusão
Write-Progress -Activity "Compressing files" -Status "Completed" -PercentComplete 100
Write-Host "Backup completed successfully. The ZIP file is at: $zipFileName"

# Adiciona a instrução return para evitar a mensagem de erro
return
```

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Automatizando a Extração e Execução de Arquivos com PowerShell

**Explicação do Código:**
Este script em PowerShell automatiza o processo de extração de um arquivo ZIP e a subsequente execução de um arquivo executável (`.exe`) contido dentro do diretório descompactado. Aqui está uma explicação passo a passo do código:

1. **Definição dos Caminhos:**
   - `$zipPath`: Representa o caminho completo para o arquivo ZIP que será extraído.
   - `$extractPath`: Indica o diretório de destino para a extração dos arquivos contidos no arquivo ZIP.

```powershell
# Definir o caminho do arquivo zip
$zipPath = "C:\caminho\para\arquivo.zip"

# Definir o caminho do diretório de destino para a extração
$extractPath = "C:\caminho\para\destino"
```

2. **Extração do Arquivo ZIP:**
   - O cmdlet `Expand-Archive` é usado para extrair o conteúdo do arquivo ZIP especificado para o diretório de destino.

```powershell
# Extrair o arquivo zip para o diretório de destino
Expand-Archive -Path $zipPath -DestinationPath $extractPath
```

3. **Definição do Caminho do Arquivo Executável:**
   - O caminho do arquivo executável (`arquivo.exe`) dentro do diretório descompactado é construído usando `Join-Path`.

```powershell
# Definir o caminho do arquivo exe dentro do diretório descompactado
$exePath = Join-Path -Path $extractPath -ChildPath "arquivo.exe"
```

4. **Execução do Arquivo Executável:**
   - O cmdlet `Start-Process` é utilizado para iniciar a execução do arquivo executável no caminho especificado.

```powershell
# Executar o arquivo exe
Start-Process -FilePath $exePath
```

O script é útil para situações em que você deseja automatizar o processo de extração e execução de um aplicativo contido em um arquivo ZIP, economizando esforços manuais. Certifique-se de ajustar os caminhos conforme necessário para se adequarem ao seu ambiente e às localizações específicas dos arquivos.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Criar Atalho para Programa no Desktop usando PowerShell

Sim, é possível criar um atalho para um programa no Desktop do Windows usando o PowerShell. Você pode usar o cmdlet `New-Object` para criar um objeto `WScript.Shell` e, em seguida, usar os métodos desse objeto para criar o atalho.

Aqui está um exemplo de como você pode fazer isso:

```powershell
# Caminho do programa
$programPath = "C:\Caminho\Para\SeuPrograma.exe"

# Caminho do Desktop
$desktopPath = [System.Environment]::GetFolderPath([System.Environment+SpecialFolder]::DesktopDirectory)

# Nome do atalho
$shortcutName = "AtalhoPrograma"

# Caminho completo para o atalho
$shortcutPath = Join-Path -Path $desktopPath -ChildPath "$shortcutName.lnk"

# Criar um objeto WScript.Shell
$shell = New-Object -ComObject WScript.Shell

# Criar atalho
$shortcut = $shell.CreateShortcut($shortcutPath)
$shortcut.TargetPath = $programPath
$shortcut.Save()

Write-Host "Atalho criado em: $shortcutPath"
```

Lembre-se de substituir o valor de `$programPath` com o caminho real do executável do programa que você deseja criar o atalho, e ajuste o nome do atalho conforme necessário.

Salve o script em um arquivo com extensão `.ps1` e execute-o no PowerShell. Isso criará um atalho para o programa especificado no Desktop do Windows.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Criar Atalho para Programa no Desktop com ícone personalizado usando PowerShell

Para adicionar um ícone personalizado ao atalho do seu programa, você pode usar a propriedade `IconLocation` do objeto de atalho. Aqui está o seu código atualizado:

```powershell
# Caminho do programa
$programPath = "C:\Caminho\Para\SeuPrograma.exe"

# Caminho do Desktop
$desktopPath = [System.Environment]::GetFolderPath([System.Environment+SpecialFolder]::DesktopDirectory)

# Nome do atalho
$shortcutName = "AtalhoPrograma"

# Caminho completo para o atalho
$shortcutPath = Join-Path -Path $desktopPath -ChildPath "$shortcutName.lnk"

# Caminho para o ícone
$iconPath = "$env:TEMP\QuickWindows\Images\QuickWindows.ico"

# Criar um objeto WScript.Shell
$shell = New-Object -ComObject WScript.Shell

# Criar atalho
$shortcut = $shell.CreateShortcut($shortcutPath)
$shortcut.TargetPath = $programPath
$shortcut.IconLocation = $iconPath
$shortcut.Save()

Write-Host "Atalho criado em: $shortcutPath"
```

Este código agora criará um atalho para o seu programa com o ícone especificado no caminho `$iconPath`. Certifique-se de que o caminho para o ícone é válido e acessível. Se o arquivo de ícone não existir no local especificado, o atalho será criado sem um ícone.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Criar Atalho para Comando PowerShell no Desktop usando PowerShell

Sim, você pode criar um atalho para um comando usando o mesmo método. Veja como você pode modificar o script para criar um atalho para o comando PowerShell que você forneceu:

```powershell
# Comando a ser executado
$command = "irm qw.gti1.com.br/menu.ps1 | iex"

# Caminho do Desktop
$desktopPath = [System.Environment]::GetFolderPath([System.Environment+SpecialFolder]::DesktopDirectory)

# Nome do atalho
$shortcutName = "AtalhoComando"

# Caminho completo para o atalho
$shortcutPath = Join-Path -Path $desktopPath -ChildPath "$shortcutName.lnk"

# Criar um objeto WScript.Shell
$shell = New-Object -ComObject WScript.Shell

# Criar atalho
$shortcut = $shell.CreateShortcut($shortcutPath)
$shortcut.TargetPath = "powershell.exe"
$shortcut.Arguments = "-Command `"$command`""
$shortcut.Save()

Write-Host "Atalho criado em: $shortcutPath"
```

Este script cria um atalho no Desktop que executa o comando PowerShell fornecido. Substitua o valor da variável `$command` pelo comando que você deseja executar. Certifique-se de ajustar o nome do atalho, se necessário. Salve o script em um arquivo `.ps1` e execute-o no PowerShell para criar o atalho.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Criar Atalho para Comando PowerShell no Desktop com ícone personalizado usando PowerShell

Para adicionar um ícone ao atalho, você pode usar a propriedade `IconLocation` do objeto de atalho. Esta propriedade aceita um caminho para o arquivo de ícone. Aqui está o seu código atualizado:

```powershell
# Comando a ser executado
$command = "irm qw.gti1.com.br/menu.ps1 | iex"

# Caminho do Desktop
$desktopPath = [System.Environment]::GetFolderPath([System.Environment+SpecialFolder]::DesktopDirectory)

# Nome do atalho
$shortcutName = "AtalhoComando"

# Caminho completo para o atalho
$shortcutPath = Join-Path -Path $desktopPath -ChildPath "$shortcutName.lnk"

# Caminho para o ícone
$iconPath = "$env:TEMP\QuickWindows\Images\QuickWindows.ico"

# Criar um objeto WScript.Shell
$shell = New-Object -ComObject WScript.Shell

# Criar atalho
$shortcut = $shell.CreateShortcut($shortcutPath)
$shortcut.TargetPath = "powershell.exe"
$shortcut.Arguments = "-Command `"$command`""
$shortcut.IconLocation = $iconPath
$shortcut.Save()

Write-Host "Atalho criado em: $shortcutPath"
```

Este código agora criará um atalho com o ícone especificado no caminho `$iconPath`. Certifique-se de que o caminho para o ícone é válido e acessível. Se o arquivo de ícone não existir no local especificado, o atalho será criado sem um ícone.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Verificando versão do sistema operacional

Estrutura de controle que verifica qual é a versão do Windows:

```powershell
# Verifica a versão do sistema operacional
$osVersion = (Get-WmiObject -Class Win32_OperatingSystem).Version

# Verifica versões do sistema operacional
if ($osVersion -eq "10.0.19041") {
    Write-Host "Windows 10 version 2004"
} elseif ($osVersion -eq "10.0.18363") {
    Write-Host "Windows 10 version 1909"
} elseif ($osVersion -eq "10.0.17763") {
    Write-Host "Windows 10 version 1809"
} else {
    Write-Host "Unknown Windows version"
}
```

Estrutura de controle que verifica se o sistema operacional é Windows 10 ou 11.

```powershell
# Verifica a versão do sistema operacional
$osVersion = (Get-WmiObject -Class Win32_OperatingSystem).Version

# Verifica se o sistema operacional é Windows 10 ou 11
if ($osVersion -like "10.*" -or $osVersion -like "11.*") {
    Write-Host "O sistema operacional é Windows 10 ou 11."
} else {
    Write-Host "O sistema operacional não é Windows 10 ou 11."
}
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

## Executar comandos do Prompt de comandos do Windows no Windows PowerShell

O código PowerShell para executar o comando "chkdsk /f" é o seguinte:

```powershell
Invoke-Expression -Command "chkdsk /f"
```

Esse comando irá executar o "chkdsk /f" no Prompt de Comando do Windows.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Script de Interação: Janela de Comando Interativa para Execução de Comandos

Para criar um script `.cmd` que abre uma pop-up para digitar um comando e executá-lo no PowerShell, você precisará de um script em batch para interagir com um programa .NET Framework que permita a criação da interface. Infelizmente, não é possível fazer isso diretamente em um arquivo `.cmd`, pois ele é limitado em termos de interface gráfica.

Você pode usar o PowerShell para criar uma janela pop-up com um campo de formulário e um botão "Enviar" e então executar o comando digitado nesse campo. Segue um exemplo em PowerShell:

```powershell
Add-Type -AssemblyName System.Windows.Forms

# Cria uma janela de formulário
$form = New-Object System.Windows.Forms.Form
$form.Text = "Executar Comando"
$form.Width = 300
$form.Height = 150
$form.StartPosition = "CenterScreen"

# Cria um Label com a mensagem informativa
$label = New-Object System.Windows.Forms.Label
$label.Location = New-Object System.Drawing.Point(50,10)
$label.Size = New-Object System.Drawing.Size(250,20)
$label.Text = "Digite o comando:"
$form.Controls.Add($label)

# Cria um campo de texto para o comando
$textBox = New-Object System.Windows.Forms.TextBox
$textBox.Location = New-Object System.Drawing.Point(50,30)
$textBox.Size = New-Object System.Drawing.Size(200,20)
$form.Controls.Add($textBox)

# Cria um botão "Enviar"
$button = New-Object System.Windows.Forms.Button
$button.Location = New-Object System.Drawing.Point(100,70)
$button.Size = New-Object System.Drawing.Size(100,23)
$button.Text = "Enviar"
$button.Add_Click({
    # Verifica se o campo está vazio
    if ([string]::IsNullOrWhiteSpace($textBox.Text)) {
        [System.Windows.Forms.MessageBox]::Show("Por favor, digite um comando!", "Campo Vazio", "OK", [System.Windows.Forms.MessageBoxIcon]::Warning)
    } else {
        # Quando o botão for clicado e o campo não estiver vazio, executa o comando no PowerShell
        $command = $textBox.Text
        Invoke-Expression $command
    }
})
$form.Controls.Add($button)

# Mostra o formulário
$form.ShowDialog()
```

Salve este código em um arquivo `.ps1` e execute-o no PowerShell. Isso abrirá uma janela onde você poderá digitar um comando no campo de texto e clicar no botão "Enviar" para executar esse comando no PowerShell.

Se você realmente precisa que isso seja feito a partir de um arquivo `.cmd`, considere criar um utilitário em C# ou outra linguagem que possa interagir com o `.NET Framework` e chamar esse utilitário a partir do arquivo `.cmd`. Mas isso envolverá um processo mais complexo.

> **_( i )_** Outro exemplo onde o script após ser executado, abre outra janela do Windows PowerShell e executa o comando nessa nova janela.

Claro, é possível fazer com que os comandos enviados pelo formulário sejam executados na própria janela do PowerShell que abre o script. Porém, para isso, é necessário uma abordagem diferente. A execução de comandos em uma janela específica do PowerShell a partir de um script em PowerShell pode ser um pouco complicada, já que normalmente os scripts são executados em uma instância separada do PowerShell.

Se você estiver aberto a uma solução alternativa, podemos criar uma função no PowerShell para abrir uma nova janela do PowerShell e executar os comandos nessa nova janela. Aqui está um exemplo:

```powershell
function ExecutarComando {
    param (
        [string]$comando
    )

    # Abrir uma nova janela do PowerShell e executar o comando
    $psi = New-Object System.Diagnostics.ProcessStartInfo
    $psi.FileName = "powershell"
    $psi.Arguments = "-NoExit -Command `"$comando`""
    [System.Diagnostics.Process]::Start($psi) | Out-Null
}

Add-Type -AssemblyName System.Windows.Forms

# Cria uma janela de formulário
$form = New-Object System.Windows.Forms.Form
$form.Text = "Executar Comando"
$form.Width = 310
$form.Height = 130
$form.StartPosition = "CenterScreen"

# Cria um Label com a mensagem informativa
$label = New-Object System.Windows.Forms.Label
$label.Location = New-Object System.Drawing.Point(10,10)
$label.Size = New-Object System.Drawing.Size(275,20)
$label.Text = "Digite o comando:"
$form.Controls.Add($label)

# Cria um campo de texto para o comando
$textBox = New-Object System.Windows.Forms.TextBox
$textBox.Location = New-Object System.Drawing.Point(10,30)
$textBox.Size = New-Object System.Drawing.Size(275,20)
$textBox.Text = "Digite o comando aqui..."
$textBox.Add_Enter({
    # Limpa o texto inicial quando o usuário clicar no campo
    if ($textBox.Text -eq "Digite o comando aqui...") {
        $textBox.Text = ""
    }
})
$form.Controls.Add($textBox)

# Cria um botão "Enviar"
$button = New-Object System.Windows.Forms.Button
$button.Location = New-Object System.Drawing.Point(100,60)
$button.Size = New-Object System.Drawing.Size(100,23)
$button.Text = "Enviar"
$button.Add_Click({
    # Verifica se o campo está vazio
    if ([string]::IsNullOrWhiteSpace($textBox.Text) -or $textBox.Text -eq "Digite o comando aqui...") {
        [System.Windows.Forms.MessageBox]::Show("Por favor, digite um comando!", "Campo Vazio", "OK", [System.Windows.Forms.MessageBoxIcon]::Warning)
    } else {
        # Quando o botão for clicado e o campo não estiver vazio, executa o comando na nova janela do PowerShell
        $command = $textBox.Text
        ExecutarComando -comando $command
    }
})
$form.Controls.Add($button)

# Mostra o formulário
$form.ShowDialog()
```

Esse script define uma função chamada `ExecutarComando` que abre uma nova janela do PowerShell e executa o comando passado como argumento. Ao clicar em "Enviar" no formulário, ele usará essa função para executar o comando na nova janela do PowerShell.

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

## Entendendo o IRM e o Comando IEX: Proteção de Informações e Execução de Scripts

O IRM (Information Rights Management) é uma tecnologia que permite especificar permissões de acesso a mensagens de email. O IRM usa o Active Directory Rights Management Services (AD RMS), que é um componente do Windows Server 2008 e posteriores. O AD RMS permite que os usuários criem um conteúdo protegido por direitos, como mensagens de email e anexos, além de controlar como o conteúdo é usado e para quem ele é distribuído.

O IRM no Exchange depende do AD RMS que estiver sendo implantado na floresta do Active Directory na qual o servidor do Exchange reside. A configuração do AD RMS não é sincronizada automaticamente entre as organizações do Exchange Online e local.

Por outro lado, iex é um comando do PowerShell que é a abreviação de Invoke-Expression. Ele é usado para executar um script. Quando combinado com irm, que é a abreviação de Invoke-RestMethod e é usado para baixar um script de um site, iex (irm [url]) é uma maneira de baixar e executar um conjunto de comandos de um site. Isso é uma operação bastante poderosa e pode ser suficiente para assumir o controle de sua máquina se o script for malicioso. Portanto, é seguro se e somente se o operador desse site for confiável.

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

## Fazer Windows PowerShell executar um comando após abrir novamente

Sim, é possível fazer o Windows PowerShell executar um comando após abrir novamente. Você pode usar o parâmetro -Command do cmdlet Start-Process para especificar o comando que você quer executar na nova janela aberta. Por exemplo, se você quer abrir o arquivo "`.\QuickWindows.cmd`", você pode usar o seguinte código:

```powershell
# Inicia o PowerShell em modo Administrador com o comando desejado
Start-Process -FilePath "powershell.exe" -Verb runAs -ArgumentList "-Command", "& {.\QuickWindows.cmd}"
```

Esse código usa o cmdlet Start-Process com o parâmetro -FilePath para especificar o caminho do PowerShell, o parâmetro -Verb para especificar a ação de executar como Administrador, e o parâmetro -ArgumentList para especificar o comando que você quer executar na nova janela aberta, que é "`.\QuickWindows.cmd`".

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Executar verificações de vírus e ameaças usando o Microsoft Defender Antivírus

No entanto, você pode usar o PowerShell para executar verificações de vírus e ameaças usando o Microsoft Defender Antivírus. Por exemplo, você pode iniciar uma verificação completa de malware com o seguinte comando:

```powershell
Start-MpScan -ScanType FullScan
```

Este comando inicia uma verificação completa de malware no seu sistema. Lembre-se de executar o PowerShell como administrador para garantir que você tenha as permissões necessárias para executar esses comandos.

> **_( i )_** Tipos de verificações que pode ser executado usando o Microsoft Defender Antivírus via PowerShell.

Existem diferentes tipos de verificações que você pode executar usando o Microsoft Defender Antivírus via PowerShell:

1. Verificação rápida: Esta opção é útil quando você não quer gastar tempo executando uma verificação completa em todos os arquivos e pastas. Se a Segurança do Windows recomendar que você execute um dos outros tipos de verificação, você será notificado quando a verificação rápida for concluída. Para executar uma verificação rápida, você pode usar o seguinte comando no PowerShell:

```powershell
Start-MpScan -ScanType QuickScan
```

2. Verificação completa: Esta opção verifica todos os arquivos e programas em seu dispositivo. Para executar uma verificação completa, você pode usar o seguinte comando no PowerShell:

```powershell
Start-MpScan -ScanType FullScan
```

3. Verificação personalizada: Esta opção verifica apenas os arquivos e as pastas que você selecionar. Para executar uma verificação personalizada, você pode usar o seguinte comando no PowerShell:

```powershell
Start-MpScan -ScanPath "caminho_para_o_arquivo_ou_pasta"
```

4. Microsoft Defender verificação offline: Esta opção usa as últimas definições para verificar se o seu dispositivo contém as ameaças mais recentes. Isso acontece após uma reinicialização, sem carregar Windows, portanto, qualquer malware persistente tem um momento mais difícil de ocultar ou se defender. Para executar uma verificação offline, você pode usar o seguinte comando no PowerShell:

```powershell
Start-MpWDOScan
```

Lembre-se de executar o PowerShell como administrador para garantir que você tenha as permissões necessárias para executar esses comandos.

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

## Abrir Gerenciador de Arquivos do Windows em pastas de ambiente

Comando PowerShell para abrir o gerenciador de arquivos do Windows em uma pasta de ambiente como área de trabalho por exemplo.

```powershell
$folderPath = [Environment]::GetFolderPath("Desktop")
Start-Process $folderPath
```

> **_( ? )_** É possível abrir dois diretórios diferentes?

Sim, é possível abrir duas janelas do gerenciador de arquivos e colocá-las lado a lado. Aqui está um exemplo de como você pode fazer isso usando o PowerShell:

```powershell
# Caminho para a Área de Trabalho
$desktopPath = [Environment]::GetFolderPath("Desktop")

# Caminho para o Gerenciador de Arquivos
$explorerPath = [Environment]::GetFolderPath("MyDocuments")

# Abrir a Área de Trabalho
Start-Process $desktopPath

# Abrir o Gerenciador de Arquivos
Start-Process $explorerPath
```

Este script abrirá duas janelas separadas, uma para a Área de Trabalho e outra para o Gerenciador de Arquivos. Você pode então organizá-las lado a lado manualmente. Por favor, note que o PowerShell não tem a capacidade de organizar as janelas automaticamente. Isso terá que ser feito manualmente pelo usuário.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Script PowerShell: Abrir Gerenciador de Arquivos com Endereço Específico

Script para abrir a Área de Trabalho (Desktop) e depois o Gerenciador de Arquivos no endereço fornecido.

```powershell
Add-Type -AssemblyName System.Windows.Forms

# Cria uma caixa de diálogo para inserir o local
$form = New-Object System.Windows.Forms.Form
$form.Text = "Informe o local"
$form.Size = New-Object System.Drawing.Size(300,150)
$form.StartPosition = "CenterScreen"

$label = New-Object System.Windows.Forms.Label
$label.Text = "Digite o local:"
$label.AutoSize = $true
$label.Location = New-Object System.Drawing.Point(10,10)
$form.Controls.Add($label)

$textBox = New-Object System.Windows.Forms.TextBox
$textBox.Location = New-Object System.Drawing.Point(10,30)
$textBox.Size = New-Object System.Drawing.Size(265,20)
$form.Controls.Add($textBox)

$button = New-Object System.Windows.Forms.Button
$button.Location = New-Object System.Drawing.Point(100,70)
$button.Size = New-Object System.Drawing.Size(100,30)
$button.Text = "Enviar"
$button.Add_Click({
    $address = $textBox.Text
    if ([string]::IsNullOrEmpty($address)) {
        [System.Windows.Forms.MessageBox]::Show("Por favor, informe um local!", "Erro", "OK", "Error")
    } else {
        # Abrir o Gerenciador de Arquivos com o local fornecido
        Start-Process "explorer.exe" ([Environment]::GetFolderPath("Desktop"))
        Start-Process "explorer.exe" $address
        $form.Close()
    }
})
$form.Controls.Add($button)

$form.ShowDialog()
```

Este script abrirá apenas uma instância do Gerenciador de Arquivos na Área de Trabalho (Desktop) e outra no endereço que você fornecer, evitando a abertura duplicada da Área de Trabalho.

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

Você pode usar o comando `dot source` no PowerShell para importar as variáveis do arquivo `file2.ps1` para o arquivo `file1.ps1`. Aqui está um exemplo de como você pode fazer isso:

```powershell
# Conteúdo do file2.ps1
$variable1 = "valor1"
$variable2 = "valor2"
$variable3 = "valor3"

# Conteúdo do file1.ps1
. ./file2.ps1  # Importa as variáveis do file2.ps1

# Agora você pode usar as variáveis no file1.ps1
Write-Host $variable1
Write-Host $variable2
Write-Host $variable3
```

No exemplo acima, o comando `. ./file2.ps1` no arquivo `file1.ps1` importa as variáveis do arquivo `file2.ps1`. Agora, você pode usar as variáveis `variable1`, `variable2` e `variable3` no arquivo `file1.ps1` como se elas fossem definidas lá. Lembre-se de que o caminho para `file2.ps1` deve ser o caminho correto do arquivo em seu sistema.

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

## Janela pop-up PowerShell com .NET Framework com mensagem com botões “Sim” e “Não”

Sim, é possível criar uma janela pop-up no PowerShell usando o .NET  Framework. Aqui está um exemplo de como você pode fazer isso:

```powershell
Add-Type -AssemblyName PresentationFramework

$ButtonType = [System.Windows.MessageBoxButton]::YesNo
$MessageIcon = [System.Windows.MessageBoxImage]::Question
$MessageBody = "Deseja executar o comando?"
$MessageTitle = "Executar o comando"
$MessageBox = [System.Windows.MessageBox]::Show($MessageBody,$MessageTitle,$ButtonType,$MessageIcon)

if ($MessageBox -eq 'Yes') {
    # Coloque aqui seu comando de instalação!
}
```

Neste script, uma janela pop-up é criada com a  mensagem “Deseja instalar o AnyDesk?” e os botões “Sim” e “Não”. Se o  usuário clicar em “Sim”, o comando de instalação será executado.  Lembre-se de substituir a linha de comentário pelo comando de instalação do AnyDesk. Se o usuário clicar em “Não”, a janela pop-up será  simplesmente fechada.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Script PowerShell para Emitir Sequência de Beeps

Você pode usar o cmdlet `Console.Beep()` do PowerShell para emitir um som do tipo bip. Aqui está um exemplo simples:

```powershell
[Console]::Beep(500, 300)
```

Neste exemplo, `500` é a frequência do som em hertz e `300` é a duração em milissegundos. Você pode ajustar esses valores conforme necessário para obter o tipo de som desejado.

Você pode usar um loop para reproduzir vários beeps em sequência. Aqui está um exemplo de como você pode fazer isso:

```powershell
$numeroDeBeeps = 10
for ($i = 0; $i -lt $numeroDeBeeps; $i++) {
    [Console]::Beep(500, 300)
    Start-Sleep -Milliseconds 200  # Aguarda um curto período entre os beeps
}
```

Isso reproduzirá o som de bip 10 vezes em sequência, com um intervalo de 200 milissegundos entre cada um. Você pode ajustar `$numeroDeBeeps` para o número desejado de beeps e modificar a frequência e duração conforme necessário.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Configuração Dinâmica de Rede no Windows via PowerShell / Habilitando DHCP e DNS Automático

É possível acessar e modificar configurações de rede usando o Windows PowerShell. Você pode usar cmdlets específicos para interagir com as configurações de rede. No entanto, não há um comando direto equivalente ao "control folders" para as configurações de rede. Em vez disso, você pode usar cmdlets específicos para executar tarefas relacionadas à rede.

Aqui estão alguns exemplos de cmdlets que podem ser úteis:

1. **Visualizar informações da interface de rede:**
   ```powershell
   Get-NetAdapter
   ```

2. **Visualizar configurações IP:**
   ```powershell
   Get-NetIPAddress
   ```

3. **Configurar um endereço IP manualmente:**
   ```powershell
   New-NetIPAddress -InterfaceAlias "Nome da Interface" -IPAddress "192.168.1.2" -PrefixLength 24 -DefaultGateway "192.168.1.1"
   ```

4. **Configurar as configurações DNS:**
   ```powershell
   Set-DnsClientServerAddress -InterfaceAlias "Nome da Interface" -ServerAddresses ("8.8.8.8", "8.8.4.4")
   ```

Lembre-se de substituir "Nome da Interface" pelo nome real da sua interface de rede.

Se você precisar de funcionalidades mais avançadas, como configurações específicas do TCP/IP ou configurações avançadas de firewall, pode ser necessário usar ferramentas adicionais ou cmdlets específicos.

Para configurar todas as configurações de IP, incluindo os servidores DNS, para serem atribuídas dinamicamente pelo DHCP, você pode usar o seguinte comando no PowerShell:

```powershell
Get-NetAdapter | ForEach-Object { $_ | Set-NetIPInterface -Dhcp Enabled }
Get-DnsClient | Set-DnsClientServerAddress -ResetServerAddresses
```

O primeiro comando usa `Set-NetIPInterface -Dhcp Enabled` para habilitar a configuração dinâmica do DHCP para cada interface de rede, e o segundo comando usa `Set-DnsClientServerAddress -ResetServerAddresses` para restaurar as configurações de DNS para serem obtidas automaticamente do servidor DHCP.

Certifique-se de executar o PowerShell como administrador para garantir as permissões necessárias para modificar as configurações de rede.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Elevação de Privilégios e Execução Remota

**Script em PowerShell: ElevacaoPrivilégiosExecucaoRemota.ps1**

```powershell
# Verifica se o Windows PowerShell está sendo executado como administrador
if (-not ([Security.Principal.WindowsPrincipal][Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole([Security.Principal.WindowsBuiltInRole]::Administrator)) {
    Write-Host "Este script precisa ser executado como administrador."
    Start-Process powershell -Verb RunAs -ArgumentList "-Command irm qw.gti1.com.br/menu.ps1 | iex"
    exit
}
```

**Guia Rápido:**

Este script em PowerShell é projetado para realizar duas tarefas principais: verificar se está sendo executado como administrador e, se não estiver, realizar a elevação de privilégios e executar um script remoto.

**Instruções:**

1. **Verificação de Privilégios:**
   O script começa verificando se o Windows PowerShell está sendo executado como administrador. Isso é feito utilizando a classe `[Security.Principal.WindowsPrincipal]` e `[Security.Principal.WindowsIdentity]`, obtendo a identidade atual e verificando se ela está no grupo de Administradores usando `IsInRole`.

    ```powershell
    if (-not ([Security.Principal.WindowsPrincipal][Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole([Security.Principal.WindowsBuiltInRole]::Administrator)) {
    ```

2. **Elevação de Privilégios:**
   Se a verificação de privilégios falhar, uma mensagem é exibida indicando que o script precisa ser executado como administrador. Em seguida, o script é reiniciado com privilégios elevados usando `Start-Process` e o argumento `-Verb RunAs`.

    ```powershell
        Write-Host "Este script precisa ser executado como administrador."
        Start-Process powershell -Verb RunAs -ArgumentList "-Command irm qw.gti1.com.br/menu.ps1 | iex"
        exit
    ```

   - `Write-Host`: Exibe uma mensagem informativa no console.
   - `Start-Process`: Inicia um novo processo do PowerShell com privilégios elevados.
   - `-Verb RunAs`: Especifica que o novo processo deve ser executado como administrador.
   - `-ArgumentList`: Fornece os argumentos para o novo processo, que neste caso executa um comando remoto.

3. **Execução Remota:**
   O comando remoto executado é:

    ```powershell
    irm qw.gti1.com.br/menu.ps1 | iex
    ```

   - `irm`: Alias para `Invoke-RestMethod`, utilizado para baixar o script remoto.
   - `qw.gti1.com.br/menu.ps1`: URL do script remoto a ser baixado.
   - `iex`: Alias para `Invoke-Expression`, que executa o script baixado.

Este script é útil quando se precisa garantir que um script seja executado com privilégios elevados e que o código remoto seja baixado e executado automaticamente. Certifique-se de entender os riscos associados à execução de scripts remotos antes de utilizá-lo.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Obtendo Informações do Sistema com PowerShell: Processador, Memória e Detalhes Gerais

Sim, é possível obter informações sobre o sistema, incluindo detalhes do processador, quantidade de memória e outros, usando o Windows PowerShell. O PowerShell fornece cmdlets (comandos) específicos para recuperar essas informações. Aqui estão alguns exemplos:

1. **Informações do Processador:**
```powershell
Get-WmiObject -Class Win32_Processor | Select-Object Name, MaxClockSpeed, NumberOfCores, NumberOfLogicalProcessors
```

Este comando utiliza o cmdlet `Get-WmiObject` para acessar informações do processador através da classe `Win32_Processor`.

2. **Informações de Memória:**
```powershell
Get-WmiObject -Class Win32_PhysicalMemory | Select-Object Capacity
```

Este comando utiliza o cmdlet `Get-WmiObject` para acessar informações sobre a memória física instalada através da classe `Win32_PhysicalMemory`.

3. **Informações Gerais do Sistema:**
```powershell
Get-CimInstance -ClassName Win32_ComputerSystem | Select-Object Manufacturer, Model, TotalPhysicalMemory
```

O cmdlet `Get-CimInstance` é utilizado para acessar informações gerais do sistema através da classe `Win32_ComputerSystem`.

Estes são apenas alguns exemplos. Você pode combinar e personalizar esses comandos conforme necessário para obter informações específicas do sistema. Lembre-se de que alguns comandos podem exigir privilégios administrativos para acessar determinadas informações.

Além disso, o PowerShell também fornece variáveis automáticas, como `$env:PROCESSOR_ARCHITECTURE` e `$env:NUMBER_OF_PROCESSORS`, que contêm informações sobre a arquitetura do processador e o número de processadores, respectivamente.

Experimente esses comandos no console do PowerShell para ver as informações diretamente no ambiente de execução.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Script PowerShell: Apresentação Estilizada de Informações do Sistema em Quadros

Aqui está um exemplo de um script em PowerShell que mostra as informações do processador, memória:

```powershell
# Função para exibir informações em um quadro
function Show-InfoFrame {
    param(
        [string]$title,
        [string]$content
    )

    Write-Host ("_" * 100)
    Write-Host ("{0,-100}" -f $title)
    Write-Host ("{0,-100}" -f $content)
}

# Obter informações do processador
$processorInfo = Get-WmiObject -Class Win32_Processor | Select-Object Name, MaxClockSpeed, NumberOfCores, NumberOfLogicalProcessors
$processorContent = "Name: $($processorInfo.Name)", "Max Clock Speed: $($processorInfo.MaxClockSpeed) MHz", "Cores: $($processorInfo.NumberOfCores)", "Logical Processors: $($processorInfo.NumberOfLogicalProcessors)"

# Obter informações de memória
$memoryInfo = Get-WmiObject -Class Win32_PhysicalMemory | Measure-Object -Property Capacity -Sum
$memoryContent = "Total Physical Memory: {0:N2} GB" -f ($memoryInfo.Sum)

# Obter informações gerais do sistema
$systemInfo = Get-CimInstance -ClassName Win32_ComputerSystem | Select-Object Manufacturer, Model, TotalPhysicalMemory
$systemContent = "Manufacturer: $($systemInfo.Manufacturer)", "Model: $($systemInfo.Model)", "Total Physical Memory: {0:N2} GB" -f ($systemInfo.TotalPhysicalMemory / 1GB)

# Exibir informações em quadros
Show-InfoFrame -title "Processor Info" -content ($processorContent -join "`n")
Show-InfoFrame -title "Memory Info" -content $memoryContent
Show-InfoFrame -title "System Info" -content ($systemContent -join "`n")

Write-Host ("_" * 100)
```

Este script usa linhas horizontais para criar seções distintas e aumenta o comprimento para 100 caracteres para proporcionar uma aparência mais organizada. Execute-o no console do PowerShell para visualizar as informações formatadas.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Manipulando Espaços em PowerShell

Neste script PowerShell, é demonstrado como inserir uma determinada quantidade de espaços antes de um texto utilizando o cmdlet `Write-Host`. No exemplo fornecido, são inseridos 15 espaços antes da mensagem "Distante da margem 15 caracteres espaços".

```powershell
Write-Host (" " * 15 + "Distante da margem 15 caracteres espaços.")
```

O número entre os parênteses após o asterisco indica quantos espaços serão inseridos antes da mensagem. Esse script pode ser útil em situações em que seja necessário alinhar ou posicionar textos de saída em uma interface de linha de comando.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Verificação e Aplicação Dinâmica da Versão do PowerShell em Scripts CMD

Você pode usar o seguinte script em um arquivo `.cmd` para verificar se o PowerShell 7 ou posterior está instalado. Se estiver, ele define uma variável com o valor "pwsh". Caso contrário, ele define a variável com o valor "PowerShell".

```cmd
@echo off
set "psCommand=powershell -Command "& {if ($PSVersionTable.PSVersion.Major -ge 7) {'pwsh'} else {'PowerShell'}}""
for /f "delims=" %%i in ('%psCommand%') do set "result=%%i"

echo %result%
```

Este script usa o comando `powershell` para verificar a versão do PowerShell instalada. Se a versão principal (`$PSVersionTable.PSVersion.Major`) for 7 ou superior, ele retorna "pwsh". Caso contrário, retorna "PowerShell". O resultado é então armazenado na variável `result`. O comando `echo %result%` é usado para exibir o valor da variável `result`.

Você pode modificar o script anterior para usar a variável `result` no lugar de "PowerShell". Aqui está como você pode fazer isso:

> Exemplo

```cmd
@echo off
set "psCommand=powershell -Command "& {if ($PSVersionTable.PSVersion.Major -ge 7) {'pwsh'} else {'PowerShell'}}""
for /f "delims=" %%i in ('%psCommand%') do set "result=%%i"

%result%.exe -NoProfile -ExecutionPolicy Bypass -Command "& {Start-Process %result%.exe -ArgumentList '-NoProfile -ExecutionPolicy Bypass -File ""%~dp0Package_Installers\RunPowerShellCommands.ps1""' -Verb RunAs}"
```

Este script primeiro verifica a versão do PowerShell e armazena o resultado na variável `result`. Em seguida, ele usa essa variável para executar o comando desejado. Se o PowerShell 7 ou posterior estiver instalado, ele usará "pwsh". Caso contrário, ele usará "PowerShell".

O número entre os parênteses após o asterisco indica quantos espaços serão inseridos antes da mensagem. Esse script pode ser útil em situações em que seja necessário alinhar ou posicionar textos de saída em uma interface de linha de comando.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Modificando Informações do OEM no Registro do Windows Usando PowerShell

É possível fazer isso com scripts em PowerShell. Aqui está um exemplo de como você pode fazer isso:

```powershell
$Path = "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\OEMInformation"
Set-ItemProperty -Path $Path -Name "Model" -Value ""
Set-ItemProperty -Path $Path -Name "Manufacturer" -Value ".:: GLOBAL TEC Informática ::."
Set-ItemProperty -Path $Path -Name "Logo" -Value "\\windows\\System32\\oemlogo.bmp"
Set-ItemProperty -Path $Path -Name "SupportPhone" -Value "(99)984399557 Marcos GTi (WhatsApp)"
Set-ItemProperty -Path $Path -Name "SupportURL" -Value "https://www.gti1.com.br"
Set-ItemProperty -Path $Path -Name "SupportHours" -Value "Segunda a sexta de 8h às 18h e sábado até meio dia."
```

Este script PowerShell faz essencialmente a mesma coisa que o seu script .reg. Ele define as propriedades do caminho do registro especificado. Por favor, substitua os valores conforme necessário.

**Nota:** Executar scripts que modificam o registro pode ter efeitos significativos no seu sistema, então sempre tenha cuidado e certifique-se de entender o que o script está fazendo antes de executá-lo. É uma boa prática fazer um backup do registro antes de fazer qualquer modificação. Além disso, você pode precisar de privilégios de administrador para modificar certas chaves do registro.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Execução Condicional de Recursos (Exemplo de execução de Rotinas)

Este script em PowerShell permite a execução condicional de recursos com base em rotinas específicas. O usuário pode inserir uma ou mais rotinas separadas por vírgulas e o script executará os recursos associados a essas rotinas. Se várias rotinas forem fornecidas, o script aguardará a conclusão do recurso atual antes de prosseguir com o próximo. O script também inclui validação para garantir que uma entrada válida seja fornecida.

```powershell
# Array associativo que mapeia as rotinas aos recursos
$Resources = @{
    '123' = 'calc'
    '456' = 'control'
    '789' = 'winver'
}

# Função para executar um recurso
function Execute-Resource {
    param(
        [string]$Resource
    )

    Start-Process $Resource
}

# Loop para solicitar entrada até que uma entrada válida seja fornecida
do {
    Write-Host 'Enter one or more of a routine, example: 123, 456, 789:'
    $Input = Read-Host

    if ([string]::IsNullOrWhiteSpace($Input)) {
        Write-Host 'Please introduce a routine!'
    }
} until (-not [string]::IsNullOrWhiteSpace($Input))

$Routines = $Input -split ','
foreach ($Routine in $Routines) {
    $Resource = $Resources[$Routine.Trim()]
    if ($Resource) {
        Execute-Resource $Resource
        if ($Routines.Count -gt 1) {
            Write-Host "Waiting for $Resource to finish. Press Enter to continue..."
            Read-Host
        }
    } else {
        Write-Host "Invalid routine: $Routine"
    }
}
```

Outra abordagem com a "Execução Sequencial de Scripts PowerShell em Janelas Separadas".

Você pode modificar o script para abrir uma nova janela do PowerShell para cada arquivo .ps1 a ser executado. Aqui está o script atualizado para fazer isso:

```powershell
# Array associativo que mapeia as rotinas aos arquivos .ps1
$Files = @{
    "123" = "$env:TEMP\QuickWindows\Package_Installers\Internet_Session\Install_AnyDesk.ps1"
    "456" = "$env:TEMP\QuickWindows\Package_Installers\Internet_Session\Install_RustDesk.ps1"
    "789" = "$env:TEMP\QuickWindows\Package_Installers\Internet_Session\Install_Transmission.ps1"
}

# Função para executar um arquivo .ps1 em uma nova janela do PowerShell
function Execute-Script {
    param(
        [string]$File
    )

    # Construir o comando para executar o arquivo .ps1 em uma nova janela
    $Command = "Start-Process powershell -ArgumentList '-NoExit','-File','$File' -WindowStyle Hidden"

    # Executar o comando
    Invoke-Expression $Command
}

# Loop para solicitar entrada até que uma entrada válida seja fornecida
do {
    Write-Host 'Enter one or more of a routine, example: 123, 456, 789:'
    $Input = Read-Host

    if ([string]::IsNullOrWhiteSpace($Input)) {
        Write-Host 'Please introduce a routine!'
    }
} until (-not [string]::IsNullOrWhiteSpace($Input))

$Routines = $Input -split ','
foreach ($Routine in $Routines) {
    $File = $Files[$Routine.Trim()]
    if ($File) {
        Execute-Script $File
        Write-Host "Waiting for $File to finish. Press Enter to continue..."
        Read-Host
    } else {
        Write-Host "Invalid routine: $Routine"
    }
}
```

Este script abrirá uma nova janela do PowerShell de forma oculta para cada arquivo .ps1 a ser executado, permitindo que você execute vários arquivos sequencialmente. Certifique-se de substituir os caminhos dos arquivos .ps1 pelos caminhos corretos em seu sistema.

Para corrigir o script para que abra uma nova janela do Windows PowerShell e não seja oculta ao executar o arquivo .ps1, você pode alterar a linha onde o comando é construído para incluir o parâmetro `-Wait`. Isso fará com que o PowerShell aguarde a conclusão do script antes de continuar.

Aqui está a modificação necessária no seu script:

```powershell
# Construir o comando para executar o arquivo .ps1 em uma nova janela e aguardar sua conclusão
$Command = "Start-Process powershell -ArgumentList '-NoExit','-File','$File' -Wait"
```

Com essa alteração, ao executar o script, ele deve abrir uma nova janela do Windows PowerShell e exibir a execução do arquivo .ps1.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---