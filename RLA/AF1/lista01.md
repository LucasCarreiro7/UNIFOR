# UNIFOR
**Nome:** Lucas Carreiro Gomes

**Disciplina:** Raciocínio Lógico Algorítmico

## Lista de exercícios 01

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
E --LOOP--> B
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


### Exercício 02

#### Pseudocódigo
```
ALGORITMO
DECLARE S, NS NUMÉRICO
INÍCIO
ESCREVA “Digite o salário atual”
LEIA S
ENQUANTO
   S < 0
   ESCREVA "Digite um número positivo"
FIM_ENQUANTO
SE S ≤ 500
   NS ← S + 0.2 * S
   ESCREVA “Novo salário =”, NS
SENÃO
   NS ← S + 0.1 * S
   ESCREVA “Novo salário =”, NS
FIM_ALGORITMO
```
#### Fluxograma
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite o salário atual}}
B --> C[\numero\]
C --> C2{S < 0}
C2 --FALSE--> D{S <= 500}
C2 --TRUE--> C3{{Digite um número positivo}}
C3 --> C4[\numero\]
C4 --> B
D --FALSE--> E[NS == S + 0.1 * S]
D --TRUE--> F[NS == S + 0.2 * S]
E --> G{{Novo salário =, NS}}
G --> Z([FIM])
F --> H{{Novo salário =, NS}}
H --> Z
```
#### Teste de mesa
| salário | S < 0 | S <= 500 | NS | Saída |
| -- | -- | -- | -- | -- |
| 700 | F | F | 770 | Novo salário = 770 |
| 400 | F | V | 480 | Novo salário = 480 |
| -300 | V |  |  | Digite um número positivo |

### Exercício 03

#### Pseudocódigo
```
ALGORITMO
DECLARE N1, N2, média: real e positivo
INÍCIO
ESCREVA "Digite suas duas notas"
LEIA N1, N2
ENQUANTO
   N1 OU N2 < 0
   ESCREVA "Digite dois números positivos"
FIM_ENQUANTO
M == (N1 + N2) / 2
SE M >= 6
   ESCREVA "Aluno aprovado"
SENAO
   ESCREVA "Aluno reprovado"
FIM_ALGORITMO
```
#### Fluxograma
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite suas duas notas}}
B --> C[\numero\]
C --> C2{N1 OU N2 < 0}
C2 --FALSE--> D["M == (N1 + N2) / 2"]
C2 --TRUE--> C3{{Digite dois números positivos}}
C3 --> C4[\numero\]
C4 --> B
D --> E{M >= 6}
E --FALSE--> F{{Aluno reprovado}}
E --TRUE--> G{{Aluno aprovado}}
F --> Z([FIM])
G --> Z
```
#### Teste de mesa
| N1 | N2 | N1 OU N2 < 0 | M | M >= 6 | Saída |
| -- | -- | -- | -- | -- | -- |
| 8 | 9 | F | 8,5 | V | Aluno aprovado |
| 4 | 5 | F | 4,6 | F | Aluno reprovado |
| 8 | 3 | F | 5,5 | F | Aluno reprovado |
| -1 | 8 | V |  |  | Digite dois números positivos |

### Exercício 04

#### Pseudocódigo
```
ALGORITMO
DECLARE I, X: INTEIRO E POSITIVO
ESCREVA “Digite sua idade”
LEIA I
ENQUANTO
   I < 0
   ESCREVA "Digite um número positivo"
FIM_ENQUANTO
SE I ≥ 18
   ENTÃO ESCREVA “Candidato pode tirar a CNH”
SENÃO
   18 – I = X
   ESCREVA “Candidato não pode tirar a CNH. Tempo restante em anos:”, X
FIM_ALGORITMO
```
#### Fluxograma
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite sua idade}}
B --> C[\numero\]
C --> C2{I < 0}
C2 --FALSE--> D[I >= 18]
C2 --TRUE--> C3{{Digite um número positivo}}
C3 --> C4[\numero\]
C4 --> B
D --FALSE--> E[X == 18 - I]
E --> F{{Candidato não pode tirar a CNH. Tempo restante em anos:, X}}
D --TRUE-->G{{Candidato pode tirar a CNH}}
F --> Z([FIM])
G --> Z
```
#### Teste de mesa
| I | I < 0 | I >= 18 | X | Saída |
| -- | -- | -- | -- | -- |
| 18 | F | V |  | Candidato pode tirar a CNH |
| 20 | F | V |  | Candidato pode tirar a CNH |
| 16 | F | F | 2 | Candidato não pode tirar a CNH. Tempo restante em anos: 2 |
| -4 | V |  |  | Digite um número positivo |
