# UNIFOR

**Nome**: Janderson Vieira Costa
**Disciplina**: Raciocínio Lógico Algoritmo

## Exercício 1
### Fluxograma
````mermaid
flowchart TD
A([Início]) --> B{{Informe suas notas:}}
B --> C[/N1, N2, N3, N4/]
C --> D[M = N1 + N2 + N3 + N4 / 4]
D --> E{{A média é:, M}}
E --> F([Fim])
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
