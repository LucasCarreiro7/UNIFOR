# UNIFOR
**Nome:** Lucas Carreiro

**Disciplina**: Raciocínio Lógico Algorítmico

## Exercício 03
### Fluxograma
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite um número:}}
B --> C[\número\]
C --> D{número > 0}
D --NÃO--> F[O número não é positivo]
D --SIM--> E[resto = número % 2]
F --> Z([FIM])
E --> G{resto == 0}
G --NÃO--> H{{O número é ímpar!}}
G --SIM--> I{{O número é par!!}}
H --> Z
I --> Z
```
### Pseudocódigo
```
1 ALGORITMO verifica_par_ímpar
2 DECLARE número, resto: INTEIRO
3 ESCREVA "Digite um número:"
INÍCIO
4 LEIA número
5 SE número > 0 ENTÃO
6		resto = número % 2
7		SE resto = 0 ENTÃO
8			ESCREVA "O número é par!"
9		SENÃO
10			ESCREVA "O número é ímpar!"
11 SENÃO 
12		ESCREVA "O número não é positivo!"
13 FIM_ALGORITMO
```
