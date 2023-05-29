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

São responsáveis por **organizar o conteúdo da página**, ou seja, textos, mídias e links, por exemplo. Algumas das principais tags textuais, inclusive vistas anteriormente, são: 
~~~~
<p>, <h1> ... <h6>, <img> e <a>. Essas tags e suas funções serão descritas a seguir.
~~~~

**Tags semânticas**

A partir da HTML5 foram inseridas tags com a função semântica de **organizar a estrutura de conteúdo de uma página**. Logo, voltando ao exemplo de seções básicas de uma página, nossa página ficaria assim:

**Exemplo**
*pasta exemplo 6, simple2*

Ao analisar a figura, é possível perceber que existem tags específicas para cada seção do conteúdo. Essa é uma característica importante da HTML, chamada de semântica.

Logo, semântica, neste contexto, pode ser considerada a correta utilização de uma tag HTML de acordo com o seu conteúdo ou finalidade.

Isso cria uma organização no documento que facilita tanto para você, que o escreveu, quanto para outras pessoas que venham a editar o mesmo documento. Além disso, muitos dispositivos fazem uso dessa marcação para uma correta interpretação do conteúdo ali contido.

Veja outras tags e suas respectivas funções:
~~~~
<article> - Inclui um bloco  de conteúdo que deve ser usado quando se deseja inserir um artigo, como um post de um blog, por exemplo.
~~~~
~~~~
<section> - Define uma seção no documento. É normalmente utilizado para agrupar seções. Por exemplo: uma <section> pode agrupar várias   <article>
~~~~
~~~~
<h1> a <h6>  - Usados para determinar o tamanho do caractere, h1 é para títulos e quanto maior o numero, menor o caractere.
~~~~
~~~~
<p> - inserir parágrafos no texto
~~~~
~~~~
<pre> - inserir texto pré formatado.
~~~~
~~~~
<div> - embora não seja considerada semântica, pode ser usada para agrupar algum tipo de conteúdo que não tenha nenhuma semântica específica ou que não se encaixa bem dentro de uma tag semântica. 
~~~~
~~~~
<span> - É semelhante à <div>. Entretanto, enquanto a <div> é um elemento não semântico no bloco (quando usada, quebra o conteúdo em uma seção), a <span> é embutida (não quebra o conteúdo, apenas o agrupa).
~~~~
~~~~
<a> - usada para inserir links
~~~~
~~~~
<br /> - Usada para inserir quebra de linha. 
~~~~
~~~~
<hr> - Insere uma linha horizontal no documento. Normalmente é utilizada quando se pretende alterar a temática de um texto.
~~~~
### Tipos de tags: textuais e semânticas

*vide pasta tags textuais e semanticas*

*vide pasta vamos praticar 1*

###Tags de formatação

A última versão HTML ainda dá suporte a algumas tags direcionadas à formatação visual de conteúdo. Embora possam ser substituídas por CSS, quatro delas merecem atenção especial:

~~~~
<b>: aplica o efeito de negrito em um texto;
<strong>: aplica o efeito de negrito em um texto e o marca como importante;
<i>: aplica o efeito de itálico em um texto;
<em>: aplica o efeito de itálico e dá ênfase a um texto.
~~~~

**O destaque que tais elementos merecem diz respeito à função semântica que as tags < strong > e < em > exercem.**

É interessante notar que as duas produzem o mesmo efeito visual (que <b> e <i> respectivamente) em um texto, ou seja, marcá-lo como negrito e/ou itálico. Entretanto, há uma diferença importante entre elas, que vai além da visualização do texto no navegador pela maioria dos usuários. A função semântica de ambas é perceptível em dispositivos de leitura de tela, que transformam o texto em áudio, e normalmente são utilizados por pessoas com deficiência visual.

**Tags obsoletas**

A cada nova versão da HTML, novas tags são criadas, assim como antigas são descontinuadas. Estas, chamadas de obsoletas, embora ainda possam ter suporte em boa parte dos navegadores, devem ser evitadas pelo seguinte motivo:

*   Em primeiro lugar, porque provavelmente foram substituídas por novas tags, com melhor semântica.
*   Em segundo lugar, pelo risco de desconfigurarem o conteúdo da página, uma vez que os browsers podem deixar de suportá-las a qualquer momento.

| Tag | Função|
|-----|-------|
|< applet > | Identifica a inclusão de um applet Java |
|< center > | Centraliza horizontalmente o conteúdo de um bloco |
|< dir > | Container para lista de diretórios ou arquivos. |
|< font > | Determina características relacionadas a fontes de um determinado elemento |
|< image> | Ancestral da tag < img >, era usado nas primeiras versões HTML para inserção de imagens |

Atualmente consideradas obsoletas, as tags <center> e <font> ainda são usadas em muitas páginas HTML. Ambas se enquadram no conceito de que não é função da HTML cuidar da apresentação. Logo, as duas foram substituídas por propriedades CSS.

**Exemplo prático de comparação das tags obsoletas:**
*vide pasta tags obsoletas*


# Tags HTML complexas

## Listas na HTML

Neste módulo, daremos continuidade à estruturação de conteúdo com a utilização de tags. Novas tags para a representação de novos tipos de conteúdo serão apresentadas: as listas, as tabelas, os vídeos e os áudios.

### Listas

O HTML fornece suporte para a representação visual de três tipos de listas: as **ordenadas**, as **não ordenadas** e as **de definição**, veja:

* Ordenadas

    Usadas quando desejamos listar dados com a necessidade de representar a sua ordenação de forma numérica ou alfabética.

* Não ordenadas

    Usadas quando não há necessidade de listar ordenadamente.

* De definição

    Usadas quando precisamos listar itens e atribuirmos uma descrição a eles.

*Outra característica importante das listas é que a sua marcação HTML é composta por uma tag de container, ou tag “pai”, e por seus itens ou “filhos”. Além disso, a lista de definição possui ainda um terceiro item, que é justamente o utilizado para descrevê-lo. Veja na tabela a seguir cada tipo de lista:*



| Tipo | Tag Container | Tag Item |
|-----|-------
| Ordenadas | < ol > | < li > |
| Não ordenadas | < ul > | < li > |
| Definição | < dl > | < dt > |

**Exemplos na pasta exemplos de listas**

**Cabe destacar que tanto o símbolo de ordenação (a numeração, no exemplo acima), no caso da primeira, quanto o símbolo visual (o bullet – pequeno círculo preto), no caso da segunda, podem ser alterados com a utilização de CSS.**


## Tabelas na HTML

Quando precisamos lidar com dados tabulares em uma página web utilizamos tabelas. As tabelas usadas nesse documento são exemplos do tipo de dado e também da apresentação obtida ao utilizarmos tais elementos na HTML.

### Estrutura das Tabelas

A marcação HTML relacionada às tabelas contém, além da tag principal <table>, outras tags. A principal define o container geral.

De forma hierárquica, a seguir temos as tags para a definição de linhas <tr>> e colunas <td>. Com estas três tags é possível representarmos uma tabela simples. Entretanto, há tags adicionais que podem ser usadas e que ajudam a melhor organizar o conteúdo.

A tabela abaixo apresenta as tags de marcação, e suas respectivas funções, relacionadas às tabelas:

| Tag | Função |
|-----|--------|
| < table > | Container principal da tabela |
| < tr > | Representa as linhas, sendo composta pelas tags relacionadas as colunas |
| < td > | Representa as colunas e precisa ser inserida dentro da tag de linha. |
| < th > | Também representa colunas e é usada para exibir o título de uma coluna, possuindo, neste sentido, função semântica. Assim como a tag < td >, deve estar contida em uma tag de linha. Este elemento apresenta estilos próprios, sendo renderizado de forma diferente das colunas comuns.|
| < thead > | Armazena o cabeçalho da tabela, sendo composto por linhas e colunas. Este elemento, a exemplo do que vimos anteriormente, tem função semântica em termos de estruturação de conteúdo. |
| < tfoot > | Armazena o rodapé da tabela, tendo também função semântica em termos de estruturação. |

As tabelas, normalmente, são organizadas de maneira uniforme: linhas sobre linhas, colunas após colunas, célula ao lado de célula. Logo, as colunas costumam ter a mesma largura, assim como as linhas a mesma altura. Entretanto, há situações nas quais é preciso mudar um pouco essa organização. Por exemplo, pode ser necessário mesclar duas colunas ou mesmo duas ou mais linhas.

Para isso, fazemos uso de alguns atributos - que têm função de destaque ao tratarmos das tags relacionadas às tabelas. São eles: rowspan e colspan. Como o próprio nome indica, estes atributos têm a função de expandir as linhas ou colunas. Sua declaração é acompanhada de um número que indica a quantidade de células a serem utilizadas para expansão da linha ou coluna.

### As tabelas e a semântica

Podemos dizer que as tabelas foram, desde a criação do código HTML, o elemento mais utilizado fora de sua função semântica. Isto se deve ao fato de que a estrutura básica de uma página HTML lembra muito a estrutura de uma tabela: cabeçalho, rodapé, seções (linhas) etc. Logo, foi prática comum ao longo de muitos anos a codificação de páginas Web completas fazendo-se uso de tabelas. Além de ir de contra a semântica, tal uso traz consigo outros problemas, como o peso das páginas e a redução da acessibilidade, entre outros.

**Exemplo de tabelas: vide pasta tabelas exemplo**

### Aplicação 

Como vimos, um documento HTML pode conter tanto tabelas simples quanto mais complexas. Tendo como base o arquivo HTML usado nos módulos anteriores e o conteúdo já visto, chegou a hora de **codificarmos**. No editor de texto, comece criando uma nova seção no seu HTML e insira:

* uma tabela simples;
* uma tabela que contenha título;
* uma tabela com cabeçalho e rodapé;
* uma tabela com linhas e colunas expandidas;
* um exemplo completo;

*salve o arquivo e veja o resultado no navegador.*

*Tabelas vide vamos praticar 2*

## Mídias na HTML

### Mídias: vídeo e áudio

O suporte à multimídia na HTML vem melhorando ao longo dos anos e versões. Com o advento da HTML5, tornou-se possível, de forma muito simples, **incorporar vídeo e áudio em uma página Web**. Para isso, são usadas as tags < video > e < audio >, veja:

~~~~~
<video src= “http://www.youtube.com/watch?v=20SHvU@PKsM” controle></video>
<audio src= “/audios/sample.ogg” controls autoplay loop></audio>
~~~~~

Como visto, os atributos também têm suma importância ao fazermos uso das tags de vídeo e áudio. No exemplo acima, temos, inicialmente, o atributo “src” – que informa o endereço, podendo ser de um site, ou mesmo de um arquivo local – no seu computador ou no servidor onde a página Web fica hospedada.

> Os atributos “controls”, “autoplay” e “loop”, que são específicos para este tipo de mídia em questão, fornecem suporte ao controle do conteúdo (vídeo ou áudio) incorporado pelo navegador, além de definirem alguns comportamentos, como o autoplay e o loop, que são autoexplicativos.

Os três atributos aqui descritos são apenas uma prévia, uma vez que há alguns outros disponíveis. Outros componentes importantes, contidos na especificação do HTML5, são os eventos que permitem o controle de mídia embutida com a utilização de Javascript. São os chamados “Media Events”.

## Teoria na prática

Ao final deste módulo, vamos inserir novas tags em nosso arquivo HTML. Inclua ao menos uma tag de vídeo e uma de áudio. Além disso, experimente inserir e remover os controles mencionados, sempre salvando e comparando os resultados no navegador.

**vide exemplo midias_exemplo**

### Vamos praticar: 

**vide vamos_praticar_3**

# Formulários em páginas web

## Estrutura básica do formulário

A exemplo do que vimos com as tabelas, o formulário é composto por uma  **tag principal**, um  **container**, e várias  **tags “filhas”**.Tags como campos de texto, de uma ou mais linhas; campos de seleção; e botões fazem parte de sua estrutura.

Além disso, para maior clareza, também usamos tags para informar a função dos campos do formulário. São as chamadas “label”. A tabela a seguir lista as tags comumente usadas em um formulário:

|Tag| Função |
|--|--|
|< form>  |Container principal do formulário  |
|< input> | Campo do formulário. Como há diversos tipos de campos, fazemos uso do atributo “type” para informar o tipo a ser utilizado – conforme veremos mais adiante.|
|< textarea >|Campo de texto de múltiplas linhas.|
|< select > e < option >|Campos de seleção, onde o container é definido pela tag < select > e os itens pela tag < option >.|
|button|Campo de botão. Permite que uma ação seja executada no formulário – enviar o formulário, limpar os dados etc. |
|label|Usado para definir um título, uma legenda, que descreva para que serve cada campo do formulário|

***

### Conhecendo melhor os elementos e atributos do formulário

Na próxima imagem temos o **fragmento HTML correspondente a um formulário**. Nela é possível ver as tags já mencionadas, assim como algumas tipificações nos campos e novos atributos. Falaremos sobre ambos a seguir:

**Vide exemplo_de_formulário1**

É fácil identificar para o que serve cada campo do formulário anterior ao lermos o conteúdo da tag < label>. Além disso, a tag < fieldset> cria seções dentro do formulário, ajudando a separar os campos no código e a visualizar a página no navegador.

Isso fica ainda mais claro quando vinculamos ao < fieldset> a tag < legend>.

Como vimos, é necessária uma atenção especial aos atributos quando tratamos de formulários.

Para melhor visualização e entendimento, todos os atributos contidos no código mencionado são descritos nesta tabela:

|Tag|Atributo  |Função do atributo |
|--|--|--|
| < form > |action  |  Define a URL (endereço) para a qual os dados do formulário serão enviados.
|< form>|method |Define o método HTTP (POST ou GET) para envio dos dados.
| < label>| for|Vincula a tag < label> ao campo ao qual ela se refere. Este vínculo faz com que seja possível clicar na label para ativar o campo relacionado.
| < input>| minlength, maxlength| Definem a quantidade de caracteres mínima e máxima, respectivamente, permitida em um campo.
|< input>, < button>|type|Define o tipo do campo e, sobretudo, como ele se comporta.
|< option>|value|Este atributo também pode ser utilizado na tag < input>. Ele define o valor do campo. No caso da < option>, os seus valores possíveis são previamente definidos quando a página é codificada. Já na < input>, embora também possa ser previamente definido, normalmente é o usuário quem define o seu valor.

## Atributos do formulário
### O atributo *"type"*

Este atributo, dada a sua importância, precisa ser visto de forma aprofundada. Como já dito, além de  **definir o tipo do campo**, ele também  **determina como este se comporta**. No código apresentado na tabela é utilizado apenas o tipo “text”, que, no caso da tag <input>, corresponde ao seu valor padrão.

Alguns outros tipos comuns são:

 - Password
	 - Marca textos com asteriscos
 - Hidden
	 - Esconde o campo para não ser exibido no navegador.
 - Checkbox
	 - Usado para seleção de valor através de click/check.
 - Radio
	 - Usado para seleção exclusiva de valor – quando é apresentada mais de uma opção, apenas uma poderá ser selecionada, ao contrário do tipo “checkbox”.
 - Submit
	 - Associada à tag < button>, dispara o evento que envia/submete o formulário.
 - Reset 
	 - Associada à tag <button>, dispara o evento que limpa os valores do formulário.
 - Button
	 - Uma tag < input> pode ser do tipo “button” – exercendo, assim, a mesma função da tag < button>.

Ao longo de vários anos, havia apenas esses tipos disponíveis na HTML. Com isso, algumas necessidades − fossem de inserção de tipos de dados específicos, fossem de validação de valores, conforme veremos mais adiante −  **não podiam**  ser supridas  **apenas com a utilização de tags**, sendo necessário combinar códigos Javascript e CSS. Por exemplo: um campo para seleção de data.

Além disso,  **novos tipos de dados**, com características específicas,  **ganharam importância ao longo dos anos**. Podemos citar, como exemplo, o e-mail. Embora seja um campo de texto, ele possui um padrão de composição próprio, como o uso de @, entre outras características.

### Novos atributos e tipos

Pensando nas deficiências citadas, e como é comum na evolução da HTML, a HTML5 definiu **novos tipos de entrada** e também **novos atributos relacionados** a formulários. Entre eles, podemos destacar:

**Atributos:**                     

|Atributo | Função | Comentário|
|----|-----|----|
| place |Exibir um texto no campo de input.|Utilizado para dar uma dica ao usuário sobre o dado a ser inserido.
|required | Determinar se um campo é obrigatório | Utilizado na validação dos dados de um formulário
|autofocus | fixar o foco no campo | Utilizado quando desejamos que, ao carregar o formulário, um determinado campo seja focado.
|pattern | Validar o valor de um campo com base em uma expressão regular | O campo de tel. é um bom exemplo de utilização desse atributo. Com ele podemos, por exemplo, determinar a quantidade de caracteres e o formato esperado para um campo.



**Exemplo de pattern:**
As RegEX expressões regulares – podem ser consideradas um recurso de linguagem de programação para a análise e manipulação de texto.

## Tipos
| tipo | Função  | Comentário |
|--|--|--|
|tel|Inserir números de telefone.|Para uma melhor usabilidade, deve ser usado em conjunto com o atributo pattern.|
|datetime|Inserir datas com o fuso horário em UTC a partir de um calendário.|
|date|Inserir datas sem fuso horário a partir de um calendário. |
| number|Inserir números.|Cria um componente diferente do imput normal, em que, por meio de setas, os números podem ser incrementados ou decrementados.|

*Uma lista completa dos atributos e tipos pode ser encontrada nas referências mencionadas na seção Explore +.*

### Validação de dados em formulários

Para explicarmos a criação de um formulário HTML, apresentamos tags e atributos que nos permitem montar um formulário já funcional, pronto para ser preenchido e submetido. Entretanto, há um outro aspecto relacionado a esses elementos que precisa ser discutido:  **A validação de dados**.

A importância da validade dos dados concorre com a importância da utilização das tags corretas e que permitam a  **melhor experiência possível aos usuários**. Podemos dizer que, ao pensarmos na estrutura do formulário, nas tags e atributos, estamos pensando em quem vai preencher o formulário.

**Exemplo**
Imagine que podemos permitir a inserção de uma data de nascimento através da digitação de valores ou a partir da seleção em um elemento do tipo calendário. Agora pense em quem vai receber as informações provenientes do formulário. Em um campo de texto simples, sem nenhum tipo de padrão, serão recebidas as mais variadas combinações de dados.

Por exemplo: 01 de janeiro de 1980; 01/01/1980; 01011980 etc. Imaginando esse cenário, é possível entender a importância da validação das informações.

##  Como funciona a validação?

A validação é um processo que pode, e deve, ocorrer tanto no  **lado cliente**  – no navegador – quanto no  **lado servidor**. Pensando no lado cliente, essa ação ocorre assim que o formulário é submetido, antes que os dados sejam recebidos pelo servidor de destino.

Até há bem pouco tempo, para validar um formulário era necessário fazer uso de Javascript. Entretanto, na HTML5 é possível fazê-lo de forma nativa, sem o uso de linguagens de programação.

### Tipos de validação
Na HTML5 há dois tipos de validação possíveis:

* Que verifica se o dado inserido em um campo é consistente com o seu tipo e/ou padrão (pattern).
* Que verifica se um campo obrigatório foi preenchido.

**Exemplo**

Quanto à primeira validação, podemos citar novamente o elemento input do tipo “e-mail”.

Um endereço de e-mail é um dado que possui uma formatação pré-definida: precisa ter o “@”; precisa ter a extensão de domínio “.com / .com.br” etc.

Logo, declarar uma tag input com o type “e-mail” faz com que, naturalmente, seja validado o seu conteúdo.

Algo semelhante acontece com a utilização do atributo pattern, sendo que, neste caso, é você quem define o que um campo precisa conter para ser considerado válido. Por exemplo: determinar o formato desejado para um campo que receba um número de telefone.

Você pode definir que ele contenha o DDD, com dois caracteres numéricos, seguido por dois conjuntos de números – um contendo 5 e outro contendo 3 ou 4 caracteres – o que geraria este código: pattern=“[0−9]2  [0-9]{5}-[0-9]{3,4}$”.

Além da validação pelo tipo de dado, há também a validação de campos obrigatórios. Logo, quando precisamos que determinado campo não fique em branco, usamos o atributo “required”.

*vamos praticar*
**vide vamos_praticar4**

**Fim da matéria html**
****
# Linguagem de marcação e estilos - CSS

*A CSS, ou folhas de Estilo em Cascata (Cascading Style Sheets), é uma linguagem de estilo que fornece total controle sobre a apresentação de um documento escrito em HTML.*

*No ambiente web, a HTML é a linguagem responsável pela estrutura do conteúdo de uma página. Embora também seja capaz de organizar o conteúdo visualmente, é função da CSS cuidar desse aspecto e de tudo relacionado ao estilo e layout da página.*

*Com a CSS, é possível, por exemplo, alterar a forma e o posicionamento dos elementos, as cores, tipos e tamanhos de fontes, e muito mais.*

*seletores css:*
mídias/tabela-seletores-css3.png

## Fundamentos do CSS

A CSS, ou Folhas de Estilo em Cascata (Cascading Style Sheets), é uma linguagem de estilo que fornece total controle sobre a apresentação de um documento escrito em HTML. Por meio dela, é possível, por exemplo, alterar a forma e o posicionamento dos elementos, as cores, os tipos e tamanhos de fontes e muito mais.

A CSS permite a aplicação seletiva de estilos a elementos em uma página HTML. Isso significa dizer que um ou mais estilos podem ser aplicados em um documento inteiro ou mesmo em apenas parte dele. Além disso, um mesmo tipo de elemento pode ter, ao longo do documento, diferentes estilos.

## Sintaxe do CSS

Para aplicar um estilo CSS a um elemento específico, é necessário identificá-lo e apontar qual de suas propriedades queremos alterar e qual valor queremos atribuir-lhe. Essas três informações definem a sintaxe da CSS, conforme pode ser visto no exemplo a seguir.

~~~~~~~~
p{
    background-color: blue;
}
~~~~~~~~
p = Seletor
background-color: = propriedade
blue = valor

Tendo o exemplo anterior como base, podemos perceber que, para aplicarmos um estilo utilizando CSS, são necessários:

*   O seletor: nesse caso, a tag HTML < p >.
*   Ao menos uma propriedade: a cor de fundo (background-color).
*   Ao menos um valor para a propriedade: blue.

Essa declaração de estilo faria com que todas as tags < p > do documento apresentassem a cor azul ao fundo. O exemplo utilizou apenas uma declaração (propriedade + valor), mas é possível inserir em conjunto várias outras.

Além dos aspectos mencionados acima, há outros importantes com relação à sintaxe:

*   A propriedade e seu valor devem ser separados por dois pontos “:”.

*   Uma declaração deve ser separada da declaração subsequente com a utilização do ponto e vírgula “;”.

*   O conjunto de estilos aplicados a um seletor é envolvido por chaves “{“ e “}”.


Vamos ver a seguir um exemplo de duas propriedades atribuídas à tag < p > e o resultado dessas declarações no navegador.

**vide exemplos:**
*básico*

## Seletores

Vimos nos exemplos anteriores um estilo sendo declarado em uma tag HTML < p >. Nós nos referimos a essa tag como sendo o seletor ao qual o estilo foi aplicado. Existem muitos outros seletores disponíveis além daqueles correspondentes às tags HTML, conforme veremos a seguir.

## Seletores class e id

O seletor de classe é definido a partir da declaração do atributo class em um elemento HTML. Já o seletor de identificação é definido com o atributo id.

Em termos de nomenclatura para a definição do nome da classe ou do identificador, não existe uma regra a ser seguida. Procure utilizar nomes que façam sentido, que tenham relação com a função do elemento na página e que, de fato, ajudem a identificá-lo ou classificá-lo.

Logo abaixo, podemos ver um exemplo de sintaxe correspondente à declaração desses dois atributos na HTML e na CSS. Na primeira parte da imagem, é apresentado um fragmento de código HTML. Repare que uma mesma classe, a “texto vermelho”, foi atribuída à tag < h1 > e a uma das tags < p >. Com isso, vemos que uma classe pode ser atribuída a mais de um elemento. Em seguida, note a sintaxe para atribuição de múltiplas classes a um elemento na segunda tag < p >, à qual foram atribuídas as classes “texto_descricao” e “texto_vermelho”.

Em relação ao código CSS, veja que o seletor de id é representado por uma “#” e o de class é representado por um “.”, sendo seguidos de seus nomes. Além disso, foram apresentadas duas formas de sintaxe que produzirão o mesmo efeito. A diferença entre ambas é que, na segunda, o nome da tag à qual a identificação ou classe foi atribuída precede o respectivo sinal.

**vide fragmentos HTML**

## Restrições e boas práticas na utilização do identificador

Embora não exista um padrão ou preferência quanto a utilizar o seletor id ou class, é importante frisar novamente que um id deve ser aplicado a apenas um elemento, enquanto a class pode ser aplicada a um ou vários elementos.

Embora o navegador não verifique se um mesmo id foi utilizado em diferentes elementos, tal método pode trazer alguns problemas de estilização e comportamento, uma vez que esse seletor também é bastante usado pelo Javascript. Frente a isso, adote a boa prática de definir identificadores únicos.

### Seletores de atributo 

Esses seletores utilizam nomes de atributos dentro de colchetes, sendo possível combiná-los com valores. Abaixo são mostrados alguns dos seletores de atributo disponíveis:

*   [checked] - seleciona todos os elementos que possuem o atributo checked.
*   [type=’text’] - seleciona todos os elementos do tipo text.

Os seletores de atributo são flexíveis, permitindo inúmeras combinações. Por exemplo, é possível usá-los para selecionar todas as imagens com uma determinada extensão, selecionar todos os elementos com o atributo title contendo determinado valor etc.

### Seletores baseados em relacionamento

É possível declarar estilos utilizando a relação entre os elementos. A tabela a seguir mostra os principais seletores baseados em relacionamento.

| Seletor | Seleção |
|-----|------|
| H1 P | Qualqyer elemento P que seja descendente (filho, neto etc.) de um elemento H1 |
| H1 > P | Qualquer elemento P que seja filho de um elemento H1 |
| H1 + P | Qualquer elemento P que seja o próximo irmão de um elemento H1 (ou seja, o próximo filho de um mesmo pai.) |


Para uma melhor compreensão quanto à descendência e ao parentesco mencionados, veja a figura abaixo. Essa é uma representação simbólica da árvore DOM (representação estruturada do documento HTML em formato de árvore) contendo elementos representando tags HTML. Veja ainda a explicação de cada relação e aplicação dos seletores baseados em relacionamento.

### Propriedade CSS

Existem inúmeras propriedades CSS, desde as definidas pela sua especificação, ditas propriedades padrão, até as proprietárias, que funcionam apenas em alguns navegadores. A fim de garantir uma maior compatibilidade, assim como otimizar o desenvolvimento, deve-se sempre dar preferência às primeiras. A seguir, são apresentadas algumas das propriedades mais comuns da CSS.

| Propriedade| Função |
|--|--|
| Background | Estabiliza o fundo de elementos. Para tal há uma série de propriedades, além do atalho "Background", como "background-color", "background-image" etc. 
| Border | Controla as bordas de um elemento, sendo possível definir suas cores, espessuras, entre outras propriedades
| Top, Botton, Right e Left | Controlam o posicionamento, relativo ou absoluto, dos elementos em relação a outros elementos. 
| Font-family, Font-size, Font-weight etc | Série de propriedades usada para estilizar o conteúdo textual de um elemento no que diz respeito a fonte, como a família de fontes, seu tamanho, peso (mais clara ou mais escura - negrito) etc. 
| Height | Define a altura de um elemento
| List-style, List-style-image etc | Propriedades usadas para estilizar as listas HTML.
| Margin | Controla a distância em função da margem de um elemento para outro
| Padding | Controla a distância entre as bordas e o conteúdo de eum elemento
| Position | Define como um elemento deve ser posicionado na página
| Text-... | Muitas propriedades controlam o comportamento do conteúdo textual de um elemento, como alinhamento (justificado, centralizado etc), aparência (sublinhado etc.) etc.
| Width | Define a largura de um elemento
| Z-index | Define a profundidade de um elemento -usado, por exemplo, para sobreposição de elementos. 

****
### Integrando a CSS à HTML

Há três formas usuais de aplicar estilos em um documento HTML fazendo uso de CSS: Inline, Interna e Externa.

Além dessas, a HTML5 permite ainda a aplicação em escopo. Vamos conhecer um pouco mais de cada uma delas?

*   CSS inline
    *   Essa forma implica em declarar o estilo CSS diretamente na tag, no código HTML. Veja a seguir um exemplo de um estilo apresentado anteriormente sendo aplicado de forma inline.

A declaração inline faz uso do atributo style procedido por declarações separadas por ponto e vírgula “;”. Esse atributo pode ser usado em qualquer tag HTML.
~~~~~~~~
<p style="background-color: blue;">Texto parágrafo</p>
~~~~~~~~
*   CSS interna
    *   Também chamada de CSS incorporada, é declarada na seção < head > do documeneto HTML.

~~~~~~~~
<html>
    <head>
        <style type="text/css">
            p{
                background-color: blue;
            }
    </head>
...
</html>

~~~~~~~~

*   CSS externa
    *   Nesse caso, os estilos são declarados em um arquivo externo, com extensão “.css” e vinculados ao documento HTML por meio da tag < link > ou da diretiva @import dentro da tag < head >. Ambos os exemplos podem ser vistos logo a seguir:

~~~~~~~~
<html>
    <head>
        <link rel="stylesheet" type="text/css href="estilos.css" />
...
    </head>
</html>
~~~~~~~~

~~~~~~~~
<html>
    <head>
        <style>
            @import url("estilos.css");
        </style>
    </head>
</html>
~~~~~~~~

*   CSS em escopo
    * Essa forma de aplicação de estilo foi criada a partir da HTML5. Por meio dela, é possível aplicar estilos no âmbito de escopo, ou seja, específicos para as seções da página em que foram declarados, incluindo os seus elementos filhos. No código abaixo, a tag < p > receberá os estilos definidos, sendo a mesma regra válida para outros estilos e elementos que, porventura, venham a fazer parte da < div >.

~~~~~~~~
<div>

    <style type="text/css">
        /* Estes estilos serão aplicados apenas dentro da DIV */
        p{
            background-color: blue;
        }
    </style>
    <p>Texto do parágrafo</p>


</div>
~~~~~~~~

### Efeito cascata 

Quando trabalhamos com CSS, é comum nos depararmos com a declaração conflitante de estilos, ou seja, diferentes definições de estilo para um mesmo elemento. Nessas situações, entra em ação o Efeito Cascata. Para entendermos a definição desse efeito, é preciso abordarmos outros dois conceitos: **herança** e **especificidade**.

### Herança

A CSS permite que a aplicação de propriedades a elementos pais seja herdada pelos seus elementos filhos. Tomemos como exemplo o código abaixo.

~~~~~~~~
div{
    color: blue;
}

<div> 
    Texto solto na DIV
    <p>Texto do parágrafo que é 'filho' da Div</p>
</div>
~~~~~~~~
O resultado do fragmento de código mostrará tanto o texto solto quanto o texto dentro da tag < p > com a cor azul. Isso significa que a tag < p > herdou o estilo definido para o seu pai, a tag < div >.

> Essa capacidade de herdar estilos caracteriza o que chamamos de Efeito Cascata.

*Cabe destacar que nem todas as propriedades CSS podem ser herdadas pelos filhos. Um exemplo são as propriedades relacionadas à formatação das boxes (que veremos mais adiante), como largura, altura, entre outras.*

### Especificidade

Para entender o que é a especificidade no âmbito das folhas de estilo, vamos recorrer a mais um exemplo.

~~~~~~~~
...
div{
    color: blue;
}
<div>
    Texto solto na Div
    <p>Texto do parágrafo que é "filho" da DIV</p>
</div>
...
~~~~~~~~

Perceba que o fragmento da figura exemplo de herança em CSS foi adaptado. Antes, era aplicado o conceito de herança, assim o texto dentro da tag filha assumia o estilo definido para o seu pai. Agora, há um estilo específico definido para todas as tags < p > que sejam filhas de tags < div >. Com isso, ao visualizarmos o resultado no navegador, teremos o texto solto na cor azul e o texto dentro da tag na cor vermelha.

Esse foi um exemplo simples. A CSS é bastante flexível e nos permite definir diferentes níveis de especificidade. Entretanto, é importante termos cuidado com a sobreposição de estilos, ou seja, diferentes estilos definidos para um mesmo elemento em diferentes partes de nosso código CSS. A regra, nesse caso, é: prevalecerá o estilo mais específico. No exemplo acima, a primeira declaração (para a tag div) é generalizada; a segunda (div p), específica.

###  Dicas sobre as regras de precedência

A regra de precedência em relação às formas de inclusão da CSS segue esta ordem:

1.  Os estilos interno e de escopo têm precedência sobre os estilos em arquivos externos.
2.  Os estilos inline têm precedência sobre estilos internos, de escopo e externos. 

*Quanto aos seletores, a **regra de precedência** segue esta ordem :*

1.  Seletores de elemento
2.  Seletores de classe
3.  Seletores de identificação

Seguindo as regras de especificidade, sua aplicação resultaria na apresentação do texto dentro da tag < p > na cor vermelha, pois sua declaração de estilo é mais específica que a utilizada para a **tag < p >** (texto azul), que é generalizada. Entretanto, a utilização do valor **!important,** que se enquadra no que chamados de **css hack**, na declaração mais generalizada, faz com que esse estilo se sobreponha ao específico. Logo, o código acima resulta na apresentação do texto dentro da **tag < p >** na cor azul.


### Recursos de cores

Com a utilização de CSS, podemos manipular as cores de elementos HTML, seja na aparência das caixas seja na cor de texto. Para isso, há uma série de propriedades CSS disponíveis para diversos elementos, mas antes vamos abordar as formas de definição de cores.

### Formas de escrita de cores

As cores em CSS podem ser escritas de três modos:

*   Com palavras-chave ou notação hexadecimal: blue, red, #ffffff etc. 

*   Com um sistema de coordenada cúbica RGB, com as notações rgb() e rgba().

*   Com um sistema de coordenada cilindrica HSL, com as notações hsl() e hsla().

### Propriedades de cor

Essas propriedades se referem a quais elementos podemos definir cores.

Veja na tabela a seguir as principais propriedades relacionadas à cor, bem como os elementos aos quais podem ser aplicadas.

| **Propriedade** | **Serve para definir** | **Onde pode ser utilizada** |
|--|--|--|
| color | Cor de textos | Elementos que contenham texto, como < h1 > ... < h6 >, < p >, < header >, < section > etc. |
| background-color | Cor de fundo de elementos | Aplica-se a qualquer elemento HTML. |
| border-color | Cor da borda | Aplica-se a qualquer elemento HTML. 
| outline-color | Cor da borda externa | Aplica-se a qualquer elemento HTML. |

### Recursos de textos e fontes

A estilização de textos com o uso de CSS é dividida em duas partes.

Em linhas gerais, os navegadores aplicam estilos padrões quando renderizam conteúdos textuais. Veja a seguir algumas propriedades CSS que alteram esse comportamento padrão.

*   Layout do texto

    *   Espaçamento entre os caracteres e linhas; alinhamento em relação ao container.

*   Estilos das fontes

    *   Família, tamanho, efeitos como negrito etc.

Em linhas gerais, os navegadores aplicam estilos padrões quando renderizam conteúdos textuais. Vamos conhecer, a seguir, algumas propriedades CSS que alteram esse comportamento padrão.

### Alinhamento de texto

A propriedade text-align é usada para controlar o alinhamento do texto em razão do container no qual está inserido.

Tal propriedade pode assumir quatro valores: left, right, center e justify. Como os nomes indicam, essas propriedades alinham o texto à esquerda, à direita, ao centro ou de forma justificada.

### Espaçamento entre linhas

A propriedade line-height permite alterar o espaçamento vertical entre as linhas de texto. Seus valores possíveis são:

*   Normal

    *  Valor padrão do navegador (entre 1 e 1.2 em relação ao font-size, dependendo do navegador). 

*   Número

    *   Valor inteiro ou decimal que será multiplicado ao tamanho da fonte.

*   Comprimento

    *   Valor unidades como pixels, pontos, “em” etc.

A maneira mais recomendada para declarar o espaçamento entre linhas é utilizando o valor em número. Desse modo, o espaçamento será o resultado da multiplicação do valor definido pelo tamanho da fonte.

**Exemplo:**

*Line-height: 1.5; font-size: 12px; onde valor 1.5 será multiplicado pelo valor da propriedade font-size, resultando no valor de 18px de espaçamento.*

### Espaçamento entre letras e palavras

As propriedades letter-spacing e word-spacing permitem alterar o espaçamento entre letras e/ou palavras. Podem assumir valores de comprimento – “px”, “pt” etc.

### Fontes

Em relação às fontes, há propriedades CSS para definir família, tamanho, estilo, entre outras possibilidades. Vamos conhecer as propriedades mais usadas?

*   font-family

    Utilizada para definir a família da fonte, utilizada na página web ou em partes do seu conteúdo.

*   font-size

    É responsável por definir o tamanho do texto. 

*   font-style

    Usada na estilização de textos aplicando o efeito itálico, obliquo etc

*   font-weight

    O peso de uma fonte é definido com a utilização dessa propriedade. Com ela é possível aplicar o efeito de negrito em uma escala. 


Existem boas práticas e cuidados a serem levados em consideração quando se trabalha com estilização de fontes usando CSS. Um desses cuidados diz respeito ao **controle** sobre a **possível degradação** que pode ocorrer na página. Portanto, deve-se tomar os devidos cuidados optando pela utilização de uma lista de fontes e mantendo por último as fontes genéricas, como Serif, Sans Serif e Monospace. Desse modo, haverá maior garantia e controle sobre o que o usuário verá como resultado.

### Web fontes

As Web Fontes são um importante recurso em termos de tipografia. Se antes a sua estilização ficava restrita àquelas disponíveis nos sistemas operacionais dos usuários, a partir da implementação da regra @font-face tornou-se possível a utilização de Web Fontes. Essa nova propriedade permite a utilização de fontes que, ao serem definidas, são baixadas pelo navegador no momento de carregamento da página. Logo, sua utilização permite um controle maior do layout de uma página no que diz respeito às fontes, além da possibilidade de serem usadas fontes com maior apelo visual.

### Como utilizar a regra @font-face

A declaração da regra @font-face é feita pela definição de duas principais propriedades: font-family e src. Na primeira, definimos um nome para a família da fonte que estamos importando, usando-o ao longo do arquivo CSS. A segunda aponta para a url na qual o arquivo da fonte se encontra. Vamos ver a seguir a fonte Awesome sendo declarada.

Em relação à font-family, a partir do momento da sua declaração, o nome definido poderá ser utilizado para estilizar qualquer outro elemento ao longo do CSS – considere que podemos tanto utilizar uma única família de fontes para o documento HTML inteiro como a combinação de diferentes famílias.

O código também mostra que as fontes incorporadas podem tanto estar hospedadas localmente quanto na internet. Além disso, há outros elementos na declaração dos quais ainda não falamos. São eles: as funções  **local**  e  **format**.

Cabe destacar também os diferentes tipos existentes de web fontes. Aprofundaremos esses elementos extra a seguir.

*   Função local

    *   Essa função indica ao navegador que, antes de fazer o download da fonte definida, deverá verificar se ela já está disponível na máquina do usuário.

*   Função format

    *   Também chamada de dica, essa função opcional é utilizada quando se deseja declarar vários formatos de fontes, indicando justamente o formato de cada uma. No exemplo acima, temos os formatos “woff”, “woff2”, “ttf” e “eot”.


### Abreviaturas ou atalhos

As Folhas de Estilo permitem a aplicação de algumas propriedades utilizando abreviaturas ou atalhos. O exemplo a seguir mostra as duas formas de realizar uma mesma declaração:

**Forma original**

~~~~
p{
    margin-top: 10px;
    margin-botton: 8px;
    margin-right: 6px;
    margin-left: 4px;
}
~~~~

**Forma abreviada**

~~~~
p{
    margin: 10px 6px 8px 4px;
}
~~~~

**Forma original**

~~~~
p{
    padding-top: 10px;
    padding-botton: 8px;
    padding-right: 6px;
    padding-left: 4px;
}
~~~~
**Forma abreviada**
~~~~
p{
    padding: 10px 6px 8px 4px;
}
~~~~

**Forma original**

~~~~
p{
    border-width: 2px;
    border-style: solid;
    border-color: #cccccc;
}
~~~~

**Forma abreviada**

~~~~
p{
    border: 2px solid #cccccc;
}
~~~~

**Forma original**

~~~~
p{
    background-color: #000000;
    background-image: url(imagem.jpg);
    background-repeat: no-repeat;
    background-position: top left;
}
~~~~

**Forma abreviada**

~~~~
p{
    background: #000000 url(imagem.jpg) no-repeat top left;
}
~~~~

**Forma original**

~~~~
p{
    font-size: 1em;
    line-height: 1.5em;
    font-weight: bold;
    font-style: italic;
    font-family: verdana;
}
~~~~

**Forma abreviada**

~~~~
p{
   font: 1em/1.5em bold italic verdana;
}
~~~~

**Forma original**

~~~~
ul{
   list-style: #000000;
   list-style-type: disc;
   list-style-position: outside;
   list-style-image: url(imagem.jpg) 
}
~~~~

**Forma abreviada**

~~~~
ul{
    list-style: disc outside url(imagem.jpg)
}
~~~~

### Fontes


# Conceitos avançados de CSS

## Conceitos de box model

Nos módulos anteriores, vimos os conceitos básicos de CSS, sua sintaxe, seus elementos e suas formas de integração com HTML. Abordamos também como aprimorar o design de páginas com os estilos de cores, texto e fontes.

Neste módulo, avançaremos um pouco mais e percorreremos os conceitos de Box Model (modelo de caixas ou retângulos), Pseudoclasses e Pseudoelementos e Posicionamento.

*dentro do conceito de Box Model – que, em CSS, está relacionado a design e layout – nossos boxes possuem quatro componentes principais: margem (margin), borda (border), preenchimento (padding) e conteúdo (content).*


## Conceitos de pseudoclasses e pseudoelementos

Uma declaração CSS é composta pelo elemento que se deseja estilizar, pela propriedade a ser estilizada e pelo valor a ser atribuído. Além disso, vimos que o elemento pode ser definido de maneira ampla (utilizando-se o nome da tag), específica (pelo seu identificador único) e seletiva (com a utilização de classes).

Um elemento filho pode, ainda, herdar as propriedades de um elemento pai. Todos esses modos de definir estilo são bastante abrangentes. Entretanto, existem algumas formas especiais e muito úteis para se aplicar estilos: as  **pseudoclasses**  e os  **pseudoelementos**. Veremos a seguir as suas definições e como utilizá-las.


Uma declaração CSS é composta pelo elemento que se deseja estilizar, pela propriedade a ser estilizada e pelo valor a ser atribuído. Além disso, vimos que o elemento pode ser definido de maneira ampla (utilizando-se o nome da tag), específica (pelo seu identificador único) e seletiva (com a utilização de classes).

Um elemento filho pode, ainda, herdar as propriedades de um elemento pai. Todos esses modos de definir estilo são bastante abrangentes. Entretanto, existem algumas formas especiais e muito úteis para se aplicar estilos: as  **pseudoclasses**  e os  **pseudoelementos**. Veremos a seguir as suas definições e como utilizá-las.

##  Pseudoclasses
As pseudoclasses são utilizadas para definir um estado especial de um elemento. Por exemplo, podemos mudar o estilo de um elemento ao passarmos o mouse sobre ele (evento mouseover). Esse novo estilo é temporário, ou seja, não corresponde ao seu estado natural. Também podemos mudar o estilo de um link que foi clicado, alterando sua cor ou alguma outra propriedade.

A sintaxe para declaração da pseudoclasse é composta pela palavra-chave correspondente ao nome da pseudoclasse precedido pelo sinal de dois pontos. Veja o exemplo a seguir:

~~~~
 div:hover{background-color:#000000;}
~~~~

## Pseudoelementos

Os pseudoelementos são palavras-chave que, adicionadas/relacionadas a um seletor, permitem que uma parte específica dele seja estilizada. A imagem a seguir mostra duas declarações CSS, uma sem e outra com o uso de pseudoelemento. Em ambas, é definido que a primeira letra de texto em um parágrafo tenha tamanho e cor diferentes do restante do texto.

Ao analisar, codificar e testar o código acima, você perceberá que, no primeiro parágrafo, foi necessário utilizar um elemento a mais, a tag < span >, ao redor da primeira letra do texto para poder estilizá-la. Já no segundo parágrafo, o mesmo estilo foi alcançado apenas com o uso do pseudoelemento first-letter. A utilização do pseudoelemento diminui a quantidade de código, tornando sua compreensão mais clara.

Cabe destacar outro ponto do exemplo relacionado à sintaxe dos pseudoelementos: neles são usados dois pontos duplos (ou dobrados) para a declaração. Esse uso proposital é para diferenciá-los das pseudoclasses.

*vide imagem pseudoelementos*

## Conceitos de layout
### Layout em colunas e Grid Layout

Esses dois conceitos são importantes quando tratamos da estrutura visual de páginas HTML. Em uma definição simplista, ambos tratam de como os elementos boxes podem ser posicionados e organizados em uma página. Veja na figura layout CSS em colunas, logo a seguir, a estrutura em colunas de uma página.

*vide imagem layout e grid*

## A propriedade position

A propriedade CSS responsável pelo posicionamento é a position. Seus valores possíveis são:  **static, relative, fixed, absolute e sticky**. Além disso, as propriedades top, bottom, right e left são usadas em conjunto, a fim de definir os valores das respectivas distâncias e, consequentemente, do posicionamento. Tais propriedades, inclusive, só podem ser usadas quando for definido um valor para position. A seguir, apresentaremos cada uma dessas cinco propriedades.

### Position static

Essa é a  **posição padrão**  dos elementos. Desse modo, elementos definidos como static ou sem a propriedade position são posicionados naturalmente, de acordo com o fluxo normal da página, não assumindo nenhuma localização especial. Inclusive, as propriedades top, bottom, right e left não são refletidas em elementos estáticos.

### Position relative

A definição da propriedade “position:relative;” para um elemento faz com que ele seja posicionado de modo relativo à sua posição normal. Com isso, ao definirmos valores para as propriedades top, bottom, right e left, ajustamos a sua posição em relação à sua posição natural.

### Position fixed

O valor  **fixed**  é utilizado quando desejamos definir uma posição fixa para um elemento na página. Com isso, independentemente do scroll, de rolarmos a página para cima ou para baixo, o elemento sempre permanecerá no mesmo local. As propriedades  **top, bottom, right**  e  **left**  devem ser usadas para definir o lugar no qual o elemento será fixado. Esse elemento é posicionado em relação à viewport/janela do navegador. Com isso, ele “flutuará” sobre os demais conteúdos da página, ficando fixo onde foi colocado e não ocupando, assim, a posição original na qual foi declarado no HTML.

### Position absolute

A posição absolute faz com que um elemento seja posicionado em relação à localização do seu elemento ancestral mais próximo – o qual também deverá estar posicionado, ou seja, não poderá ser static.

Quando o elemento definido como absolute for o primeiro elemento da página, ele então será posicionado em relação ao  **< body >**. Com isso, tal elemento acompanhará a rolagem da página.

### Position sticky

Esse valor para a propriedade position faz com que um elemento seja posicionado com base na posição de rolagem da página (scroll). Com isso, seu comportamento varia entre o relativo e o fixado, dependendo da posição do scroll.

Tal propriedade é mais recente em termos de especificação, assim não possui suporte em todas as versões dos navegadores. É usada, normalmente, quando queremos criar um efeito de sobreposição de conteúdo. Na prática, o elemento é visualizado ao abrirmos uma página. Ao rolarmos para baixo, ele se mantém fixo, com os demais conteúdos passando sob ele.


# Frameworks CSS

