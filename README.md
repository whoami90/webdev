## Desenvolvimetno web com html5, css3, Javascript e PHP. 

### HTML

### CSS

### Javascript

### PHP: linguagem de programação server side

Uma das principais funções da linguagens de programação server side é permitir o acesso a informações armazenadas em banco de dados.Uma vez que apenas utilizando html, e javascript não é possível, é necessário a utilização de uma linguagem do lado servidor. As linguagens disponíveis para este fim são:

* Java
* Python
* ASP
* .NET
* PHP

PHP (Hypertext preprocessor) é uma linguagem baseada em script, open source e destinada sobretudo ao desenvolvimento web. Originalmente uma linguagem estruturada, que posteriormente adotou o paradigma de orientação a objetos. 

**Como o PHP funciona?**

É uma linguagem interpretada, ou seja, precisa 'rodar' sobre um servidor web. Todo o código gerado é interpretado pelo servidor, convertido em html e então exibido no navegador. 

    1. O código PHP gerado é interpretado pelo servidor.
    2. Esse código é convertido em formato html. 
    3. O código é exibido no navegador. 

Logo, o código fonte não pode ser visto no lado cliente, mas apenas o html gerado. 

Outra característica importante é poder ser utilizado na maior parte dos sistemas operacionais, assim como em vários servidores web diferentes, como apache, IIS e o Nginx, entre outros. 

### Anatomia de um script PHP

É composto por código delimitado pelas tags <?php e?>. A última, de fechamento, não é obrigatória. Devido a sua simplicidade, mesmo um script PHP pode conter tanto código estruturado como orientado a objetos. Pode até conter código de marcação html. Neste último caso, o código próprio do PHP deverá ficar entre as tags de abertura e fechamento. A imagem a seguir mostra dois exemplos de código, um apenas em PHP e outro mesclado com HTML. Ao analisarmos os códigos, inicialmente é importante notar que ambos possuem a extensão “.php”. Outras extensões possíveis, mas atualmente em desuso, são “.php3”, “.php4”, “.phtml”.

*php_html.php*
~~~~~
<!DOCTYPE html>
<html>
    <head>
        <title>Código PHP mesclado com código html</title>
    </head>

    <body>
        <p>
            <?php echo "Este é um texto de parágrafo escrito utilizando PHP"; ?>
        </p>

    </body>
</html>
~~~~~

*exemplo1.php*
~~~~~
<?php

$nome = $_POST['nome'];
$email = $_POST['email'];

echo "Os dados Recebidos no formulário HTML foram: ";
echo "<br/>";
echo "Nome: "   .$nome;
echo "<br/>"
echo "Email: "  .$email;
>
~~~~~
No primeiro código da imagem, temos as tags de um arquivo HTML comum, com exceção do código inserido dentro das tags <?php e ?>. Aqui temos a função “echo”, que serve para imprimir algo na tela, associado a uma frase. Quando visualizado no navegador, o código será renderizado como HTML normal. Caso exibamos a fonte, só será possível ver as tags HTML e o conteúdo, sem o código PHP em questão.

Na segunda parte da imagem, temos um exemplo de código em que são definidas duas variáveis, $nome e $email, que recebem dois valores enviados de um formulário HTML, por meio do método POST. Daí a utilização do array superglobal $_POST — cujos índices ‘nome’ e ‘email’ correspondem ao atributo ‘name’ dos campos input do formulário. A seguir, é utilizada a função “echo” para a impressão de uma frase e do conteúdo das variáveis recebidas. Repare ainda na utilização, mais uma vez, de uma tag html, a <br/>, em meio ao código PHP.

### Sintaxe

A seguir um resumo sobre a sintaxe do PHP:

*Variáveis*

No PHP, as variáveis são criadas com a utilização do simbolo de cifrão ($). Alem disso, o PHP é case sensitive, ou seja, sensível a letras maiúsculas e minúsculas.

*Tipos de dados*

O PHP é uma linguagem fracamente tipada. Logo, embora possua suporte para isto, não é necessário definir o tipo de uma variável em sua declaração. Os tipos de dados disponíveis em PHP são: booleanos, inteiros, números de ponto flutuante, strings, arrays, interáveis (iterables), objetos, recursos, NULL e call-backs.

*Operadores condicionais*

No PHP, há suporte às condicionais if, else, if e else ternários, if else e switch.

*Laços de repetição*

No PHP estão disponíveis os laços for, foreach, while e do-while.

*Funções e métodos*

O código PHP possui uma grande quantidade de funções e métodos nativos.

### Inclusão de scripts dentro de scripts

O PHP permite a inclusão de um script dentro de outro script. Isso é muito útil, sobretudo se pensarmos no paradigma de orientação a objetos, em que temos, em um programa, diversas classes, codificadas em diferentes scripts. Logo, sempre que precisarmos fazer uso de uma dessas classes, de seus métodos ou atributos, basta incluí-la no script desejado. Para incluir um script em outro, o PHP disponibiliza algumas funções:

* Include
* Require
* Include once
* Require_once

### Acesso ao sistema de arquivos

Por meio do PHP é possível ter acesso ao sistema de arquivos do servidor web. Com isso, pode-se por exemplo, manipular arquivos e diretórios, desde simples listagens a inclusão ou exclusão de dados. 

### Páginas dinâmicas e acesso a dados

#### Páginas dinâmicas

Se fôssemos implementar em uma página web tudo o que estudamos até aqui, teríamos uma página HTML básica, com um pouco de interação no próprio navegador, graças ao JavaScript, e também com um pouco de estilo, este devido ao CSS. Além disso, já sabemos que é possível enviar dados do HTML para o PHP mediante um formulário. Para prosseguirmos, é importante definirmos o que são páginas dinâmicas. A melhor forma de fazer isso, porém, é definindo o que seria o seu antônimo, ou seja, as páginas estáticas.

> HTML + JavaScript + CSS, sem conexão com uma linguagem de programação, formam o que podemos chamar de páginas estáticas. Embora seja até possível termos um site inteiro composto por páginas estáticas, isso seria muito trabalhoso e também nada usual.

**Exemplo**
Imagine um site que tenha, por exemplo, dez páginas. Agora imagine que esse site tenha a mesma estrutura visual, o mesmo cabeçalho, menu, rodapé e outros pontos em comum. Pense em um blog, por exemplo, onde o que muda são os conteúdos dos posts. No site estático, teríamos que escrever dez diferentes arquivos HTML, modificando o conteúdo em cada um deles, diretamente nas tags HTML, e só conseguiríamos reaproveitar os estilos e a interatividade de navegador utilizando CSS e JavaScript externos. Entretanto, todo o conteúdo precisaria ser digitado e muito código HTML repetido. Todo esse trabalho nos ajuda a entender o que são páginas estáticas.

> A combinação das tecnologias do lado cliente com as tecnologias do lado servidor produzem as páginas dinâmicas.

Nelas, é possível receber as informações provenientes do cliente, processá-las, guardá-las, recuperá-las e utilizá-las sempre que desejarmos. E não é só isso: podemos guardar todo o conteúdo do nosso blog no banco de dados. Com isso, teríamos apenas uma página PHP que recuperaria nosso conteúdo no banco e o exibiria no navegador. A tabela a seguir apresenta um pequeno resumo comparativo entre as páginas estáticas e dinâmicas.

***
**Inclusão/Alteração/Exclusão de conteúdo**

* Páginas estáticas

    * Manualmente, direto no código HTML

* Páginas dinâmicas

    * Automaticamente através de scripts no lado servidor, como PHP.
***
**Armazenamento de conteúdo**

* Páginas estáticas

    * Na própria página HTML

* Páginas dinâmicas

     * Em um banco de dados

***

*Outra importante característica de um site dinâmico é possibilitar a utilização de ferramentas de gestão de conteúdo (CMS) para manter as informações do site sempre atualizadas. Com isso, depois de pronto, não será mais necessário mexer nos códigos-fonte, basta acessar a ferramenta e gerenciar o conteúdo por meio dela. Já no site estático, será preciso modificar diretamente o código HTML, tornando necessário alguém com conhecimento técnico para isso.*


### Acesso a dados

Como mencionado anteriormente, o ambiente web é composto por tecnologias que rodam do lado cliente e do lado servidor. Complementando o que vimos até aqui, temos ainda, do lado servidor, o banco de dados. De forma resumida, podemos defini-lo como um repositório em que diversas informações podem ser armazenadas e posteriormente recuperadas.

Para realizar a gestão desses dados, existem os SGBD, ou sistemas gerenciadores de bancos de dados. Se, por um lado, o SGBD é responsável por montar a estrutura do banco de dados — entre outras funções —, por outro lado, para recuperarmos uma informação guardada em um banco de dados e exibi-la em uma página web, é necessário utilizar uma linguagem do lado servidor, como o PHP. Em outras palavras, não é possível acessar o banco de dados utilizando apenas HTML ou mesmo JavaScript. Sempre será necessária a utilização de uma linguagem server side para o acesso aos dados.

**SGBD**: Há diversos tipos de SGBD para as mais variadas necessidades, com opções gratuitas ou pagas. Entre os gratuitos, dois são comumente utilizados em conjunto com o PHP: MySQL e PosgreSQL.

### Formas de acesso a dados

* Apartir do HTML

    * Uma das maneiras mais comuns de enviar e recuperar dados a partir do HTML é fazendo uso de formulários. Com eles, é possível submetermos nossos dados para uma linguagem no lado servidor/PHP. Este, então, recebe as informações e as armazena no banco de dados. Da mesma forma acontece o caminho inverso. Podemos ter um formulário em nossa página HTML que solicite dados ao PHP e este as envie de volta, após recuperá-las do banco de dados.

    *Vale lembrar ainda o que vimos sobre o PHP: ele permite a utilização de códigos HTML diretamente em seus scripts. Logo, uma página web feita em PHP pode recuperar dados do banco de dados toda vez que é carregada. É isso o que acontece na maioria dos sites. Cada página visualizada é composta por conteúdo armazenado em banco de dados e código HTML produzidos por uma linguagem do lado servidor. Com isso, cada página que abrimos em sites dinâmicos implica em uma chamada/requisição ao lado servidor — script e banco de dados.

* Apartir do Javascript

    * O JavaScript possui, essencialmente, duas formas para se comunicar com linguagens do lado servidor: por meio das APIs (Application Programming Interface) XMLHttpRequest e Fetch API. A primeira é amplamente utilizada, sendo a forma mais comum de realizar essa comunicação. É normalmente associada a uma técnica de desenvolvimento web chamada AJAX. Já a segunda é mais recente e oferece algumas melhorias, embora não seja suportada por todos os navegadores.

    *A comunicação em ambas consiste em, mediante algum evento no navegador, normalmente originado em uma ação disparada pelo usuário, é enviada uma requisição ao lado servidor, como recuperar algum dado, por exemplo, tratar o seu retorno e o exibir na tela. Isso tudo sem que seja necessário recarregar toda a página.

***

# Linguagem de marcação de hipertexto HTML

*O objetivo principal de uma linguagem de marcação de hypertexto, e mais especificamente da HTML – que será usada como linguagem padrão e alvo de nosso estudo –, é o de estruturar o conteúdo de um documento. Este conteúdo pode ser composto de textos, figuras, tabelas etc*

*Estrutura, por sua vez, pode ser definida como a organização dos elementos de conteúdo. Para realizar essa função, a HTML faz uso de um sistema hierárquico de elementos chamados de tags.*

**Estrutura da linguagem HTML**

* Tags textuais 
* Tabelas e Listas
* Formulários
* Tags semânticas
* Links
* Estrutura (representada por DOM - Document Object Model)

### Estrutura
~~~~~
<! doctype html>
<html lang = "pt">
            Raiz
<head>

        Cabeçalho

</head>

<body>

        CORPO

</body>

</html>
~~~~~

~~~~~
document >

            <html>

                    <head>

                        <title>

                            text: my title

                    <body>

                            <h1>

                                text: A heading 

                            <a>        href 

                                text: link text           
~~~~~

root element - html

element - head, title, body, h1 a h6, a 

attribute - href

***

### Tags textuais

div

p 

a 

img

h1 a h6

***
### Tags de formatação  
*hoje em dia não é muito usado, no lugar é usado o css.*

strong

mark

abbr

del

em

sub

sub

### Tags semânticas
*usados em sistemas de busca*

header 

main

section

nav

article

footer

aside

***
### Tabelas e listas

*Ver documentos de exemplos em tabelas e listas*
***

# Linguagem de marcação de hypertexto - HTML

O objetivo principal de uma linguagem de marcação de hypertexto, e mais especificamente da html, é o de estruturar o conteúdo de um documento. Este conteúdo pode ser composto de textos, figuras, tabelas etc. 

Estrutura, que pode ser definida como a organização dos elementos de conteudo. Para realziar essa função, a HTML faz uso de um sistema hierárquico de elementos chamados de tags. 

## Estrutura de uma página HTML

O Doctype não é uma tag HTML, mas sim uma instrução. É uma declaração que serve para informar ao navegador qual a versão da HTML usada em um arquivo HTML.

**Ver exemplos na pasta document type definition**

****
### Estrutura de uma página web

**Elementos obrigatórios**

~~~~
<!DOCTYPE html>   
<html>              
    <head>          

    </head>
    <body>          
        
    </body>
</html>
~~~~
**!DOCTYPE - declaração do DOCTYPE**

**html - raiz do documento**

    *   Dentro do da tag raiz fica o atributo lang:
           
            <html lang="en-US"> - english United States
            <html lang="en-GB"> - english gram Brittany
            <html lang="pt-br"> - portugues Brasil

**head - cabeçalho**

    *   Dentro da tag head:

        <title> - título, visualizada na barra de titulo do navegador.
        <meta> - engloba série de informações, descrição de página, palavras chaves e etc
        <script> - responsável pela inclusão e/ou definição de scripts relacionados ao documento
        <link> - responsável pela inclusão de folhas de estilo (externas) relacionadas ao documento. Possibilita também a inclusão de favicons (pequenos itens que aparecem na barra de endereços do navegador.)
        <style> Assim como o anterior, é responsável pelo vinculo de folhas de estilo ao documento - quando elas são declaradas diretamente no documento. 

**body - corpo**

    * Responsável pela estruturação do documento, sobretudo de seu conteúdo e também apresentação, embora seja recomendado que a apresentação do documento, seja feito por meio de folhas de estilo (CSS). 

****
**Exemplos**
*Pasta exemplo 6, simple*


### Tipos e composição das tags

As tags podem ser divididas em tipos, de acordo com as suas funções: Estruturais, textuais e semânticas. Outra característica importante é que elas também podem ter atributos. A seguir, falaremos sobre cada um desses temas.

**Os atributos**

Os atributos servem para que algumas características sejam adicionadas a um elemento, a uma tag. São compostos por um nome e por um valor.

~~~~
<img src="imagem.jpg" alt="minha imagem"/>
~~~~
Esta tag é utilizada para a inserção de imagens no documento. Temos dois exemplos de atributos em sua declaração: src e alt, que são nomes de atributo; e “imagem.jpg” e “minha imagem” são seus valores, respectivamente.

O atributo “src” define o endereço e o nome da imagem. Já o atributo “alt” define um texto alternativo a ser exibido no navegador caso a imagem não seja carregada.

Há uma enorme variedade de atributos, assim como de relacionamentos entre eles e as tags. Ao longo dos próximos módulos, veremos alguns dos principais, lembrando que o site do W3C contém a lista completa de atributos e combinações. Por ora, cabe ainda destacar dois atributos de extrema importância no desenvolvimento Web:

**ID**

Utilizado para definir um identificador, que deve ser único, para uma tag em um documento.



**CLASS**

Usado para definir uma classe à qual uma ou mais tags pertencem. Com base nesses dois tipos de identificação, é possível, por exemplo, fazer referência a um ou mais atributos para inserirmos estilização visual nas páginas, através de Folhas de Estilo ou eventos e interação, através de Javascript.

Tipos de tags: **textuais e semânticas**

Até aqui, conhecemos algumas tags associadas à estrutura, dita obrigatória, de uma página. Também vimos que, na maioria dos casos, as páginas Web possuem uma mesma estrutura em termos de conteúdo. A seguir, conheceremos os tipos de tag textuais e semânticos.

**Tags textuais**

São responsáveis por **organizar o conteúdo da página**, ou seja, textos, mídias e links, por exemplo. Algumas das principais tags textuais, inclusive vistas anteriormente, são: <p>, <h1> ... <h6>, <img> e <a>. Essas tags e suas funções serão descritas a seguir.

**Tags semânticas**

A partir da HTML5 foram inseridas tags com a função semântica de **organizar a estrutura de conteúdo de uma página**. Logo, voltando ao exemplo de seções básicas de uma página, nossa página ficaria assim:

**Exemplo**
*pasta exemplo 6, simple2*

Ao analisar a figura, é possível perceber que existem tags específicas para cada seção do conteúdo. Essa é uma característica importante da HTML, chamada de semântica.

Logo, semântica, neste contexto, pode ser considerada a correta utilização de uma tag HTML de acordo com o seu conteúdo ou finalidade.

Isso cria uma organização no documento que facilita tanto para você, que o escreveu, quanto para outras pessoas que venham a editar o mesmo documento. Além disso, muitos dispositivos fazem uso dessa marcação para uma correta interpretação do conteúdo ali contido.

Veja outras tags e suas respectivas funções:

<article> - Inclui um bloco  de conteúdo que deve ser usado quando se deseja inserir um artigo, como um post de um blog, por exemplo.

<section> - Define uma seção no documento. É normalmente utilizado para agrupar seções. Por exemplo: uma <section> pode agrupar várias   <article>

<h1> a <h6>  - Usados para determinar o tamanho do caractere, h1 é para títulos e quanto maior o numero, menor o caractere.

<p> - inserir parágrafos no texto

<pre> - inserir texto pré formatado.

<div> - embora não seja considerada semântica, pode ser usada para agrupar algum tipo de conteúdo que não tenha nenhuma semântica específica ou que não se encaixa bem dentro de uma tag semântica. 

<span> - É semelhante à <div>. Entretanto, enquanto a <div> é um elemento não semântico no bloco (quando usada, quebra o conteúdo em uma seção), a <span> é embutida (não quebra o conteúdo, apenas o agrupa).

<a> - usada para inserir links

<br /> - Usada para inserir quebra de linha. 

<hr> - Insere uma linha horizontal no documento. Normalmente é utilizada quando se pretende alterar a temática de um texto.

