# [Laboratório GTi](../../README.md#laborat%C3%B3rio-gti "Laboratório GTi")

## Softwares e Utilitários para Linux

[![Pacotes Linux](./images/cardboard-boxes-apt-dpkg.jpg?raw=true "Pacotes Linux")](./images/cardboard-boxes-apt-dpkg.jpg?raw=true "Pacotes Linux")

### *Sumário*

> Internet

- [Melhorando a Velocidade de Download no Linux com Aceleradores de Download](#melhorando-a-velocidade-de-download-no-linux-com-aceleradores-de-download "Melhorando a Velocidade de Download no Linux com Aceleradores de Download")
- [Baixando com Facilidade: Utilizando o Comando wget no Linux](#baixando-com-facilidade-utilizando-o-comando-wget-no-linux "Baixando com Facilidade: Utilizando o Comando wget no Linux")
- [Instalação e Uso do `PDFTK` no Debian Linux](#instala%C3%A7%C3%A3o-e-uso-do-pdftk-no-debian-linux "Instalação e Uso do PDFTK no Debian Linux")
- [Converter imagens de um formato para outro com `ImageMagick`](# "Converter imagens de um formato para outro com ImageMagick")

---

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Melhorando a Velocidade de Download no Linux com Aceleradores de Download

Sim, existem vários aceleradores de download disponíveis para Linux que podem ajudar a melhorar a velocidade de download de arquivos da Internet. Alguns dos aceleradores de download populares para Linux incluem:

1. **Axel:** O Axel é um acelerador de download de linha de comando que suporta várias conexões simultâneas, o que pode melhorar significativamente as velocidades de download. É simples de usar e amplamente disponível nos repositórios de pacotes das distribuições Linux.

   [![Axel](./images/axel.png?raw=true "Axel")](ht./images/axel.png?raw=true "Axel")

   Para instalar o Axel, você pode usar o seguinte comando, dependendo da sua distribuição:

   ```bash
   sudo apt-get install axel  # Para distribuições Debian/Ubuntu
   sudo yum install axel      # Para distribuições CentOS/RHEL
   ```

2. **aria2:** O aria2 é uma ferramenta de download de código aberto que suporta downloads segmentados, torrent, metalink e muito mais. Ele possui uma interface de linha de comando e pode ser altamente configurável para atender às suas necessidades específicas.

   [![aria2](./images/aria2.png?raw=true "aria2")](./images/aria2.png?raw=true "aria2")

   Para instalar o aria2, você pode usar o seguinte comando:

   ```bash
   sudo apt-get install aria2  # Para distribuições Debian/Ubuntu
   sudo yum install aria2      # Para distribuições CentOS/RHEL
   ```

3. **uGet:** O uGet é um gerenciador de download de código aberto com uma interface gráfica do usuário. Ele oferece recursos avançados de gerenciamento de downloads, como agendamento, categorização e integração com navegadores.

   [![uGet](./images/uget.jpg?raw=true "uGet")](./images/uget.jpg?raw=true "uGet")

   Para instalar o uGet, você pode usar o seguinte comando:

   ```bash
   sudo apt-get install uget  # Para distribuições Debian/Ubuntu
   sudo yum install uget      # Para distribuições CentOS/RHEL
   ```

4. **KGet:** O KGet é um gerenciador de download específico para o ambiente de desktop KDE. Ele oferece uma interface gráfica intuitiva e pode ser usado em sistemas Linux que utilizam o KDE Plasma.

   [![KGet](./images/KGet.png?raw=true "KGet")](./images/KGet.png?raw=true "KGet")

   Para instalar o KGet, você pode usar o seguinte comando:

   ```bash
   sudo apt-get install kget  # Para distribuições Debian/Ubuntu
   ```

Cada uma dessas ferramentas tem suas próprias características e vantagens, então escolha a que melhor atende às suas necessidades e preferências. Todas elas podem ajudar a melhorar a velocidade de download de arquivos da Internet.

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Baixando com Facilidade: Utilizando o Comando wget no Linux

O comando `wget` é uma ferramenta de linha de comando disponível em sistemas Linux e UNIX que é usada para baixar arquivos da Internet. O nome "wget" significa "Web Get", o que descreve bem a função da ferramenta: ela permite que você obtenha arquivos e conteúdo diretamente da web para o seu sistema local. Aqui estão algumas das principais características e usos do comando `wget`:

1. **Download de Arquivos:** O uso mais comum do `wget` é para baixar arquivos da Internet. Você pode especificar a URL do arquivo que deseja baixar como argumento para o comando. Por exemplo:

   ```bash
   wget https://example.com/arquivo.zip
   ```

   Isso baixará o arquivo "arquivo.zip" do site "example.com" para o diretório atual.

2. **Download Recursivo:** O `wget` permite realizar downloads recursivos, o que significa que você pode baixar todo um site ou diretório da web, incluindo seus subdiretórios e arquivos. Para isso, você pode usar a opção `-r` ou `--recursive`. Por exemplo:

   ```bash
   wget -r https://example.com/diretorio/
   ```

   Isso baixará todo o conteúdo do diretório "diretorio" e seus subdiretórios.

3. **Retomar Downloads:** O `wget` é capaz de retomar downloads interrompidos. Se você estiver baixando um arquivo grande e a conexão for interrompida, pode usar o `wget` para continuar o download de onde parou. Basta usar a opção `-c` ou `--continue`. Por exemplo:

   ```bash
   wget -c https://example.com/arquivo-grande.zip
   ```

4. **Limitar Largura de Banda:** Você pode limitar a largura de banda usada pelo `wget` para não sobrecarregar sua conexão. Isso pode ser útil ao baixar grandes arquivos. Use a opção `--limit-rate` seguida pela taxa desejada em bytes por segundo.

   ```bash
   wget --limit-rate=100k https://example.com/arquivo-grande.zip
   ```

5. **Autenticação:** O `wget` permite que você forneça credenciais de autenticação para acessar recursos protegidos por senha na web. Use a opção `--user` para especificar o nome de usuário e `--password` para especificar a senha.

   ```bash
   wget --user=seu_nome_de_usuario --password=sua_senha https://example.com/recursos-restritos
   ```

6. **Conversão de Links Relativos:** Quando você baixa um site inteiro, o `wget` pode converter os links relativos para que funcionem localmente. Use a opção `--convert-links` para ativar essa funcionalidade.

   ```bash
   wget --recursive --convert-links https://example.com/site-com-links-relativos
   ```

7. **Espelhamento de Sites:** O `wget` pode ser usado para criar espelhos de sites inteiros, o que é útil para fazer backup de sites ou criar cópias locais de conteúdo da web.

[![WGet](./images/comando-wget-linux.png?raw=true "WGet")](./images/comando-wget-linux.png?raw=true "WGet")

O `wget` é uma ferramenta poderosa e versátil para gerenciar downloads de arquivos e recursos da web em sistemas Linux e UNIX. É amplamente utilizado por administradores de sistemas e usuários avançados para diversas tarefas relacionadas à web. Certifique-se de usar com responsabilidade e respeitar os direitos autorais e os termos de uso ao baixar conteúdo da Internet.

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Instalação e Uso do PDFTK no Debian Linux

O **PDFTK (PDF Toolkit)** é uma ferramenta de linha de comando eficiente para manipular arquivos PDF, como unificação, separação e rotacionamento de páginas.

### 🛠️ Instalação via Terminal (Debian/Ubuntu)

```bash
sudo apt update
sudo apt install pdftk
```

> 💡 Em versões mais recentes do Debian/Ubuntu, o pacote pode ser `pdftk-java`, que oferece a mesma funcionalidade:

```bash
sudo apt install pdftk-java
```

Verifique a instalação com:

```bash
pdftk --version
```

### 📄 Exemplo Genérico: Unificar Vários PDFs

Para unir todos os arquivos `.pdf` de um diretório em um único PDF de saída:

```bash
pdftk diretorio/*.pdf cat output diretorio/arquivos_unificados.pdf
```

> 🔄 Substitua `diretorio/` pelo caminho do seu diretório de arquivos PDF.
>  O resultado será salvo como `arquivos_unificados.pdf` no mesmo local.

### ✅ Dicas Extras

- Para unir arquivos em ordem específica:

  ```bash
  pdftk A=arquivo1.pdf B=arquivo2.pdf C=arquivo3.pdf cat A B C output unificado.pdf
  ```

- Para dividir um PDF em páginas individuais:

  ```bash
  pdftk entrada.pdf burst
  ```

- Para extrair páginas específicas:

  ```bash
  pdftk entrada.pdf cat 1-3 5 7-10 output extraido.pdf
  ```

Aqui vai um exemplo de **uso inline do `pdftk`** com os arquivos listados um por linha e o comando completo ao final:

```bash
pdftk \
"Diretorio A/receitas de bolo.pdf" \
"Diretorio B/Outras receitas.pdf" \
"Diretorio C/Sobremesas.pdf" \
cat output "Unificados/receitas_completas.pdf"
```

> 🔹 O caractere `\` no final de cada linha serve para quebrar o comando sem executá-lo, mantendo tudo como um único comando no terminal.
> 🔹 Os caminhos com espaços devem estar **entre aspas**.

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Converter imagens de um formato para outro com ImageMagick

Existe uma ferramenta excelente (e a mais usada) via terminal no Linux para **converter imagens** de um formato para outro, inclusive **para JPG**. O nome dela é **ImageMagick**.

### Como instalar o ImageMagick
Na maioria das distribuições baseadas em Debian/Ubuntu (como Ubuntu, Linux Mint, Pop!_OS etc.), rode:

```bash
sudo apt update
sudo apt install imagemagick
```

Se estiver usando Fedora, Arch ou outra distro, o comando muda um pouco (ex: `sudo dnf install ImageMagick` ou `sudo pacman -S imagemagick`).

### Converter uma única imagem para JPG
```bash
convert imagem.png imagem.jpg
```

Ou, se quiser controlar a qualidade (quanto menor o número, menor o arquivo, mas pior a qualidade):

```bash
convert imagem.png -quality 90 imagem.jpg   # 90 é uma boa qualidade
```

### Converter várias imagens de uma vez (batch)
Entre na pasta onde estão as imagens e use o `mogrify` (é o jeito mais prático para conversão em lote):

```bash
# Converte todos os PNG para JPG (mantém os originais)
mogrify -format jpg *.png

# Converte todos os WEBP para JPG
mogrify -format jpg *.webp

# Converte PNG, GIF, TIFF etc. de uma vez
mogrify -format jpg *.png *.gif *.tif
```

**Dica importante**: O `mogrify -format jpg` **cria** os arquivos .jpg e **deixa** os originais intactos.  
Se quiser **apagar** os originais depois (para economizar espaço), faça:

```bash
mogrify -format jpg *.png && rm *.png
```

### Outras opções úteis
- Converter e colocar em uma pasta diferente:
  ```bash
  mkdir jpgs
  mogrify -format jpg -path jpgs *.png
  ```

- Converter com qualidade específica:
  ```bash
  mogrify -format jpg -quality 85 *.png
  ```

### Alternativas via terminal
- **ffmpeg** (ótimo também, especialmente se você já usa para vídeo):
  ```bash
  ffmpeg -i imagem.png -q:v 2 imagem.jpg
  ```
  Para batch:
  ```bash
  for f in *.png; do ffmpeg -i "$f" "${f%.png}.jpg"; done
  ```

- **GraphicsMagick** (mais leve em alguns casos): similar ao ImageMagick, comando `gm convert`.

O **ImageMagick** é de longe a solução mais completa e recomendada para o que você quer fazer.

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---