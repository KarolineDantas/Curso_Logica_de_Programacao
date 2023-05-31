# Utilizando atribuições
```Algoritmo "MeuNome"
var 
  nome: caractere
inicio
  Escreval("Digite seu nome: ")
  Leia(nome)
  Escreval("Muito prazer, " + nome)

FimAlgoritmo
```
**Execução no VisuAlg:**
![Captura de tela 2023-05-31 140046](https://github.com/KarolineDantas/Curso_Logica_de_Programacao/assets/107884724/5aff5268-a72c-4fad-9e07-13cd8ae56aa1)



### Para praticar
1) Solicitar dois números para o usuaário e mostrar a soma entre eles

``` 
Algoritmo "Pratica1"

var 
  n1, n2, soma: inteiro
inicio
  Escreval("Digite o primeiro número: ")
  Leia(n1)
  Escreval("Digite o segundo número: ")
  Leia(n2)
  
  soma <- n1 + n2
  
  Escreval("A soma de " + n1 + " mais " + n2 + " é igual a " + soma)
  ```
