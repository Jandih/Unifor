# UNIFOR

**Nome**: Janderson Vieira Costa
**Disciplina**: Raciocínio Lógico Algoritmo


## Exercício 1
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Digite um número:}}
B --> C[\N\]
C --> D{N < 0}
D --F--> G[R = N % 2]
G --> H{R == 0}
H --SIM--> I{{O número é par}}
H --NÃO--> J{{O número é ímpar}}
J --> K([Fim])
I --> K
D --V--> E{{'Número ', N}}
E --> F[N =+ 1]
F --LOOP--> D
````
### Pseudocódigo
````
1 ALGORITMO par_ímpar
2 DECLARE N, R: INTEIRO
3 INÍCIO
4 ESCREVA "Digite um número:"
5 LEIA N
6 ENQUANTO N < 0 FAÇA
7 	ESCREVA "Número", N
8 	N = N + 1
9 FIM_ENQUANTO
10 R = N % 2
11 SE R == 0 ENTÃO
12 	ESCREVA "O número é par"
13 SENÃO
14  ESCREVA "O número é ímpar"
15 FIM_SE
16 FIM
````

## Exercício 2
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Digite um número:}}
B --> C[\N\]
C --> D[[i = 0 ATÉ N PASSO 3]]
D --> F([Fim])
D --> E{{'Contagem:', i}}
E --LOOP--> D
````
### Pseudocódigo
````
1 ALGORITMO contagem
2 DECLARE N, i: INTEIRO
3 INÍCIO
4 ESCREVA "Digite um número:"
5 LEIA N
6 PARA i DE 0 ATÉ N PASSO 3 FAÇA
7 	ESCREVA "i"
8 FIM_PARA
9 FIM
````

## Exercício 3
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Digite seis números para a sequência:}}
B --> C[\N1, N2, N3, N4, N5, N6\]
C --> D[soma = 0]
D --> E[[i = N1 ATÉ N6]]
E --> G{{'A soma da sequência é:', soma}}
E --> F[soma =+ i]
G --> H([Fim])
F --LOOP--> E
````
### Pseudocódigo
````
1 ALGORITMO calculadora_simples
2 DECLARE N1, N2, N3, N4, N5, N6, soma, i: INTEIRO
3 INÍCIO
4 ESCREVA "Digite seis números para a sequência:"
5 LEIA N1, N2, N3, N4, N5, N6
6 soma = 0
7 PARA i DE N1 ATÉ N6 FAÇA
8 soma = soma + i
9 FIM_PARA
10 ESCREVA "A soma da sequência é:", soma
11 FIM
````

## Exercício 4
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Insira sua nota:}}
B --> C[\N\]
C --> D{N >= 0}
D --F--> H[M = T / Q]
H --> I{{'Foram lidas', Q, 'notas. A média aritmética é', M}}
I --> J([Fim])
D --V--> F[\Q\]
F --> G[T = N1 + N2 + N3 ...]
G --LOOP--> D
````
### Pseudocódigo
````
1 ALGORITMO notas
2 DECLARE Q: INTEIRO, N, T, M: REAL
3 INÍCIO
4 ESCREVA "Insira sua nota:"
5 LEIA N
6 ENQUANTO N >= 0 FAÇA
7 	LEIA Q
8 	T = N1 + N2 + N3 ...
9 FIM_ENQUANTO
10 M = T / Q
11 ESCREVA "Foram lidas", Q, "notas. A média aritmética é", M
12 FIM
````

