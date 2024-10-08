# [Laboratório GTi](../../README.md#laborat%C3%B3rio-gti "Laboratório GTi")

## Softwares para terminais

[![Terminal Linux](./images/terminai_linux.jpg?raw=true "Terminal Linux")](./images/terminai_linux.jpg?raw=true "Terminal Linux")

### *Sumário*

- [Executando Mapas ASCII no Terminal com MapSCII](#executando-mapas-ascii-no-terminal-com-mapscii "Executando Mapas ASCII no Terminal com MapSCII")

---

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---

## Executando Mapas ASCII no Terminal com MapSCII

O MapSCII é uma ferramenta interessante que permite visualizar mapas no estilo ASCII direto no terminal. Para executá-lo a partir do GitHub, siga estas etapas:

1. Abra um terminal. Você pode fazer isso pressionando `Ctrl` + `Alt` + `T` ao mesmo tempo.

2. Certifique-se de ter o Node.js instalado em seu sistema. Você pode verificar isso digitando:

```bash
node -v
```

Se o Node.js não estiver instalado, você precisará instalá-lo. No Debian ou no Linux Mint, você pode fazer isso com o seguinte comando:

```bash
sudo apt install nodejs
```

3. Clone o repositório do MapSCII do GitHub:

```bash
git clone https://github.com/rastapasta/mapscii.git
```

4. Entre no diretório que foi criado após o clone:

```bash
cd mapscii
```

5. Instale as dependências do Node.js:

```bash
npm install
```

6. Após a instalação das dependências, execute o MapSCII:

```bash
npm start
```

Isso iniciará o MapSCII e você verá o mapa ASCII no terminal. Você pode navegar pelo mapa usando as teclas de seta e as teclas "W", "A", "S" e "D". Para sair do MapSCII, pressione `Ctrl` + `C`.

[![MapSCII](./images/mapscii.png?raw=true "MapSCII")](./images/mapscii.png?raw=true "MapSCII")

Lembre-se de que essa é uma ferramenta experimental e de entretenimento. A qualidade do mapa ASCII pode variar, dependendo da área que você está visualizando. Divirta-se explorando!

[(&larr;) Voltar](../../README.md#laborat%C3%B3rio-gti "Voltar ao Sumário") | 
[(&uarr;) Subir](#sum%C3%A1rio "Subir para o topo")

---