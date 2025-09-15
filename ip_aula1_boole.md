---
theme: default
lineNumbers: true
colorSchema: dark
layout: image
image: /img/layered-steps-right.svg
title: Álgebra de Boole
exportFilename: ip_aula1_boole
author: José Roberto Bezerra
---

# {{ $slidev.configs.title }}
Introdução a Programação

---

# Objetivo de Aprendizagem
- Compreender os conceitos elementares da Álgebra de *Boole*

---

# Agenda
- Álgebra de dois valores
- Tabela verdade
- Operadores AND (E) e OR (OU)


---
layout: section
---

# Álgebra de Dois Valores <MarkerPattern />

---
layout: quote
---

> Define-se como Álgebra de *Boole* (ou Booleana) um conjunto de operadores que são assumidos como válidos sem necessidade de prova.

---

# Características AB

- As variáveis assumem um número finito de valores constantes
  - Em números reais as variáveis podem assumir valores de $+\infty$ a $-\infty$
- Variáveis booleanas podem assumir dois valores
  - [F, V]
  - [H, L] (*High* ou *Low*)
  - [On, Off]
  - [Acesso, Apagado]
  - [Certo, Errado]
- **O que há em comum com esses valores?**

---

# Funções Reais

- Considere como exemplo a função $f(x) = x + 5$
- Como poderíamos representar todos os valores dessa função?

---

# Função

|  $x$ | $f(x)$ |
|:--:|:----:|
|  0 |   5  |
|  1 |   6  |
|  2 |   7  |
|  3 |   8  |
|  4 |   9  |
|  5 |  10  |


---

# Gráfico

```mermaid
xychart-beta
    title "f(x) = x + 5"
    x-axis "x" 0 --> 5 
    y-axis "y" 0 --> 10
    line [5, 6, 7, 8, 9, 10]
```

---

# Tabela Verdade

- O número de estados que uma função booleana pode assumir é **finito**
- Pode-se descrever **completamente** uma função booleana utilizando tabelas
- Uma Tabela Verdade (TV) lista os valores de entrada que as variáveis podem assumir e o valor de saída da função

---

# Exemplo de Tabela Verdade

|  **A** | **B**    | **S**   |
|:--:|:----:|:---:|
| 0   |   0  | 0 |
|  0  |   1  | 1 |
|  1  |  0   | 1 |
|  1  | 1    | 0 |

---
layout: section
---

# Operadores Elementares

---

# Operadores

- Funções booleanas ou Operadores
  - **OR** (OU, $+$)
  - **AND** (E, $\cdot$)
  - **NOT** (Negação, Complemento, ~)


---
layout: quote
---

> A operação **OR** resulta 1 se pelo menos uma das variáveis de entrada vale 1. Também conhecida como adição lógica.

---

# OR

> A operação **OR** resulta 1 se pelo menos uma das variáveis de entrada vale 1. Também conhecida como adição lógica.

<br>

| $0 + 0$ |   =  |  ? |
|:--:|:----:|:---:|
|  $0+1$  |   =  | ? |
|  $1+0$  |   =  | ? |
|  $1+1$  |   =  |  ? |

---

# OR

| $0 + 0$ |   =  | 0 |
|:--:|:----:|:---:|
|  $0+1$  |   =  | 1 |
|  $1+0$  |   =  | 1 |
|  $1+1$  |   =  | 1 |

---

# Tabela Verdade OR

| **A**|**B**|**OR**|
|:--:|:----:|:---:|
| 0   |   0  | 0 |
|  0  |   1  | 1 |
|  1  |   0  | 1 |
|  1  |   1  | 1 |


---

# Características OR

- Operador binário
- Apenas um **ÚNICO** valor 1 na entrada faz com que a saída seja 1
- Somente com **TODOS** os valores de entrada 0 a saída será 0

---
layout: quote
---

> A operação **AND** resulta 0 se pelo menos uma das variáveis de entrada valer 0. Também conhecida como multiplicação lógica


---

# AND

> A operação **AND** resulta 0 se pelo menos uma das variáveis de entrada valer 0. Também conhecida como multiplicação lógica

<br>

| $0 \cdot 0$ |   =  | ? |
|:--:|:----:|:---:|
|  $0 \cdot 1$  |   =  | ? |
|  $1 \cdot 0$  |   =  | ? |
|  $1 \cdot 1$  |   =  | ? |

---
layout: default
---

# AND

| $0 \cdot 0$ |   =  | 0 |
|:--:|:----:|:---:|
|  $0 \cdot 1$  |   =  | 0 |
|  $1 \cdot 0$  |   =  | 0 |
|  $1 \cdot 1$  |   =  | 1 |

---

# Tabela Verdade AND

| **A**|**B**|**AND**|
|:--:|:----:|:---:|
| 0   |   0  | 0 |
|  0  |   1  | 0 |
|  1  |   0  | 0 |
|  1  |   1  | 1 |


---

# Características AND

- Operador binário
- Apenas um **UMA** entrada com valor 0 faz com que a saída seja 0
- Somente com **TODOS** os valores de entrada 1 a saída será 1

---
layout: quote
---

> A operação NOT tem como resultado o valor complementar ao que a variável apresenta. Também chamado de Negação, Inversão ou Complementação.

---

# NOT

| $\overline{0}$ |   =  | ? |
|:--:|:----:|:---:|
|  $\overline{1}$  |   =  | ? |

---
layout: default
---

# NOT

| $\overline{0}$ |   =  | 1 |
|:--:|:----:|:---:|
|  $\overline{1}$  |   =  | 0 |

---

# Tabela Verdade NOT

| **A**|$\overline{A}$|
|:--:|:---:|
| 1   |   0  |
|  0  |   1  |


---

# Características NOT

- Operador unário
- Definida para uma variável apenas

---
layout: section
---

# Expressões Booleanas

---
layout: quote
---

> Uma expressão ou função booleana é uma combinação de operadores e variáveis que resultam em um valor booleano (ou lógico).

---
layout: fact
---

# $W = X + Y \cdot \overline{Z}$

---

# Exemplo
$W = X + Y \cdot \overline{Z}$

<br>

- Quais as variáveis de entrada?
- Quantas linhas são necessárias para escrever a TV?
- Qual a precedência entre as operações?

---

# Quais as variáveis de entrada?
$W = X + Y \cdot \overline{Z}$

<br>

> A variável de saída $W$ é expressa como uma função de 3 variáveis de entrada, $X$, $Y$ e $Z$

---

# Quantas linhas são necessárias na TV?
$W = X + Y \cdot \overline{Z}$

<br>

> Se temos 3 variáveis de entrada, existem $2^3$ combinações possíveis dos valores, logo a TV contém 8 linhas.

---

# Qual a precedência entre as operações?
$W = X + Y \cdot \overline{Z}$

- Assim como nas expressões algébricas, nas booleanas há precedência nas operações da seguinte forma:
  - AND
  - OR
  - NOT (Assim que possível)

---
layout: full
---

# $W = X + Y \cdot \overline{Z}$

| **$X$** | **$Y$** | **$Z$** | **$\overline{Z}$** | **$Y \cdot \overline{Z}$** | **$W$** |
|:-------:|:-------:|:-------:|:------------------:|:--------------------------:|:-------:|
|   |   |   |               |                      |   |
|   |   |   |               |                      |   |
|   |   |   |               |                      |   |
|   |   |   |               |                      |   |
|   |   |   |               |                      |   |
|   |   |   |               |                      |   |
|   |   |   |               |                      |   |
|   |   |   |               |                      |   |


---
layout: full
---

| **$X$** | **$Y$** | **$Z$** | **$\overline{Z}$** | **$Y \cdot \overline{Z}$** | **$W$** |
|:-------:|:-------:|:-------:|:------------------:|:--------------------------:|:-------:|
|    0    |    0    |    0    |          1         |              0             |    0    |
|    0    |    0    |    1    |          0         |              0             |    0    |
|    0    |    1    |    0    |          1         |              1             |    1    |
|    0    |    1    |    1    |          0         |              0             |    0    |
|    1    |    0    |    0    |          1         |              0             |    1    |
|    1    |    0    |    1    |          0         |              0             |    1    |
|    1    |    1    |    0    |          1         |              1             |    1    |
|    1    |    1    |    1    |          0         |              0             |    1    |

---
layout: section
---

# Exemplo de Aplicação

---

# Exemplo de Aplicação

Em um processo químico é desejável que um alarme seja ativado sempre que a temperatura exceder um certo valor máximo ou sempre que a pressão estiver acima de um certo limite. Como o seria o diagrama de blocos de uma solução tecnológica para esse problema?

---

# Diagrama

```mermaid {scale: 1}
graph LR
  SetT[Tmax]
  SetP[Pmax]
  SensorT[Sensor de<br>Temperatura] --> Comp1
  SetT --> Comp1
  SensorP[Sensor de<br>Pressão] --> Comp2
  SetP --> Comp2
  Comp1[Comparador] --> OR
  Comp2[Comparador] --> OR
  OR --> ALARM
```

---
layout: fact
---

# Perguntas

---
layout: fact
---

# Exercícios

---

# 1
Para cada uma das expressões booleanas abaixo, escrever a tabela verdade para determinar o valor da variável de saída $S$.
1. $S = \overline{A} + B\overline{C}$
2. $S = AB + \overline{CD}$
3. $S = X + Y + \overline{ZW}$

---

# 2
Em um sistema de segurança residencial, uma sirene deve ser acionada sempre que a porta principal estiver aberta E o sensor de movimento interno for ativado após o horário programado (22h). No entanto, o morador pode desativar manualmente todo o sistema com uma chave, independentemente das outras condições.

- Como seria o diagrama de blocos de uma solução tecnológica para esse problema?
- Identifique também as variáveis de entrada e a saída.

---

# Referências
- [George Boole](https://pt.wikipedia.org/wiki/George_Boole)
- [Brasil Escola](https://brasilescola.uol.com.br/informatica/algebra-booleana.htm)

---
layout: image
image: ./img/layered-steps-down.svg
---

# {{ $slidev.configs.author }}
jbroberto@ifce.edu.br<br><br>
https://gihtub.com/jbroberto76



<br><br><br>
<PoweredBySlidev />

##### Imagem by [https://haikei.app/](https://haikei.app/)