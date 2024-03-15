# UNIFOR

**Nome**: Janderson Vieira Costa
**Disciplina**: Raciocínio Lógico Algoritmo

## Exercício 1
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Informe a primeira nota:}}
B --> C[\N1\]
C --> D{{Informe a segunda nota:}}
D --> E[\N2\]
E --> F{{Informe a terceira nota:}}
F --> G[\N3\]
G --> H{{Informe a quarta nota:}}
H --> I[\N4\]
I --> J[M = N1 + N2 + N3 + N4 / 4]
J --> K{{'A média é:', M}}
K --> L([Fim])
````
### Pseudocódigo
````
1 ALGORITMO calcular_média
2 DECLARE N1, N2, N3, N4, M: INTEIRO
3 INÍCIO
4 ESCREVA "Informe a primeira nota:"
5 LEIA N1
6 ESCREVA "Informe a segunda nota:"
7 LEIA N2
8 ESCREVA "Informe a terceira nota:"
9 LEIA N3
10 ESCREVA "Informe a quarta nota:"
11 LEIA N4
12 M = (N1 + N2 + N3 + N4) / 4
13 ESCREVA "A média é:", M
14 FIM
````

## Exercício 2
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Informe o valor em Celsius:}}
B --> C[\C\]
C --> D[F = 1.8 * C + 32]
D --> E{{'O resultado em Fahrenheit é:', F}}
E --> F([Fim])
````
### Pseudocódigo
````
1 ALGORITMO conversão_celsius_fahrenheit
2 DECLARE C, F: REAL
3 INÍCIO
4 ESCREVA "Informe o valor em Celsius:"
5 LEIA C
6 F = 1.8 * C + 32
7 ESCREVA "O resultado em Fahrenheit é:", F 
8 FIM
````

## Exercício 3
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Digite o primeiro número:}}
B --> C[\N1\]
C --> D{{Digite o segundo número:}}
D --> E[\N2\]
E --> F{{Digite um dos operadores +, -, *, /:}}
F --> G[\O\]
G --> H{O = '+'}
H --F--> I{O = '-'}
H --V--> J[R = N1 + N2]
I --F--> K{O = '*'}
I --V--> L[R = N1 - N2]
K --F--> M{O = '/'}
K --V--> N[R = N1 * N2]
M --F--> O{{Operador inválido}}
M --V--> P{N2 != 0}
P --F--> Q{{Não é possível efetuar a divisão}}
P --V--> R[R = N1 / N2]
Q --> S([Fim])
O --> S([Fim])
J --> T{{'O resultado da operação é:', R}}
L --> T{{'O resultado da operação é:', R}}
N --> T{{'O resultado da operação é:', R}}
R --> T{{'O resultado da operação é:', R}}
T --> S([Fim])
````
### Pseudocódigo
````
1 ALGORITMO calculadora_simples
2 DECLARE N1, N2, R: REAL; O: CARACTERE
3 INÍCIO
4 ESCREVA "Digite o primeiro número:"
5 LEIA N1
6 ESCREVA "Digite o segundo número:"
7 LEIA N2
8 ESCREVA "Digite um dos operadores (+, -, *, /):"
9 LEIA O
10 ESCOLHA
11 	CASO O = "+"
12 		[R = N1 + N2]
13 	CASO O = "-"
14 		[R = N1 - N2]
15 	CASO O = "*"
16 		[R = N1 * N2]
17 	CASO O = "/"
18 		SE N2 != 0 ENTÃO
19 			[R = N1 / N2]
20 		SENÃO
21 			ESCREVA "Não é possível efetuar a divisão"
22 		FIM_SE
23 	SENÃO
24 		ESCREVA "Operador inválido"
25 FIM_ESCOLHA
26 ESCREVA "O resultado da operação é:", R
27 FIM
````

## Exercício 4
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Informe a idade:}}
B --> C[\I\]
C --> D{I >= 5 <= 7}
D --F--> E{I >= 8 <= 10}
D --V--> F[C = Infantil A]
E --F--> G{I >= 11 <= 13}
E --V--> H[C = Infantil B]
G --F--> I{I >= 14 <= 17}
G --V--> J[C = Juvenil A]
I --F--> K[C = Adulto]
I --V--> L[C = Juvenil B]
K --> M([Fim])
F --> M
H --> M
J --> M
L --> M
````
### Pseudocódigo
````
1 ALGORITMO classificação_idade
2 DECLARE I: INTEIRO; C: CARACTERE
3 INÍCIO
4 ESCREVA "Informe a idade:"
5 LEIA I
6 ESCOLHA
7 	CASO I >= 5 <= 7
8 		C = Infantil A
9 	CASO I >= 8 <= 10
10 		C = Infantil B
11 	CASO I >= 11 <= 13
12 		C = Juvenil A
13 	CASO I >= 14 <= 17
14 		C = Juvenil B
15 	SENÃO
16 		C = Adulto
17 FIM_ESCOLHA
18 FIM
````
