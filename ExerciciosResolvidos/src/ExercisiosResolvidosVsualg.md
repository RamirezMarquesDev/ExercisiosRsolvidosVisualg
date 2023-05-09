#Exercisíos Resolvidos VisualG 1
--------------------------------------------------

##### Ramirez Marques
#### **Parte 1: Enquanto**
--------------------------------------------------
**01 - Leia uma quantidade indeterminada de duplas de valores inteiros X e** **Y.**
**Escreva para cada X e Y uma mensagem que indique se estes valores foram**
**digitados em ordem crescente ou decrescente. O programa deve finalizar** **quando**
**forem digitados dois valores iguais.**

```1.Parte 1: Enquanto
algoritmo "Condicional_enqunto1"
var
   x, y : inteiro
inicio
      escreva ("Digite 2 numeros Inteiros: ")
      leia (x)
      leia (y)
      enquanto (x<>y)faca
          se x < y entao
            escreval ("Cresente!")
         senao
            escreval ("decrescente!")
         fimse
      escreva ("Digite 2 numeros Inteiros: ")
      leia (x)
      leia (y)
      fimenquanto
      escreva ("Os valores iguais!")
fimalgoritmo
```
**02 - Faça um programa para ler um número indeterminado de dados, contendo** **cada**
**um, a idade de um indivíduo. O último dado, que não entrará nos** **cálculos, contém**
**um valor de idade negativa. Calcular e imprimir a idade média deste grupo** **de**
**indivíduos. Se for entrado um valor negativo na primeira vez, mostrar a** **mensagem**
**"IMPOSSIVEL CALCULAR".**

```2. Parte 1: Enquanto

algoritmo "condicional_enquanto2"
var
   idade,soma,qtd: inteiro
   media: real
inicio
      escreval ("Digite as idades: ")
      leia (idade)
      soma <- 0
      qtd <- 0
      enquanto (idade >= 0) faca
           soma <- soma + idade
           qtd <- qtd + 1
           leia (idade)
           fimenquanto
           se qtd = 0 entao
             escreval ("Idade Inválida!")
             senao
                media <- soma / qtd
                escreval ("Média = ", media)
           fimse

fimalgoritmo
```
**03 - Escreva um programa que repita a leitura de uma senha até que ela** **seja válida.**
**Para cada leitura densenha incorreta informada, escrever a mensagem** **"Senha**
**Inválida! Tente novamente:". Quando a senha for informada corretamente** **deve ser**
**impressa a mensagem "Acesso Permitido" e o algoritmo encerrado. Considere** **que**
**a senha correta é o valor 2002.**

```3. Parte 1: Enquanto

algoritmo "condicional_enquanto3"
var
   senha: inteiro
inicio
      escreval ("Digite sua Senha de Quatro Digitos: ")
      leia (senha)
      enquanto senha <> 2002 faca
              escreval ("Senha Inválida!")
              escreval ("Digite sua Senha: ")
              leia (senha)
      fimenquanto
      se senha = 2002 entao
         escreval ("Acesso Permitido!")
      fimse
fimalgoritmo
```
**04 - Escreva um programa para ler as coordenadas (X,Y) de uma quantidade**
**indeterminada de pontos no sistema cartesiano. Para cada ponto escrever o**
**quadrante a que ele pertence (Q1, Q2, Q3 ou Q4). O algoritmo será** **encerrado**
**quando pelo menos uma de duas coordenadas for NULA (nesta situação sem**
**escrever mensagem alguma).**

```4. Parte 1: Enquanto

algoritmo "condicional_enquanto4"
var
   x,y: inteiro
inicio
      escreval ("Informe 2 cordenadas de um Plano Cartesiano: ")
      leia (x)
      leia (y)
      enquanto (x <> 0) e (y <> 0 ) faca
              se (x > 0) e (y > 0) entao
                escreval ("Quadrante 1!")
                senao
                  se (x < 0) e (y > 0) entao
                    escreval ("Quadrante 2")
                    senao
                      se (x < 0) e (y < 0) entao
                        escreval ("Quadrante 3")
                        senao
                          escreval ("Quadrante 4")
                      fimse
                  fimse
              fimse
      escreval ("Informe 2 cordenadas de um Plano Cartesiano: ")
      leia (x)
      leia (y)
      fimenquanto
fimalgoritmo
```
**05 - Faça um programa que leia as notas referentes às duas avaliações de** **um**
**aluno. Calcule e imprima a média semestral. Faça com que o algoritmo só** **aceite**
**notas válidas (uma nota válida deve pertencer ao intervalo [0,10]). Cada** **nota deve**
**ser validada separadamente.**

```5. Parte 1: Enquanto

algoritmo "condicional_enquanto5"
var
   n1,n2, media: real
inicio
      escreval ("Informe a Primeira Nota: ")
      leia (n1)
      enquanto (n1 < 0) ou (n1 > 10) faca
        escreval ("Valor da N1 Inválido! Digite Novamente: ")
        leia (n1)
      fimenquanto
      escreval ("Informe a Segunda Nota: ")
      leia (n2)
      enquanto (n2 < 0) ou (n2 > 10) faca
        escreval ("Valor da N2 Inválido! Digite Novamente: ")
        leia (n2)
      fimenquanto
      media <- ((n1 + n2)/2)
      escreval ("Média do Aluno: ",media)
fimalgoritmo
```
**06 - Um posto de combustíveis deseja determinar qual de seus produtos** **tem a**
**preferência de seus clientes. Escreva um algoritmo para ler o tipo de** **combustível**
**abastecido (codificado da seguinte forma: 1. Álcool 2. Gasolina 3.** **Diesel 4. Fim).**
**Caso o usuário informe um código inválido (fora da faixa de 1 a 4) deve** **ser solicitado**
**um novo código (até que seja válido). O programa será encerrado quando** **o código**
**informado for o número 4, devendo então mostrar a mensagem "MUITO**
**OBRIGADO", bem como as quantidades de cada combustível.**

```6. Parte 1: Enquanto

algoritmo "condicional_enquanto6"
var
   alcool,gasolina,diesel,codigo: inteiro
inicio
      alcool <- 0
      gasolina <- 0
      diesel <- 0
      escreval ("Informe o Código do combustível: ")
      leia (codigo)
      enquanto (codigo < 1) ou (codigo > 4) faca
          escreval ("Código Inválido! Favor Digíte Novamente: ")
          leia (codigo)
      fimenquanto
      enquanto (codigo >= 1) e (codigo <= 3) faca
               se (codigo = 1) entao
                  alcool <- alcool + 1
                 senao
                   se (codigo = 2) entao
                      gasolina <- gasolina + 1
                     senao
                       se (codigo = 3) entao
                          diesel <- diesel + 1
                       fimse
                   fimse
                       fimse
      escreval ("Informe o Código do combustível: ")
      leia (codigo)
      fimenquanto
      escreval ("MUITO OBRIGADO!")
      escreval ("Alcool: ", alcool)
      escreval ("Gasolina: ", gasolina)
      escreval ("Diesel: ", Diesel)
fimalgoritmo
                   
```

**07 - O programa deve ler um valor inteiro X indefinidas vezes. (O** **programa irá parar**
**quando o valor de X for igual a 0). Para cada X lido, imprima a soma dos** **5 pares**
**consecutivos a partir de X, inclusive o X, se for par. Se o valor de** **entrada for 4, por**
**exemplo, a saída deve ser 40, que é o resultado da operação:** **4+6+8+10+12,**
**enquanto que se o valor de entrada for 11, por exemplo, a saída deve ser** **80, que é**
**a soma de 12+14+16+18+20.**

```7 parte 1: Enquanto

algoritmo "exercicio_enquanto7"
var
   x, soma: inteiro

inicio
   escreval ("Digite um numero inteiro: ")
   leia (x)
   enquanto x<>0 faca
      se x%2 = 0 entao
         soma <- x * 5 + 20
      senao
         soma <- (x+1)*5 + 20
      fimse
      escreval ("SOMA = ", soma)
      escreval("Digite um número inteiro: ")
      leia (x)
   fimenquanto
fimalgoritmo
```