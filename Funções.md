# Definição de funções

    São tipos de objetos com a incrível capacidade de serem invocados.

# Podem ser literais

    Uma função não é um objeto, embora possa ser usando o new, elas não necessitam nem de um nome, pode ser simplesmente assim:

    function (){

    }

# Hoisting

    É a capacidade do JS de "içar" uma function declaration, básicamente, assim que o JS é rodado, todas as funções são automáticamente jogadas para o topo do arquivo, evitando que haja a chamada de uma função antes da função ser criada. Essa estratégia não funciona quando estamos usando uma "function Express" que seria a seguinte forma:

        const teste = function teste(){
            console.log("teste")
        }
        teste()

        Dessa forma se chamassemos a função antes, não iria funcionar, aconteceria um erro de teste is not defined

    Hoisting também funciona com variáveis, porém um pouco diferente, o javascript apenas cria a variável, mas a atribuição de valor segue sendo feita na linha que o desenvolvedor escolheu, tanto que se fizermos o seguinte:

        console.log(minhaVar)
        var minhaVar = "variavel"

        Seria printado undefined, mas a váriavel existiria, apenas ainda não teria valor.
    
    O problema desse hoisting é que ele apenas funciona com var, que como já foi abordado é um tipo de variável que evitaremos usar, por diversos motivos, mas principalmente por poder básicamente duplicar uma variável com o mesmo nome

# Objetos de primeira classe

    Funções em javascrpit são tratadas como qualquer outro objeto, ou seja, pode ser passada como parametro para uma outra função, funções tamvbém podem ser atribuídas como propriedades de objetos (métodos), podem ser retornadas como resultados de outras funções e até mesmo podem ter suas próprias propriedades, já que tudo no javascript é como se fosse objeto.

# 