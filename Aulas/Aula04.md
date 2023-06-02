## Operadores Relacionais
1) maior que >
2) menor que <
3) maior ou igual a >=
4) menor ou igual a <=
5) igual a =
6) diferente de <>

## Operadores Lógicos
1) E
2) OU
3) NÃO


## Exercícios práticos
**1) Comparar valores numéricos**
```
Algoritmo "Pratica1"

Var

 A, B, C: Inteiro

Inicio
 A <- 2
 B <- 3
 C <- 5
 
 Escreval(A>B)

Fimalgoritmo
```

**2) Comparar valores numéricos utilizando operadores lógicos**
```
Algoritmo "Pratica2"

Var

 A, B, C: Inteiro

Inicio
 A <- 2
 B <- 3
 C <- 5
 
 Escreval((A=B) OU (C>A))

Fimalgoritmo
```

**3) Verificando se um triângulo é equilátero ou escaleno**

Lembrando que um triângulo é escaleno quando todos os lados possuem medidas diferentes; 
ou equilátero, quando todos os lados são iguais.

```
Algoritmo "triangulos"

Var
  L1, L2, L3: Real
  EQ, ES: Logico

Inicio
  Escreval("Digite o primeiro lado:")
  Leia(L1)
  Escreval("Digite o segundo lado:")
  Leia(L2)
  Escreval("Digite o terceiro lado:")
  Leia(L3)
  
  EQ <- (L1 = L2) e (L2 = L3)
  ES <- (L1 <> L2) e (L2 <> L3) e (L1 <> L3)
  
  Escreval("O triângulo é equiláterio?", EQ)
  Escreval("O triângulo é escaleno?", ES)
Fimalgoritmo
```
