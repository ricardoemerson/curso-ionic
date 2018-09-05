# Criando Aplicações Móveis com Ionic

## Instalar Node.js

Acessar o site  [node.js](https://nodejs.org) e solicitar o download do Node.js utilizando o primeiro botão de download que possui a versão recomendada para a maioria dos usuários (LTS).

Após o download e instalação, o Node.js estará instalado no seu sistema operacional e o NPM (Node Package Manager - Gerenciador de Pacotes do Node.js) estará disponível para instalação dos mais variados tipos de pacotes.

Os pacotes adicionados podem ter visibilidade global, ou seja, podem ser utilizados em qualquer projeto ou podem ter a visibilidade a nível de projeto, estando disponível apenas na pasta do projeto em que foi instalado.

Para instalação de pacotes **globais** temos as seguintes opções:

```sh
# Instalando um pacote pra ser utilizado globalmente no sistema operacional:
npm install -g yarn
npm i -g json-server http-server
```

## Atualizando o NPM

```sh
# Atualizar para a última versão do npm:
npm i -g npm to update
```

## Instalando o Ionic

Para criarmos aplicativos móveis utilizando o Ionic, devemos realizar a instalação do mesmo, juntamento com o Apache Cordova, para que possamos utilizar o recurso do Ionic Native é um wrapper TypeScript para plugins Cordova / PhoneGap que facilitam a adição de qualquer funcionalidade nativa que você precisa ao seu aplicativo móvel.

```sh
npm install -g ionic cordova
```

## Instalando o Visual Studio Code

Para edição do código fonte do aplicativo será utilizado o editor de textos [**Visual Studio Code**](https://code.visualstudio.com/). O **VSCODE** como também é conhecido tem se tornado muito popular entre os desenvolvedores e tem conquistado muitos adeptos.

![ ](images/vscode.jpg)

> O **Visual Studio Code** é um [editor de](https://pt.wikipedia.org/wiki/Editor_de_texto) [código-fonte](https://pt.wikipedia.org/wiki/C%C3%B3digo-fonte) desenvolvido pela [Microsoft](https://pt.wikipedia.org/wiki/Microsoft) para [Windows](https://pt.wikipedia.org/wiki/Windows), [Linux](https://pt.wikipedia.org/wiki/Linux) e [macOS](https://pt.wikipedia.org/wiki/MacOS). Ele inclui suporte para [depuração](https://pt.wikipedia.org/wiki/Depura%C3%A7%C3%A3o), controle [Git](https://pt.wikipedia.org/wiki/Git) incorporado, [realce de sintaxe](https://pt.wikipedia.org/wiki/Realce_de_sintaxe), complementação inteligente de código, *snippets* e [refatoração de código](https://pt.wikipedia.org/wiki/Refatora%C3%A7%C3%A3o). 
>
> O Visual Studio Code pode ser estendido através de [plugins](https://pt.wikipedia.org/wiki/Plug-in), disponíveis através de um repositório central. Isso inclui adições ao editor e suporte para linguagens de programação.
>
> Fonte: [Wikipedia](https://pt.wikipedia.org/wiki/Visual_Studio_Code)

### Extenções Úteis para o Desenvolvimento de Código com Ionic/Angular

- All Autocomplete
- Angular 2, 4 and upcoming latest Typescript HTML ES6 fequently used snippets
- Angular 6 Snippets - TypeScript, Html, Angular Material, ngRx, RxJS & Flex Layout
- Angular Language Service
- Angular v6 Snippets
- Auto Import
- Auto Rename Tag
- Bracket Pair Colorizer
- Close All
- Color Highlight
- Copy Relative Path
- Indenticator
- Ionic 3 ionView Snippets
- Ionic 3 snippets
- JavaScript (ES6) code snippets
- json2ts
- Multiple cursor case preserve
- Text Manipulator
- Trailing Spaces
- TSLint
- TypeScript Hero
- vscode-icons

### Principais configurações:

```js
{
   "editor.fontFamily": "Menlo, Monaco, 'Courier New', monospace",
    "editor.fontSize": 17,
    "window.zoomLevel": 0,
    "editor.tabSize": 2,
    "editor.formatOnType": true,
    "workbench.iconTheme": "vscode-icons",
    "workbench.colorCustomizations": {
      "tab.activeBackground": "#01579b",
      "editor.lineHighlightBackground": "#38393A",
      "editorGutter.background": "#2A2A2B",
    },
    "vsicons.projectDetection.autoReload": true,
    "editor.snippetSuggestions": "top",
    "emmet.showSuggestionsAsSnippets": true,
    "editor.wordWrap": "on",
    "files.insertFinalNewline": true,
    "editor.renderLineHighlight": "all",

    "terminal.integrated.fontFamily": "Menlo, Monaco, 'Courier New', monospace",
    "terminal.integrated.fontSize": 16,
    "typescript.check.tscVersion": false,
    "editor.minimap.enabled": true,
    "extensions.autoUpdate": true,
    "editor.renderIndentGuides":	true,
    "editor.dragAndDrop":	true,
    "search.smartCase": true
}
```