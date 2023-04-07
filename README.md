# Exercícios de JAVASCRIPT

Este repositório contém exercícios de JAVASCRIPT. Abaixo você pode encontrar alguns exemplos que cobrem conceitos básicos e intermediários.

<hr>

## Como utilizar:
Faça o clone deste repositório para a sua maquina, só seguir o comando abaixo:

```
git clone https://github.com/lucaspaulus/atividadePratica-01-Logica-simples-e-estruturas-condicionais-1
```
Depois de feito o clone do repositório, certifique que tenha instalado a extensão Live Server no vscode, clique com o botão direito no index.html e clique 
em abrir com Live Server.

## Exemplos:
1. Crie uma variável JavaScript e coloque nela o valor de sua idade.
Mostre no html usando o document.write() o dado contido na
variável junto da frase "Minha idade é x anos", sendo "x" o valor
armazenado na sua variável.
<br>

```
function myAge(){
    let age = 27
    //document.write(`Minha idade é ${age} anos`)
    return `Minha idade é ${age} anos` 
}
//console.log(myAge())
```
<hr>

2. Crie três variáveis JavaScript, em duas delas atribua os valores que
você quiser e na outra atribua o valor da soma das duas primeiras
variáveis. Apresente valor da soma no documento html junto da
frase "A resultado da soma de x e y é z", sendo x o valor armazenado
na primeira variável, y o valor armazenado segunda variável e z o
valor armazenado na terceira variável

<br>


```
function sumOfTwoNumbers(){
    const x = 10
    const y = 15
    const z = x + y

    return `A resultado da soma de ${x} e ${y} é ${z}`
}
//console.log(sumOfTwoNumbers())
```

<hr>

3. Crie três variáveis, na primeira variável coloque o total de uma
compra, por exemplo 149.90. Na segunda variável coloque a
quantidade de parcelas, por exemplo 2. Na terceira variável coloque
o valor da parcela. Apresente no documento html as seguintes
informações:
"O valor total da compra foi R$_,_"
"Forma de pagamento: _x de R$_,_"

<br>


```
function convertToBrl(inputValue){
    return inputValue.toFixed(2).replace(".", ",")
}

function installmentsCalc(){
    const total = 150.45
    const installments = 2
    const installmentsValue = total / installments

  
    return `O valor total da compra foi R$ ${convertToBrl(total)}
    Forma de pagamento:  ${installments}x de R$ ${convertToBrl(installmentsValue)}`

}
//console.log(installmentsCalc())
```

<hr>


4. Crie duas variáveis. Na primeira coloque um total de minutos e
defina um valor para ela (por exemplo, minutos = 120). Na segunda
coloque o total em segundos destes minutos armazenados na
primeira variável. Apresente no documento html a seguinte
informação: "_ minutos equivale à _ segundos!"
<br>

```
function convertMinutesToSeconds(){
    let minutes = 60
    let seconds = minutes * 60
    return `${minutes} minutos equivale à ${seconds} segundos!`
}

//console.log(convertMinutesToSeconds())

```

5. Crie cinco variáveis. Na primeira armazene o nome de um aluno. Na
segunda, terceira e quarta coloque 3 notas (valores de 0 à 10).
Calcule a média das notas e armazene na quinta variável criada.
Apresente no documento html a seguinte informação:
"O aluno _____ ficou com média _,_"
<br>

```
function calculateGrades(){
    let student = "lucas"
    let studentFirstGrade = 10
    let studentSecondGrade = 8
    let studentThirdGrade = 7
    let result = (studentFirstGrade + studentSecondGrade + studentThirdGrade) / 3

    return `O aluno ${student} ficou com média ${result.toFixed(1)}`
}
//console.log(calculateGrades())
```
<hr>


6. Desenvolva um algoritmo que armazene o valor 10 em uma variável
A e o valor 20 em uma variável B. A seguir (utilizando apenas
atribuições entre variáveis) troque os seus conteúdos fazendo com
que o valor que está em A passe para B e vice-versa. Ao final,
escrever os valores que ficaram armazenados nas variáveis.
<br>

```
function swapNumbers(){

    let A = 10
    let B = 20
    let temp = A
    A = B
    B = temp

    return `Novo valor da variável A e B respectivamente é: ${A} e ${B}`
}

//console.log(swapNumbers())
```

<hr>

7. Desenvolva um algoritmo para ler o número total de eleitores de um
município, o número de votos brancos, nulos e válidos. Calcular e
escrever o percentual que cada um representa em relação ao total
de eleitores.
<br>

```
function percentOfVoters(votingDistrict, blankVotes, nullVotes,validVotes ){

    let percentBlankVotes = (blankVotes * 100) / votingDistrict
    let percentNullVotes = (nullVotes * 100) / votingDistrict
    let percentValidVotes = ( validVotes * 100) / votingDistrict

    return `Os valores percentuais de Votos em branco, Voto nulo e Votos válidos em relação ao total de eleitores, 
respectivamente são:  ${percentBlankVotes}% -> Brancos, ${percentNullVotes}% -> 
Nulos e ${percentValidVotes}% -> Válidos`
}

//console.log(percentOfVoters(100000,1000,5400,93600))
```

<hr>

8. Desenvolva um algoritmo para ler dois valores e imprimir uma das
três mensagens a seguir:
a. ‘Números iguais’, caso os números sejam iguais;
b. ‘Primeiro é maior’, caso o primeiro seja maior que o segundo;
c. ‘Segundo maior’, caso o segundo seja maior que o primeiro.
<br>

```
function checkTwoNumbers(firstNumber, secondNumber){

    let message = ""

    if(firstNumber === secondNumber){
        message = "Números iguais"
    }else if (firstNumber > secondNumber){
        message = "Primeiro é maior"
    }else {
        message = "Segundo é maior"
    }

    return message
    
}

//console.log(checkTwoNumbers(60,50))
```

<hr>

9. As maçãs desta estação custam R$0,30 se forem compradas
menos do que uma dúzia, e R$0,25 se forem compradas pelo menos
doze. Desenvolva um algoritmo que leia o número de maçãs
compradas, calcule e escreva o valor total da compra.
<br>

```
function appleStore(qtyApples){

    let lessThanDozen = 0.30
    let oneDozen = 0.25
    let totalPurchase = 0

    if(qtyApples >= 12 ){
        totalPurchase = qtyApples * oneDozen
    }else{
        totalPurchase = qtyApples * lessThanDozen
    }

    return `O total da compra é R$ ${convertToBrl(totalPurchase)}`
}
//console.log(appleStore(12))
```

<hr>


10. Escreva um algoritmo que tenha como valores de entradas o nome
e idade do usuário e imprima no terminal o nome, a idade e o ano
de nascimento do usuário. Ex: “Nome: Pedro, Idade: 22 anos, nasceu
em 2000”.
OBS: Pegue o ano atual como base
<br>

```
function findYearOfBirth(age){
    let date = new Date()
    let currentYear = date.getFullYear()
    let yearOfBirth = currentYear - age

    return yearOfBirth
}

function personalInformation(userName, age){
    

    return `Nome: ${userName}, Idade: ${age} anos, nasceu em ${findYearOfBirth(age)}.`
    

}

//console.log(personalInformation("Lucas", 27))
```

<hr>

11. Crie um algoritmo que armazene um número inteiro positivo, e gere
um alerta com as seguintes mensagens:
a. “Número é par!”, se o valor armazenado for par;
b. “Número é impar!”, se o valor armazenado for ímpar;
<br>

```
function evenOrOdd(number){
    let arrayNumber = number.toString().split('')
    let isInteger = arrayNumber.includes(".")

    if(number < 0){
        return "O numero não é valido, favor digitar um número inteiro positivo"
    }else if (isInteger){
        return "O numero não é valido, favor digitar um número inteiro positivo"
    }

    if(number % 2 === 0){
        return `Número é par!`
    }else{
        return `Número é impar!`
    }
}

//console.log(evenOrOdd(99))
```

<hr>

12. Escreva um algoritmo que armazene o ano atual e o ano de
nascimento de uma pessoa. Escrever uma mensagem no console
que diga se ela poderá ou não votar este ano (não é necessário
considerar o mês em que a pessoa nasceu).
<br>

```
function verifyVoter(yearOfBirth){
    let date = new Date()
    let currentYear = date.getFullYear()

    let age = currentYear - yearOfBirth

    if(age >= 18){
        return `Você tem ${age} anos, O seu voto é obrigatório`
    }else if (age === 16 || age === 17){
        return `Você tem ${age} anos, Pode votar mas não é obrigatório`
    }else{
        return `Você tem ${age} anos, Você não pode votar este ano`
    }

}

//console.log(verifyVoter(1996))
```

<hr>


## Conclusão
Estes são apenas alguns exemplos básicos de JavaScript que podem ajudar a entender os conceitos básicos da linguagem. Para avançar na programação é importante estudar com mais profundidade, praticar e buscar referências de outros projetos e recursos na internet.
