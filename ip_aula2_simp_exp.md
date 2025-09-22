---
theme: default
lineNumbers: true
colorSchema: dark
layout: image
image: ./img/layered-steps-right.svg
title: Simplificação de Expressões
description: Introdução a Programação
exportFilename: ip_aula2_simp_exp
author: José Roberto Bezerra
---

# {{ $slidev.configs.title }}
{{ $slidev.configs.description }}

---

# Objetivos de Aprendizagem
- Conhecer propriedades elementares
- Simplificar expressões booleanas

---

# Agenda
- Propriedades da Álgebra de Boole
- Teoremas de De Morgan
- Simplificação de Expressões
    - Soma de Produtos
    - Produto de Somas

---
layout: section
---

# Propriedades

---

# Propriedades da Álgegra de Boole
OR
<br><br><br>
$$
\begin{aligned}
A + 0 = A \\
A + 1 = 1 \\
A + A = A \\
A + \overline{A} = 1 \\
\end{aligned}
$$

---

# Propriedades da Álgegra de Boole
AND
<br><br><br>
$$
\begin{aligned}
A \cdot 0 = 0 \\
A \cdot 1 = A \\
A \cdot A = A \\
A \cdot \overline{A} = 0 \\
\end{aligned}
$$

---

# Propriedades da Álgegra de Boole
NOT
<br><br><br>

$$
\begin{aligned}
\overline{\overline{A}} = A
\end{aligned}
$$

---
layout: section
---

# Teoremas de De Morgan

---

# Teoremas de De Morgan
Primeiro

$$
\begin{aligned}
\overline{A \cdot B \cdot C} = \overline{A} + \overline{B} + \overline{C}
\end{aligned}
$$

---

# Teoremas de De Morgan
Segundo

$$
\begin{aligned}
\overline{A + B + C} = \overline{A} \cdot \overline{B} \cdot \overline{C}
\end{aligned}
$$

---

# Demonstração
Primeiro Teorema de De Morgan

$$
\begin{aligned}
\overline{A \cdot B} = \overline{A} + \overline{B}
\end{aligned}
$$

| $A$ | $B$ | $\overline{A \cdot B}$ | $\overline{A}+\overline{B}$ |
|:-------:|:-------:|:--------------------------:|:-------------------------------:|
|    0    |    0    |              ?             |                ?                |
|    0    |    1    |              ?             |                ?                |
|    1    |    0    |              ?             |                ?                |
|    1    |    1    |              ?             |                ?                |

---

# Demonstração
Primeiro Teorema de De Morgan

$$
\begin{aligned}
\overline{A \cdot B} = \overline{A} + \overline{B}
\end{aligned}
$$

| $A$ | $B$ | $\overline{A \cdot B}$ | $\overline{A}+\overline{B}$ |
|:-------:|:-------:|:--------------------------:|:-------------------------------:|
|    0    |    0    |              **1**         |            **1**                |
|    0    |    1    |              **1**         |            **1**                |
|    1    |    0    |              **1**         |            **1**                |
|    1    |    1    |              **0**         |            **0**                |

---

# Demonstração
Segundo Teorema de De Morgan

$$
\begin{aligned}
\overline{A + B} = \overline{A} \cdot \overline{B}
\end{aligned}
$$

| $A$ | $B$ | $\overline{A + B}$ | $\overline{A} \cdot \overline{B}$ |
|:-------:|:-------:|:----------------------:|:-------------------------------------:|
|    0    |    0    |            ?           |                   ?                   |
|    0    |    1    |            ?           |                   ?                   |
|    1    |    0    |            ?           |                   ?                   |
|    1    |    1    |            ?           |                   ?                   |

---

# Demonstração
Segundo Teorema de De Morgan

$$
\begin{aligned}
\overline{A + B} = \overline{A} \cdot \overline{B}
\end{aligned}
$$

| $A$ | $B$ | $\overline{A + B}$ | $\overline{A} \cdot \overline{B}$ |
|:-------:|:-------:|:----------------------:|:-------------------------------------:|
|    0    |    0    |            **1**       |                   **1**               |
|    0    |    1    |            **0**       |                   **0**               |
|    1    |    0    |            **0**       |                   **0**               |
|    1    |    1    |            **0**       |                   **0**               |

---
layout: section
---

# Simplificação de Expressões Booleanas

---
layout: quote
---

> Dada uma função Booleana, descrita por sua tabela verdade, simplificar ou derivar essa expressão é encontrar uma equação que a descreva.

---

# Descrevendo uma Função Booleana

- Pode-se definir uma função Booleana descrevendo-se todas as situações em que a função vale 1 ou todas as situações em que a função vale 0
- Há duas formas de realizar a descrição de uma função
    - Soma de Produtos (SDP)
    - Produto de Somas (PDS)
- Utilizando-se um dos métodos é possível descrever **completamente** uma função Booleana

---

# Soma de Produtos

| $A$ | $B$ | $C$ | mintermo |
|:-------:|:-------:|:-------:|:------------:|
|    0    |    0    |    0    |       ?      |
|    0    |    0    |    1    |       ?      |
|    0    |    1    |    0    |       ?      |
|    0    |    1    |    1    |       ?      |
|    1    |    0    |    0    |       ?      |
|    1    |    0    |    1    |       ?      |
|    1    |    1    |    0    |       ?      |
|    1    |    1    |    1    |       ?      |

---

# Soma de Produtos

| $A$ | $B$ | $C$ |                     mintermo                     |
|:-------:|:-------:|:-------:|:----------------------------------------------------:|
|    0    |    0    |    0    | $\overline{A} \cdot \overline{B} \cdot \overline{C}$ |
|    0    |    0    |    1    |       $\overline{A} \cdot \overline{B} \cdot C$      |
|    0    |    1    |    0    |       $\overline{A} \cdot B \cdot \overline{C}$      |
|    0    |    1    |    1    |            $\overline{A} \cdot B \cdot C$            |
|    1    |    0    |    0    |       $A \cdot \overline{B} \cdot \overline{C}$      |
|    1    |    0    |    1    |            $A \cdot \overline{B} \cdot C$            |
|    1    |    1    |    0    |            $A \cdot B \cdot \overline{C}$            |
|    1    |    1    |    1    |                  $A \cdot B \cdot C$                 |

---

# Soma de Produtos

- Cada termo produto construído conforme a regra anteriormente descrita é denominado **mintermo** (ou minitermo)
- Para um dado mintermo, se substituirmos os valores das variáveis associadas, obteremos 1.
- Porém, se substituirmos nesse mesmo mintermo quaisquer outras combinações de valores, obteremos 0
- Dessa forma, se quisermos encontrar a equação para uma função a partir de sua tabela verdade, basta montarmos um **OU** entre os mintermos associados aos 1s da função

---
layout: two-cols-header
---

# Exemplo 1

:: left::

<v-clicks depth="2">

- Quais os valores de $(A, B, C)$ em que $F$ vale 1?
    - $(0 1 0), (0 1 1), (1 0 1), (1 1 0)$
- Ou seja, quais os mintermos associados?
    - $\overline{A} \cdot B \cdot \overline{C}$
    - $A \cdot \overline{B} \cdot C$
    - $\overline{A} \cdot B \cdot C$
    - $A \cdot B \cdot \overline{C}$

</v-clicks>


::right::

| $A$ | $B$ | $C$ | F |
|:-------:|:-------:|:-------:|:-----:|
|    0    |    0    |    0    |   0   |
|    0    |    0    |    1    |   0   |
|    0    |    1    |    0    | **1** |
|    0    |    1    |    1    | **1** |
|    1    |    0    |    0    |   0   |
|    1    |    0    |    1    | **1** |
|    1    |    1    |    0    | **1** |
|    1    |    1    |    1    |   0   |

---
layout: fact
---

$$F_{min} = \overline{A} \cdot B \cdot \overline{C} + A \cdot \overline{B} \cdot C + \overline{A} \cdot B \cdot C + A \cdot B \cdot \overline{C}$$

---

# Produto de Somas

| $A$ | $B$ | $C$ | maxtermo |
|:-------:|:-------:|:-------:|:------------:|
|    0    |    0    |    0    |       ?      |
|    0    |    0    |    1    |       ?      |
|    0    |    1    |    0    |       ?      |
|    0    |    1    |    1    |       ?      |
|    1    |    0    |    0    |       ?      |
|    1    |    0    |    1    |       ?      |
|    1    |    1    |    0    |       ?      |
|    1    |    1    |    1    |       ?      |

---

# Produto de Somas

| $A$ | $B$ | $C$ | maxtermo |
|:-------:|:-------:|:-------:|:----------------------------------------------------:|
|    0    |    0    |    0    | $A + B + C$ |
|    0    |    0    |    1    |       $A + B + \overline{C}$      |
|    0    |    1    |    0    |       $A + \overline{B} + C$      |
|    0    |    1    |    1    |            $A + \overline{B} + \overline{C}$            |
|    1    |    0    |    0    |       $\overline{A} + B + C$      |
|    1    |    0    |    1    |            $\overline{A} + B + \overline{C}$            |
|    1    |    1    |    0    |            $\overline{A} + \overline{B} + C$            |
|    1    |    1    |    1    | $\overline{A} + \overline{B} + \overline{C}$ |

---

# Produto de Somas
- Médodo Dual ao SDP
- Cada termo soma construído conforme a regra anteriormente descrita é denominado **maxtermo**
- Para um dado maxtermo, se substituirmos os valores das variáveis associadas, obteremos 0
- Porém, se substituirmos nesse mesmo maxtermo quaisquer outras combinações de valores, obteremos 1
- Dessa forma, se quisermos encontrar a equação para uma função a partir de sua tabela verdade, basta montarmos um **E (AND)** entre os maxtermos associados aos 0s da função

---
layout: two-cols-header
---

# Exemplo 2

:: left::

<v-clicks depth="2">

- Quais os valores de $(A, B, C)$ em que $F$ vale 0?
    - $(0 0 0), (0 0 1), (1 0 0), (1 1 1)$
- Ou seja, quais os maxtermos associados?
    - $A + B + C$
    - $A + B + \overline{C}$
    - $\overline{A} + B + C$
    - $\overline{A} + \overline{B} + \overline{C}$

</v-clicks>


::right::

| $A$ | $B$ | $C$ | $F$ |
|:-------:|:-------:|:-------:|:-----:|
|    0    |    0    |    0    |   0   |
|    0    |    0    |    1    |   0   |
|    0    |    1    |    0    |   1   |
|    0    |    1    |    1    |   1   |
|    1    |    0    |    0    |   0   |
|    1    |    0    |    1    |   1   |
|    1    |    1    |    0    |   1   |
|    1    |    1    |    1    |   0   |

---
layout: fact
---

$$F_{max} = (A+B+C) \cdot (A + B \overline{C}) \cdot (\overline{A} + B + C) \cdot (\overline{A} + \overline{B} + \overline{C})$$

---
layout: quote
---

> Para encontrar a equação para uma função booleana a partir de sua tabela verdade, basta montarmos um **OU (OR)** entre os mintermos associados aos 1s da função

---
layout: quote
---

> Para encontrar a equação para uma função lógica a partir de sua tabela verdade, basta montarmos um **E (AND)** entre os maxtermos associados aos 0s da função

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

Aplique as propriedades da Álgebra de Boole para simplificar as expressões abaixo:
1. $A \cdot \overline{B} + A \cdot B$
2. $(A+B) \cdot (A+\overline{B}) \cdot (\overline{A}+B)$
3. $\overline{A \cdot B} + A$
4. $(\overline{A+\overline{B}}) \cdot B$
5. $(\overline{AB})\cdot(\overline{A}+C)$

---

# 2

Aplique as propriedades da Álgebra de Boole para simplificar as expressões $F_{min}$ e $F_{max}$ encontradas anteriormente e mostrar que elas são equivalentes.
- $F_{min} = \overline{A}B\overline{C} + \overline{A}BC + A\overline{B}C + AB\overline{C}$
- $F_{max} = (A+B+C) \cdot (A+B+\overline{C}) \cdot (\overline{A}+B+C) \cdot (\overline{A}+\overline{B}+\overline{C})$ 

---
src: /src/end.md
---