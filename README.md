

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

---

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

---

## REST: Princípios e boas práticas

Representational State Transfer (Transferência de Estado Representacional), abreviado como REST, não é uma tecnologia, uma biblioteca, e nem tampouco uma arquitetura, mas sim um modelo a ser utilizado para se projetar arquiteturas de software distribuído, baseadas em comunicação via rede.

REST é um dos modelos de arquitetura que foi descrito por Roy Fielding, um dos principais criadores do protocolo HTTP, em sua tese de doutorado e que foi adotado como o modelo a ser utilizado na evolução da arquitetura do protocolo HTTP.

Muitos desenvolvedores perceberam que também poderiam utilizar o modelo REST para a implementação de Web Services, com o objetivo de se integrar aplicações pela Web, e passaram a utilizá-lo como uma alternativa ao SOAP.

### Identificação dos Recursos

Toda aplicação gerencia algumas informações. Uma aplicação de um E-commerce, por exemplo, gerencia seus produtos, clientes, vendas, etc. Essas **coisas** que uma aplicação gerencia são chamadas de **Recursos** no modelo REST.

Um recurso nada mais é do que uma abstração sobre um determinado tipo de informação que uma aplicação gerencia, sendo que um dos princípios do REST diz que todo recurso deve possuir uma identificação única. Essa identificação serve para que a aplicação consiga diferenciar qual dos recursos deve ser manipulado em uma determinada solicitação.

A identificação do recurso deve ser feita utilizando-se o conceito de URI (Uniform Resource Identifier), que é um dos padrões utilizados pela Web. Alguns exemplos de URI’s:

- http://servicorest.com.br/produtos
- http://servicorest.com.br/clientes
- http://servicorest.com.br/clientes/57
- http://servicorest.com.br/vendas

As URI’s são a interface de utilização dos seus serviços e funcionam como um **contrato** que será utilizado pelos clientes para acessá-los. 

### Vejamos agora os principais métodos do protocolo HTTP e o cenário de utilização de cada um deles:

| Verbo  | Descrição                                      |
| ------ | ---------------------------------------------- |
| GET    | Obter os dados de um recurso.                  |
| POST   | Criar um novo recurso.                         |
| PUT    | Substituir os dados de um determinado recurso. |
| PATCH  | Atualizar parcialmente um determinado recurso. |
| DELETE | Excluir um determinado recurso.                |

Veja a seguir o padrão de utilização dos métodos HTTP em um serviço REST, que é utilizado pela maioria das aplicações e pode ser considerado uma boa prática. Como exemplo será utilizado um recurso chamado Cliente.

| **Método** | **URI**      | **Utilização**                                |
| ---------- | ------------ | --------------------------------------------- |
| GET        | /clientes    | Recuperar os dados de todos os clientes.      |
| GET        | /clientes/id | Recuperar os dados de um determinado cliente. |
| POST       | /clientes    | Criar um novo cliente.                        |
| PUT        | /clientes/id | Atualizar os dados de um determinado cliente. |
| DELETE     | /clientes/id | Excluir um determinado cliente.               |

### Representações dos recursos

Os recursos ficam armazenados pela aplicação que os gerencia. Quando são solicitados pelas aplicações clientes, por exemplo em uma requisição do tipo GET, eles não “abandonam” o servidor, como se tivessem sido transferidos para os clientes. Na verdade, o que é transferido para a aplicação cliente é apenas uma **representação** do recurso.

Um recurso pode ser representado de diversas maneiras, utilizando-se formatos específicos, tais como JSON, XML, HTML, CSV, dentre outros, sendo o JSON (JavaScript Object Notation - Notação de Objetos JavaScript) o formato mais utilizado. 

Em JSON, os dados são apresentados desta forma:

Um **objeto** é um conjunto desordenado de pares nome/valor. Um objeto começa com `{` (chave de abertura) e termina com `}` (chave de fechamento). Cada nome é seguido por `:` (dois pontos) e os pares nome/valor são seguidos por `,` (vírgula).

![object](images/object.gif)

Uma **array** é uma coleção de valores ordenados. O array começa com `[` (conchete de abertura) e termina com `]` (conchete de fechamento). Os valores são separados por `,` (vírgula).

![array](images/array.gif)

Um valor (value, na imagem acima) pode ser uma cadeia de caracteres (string), ou um número, ou `true` ou `false`, ou `null`, ou um objeto ou uma array. Estas estruturas podem estar aninhadas.

![value](images/value.gif)

Exemplo de representação de um recurso no formato JSON.

```json
{
  "id": 1,
  "name": "Leanne Graham",
  "username": "Bret",
  "email": "Sincere@april.biz",
  "address": {
    "street": "Kulas Light",
    "suite": "Apt. 556",
    "city": "Gwenborough",
    "zipcode": "92998-3874",
    "geo": {
      "lat": "-37.3159",
      "lng": "81.1496"
    }
  },
  "phones": [
    "1-770-736-8031 x56442",
    "1-770-736-8031 x56443",
    "1-770-736-8031 x56444"
  ],
  "website": "hildegard.org",
  "company": {
    "name": "Romaguera-Crona",
    "catchPhrase": "Multi-layered client-server neural-net",
    "bs": "harness real-time e-markets"
  }
}
```
### JSON vs XML

Formato JSON:

``` json
{
	"employees": [
  	{ "firstName":"John", "lastName":"Doe" },
  	{ "firstName":"Anna", "lastName":"Smith" },
  	{ "firstName":"Peter", "lastName":"Jones" }
	]
}
```

Formato XML:
```xml
<employees>
  <employee>
    <firstName>John</firstName> <lastName>Doe</lastName>
  </employee>
  <employee>
    <firstName>Anna</firstName> <lastName>Smith</lastName>
  </employee>
  <employee>
    <firstName>Peter</firstName> <lastName>Jones</lastName>
  </employee>
</employees>
```

### REST x RESTFull

Existe uma certa confusão quanto aos termos **REST e RESTful.**Entretanto, ambos representam os mesmo princípios. A diferença é apenas gramatical. Em outras palavras, sistemas que utilizam os princípios REST são chamados de RESTful.

**REST:** conjunto de princípios de arquitetura
**RESTful:** capacidade de determinado sistema aplicar os princípios de REST.

### O que é API?

O acrônimo **API** que provém do inglês **Application Programming Interface** (Em português, significa Interface de Programação de Aplicações), trata-se de um conjunto de rotinas e padrões estabelecidos e documentados por uma aplicação A, para que outras aplicações consigam utilizar as funcionalidades desta aplicação A, sem precisar conhecer detalhes da implementação do software.

Desta forma, entendemos que as APIs permitem uma **interoperabilidade entre aplicações**. Em outras palavras, a comunicação entre aplicações e entre os usuários.

![ ](images/api.png)

> Fontes: 
> [Caelum](http://blog.caelum.com.br/rest-principios-e-boas-praticas)
> [Introdução ao JSON](https://www.json.org/json-pt.html)
> [Becode](https://becode.com.br/o-que-e-api-rest-e-restful)
> [w3schools.com](https://www.w3schools.com/js/js_json_xml.asp)

---

## Testando uma API

### Insomnia REST Client

> Debug APIs like a <u>human</u>, not a robot.
> Finally, a REST client you'll love.

### Crie requisições HTTP

Especifique a URL, payload, cabeçalhos e autorização em um só lugar. Então é só apertar enviar.

### Visualize os detalhes da resposta

Veja todos os detalhes em todas as respostas. Ver código de status, corpo, cabeçalhos, cookies e muito mais!

### Organize tudo

Crie áreas de trabalho ou pastas, arraste e solte solicitações e importe e exporte facilmente seus dados.

### Plataformas

**Livre** e **código aberto** disponível para  Mac, Windows, and Linux.

---

## APIS Online para Testes

### JSONPlaceholder

[Site do JSONPlaceholder](https://jsonplaceholder.typicode.com)

### REQ | RES

[Site dp REQ | RES](https://reqres.in/)

---

## Criando um Novo Aplicativo

Para criarmos um novo projeto de um aplicativo utilizando o Ionic framework, basta que iniciemos com uma das formas abaixo:

```sh
# Cria um novo aplicativo utilizando um template com a tela em branco.
ionic start myApp blank

# Cria um novo aplicativo utilizando um template de abas.
ionic start myApp tabs

# Cria um novo aplicativo utilizando um template de menu lateral (sidemenu).
ionic start myApp sidemenu
```

## Executando o Aplicativo

```sh
ionic serve
```
Em modo de desenvolvimento do aplicativo, utiliza-se o prórprio navegador de internet para testar a aplicação, uma vez que o próprio comando `ionic serve` abre o navegador após o término de sua execução.

## Executando no dispositivo - Android ou iOS

Para executarmos diretamente no

```sh
ionic cordova platform add android
ionic cordova platform add ios

# Após isso para executar o aplicativo direto no celular:
ionic cordova run android [--livereload]
ionic cordova run ios [--livereload]
```

## Gerando o build para Android (apk) ou iOS (ipa)

```sh
ionic cordova build android
ionic cordova build ios
```

## Gerar o Ícone e Splash Screen
The source **image for icons** should ideally be at least **1024×1024px** and located at <u>resources/icon.png</u>.

For best results, the **splash screen’s** artwork should roughly fit within a square (**1200×1200px**) at the center of the image and located at <u>resources/splash.png</u>. You can use https://code.ionicframework.com/resources/splash.psd as a template for your splash screen.

```sh
ionic cordova resources [platform]
```

## Habilitar o modo Desenvolvedor no Android
Abrir configurações -> Sobre -> Pressionar 6x sobre a versão do Android.
Ativar o modo e ligar a depuração USB.

