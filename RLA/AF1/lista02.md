# UNIFOR
**Nome:** Lucas Carreiro Gomes

**Disciplina:** Raciocínio Lógico Algorítmico

## Lista de exercícios 02

### Exercício 01

#### Pseudocódigo
```
ALGORITMO
DECLARE N1, N2, N3, N4: inteiro
INÍCIO
ESCREVA “Digite quatro números inteiros”
LEIA N1, N2, N3, N4
M == (N1 + N2 + N3 + N4) / 4
ESCREVA “A média é igual a:”, M
FIM_ALGORITMO
```
#### Fluxograma
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite quatro números inteiros}}
B --> C[\numero\]
C --> D["M == (N1 + N2 + N3 + N4) / 4"]
D --> E{{A média é igual a:, M}}
E --> Z([FIM])
```
#### Teste de mesa
| N1 | N2 | N3 | N4 | M | Saída |
| -- | -- | -- | -- | -- | -- |
| 7 | 10 | 11 | 18 | 11,5 | A média é igual a: 11,5 |
| 0 | 0 | 0 | 0 | 0 | A média é igual a: 0 |
| -2 | -4 | -7 | -10 | -5,75 | A média é igual a: 5,75 |

### Exercício 02

#### Pseudocódigo
```
ALGORITMO
DECLARE C, F: real
INÍCIO
ESCREVA “Digite a temperatura em Celsius”
LEIA C
F == (9 / 5) * C + 32
ESCREVA “A temperatura em Fahrenheit é:”, F
FIM_ALGORITMO
```
#### Fluxograma
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite a temperatura em Celsius}}
B --> C[\numero\]
C --> D["F == (9 / 5) * C + 32"]
D --> E{{A temperatura em Fahrenheit é:, F}}
E --> Z([FIM])
```
#### Teste de mesa
| C | F | Saída |
| -- | -- | -- |
| 25 | 77 | A temperatura em Fahrenheit é: 77 |
| 0 | 32 | A temperatura em Fahrenheit é: 32 |
| -10 | 14 | A temperatura em Fahrenheit é: 14 |

### Exercício 03

#### Pseudocódigo
```
ALGORITMO
DECLARE N1,N2: REAL, operador: CARACTERE
INÍCIO
ESCREVA "Digite dois números e um operador"
LEIA N1, N2, operador
ESCOLHA
   CASO operador == 'soma'
     S = N1 + N2
     ESCREVA "O resultado é:", S
   CASO operador == 'subtração'
     SUB = N1 - N2
     ESCREVA "O resultado é:", SUB
   CASO operador == 'multiplicação
     M = N1 * N2
     ESCREVA "O resultado é:", M
   CASO operador == "divisão"
     D = N1 / N2
       SE N2 = 0
         ESCREVA "É impossível dividir por 0"
       SENAO
         ESCREVA "O resultado é:", D
FIM_ESCOLHA
FIM_ALGORITMO
```
#### Fluxograma
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite dois números e um operador}}
B --> C[\numero, operador\]
C --> D{operador == 'soma'}
D --> E[S == N1 + N2]
E --> F{{'O resultado é:', S}}
F --> Z([FIM])
C --> G{operador == 'subtração'}
G --> H[SUB == N1 - N2]
H --> I{{'O resultado é:' SUB}}
I --> Z
C --> J{operador == 'multiplicação'}
J --> K[M == N1 * N2]
K --> L{{'O resultado é:', M}}
L --> Z
C --> M{operador == 'divisão'}
M --> N[D == N1 / N2]
N --> O{N2 = 0}
O --FALSE--> P{{'O resultado é:', D}}
O --TRUE--> R{{É impossível dividir por 0}}
P --> Z
R --> Z
```
#### Teste de mesa
| N1 | N2 | Operador | Resultado | Saída |
| -- | -- | -- | -- | -- |
| 14 | 7 | soma | 21 | O resultado é: 21 |
| 8 | 5 | subtração | 3 | O resultado é: 3 |
| 20 | 4 | multiplicação | 80 | O resultado é: 80 |
| 16 | 0 | divisão |  | É impossível dividir por 0 |
| 30 | 3 | divisão | 10 | O resultado é: 10 |

### Exercício 04

#### Pseudocódigo
```
ALGORITMO
DECLARE I: inteiro
INÍCIO
ESCREVA “Digite a idade”
LEIA I
ENQUANTO
   I < 0
   ESCREVA "Digite um número positivo"
FIM_ENQUANTO
ESCOLHA
   CASO I < 5
      ESCREVA "Idade mínima ainda não atingida"
   CASO I >= 5 E <= 7
      ESCREVA "Categoria infantil A"
   CASO I >= 8 E <= 10
      ESCREVA "Categoria infantil B"
   CASO I >= 11 E <= 13
      ESCREVA "Categoria juvenil A"
   CASO I >= 14 E <= 17
      ESCREVA "Categoria juvenil B"
   CASO I >= 18
      ESCREVA "Categoria adulto"
FIM_ESCOLHA
FIM_ALGORITMO
```
#### Fluxograma
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite a idade}}
B --> C[\numero\]
C --> C2{I < 0}
C2 --FALSE--> D{I < 5}
C2 --TRUE--> C3{{Digite um número positivo}}
C3 --> C4[\numero\]
C4 --> B
C2 --> D2{I >= 5 E <= 7}
D --> E{{Idade mínima ainda não atingida}}
E --> Z([FIM])
D2 --> F{{Categoria infantil A}}
F --> Z
C2 --> D3{I >= 8 E <= 10}
D3 --> G{{Categoria infantil B}}
G --> Z
C2 --> D4{I >= 11 E <= 13}
D4 --> H{{Categoria juvenil A}}
H --> Z
C2 --> D5{I >= 14 E <= 17}
D5 --> I{{Categoria juvenil B}}
I --> Z
C2 --> D6{I >= 18}
D6 --> J{{Categoria adulto}}
J --> Z
```
#### Teste de mesa
| I | I < 0 | I < 5 | I >= 5 E <= 7 | I >= 8 E <= 10 | I >= 11 E <= 13 | I >= 14 E <= 17 | I >= 18 | Saída |
| -- | -- | -- | -- | -- | -- | -- | -- | -- |
| 4 | F | V | F | F | F | F | F | Idade mínima ainda não atingida |
| 7 | F | F | V | F | F | F | F | Categoria infantil A |
| 8 | F | F | F | V | F | F | F | Categoria infantil B |
| 12 | F | F | F | F | V | F | F | Categoria juvenil A |
| 15 | F | F | F | F | F | V | F | Categoria juvenil B |
| 19 | F | F | F | F | F | F | V | Categoria adulto |
| -7 | V |  |  |  |  |  |  | Digite um número positivo |
