# UNIFOR
**Nome:** Lucas Carreiro Gomes

**Disciplina:** Raciocínio Lógico Algorítmico

## Lista de exercícios 03

### Exercício 01

#### Pseudocódigo
```
1 ALGORITMO verifica_par_ímpar
2 DECLARE numero, resto: INTEIRO
3 ESCREVA "Digite um número:"
4 INÍCIO
4 LEIA número
5 SE numero >= 0 ENTÃO
6   resto = numero % 2
7   SE resto == 0 ENTÃO
8     ESCREVA "O número é par"
9   SENAO
10    ESCREVA "O número é ímpar"
11   FIM_SE
12 SENAO
13   ESCREVA "Digite um número positivo"
14   FIM_SE
15 FIM
```
#### Fluxograma
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite um número:}}
B --> C[\numero\]
C --> D{número >= 0}
D --FALSE--> E{{O número não é positivo}}
D --TRUE--> F[resto = número % 2]
E --> B
F --> G{resto == 0}
G --FALSE--> H{{O número é ímpar}}
G --TRUE--> I{{O número é par }}
H --> Z([FIM])
I --> Z([FIM])
```
#### Teste de mesa
| numero | numero >= 0 | resto | resto == 0 | Saída |
| -- | -- | -- | -- | -- |
| 7 | V | 1 | F | O número é ímpar |
| 18 | V | 0 | V | O número é par |
| -2 | F |  |  | O número não é positivo |
| 0 | V | 0 | V | O número é par |

### Exercício 03

#### Pseudocódigo
```
ALGORITMO
DECLARE N1, N2,... Nn: INTEIRO
INÍCIO
ESCREVA "Digite uma sequência de números inteiros"
LEIA N1... Nn
soma == N1 + N2 +... + Nn
ESCREVA "A soma da sequência é:", soma
FIM_ALGORITMO
```
#### Fluxograma
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite uma sequência de números inteiros:}}
B --> C[\numero inteiro\]
C --> D[soma == N1 + N2 +... + Nn]
D --> E{{"A soma da sequência é:", soma}}
E --> Z([FIM])
```
#### Teste de mesa
| N1 | N2 | Nn | soma | Saída |
| -- | -- | -- | -- | -- |
| 4 | 11 | -2 | 13 | A soma da sequência é: 13 |
| 0 | -7 | 19 | 12 | A soma da sequência é: 12 |

### Exercício 04

#### Pseudocódigo
```
