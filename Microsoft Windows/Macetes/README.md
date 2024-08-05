# [GTi Laboratory](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Laboratório GTi") / Macetes técnicos

[![Macetes diversos para lidar com Windows](https://github.com/systemboys/GTi_Laboratory/raw/main/Microsoft%20Windows/Macetes/images/banner1.jpg "Macetes diversos para lidar com Windows")](https://github.com/systemboys/GTi_Laboratory/raw/main/Microsoft%20Windows/Macetes/images/banner1.jpg "Macetes diversos para lidar com Windows")

- [Programas utilizados por advogados](./Advogados/README.md#gti-laboratory--programas-utilizados-por-advogados "Programas utilizados por advogados")
- [Como Ocultar uma Unidade de Disco no Windows 10: Guia Completo](#como-ocultar-uma-unidade-de-disco-no-windows-10-guia-completo "Como Ocultar uma Unidade de Disco no Windows 10: Guia Completo")

---

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#gti-laboratory--macetes-t%C3%A9cnicos "Subir para o topo")

---

## Como Ocultar uma Unidade de Disco no Windows 10: Guia Completo

Para ocultar a unidade do disco rígido local E: no Windows 10, você pode seguir os passos abaixo:

1. **Abra o Gerenciamento de Disco:**
   - Pressione `Windows + X` e selecione "Gerenciamento de Disco".

2. **Encontre a Unidade E::**
   - Na janela do Gerenciamento de Disco, localize a unidade que você deseja ocultar (unidade E:).

3. **Remover a Letra da Unidade:**
   - Clique com o botão direito na unidade E: e selecione "Alterar letra de unidade e caminho...".
   - Na janela que abrir, clique no botão "Remover".
   - Uma mensagem de aviso aparecerá. Clique em "Sim" para confirmar.

A unidade E: será ocultada do Explorador de Arquivos, mas ainda estará acessível se você souber o caminho completo ou reassociar uma letra de unidade mais tarde.

### Alternativa usando o Editor de Política de Grupo

Se você preferir usar o Editor de Política de Grupo (disponível apenas em edições Pro e Enterprise do Windows 10), siga os passos abaixo:

1. **Abrir o Editor de Política de Grupo:**
   - Pressione `Windows + R`, digite `gpedit.msc` e pressione Enter.

2. **Navegar até a Configuração de Unidade:**
   - Vá até "Configuração do Usuário" > "Modelos Administrativos" > "Componentes do Windows" > "Explorador de Arquivos".

3. **Ocultar Unidades:**
   - No painel da direita, encontre e clique duas vezes em "Ocultar essas unidades especificadas em Meu Computador".
   - Selecione "Habilitado" e, em seguida, escolha a unidade E: na lista.
   - Clique em "OK" para aplicar as configurações.

### Usando o Editor do Registro (Regedit)

Outra opção é usar o Editor do Registro:

1. **Abrir o Editor do Registro:**
   - Pressione `Windows + R`, digite `regedit` e pressione Enter.

2. **Navegar até a Chave Correta:**
   - Navegue até `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Explorer`.

3. **Criar um Novo Valor DWORD:**
   - Clique com o botão direito no painel da direita, selecione "Novo" > "Valor DWORD (32 bits)" e nomeie-o como `NoDrives`.

4. **Definir o Valor:**
   - Clique duas vezes no novo valor `NoDrives` e insira o valor correspondente para ocultar a unidade E:.
     - O valor para E: é `16` (em decimal) ou `0x10` (em hexadecimal).
   - Clique em "OK" e reinicie o computador.

Seguindo esses passos, a unidade E: será ocultada do Explorador de Arquivos, mas ainda estará disponível para o sistema operacional e aplicativos.

[(&larr;) Voltar](https://github.com/systemboys/GTi_Laboratory#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#gti-laboratory--macetes-t%C3%A9cnicos "Subir para o topo")

---
