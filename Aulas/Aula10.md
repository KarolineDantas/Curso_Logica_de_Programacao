## Estrutura de repetição II
```
Repita
  Bloco
Ate expressao  
``` 
Qual a diferença desse comando para o Enquanto?
- Enquanto fulano *não arrumar o quarto*, não poderá sair para brincar. Somente após arruamr o quarto estará liberado.
- Já na estrutura Repita a lógica é diferente: o fulano ficará de castigo *até arrumar o quarto*.

Ou seja, a expressão a ser validada é *arrumar o quarto*. No Enquanto essa validação aparece no início,
já no Repita a expressão aparece apenas no fim.

Exemplo: o código irá somar os valores digitados pelo usuário.

```
algoritmo "Exemplo"

var
  num, soma: Inteiro
  resposta: Caractere
  
inicio
  soma <- 0
  
  Repita
    Escreval("Digite o valor que deseja somar => ") 
    Leia(num)
    Escreval("Deseja inserir mais um número na soma? [S/N] ")
    Leia(resposta)
  Até (resposta = "N")  
  
  Escreval("A soma de todos os valores é igual a", soma)
fimalgoritmo
```

## Exercícios práticos
**1) Contar de 1 até 10**
```
algoritmo "Prática 1"

var
  contador: Inteiro 
  
inicio
  
 contador <- 1

  Repita
    Escreval(contador, "...")
    contador <- contador + 1
    Até(contador > 10)
    
fimalgoritmo
```

**1.1) Contar de 1 até 10, e exibir a tabuada de um número qualquer**
```
algoritmo "Prática 1.1"

var
  contador, num, mult: Inteiro

inicio
  contador <- 1
  Escreval("Quer ver a tabuada de qual número?")
  Leia(num)

  Repita
    mult <- contador * num
    Escreval(contador, " x", num, " =", mult)
    contador <- contador + 1
    Até(contador > 10)
    
fimalgoritmo
```

**2) Quantos números são negativos?**
```
algoritmo "Prática 2"

var
  contador, num, totalNegativo: Inteiro

inicio
     Repita
      Escreval("Digite um número")
      Leia(num)
      Se (num < 0) entao
         totalNegativo <- totalNegativo + 1
      FimSe
      contador <- contador + 1
     Ate (contador > 3)
     
     Escreval("Foram encontrados",totalNegativo, " valores negativos." )
fimalgoritmo
```

**3) Calcular o fatorial de um número**
```
algoritmo "Prática 3"

var
  contador, num, fatorial: Inteiro

inicio
Escreva("Deseja ver o fatorial de qual número? ")
     Leia(num)
     contador <- num
     fatorial <- 1

     Repita
      fatorial <- fatorial * contador
      contador <- contador - 1
     Ate (contador < 1)

     Escreval("O fatorial do número",num, " é:", fatorial)
fimalgoritmo
```

**3.1) Calcular o fatorial de um número digitado pelo usuário quantas vezes ele quiser**
```
algoritmo "Prática 3.1"

var
    contador, num, fatorial: Inteiro
    resposta: Caractere

inicio

Repita
     Escreva("Digite um número: ")
     Leia(num)
     contador <- num
     fatorial <- 1

      Repita
        Fatorial <- fatorial * contador
        contador <- contador - 1
      Ate (contador < 1)
      Escreval("O fatorial do número",num, " é:", fatorial)
      Escreval("Deseja ver o fatorial de outro número? [S/N]")
      Leia(resposta)
      LimpaTela
  Ate(resposta = "N")

     
fimalgoritmo
```

**4) É um número primo?**
```
  algoritmo "Prática4"
  
  var
   contador, num, contDiv: inteiro
  
  inicio
     Escreval("Digite um número: ")
        Leia(num)
        contador <- 1


       Repita
        Se (num % contador = 0) entao
          contDiv <- contDiv + 1
        FimSe
        contador <- contador + 1
       Ate(contador > num)

       Escreval("Tem se ao todo", contDiv, " números divisiveis por", num)

       Se(contDiv = 2) entao
        Escreva(num, " é um número primo, pois possui apenas dois números divisíveis!")
       Senao
        Escreva(num, " não é um número primo, pois possui mais de dois números divisíveis!")
       FimSe

  fimalgoritmo
```

**5) Super contador**
```
algotirmo "Prática 5"

var
 resp, contador: Inteiro

inicio
  Escreval("===============")
    Escreval("|   M E N U   |")
    Escreval("===============")
    Escreval("|Digite 1 para contar de 1 a 10|")
    Escreval("|Digite 2 para contar de 10 a 1|")
    Escreval("|Digite 3 para sair|")
    Escreval("===============")
    Leia(resp)
    
    // usando o caso
    Escolha(resp)
     Caso1
      contador <- 1
      Repita
        Escreva(contador,"...")
        contador <- contador + 1
      Ate(contador > 10)
      
     Caso2
      contador <- 10
      Repita
        Escreva(contador,"...")
        contador <- contador - 1
      Ate(contador < 1)
      
     Caso3
      Escreva("Saindo....")
    FimEscolha
    
    // usando o se
    Se(resp = 1) entao
      contador <- 1
      Repita
        Escreva(contador,"...")
        contador <- contador + 1
      Ate(contador > 10)
    Senao
     Se(resp = 2) entao
      contador <- 10
      Repita
        Escreva(contador,"...")
        contador <- contador - 1
      Ate(contador < 1)
      Senao
       Escreva("Saindo....")
      FimSe
    FimSe
    
  fimalgoritmo  
```

**6) Escolhendo pessoas**
```
algotirmo "Prática 6"

var
 sexo, resp: Caractere
 cabelo, idade, homens, mulheres: Inteiro

inicio

// ESCOLHER homens maiores de 18 com cabelo castanho
// ESCOLHER mulheres entre 25 e 30 que sejam loiras

   Repita
    Escreval("==================")
    Escreval("SELETOR DE PESSOAS")
    Escreval("==================")
    Escreval("Qual o sexo? [M/F] ")
    Leia(sexo)
    Escreval("Qual a idade? ")
    Leia(idade)
    Escreval("Qual a cor do cabelo? ")
    Escreval("--------------------- ")
    Escreval("[1] Preto")
    Escreval("[2] Castanho")
    Escreval("[3] Loiro")
    Escreval("[4] Ruivo")
    Leia(cabelo)

      Se(sexo = "M") e (idade > 18) e (cabelo = 2) entao
        homens <- homens + 1
      FimSe

      Se(sexo = "F") e (idade >= 25) e (idade <= 30) e (cabelo = 3) entao
        mulheres <- mulheres + 1
      FimSe
      
    Escreval("Quer continuar? [S/N] ")
    Leia(resp)
    LimpaTela
   Ate(resp = "N")
   
   
   Escreval("---------------------------------------")
   Escreval("RESULTADO FINAL")
   Escreval("---------------------------------------")
   Escreval("Total de homens com mais de 18 anos e cabelos castanhos:", homens)
   Escreval("Total de mulheres entre 25 e 30 anos e cabelos loiros:", mulheres)
fimalgoritmo  
```
