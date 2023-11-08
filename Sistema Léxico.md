# Use Strict

    O use strict serve para que o código seja mais seguro, é uma string que você escreve para indicar que o código deve ser interpretado de modo estrito, deixa o código menos propenso a erros, desabilita algumas coisas ruins do javascript, deixando mais parecido com as versões atuais do js. Ele deve ser a primeira linha do código js.

        Faz com que variaveis não declaradas emitam um erro.

    Quando uma variável não é declarada ela fica pertencendo ao escopo global. 
    É possível fazer um uso escopado do "use strict", da seguinte maneira: 

        function foo(){
            "use strict"
            x = 20
        }
        foo()
        console.log(x)
    
        Dessa forma ele resultara em uma mensagem de erro, já sem simplesmente seria impresso o número 20.

    Outra situação seria os parâmetros dobrados, sem o use strict é possível criar uma função que receba a mesma variavel como dois parametros diferentes, e daí na hora de chamar a função ele pega somente o da ultima informação:

        function dobrar(n1,n1){
            return n1*n1
        }

        console.log(dobrar(5,7))

        Esse console retornaria 49, porque ele apenas pega o ultimo parametro informado e repete, já se, no começo da função tivesse sido usado um "use strict", ocorreria um erro indicando que teve uma duplicata de parametros, que não é permitida nesse contexto

    Um outro problema no js seria por exemplo ao executar uma função e usar o this, ele fazer uso do window, então quando você for atribuir valor a uma propriedade desse suposto objeto, você vai criar uma variavel no escopo global, devido ao this se referir a janela como um todo. Observe abaixo:

        function Teste(){
            console.log(this)
            this.a = "a"
        }

        Teste()

        Assim  funcionaria, fazendo-se necessário o uso do "use strict" para que ocorra um erro informando que a é uma propriedade indefinida.

    Por fim, também existe a opção de você adicionar uma propriedade a um literal, um não objeto, e isso óbviamente não faz sentido, então fazendo uso do "use strict" ele acusa um erro de não poder criar uma propriedade em uma string.

# This dinâmico

    Se temos propriedade e valor do mesmo nome pode-se usar de forma diferenciada, simplesmente passando o nome da função

    o this é referente a quem chama a função, e o responsável por chamar a função no escopo global é o window.

    