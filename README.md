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

