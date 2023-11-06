# Para testar JavaScript no console basta abrir o terminal e executar o comando node, assim você estará restringido a usar o terminal para JS

    No chrome também é possível realizar esses comandos js

# Também existe um plugin chamado code runner que realiza esse deploy

# Site para ver se o browser suporta coisas do ecmascript2015 ou ES6 : kangax.github.io/compat-table/es6/, outro site que faz o mesmo é o can I use

#  Existem três tipos de dizer que algo é uma string = "", '' e a forma mais moderna é a com crase: ``, a diferença entre as formas está 
#  na concatenação, observe abaixo

    let idade = 40
    # Com as aspas seria dessa forma
        console.log("a bu tem "+idade+"anos")
    # Já com cráse a concatenação é feita da seguinte forma
        console.log(`a bu tem ${idade} anos`)
        O único malefício dessa forma é que em navegadores mais antigos não funciona, devido a fazer parte do ecmascript6 rs

# Existe um verificador chamado typeof
    let idade = 40
    console.log(typeof idade)
    O retorno nesse caso seria "number"

    caso eu usasse isso para algo definido como null o retorno seria "object" devido à uma falha cometida nos primórdios do js

# Conversão de tipos

    todo retorno de interação com o usuário é uma string, e você não terá problemas para realizar quase todas  as operações matemáticas, com exceção do +
    porque ele também serve para concatenar strings, então o js não realiza uma interpretação inteligente do tipo da variavel, apenas usa como se fosse uma 
    string

        let idade = "21"
        console.log(idade + 2)
        o retorno seria 212.

    Existem três tipos de converter string

        parseInt()

            O parseInt converte para um número inteiro, por mais que o número convertido seja um float(double), ele irá converter para número inteiro, sem arredondar, ele só 
            ignora as casas decimais

        parseFloat()

            O parsefloat faz o mesmo só que para decimal, os dois tipos de parse  convertem até mesmo uma string que tenha letras, desde que, as letras sejam colocadas após o número

        método construtor do Number()

            Através do construtor Number() ele converte para qualquer tipo de número, mas se for feito uso de letras nesta string o resultado sera um NaN(Not a Number)

    A conversão de número para string funciona da seguinte maneira

        É feito o uso do .toString(), é interessante mencionar que, nesse toString existe um paramêtro, que por padrão é 10, ou seja, decimal, mas também é possível fazer 
        uso de binário(2) ou até mesmo hexadecimal(16) para realizar esta conversão.

# Operadores de Atribuição

    Tem como realizar operações matemáticas direto na atribuição, não  somente +-, todas as operações abaixo funcionam:

        let i=25
        i*=2 (multiplicação)
        i/=2 (divisão)
        i%=2 (resto)
        i**=2 (potência)

    Existe uma forma diferente de incremento e decremento, que é
    
        --i;
        ++i;

        Dessa forma primeiro se adiciona ou retira, e depois executa o resto, da forma comum isso é feito "depois"

# Truthy e Falsy values

    Falsy = 0, "", NaN, undefined, null, false
    Truthy = todos os demais são true

# Curto-circuito

    Esse conceito serve para definir de forma elegante algo

        let n = 0
        let isvalid = true
        n = n || 10
        isvalid && console.log("salve salve")
        isvalid || console.log("salve salve")

# Iterar Objetos

    Dentro do JS existe uma foram de passar por cada propriedade de um objeto, e isso é feito da seguinte maneira

        for (let prop in pessoa){
            console.log(prop)
        }

        Dessa forma será mostrado o nome da propriedade, e não o seu valor, mas para mostrar o valor pode se fazer da seguinte maneira: 

            for (let prop in pessoa){
                console.log(pessoa[prop])
            }
        
#  Métodos de objetos

    É possível na criação do seu objeto você atribuir um método ao objeto, da seguinte forma:

    const pessoa = {
        nome: "cleito",
        idade: 28,
        fazerAniversario: function(){
            this.idade++;
        }

        Pode ser feito desser jeito também:

        fazerAniversario: () => {
        só que dessa forma não irá funcionar o this, então é necessario fazer de outro jeito,  o this dentor de arrow function chama o objeto Window, ou seja a tela da sua aplicação

        pessoa.idade++;
        }
    }


# Tratamento de Erros -- Try() Catch()

    Mesma coisa que em java, mas nesse caso você da um throw Error("mensage")

# Sistema Léxico 

    

    

