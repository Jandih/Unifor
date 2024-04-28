# UNIFOR

**Nome**: Janderson Vieira Costa
**Disciplina**: Raciocínio Lógico Algoritmo

## Exercício 1
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Digite um número para a variável a:}}
B --> C[\a\]
C --> D[aux = a]
D --> E{{Digite um número para a variável b:}}
E --> F[\b\]
F --> G[a = b]
G --> H[b = aux]
H --> I{{'Novo valor de a:', a. 'Novo valor de b:', b}}
I --> J([Fim])
````
### Pseudocódigo
````
1 ALGORITMO troca_dos_valores
2 DECLARE a, b, aux: Real
3 INÍCIO
4 ESCREVA "Digite o primeiro número:" 
5 LEIA a
6 aux = a
7 ESCREVA "Digite um número para a variável b:"
8 LEIA b
9 a = b
10 b = aux
11 ESCREVA "Novo valor de a:", a. "Novo valor de b:", b
12 FIM
````
#### Teste de mesa

| a  | b  | aux | a  | b  | Saída 1 | Saída 2 | 
| -- | -- | --  | -- | -- | --      | --      | 
| 0  | 1  | 0   | 1  | 0  | a = 1   | b = 0   |

## Exercício 2
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Insira o número de alunos:}}
B --> C[\A\]
C --> D[cont = 0]
D --> J[N = 1]
J --> E{N <= A}
E --F--> H{{'Total de aprovados é:', cont}}
H --> I([Fim])
E --V--> F{{'Digite a nota do aluno:', N}}
F --> K[\N\]
K --> L{N >= 50 E N <= 100}
L --F--> M[N =+ 1]
L --V--> G[cont =+ 1]
M --LOOP--> E
G --> M
````
### Pseudocódigo
````
1 ALGORITMO contagem
2 DECLARE A, N, cont: INTEIRO
3 INÍCIO
4 ESCREVA "Insira o número de alunos:" 
5 LEIA A
6 cont = 0
7 N = 1
8 ENQUANTO N <= A FAÇA
9 	ESCREVA "Digite a nota do aluno:", N
10 	LEIA N
11 	SE N >= 50 E N <= 100 ENTÃO
12 		cont = cont + 1
13 	SENÃO
14 		N = N + 1
15 	FIM_SE
16 FIM_ENQUANTO
17 ESCREVA "Total de aprovados é:", cont
18 FIM
````
#### Teste de mesa 

| It | A  | N  | cont | N<=A  | nota, N | nota | nota_valida | cont+1 | N+1 | Saída        | 
| -- | -- | -- | --   | --    | --      | --   | --          | --     | --  | --           |
| 1  | 3  | 1  |  0   | V     | nota 1  | 60   | True        | 1      | 2   |              |
| 2  | 3  | 2  |  1   | V     | nota 2  | 40   | False       | 1      | 3   |              |
| 3  | 3  | 3  |  1   | V     | nota 3  | 90   | True        | 2      | 4   |              |
| 4  | 3  | 4  |  2   | F     |         |      |             |        |     | Aprovados: 2 |

## Exercício 3
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Insira a quantidade de números:}}
B --> C[\Q\]
C --> D{Q >= 0}
D --F--> E{{O valor deve ser >= 0}}
D --V--> Z[soma = 0]
Z --> X[i = 1]
X --> F{i <= Q}
F --F--> I{{'A soma dos números é:', soma}}
I --> J([Fim])
F --V--> Y{{Digite um número:}}
Y --> L[\N\]
L --> G[soma =+ N]
G --> H[i =+ 1]
H --LOOP--> F
E --> J
````
### Pseudocódigo
````
1 ALGORITMO soma_conjunto
2 DECLARE N, Q, soma, i: INTEIRO
3 INÍCIO
4 ESCREVA "Insira a quantidade de números:" 
5 LEIA Q
6 SE Q >= 0 ENTÃO
7 	soma = 0
8 	i = 1
9 	ENQUANTO i <= Q FAÇA
10 		ESCREVA "Digite um número:"
11 		LEIA N
12 		soma = soma + N
13 		i = i + 1
14 	FIM_ENQUANTO
15 SENÃO
16 	ESCREVA "O valor deve ser >= 0"
17 FIM_SE
18 ESCREVA "A soma dos números é:", soma
19 FIM
````
#### Teste de mesa

| It | Q  | Q>=0   | soma | i  | i<=Q   | N   | soma =+ N    | Saída                   |
| -- | -- | --     | --   | -- | --     | --  | --           | --                      |
|    | -3 | F      |      |    |        |     |              | O valor deve ser ...    |
| 1  | 0  | V      | 0    | 1  | F      |     |              | A soma dos números é 0  |
| 1  | 3  | V      | 0    | 1  | V      | 5   | 0 + 5 = 5    |                         |
| 2  | 3  | V      | 5    | 2  | V      | 10  | 5 + 10 = 15  |                         |
| 3  | 3  | V      | 15   | 3  | V      | 20  | 15 + 20 = 35 |                         |
| 4  | 3  | V      | 35   | 4  | F      |     |              | A soma dos números é 35 |

## Exercício 4
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Digite o número de termos:}}
B --> C[\N\]
C --> D[S = 0]
D --> G[[i = 0 ATÉ N]]
G --> K{{'O valor de S é:', S}}
K --> M([Fim])
G --> H[numerador = i * 2 + 1]
H --> I[denominador = i * 2 + 2]
I --> J[t = numerador / denominador]
L --LOOP--> G
J --> L[S =+ t] 
````
### Pseudocódigo
````
1 ALGORITMO soma_serie
2 DECLARE N, numerador, denominador, i: INTEIRO; S, t: REAL
3 INÍCIO
4 ESCREVA "Digite o número de termos:" 
5 LEIA N
6 S = 0
7 PARA i DE 0 ATÉ N FAÇA
8 	numerador = (i * 2) + 1
9 	denominador = (i * 2) + 2
10 	t = numerador / denominador
11 	S =+ t
12 FIM_PARA 
13 ESCREVA "O valor de S é:", S
14 FIM
````
#### Teste de mesa (0.25 ponto)

| It | N  | S  | i | numerador | denominador | t     | S += t         | Saída                  |
| -- | -- | -- |-- | --        | --          | --    | --             | --                     |
|    | 0  | 0  |   |           |             |       |                |                        |
| 1  | 4  | 0  | 0 | 2*0+1 = 1 | 2*0+2 = 2   | 1/2   | 0+1/2 = 1/2    |                        |
| 2  | 4  | 0  | 1 | 2*1+1 = 1 | 2*1+2 = 2   | 3/4   | 1/2+3/4 = 1.25 |                        |
| 3  | 4  | 0  | 2 | 2*2+1 = 1 | 2*2+2 = 2   | 5/6   | 0+1/2 = 2.08   |                        |
| 4  | 4  | 0  | 3 | 2*3+1 = 1 | 2*3+2 = 2   | 7/8   | 0+1/2 = 2.96   | O valor de S é 2.96    |

## Exercício 5
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Digite um número:}}
B --> C[\N\]
C --> D{N >= 0}
D --F--> F{{O número é negativo}}
D --V--> E[R = 1]
E --> G[[i = 1 ATÉ N]]
G --> K{{'O fatorial de', N, 'é:', R}}
K --> M([Fim])
G --> H[R =* i]
H --LOOP--> G
F --> M
````
### Pseudocódigo
````
1 ALGORITMO fatorial
2 DECLARE N, R, i: INTEIRO
3 INÍCIO
4 ESCREVA "Digite um número:" 
5 LEIA N
6 SE N >= 0 ENTÃO
7 	R = 1
8 	PARA i DE 1 ATÉ N FAÇA
9 		R = R * i
10 	FIM_PARA
11 SENÃO
12 	ESCREVA "O número é negativo"
13 FIM_SE
14 ESCREVA "O fatorial de", N, "é:", R
15 FIM
````
#### Teste de mesa

| N  | R | i | fator = fator * i | Saída               |
| -- | --| --| --                | --                  |
| 3  | 1 | 1 | 1 * 1 = 1         |                     |
| 3  | 1 | 2 | 1 * 2 = 2         |                     |
| 3  | 2 | 3 | 2 * 3 = 6         | O fatorial de 3 é 6 |

## Exercício 6
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Digite o número de termos:}}
B --> C[\N\]
C --> F{N >= 1}
F --F--> H{{O número é < 1}}
F --V--> G[a = 0]
G --> D[b = 1]
D --> Z[[i = 1 ATÉ N]]
Z --> X{{'Os primeiros', N, 'termos da sequência de Fibonacci são:', t}}
X --> Y([Fim])
Z --> E{{a}}
E --> I[t = a + b]
I --> J[a = b]
J --> K[b = t]
K --LOOP--> Z
H --> Y
````
### Pseudocódigo
````
1 ALGORITMO sequência_de_fibonaccivalor_da_série
2 DECLARE N, a, b, t, i: INTEIRO
3 INÍCIO
4 ESCREVA "Digite o número de termos:" 
5 LEIA N
6 SE N >= 1 ENTÃO
7 	a = 0
8 	b = 1
9 	PARA i DE 1 ATÉ N FAÇA
10 		ESCREVA "a "
12 		t = a + b
13 		a = b
14 		b = t
15 	FIM_PARA
16 SENÃO
17 	ESCREVA "O número é < 1"
18 FIM_SE
19 ESCREVA "Os primeiros", N, "termos da sequência de Fibonacci são:", t
20 FIM
````
#### Teste de mesa

| It | N  | a  | b  | i  | Saída | t=a+b           | a=b   | b=t             |
| -- | -- | -- | -- | -- | --    | --              | --    | --              |
| 1  | 5  | 0  | 1  | 1  | 0     | 0+1=1           | 1     | 1               |
| 2  | 5  | 1  | 1  | 2  | 1     | 1+1=2           | 1     | 2               |
| 3  | 5  | 1  | 2  | 3  | 1     | 1+2=3           | 2     | 3               |
| 4  | 5  | 2  | 3  | 4  | 2     | 2+3=5           | 3     | 5               |
| 4  | 5  | 3  | 5  | 5  | 3     | 3+5=8           | 5     | 8  
|    |    |    |    |    |Os primeiros 5 termos da sequência de Fibonacci são: 0, 1, 1, 2, 3                                      

## Exercício 7
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Digite um número:}}
B --> C[\N\]
C --> F{N >= 0}
F --F--> H{{O número deve ser positivo}}
F --V--> G[I = 0]
G --> D{N > 0}
D --F--> X{{'Número invertido:', i}}
X --> Y([Fim])
D --V--> E[D = N % 10]
E --> I[I =* 10 + D]
I --> J[N = N // 10]
J --LOOP--> D
H --> Y
````
### Pseudocódigo
````
1 ALGORITMO inversão
2 DECLARE N, I, D: INTEIRO
3 INÍCIO
4 ESCREVA "Digite um número:" 
5 LEIA N
6 SE N >= 0 ENTÃO
7 	i = 0
8 	ENQUANTO N > 0 FAÇA
9 		D = N % 10
10 		I = (I * 10) + D
12 		N = N // 10
13 	FIM_PARA
14 SENÃO
15 	ESCREVA "O número deve ser positivo"
16 FIM_SE
17 ESCREVA "Número invertido:", i
18 FIM
````
#### Teste de mesa

| It | N   | I       | N > 0 | D       | N = N // 10     | I = (I * 10) + D                  | Saída                       |
| -- | --  | --      | --    | --      | --              | --                                | --                          |
|    | -1  | 0       | F     |         |                 |                                   | O número deve ser positivo! |
| 1  | 0   | 0       | F     |         |                 |                                   | Número invertido:: 0        |
| 1  | 42  | 0       | V     | 2       | 4               | 2                                 |                             |
| 2  | 4   | 2       | V     | 4       | 0               | 24                                |                             |
| 3  | 0   | 24      | F     |         |                 |                                   | Número invertido:: 24       |

