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
4 ESCREVA "Informe suas notas" 
5 LEIA N1, N2, N3, N4
6 M = (N1 + N2 + N3 + N4) / 4
7 ESCREVA "A média é:", M
8 FIM
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
