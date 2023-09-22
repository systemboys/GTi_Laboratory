# [Laboratório GTi](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi")
# Prompt de Comandos e o PowerShell

[![Terminal Windows](https://github.com/systemboys/GTi_Laboratory/blob/main/Microsoft%20Windows/Prompt%20de%20Comandos%20e%20o%20PowerShell/images/WINDOWS-TERMINAL.png?raw=true "Terminal Windows")](https://github.com/systemboys/GTi_Laboratory/blob/main/Microsoft%20Windows/Prompt%20de%20Comandos%20e%20o%20PowerShell/images/WINDOWS-TERMINAL.png?raw=true "Terminal Windows")

- [Menu de Instalação de Programas no Prompt de Comando do Windows](#menu-de-instala%C3%A7%C3%A3o-de-programas-no-prompt-de-comando-do-windows "Menu de Instalação de Programas no Prompt de Comando do Windows")
- [Como Corrigir a Exibição de Caracteres Especiais no Prompt de Comando do Windows](#como-corrigir-a-exibi%C3%A7%C3%A3o-de-caracteres-especiais-no-prompt-de-comando-do-windows "Como Corrigir a Exibição de Caracteres Especiais no Prompt de Comando do Windows")

---

## Menu de Instalação de Programas no Prompt de Comando do Windows

Para criar um menu no Prompt de Comandos ou PowerShell do Windows que permite ao usuário baixar e instalar programas, você pode usar scripts em lote (batch scripts) para simplificar esse processo. Abaixo, vou mostrar um exemplo de como criar um menu simples para baixar e instalar o WinRAR usando um script em lote. Certifique-se de que o usuário execute o script com privilégios administrativos, pois a instalação de programas normalmente requer direitos de administrador. 

Aqui está um exemplo de script em lote:

```batch
@echo off
chcp 65001
title Menu de Instalação

:menu
cls
echo ╭───────────────────────────────────────╮
echo │          SELECIONE UMA OPÇAO          │
echo ╰───────────────────────────────────────╯
echo.
echo ╭───────────────────────────────────────╮
echo │ 1 │ Baixar e Instalar WinRAR          │
echo │ 2 │ Sair                              │
echo ╰───────────────────────────────────────╯
echo.

set /p opcao=Digite o número da opção desejada: 

if "%opcao%"=="1" (
    echo Baixando WinRAR...
    bitsadmin /transfer "DownloadWinRAR" https://exemplo.com/winrar.exe "%CD%\winrar.exe"
    echo.
    echo Instalando WinRAR...
    start /wait "" "%CD%\winrar.exe"
    del /f /a winrar.exe
    echo.
    echo WinRAR instalado com sucesso!
    pause
) else if "%opcao%"=="2" (
    echo Saindo...
    exit
) else (
    echo Opção inválida. Tente novamente.
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
[(&uarr;) Subir](#prompt-de-comandos-e-o-powershell "Subir para o topo")

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
[(&uarr;) Subir](#prompt-de-comandos-e-o-powershell "Subir para o topo")

---