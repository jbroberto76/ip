---
theme: default
transition: fade
lineNumbers: true
colorSchema: dark
layout: image
image: /img/layered-steps-right.svg
title: Exercícios
description: Introdução a Programação
exportFilename: ip_aula4_exrc
author: José Roberto Bezerra
---

# {{ $slidev.configs.title }}
{{ $slidev.configs.description }}

---

# Objetivos de Aprendizagem
- Resolução de exercícios similares a primeira avaliação

---

# Agenda
- Exercício 1
- Exercício 2
- Primeira avaliação

---
layout: section
---

# Exercício 1

---

# 1
Análise de crédito

> Um banco usa um sistema automático para pré-selecionar clientes para empréstimo com base em três critérios binários:

<br>

R (Renda estável):
1 = Renda estável ≥ R$ 2000, 0 = Caso contrário.

D (Sem dívidas):
1 = Não possui dívidas em atraso, 0 = Possui dívidas.

E (Empregado):
1 = Está empregado atualmente, 0 = Desempregado.

---

# 1
Análise de crédito

<br>

> Projete um circuito lógico que ative um sinal A (Aprovado para análise) sempre que:

<br>

- O cliente tiver Renda estável E estiver Empregado;
- OU se estiver Sem dívidas E com Renda estável, independente de estar empregado ou não.

---

# 1
Análise de crédito (**Solução**)

1. Compreender o enunciado. Entender o problema;
2. Observar as condições exigidas. Esboçar a tabela verdade;
3. A partir da TV, extrair a expressão que representa a solução através de mintermos ou maxtermos;
4. Simplificar a expressão, se possível;
5. Desenhar o circuito que representa a a expressão obtida
6. Simular no *Circuit Verse*
7. A TV da simulação é idêntica a TV da interpretação do problema?

---
zoom: 0.9
---

# 1
Análise de crédito (**Solução**) + Tabela Verdade obtida pela interpretação do problema

| R | D | E | A |
|---|---|---|---|
| 0 | 0 | 0 |  |
| 0 | 0 | 1 |  |
| 0 | 1 | 0 |  |
| 0 | 1 | 1 |  |
| 1 | 0 | 0 |  |
| 1 | 0 | 1 |  |
| 1 | 1 | 0 |  |
| 1 | 1 | 1 |  |

---
zoom: 0.9
---

# 1
Análise de crédito (**Solução**) + TV obtida pela interpretação do problema

| R | D | E | $A_i$ |
|---|---|---|-------|
| 0 | 0 | 0 | **0** |
| 0 | 0 | 1 | **0** |
| 0 | 1 | 0 | **0** |
| 0 | 1 | 1 | **0** |
| 1 | 0 | 0 | **0** |
| 1 | 0 | 1 | **1** |
| 1 | 1 | 0 | **1** |
| 1 | 1 | 1 | **1** |

---
zoom: 0.9
---

# 1
Análise de crédito (**Solução**) + Mintermos da expressão

| R | D | E | $A_i$ |
|---|---|---|-------|
| 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 0 |
| 0 | 1 | 0 | 0 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 **($R \cdot \overline{D} \cdot E$)** | 
| 1 | 1 | 0 | 1 **($R \cdot D \cdot \overline{E}$)** |
| 1 | 1 | 1 | 1 **($R \cdot D \cdot E$)** |

---

# 1
Análise de crédito (**Solução**) + Simplificação da Expressão usando mintermos

$$
\begin{aligned}
A &= (R \cdot \overline{D} \cdot E) + (R \cdot D \cdot \overline{E}) + (R \cdot D \cdot E) \\
& = R \cdot (\overline{D}E + D\overline{E} + DE)\\
& = R \cdot (\overline{D}E + D (\overline{E} + E))\\
& = R \cdot (\overline{D}E + D (1))\\
& = R \cdot (\overline{D}E + D)\\
& = R \cdot (D + E)\\
\end{aligned}
$$

---

# 1
Análise de crédito (**Solução**) + Simulação

<br>

[Circuit Verse](https://circuitverse.org/simulator)

---
image: /img/analise_cred.png
layout: image-right
backgroundSize: contain
---

# 1
Análise de crédito (**Solução**) + Simulação

<br>

[Circuit Verse](https://circuitverse.org/simulator)

---
zoom: 0.9
---

# 1
Análise de crédito (**Solução**) + TV obtida da simulação

| R | D | E | $A_s$ |
|---|---|---|-------|
| 0 | 0 | 0 | **0** |
| 0 | 0 | 1 | **0** |
| 0 | 1 | 0 | **0** |
| 0 | 1 | 1 | **0** |
| 1 | 0 | 0 | **0** |
| 1 | 0 | 1 | **1** |
| 1 | 1 | 0 | **1** |
| 1 | 1 | 1 | **1** |

---

# 1
Análise de crédito (**Solução**) + Conclusão

> A partir do entendimento do problema foi obtida a TV e a expressão da interpretação. Foi realizada a simulação a partir do circuito obtido na expressão e a TV da simulação do circuito coincide com a TV da interpretação.

---
layout: section
---

# Exercício 2

---

# 2
Rio+Bomba+Tanque

> A figura mostra um sistema de abastecimento de água composto de uma bomba $B$ e um tanque. A função da bomba é levar água do rio, quando estiver disponível. O reservatório possui dois sensores, um para monitorar o nível inferior, $L$, e outro para o nível superior, $H$. Os sensores funcionam da seguinte forma:

- Quando o nível da água está baixo, $H = L = 0$
- Quando o nível da água está acima do sensor, $H = 1$ ou $L = 1$

---

# 2
Rio+Bomba+Tanque

<br>

> Projete um circuito digital que utilize os sensores para realizar o acionamento de $B$ mantendo o reservatório com água sempre que houver disponibilidade.

---
zoom: 0.9
---

# 2
Rio+Bomba+Tanque (**Solução**) - TV da interpretação problema

| L | H | R | B |
|---|---|---|---|
| 0 | 0 | 0 |  |
| 0 | 0 | 1 |  |
| 0 | 1 | 0 |  |
| 0 | 1 | 1 |  |
| 1 | 0 | 0 |  |
| 1 | 0 | 1 |  |
| 1 | 1 | 0 |  |
| 1 | 1 | 1 |  |

---
zoom: 0.9
---

# 2
Rio+Bomba+Tanque (**Solução**) - TV da interpretação problema

| L | H | R | $B_i$ |
|---|---|---|-------|
| 0 | 0 | 0 | **0** |
| 0 | 0 | 1 | **1** |
| 0 | 1 | 0 | **0** |
| 0 | 1 | 1 | **0** |
| 1 | 0 | 0 | **0** |
| 1 | 0 | 1 | **1** |
| 1 | 1 | 0 | **0** |
| 1 | 1 | 1 | **0** |

---
zoom: 0.9
---

# 2
Rio+Bomba+Tanque (**Solução**) - TV com mintermos

| L | H | R | $B_i$ |
|---|---|---|-------|
| 0 | 0 | 0 | **0** |
| 0 | 0 | 1 | **1** ($\overline{L} \cdot \overline{H} \cdot R$) |
| 0 | 1 | 0 | **0** |
| 0 | 1 | 1 | **0** |
| 1 | 0 | 0 | **0** |
| 1 | 0 | 1 | **1** ($L \cdot \overline{H} \cdot R$) |
| 1 | 1 | 0 | **0** |
| 1 | 1 | 1 | **0** |

---

# 2
Rio+Bomba+Tanque (**Solução**) - Expressão a partir dos mintermos

<br>

$$
\begin{aligned}
B_i &= (\overline{L} \cdot \overline{H} \cdot R) + (L \cdot \overline{H} \cdot R)\\
&= \overline{H}R (L + \overline{L})\\
&= \overline{H}R (1)\\
&= \overline{H}R\\
\end{aligned}
$$

---

# 2
Rio+Bomba+Tanque (**Solução**) - Simulação

<br>

[Circuit Verse](https://circuitverse.org/simulator)

---
image: /img/rio_bomba_tanque.png
layout: image-right
backgroundSize: contain
---

# 2
Rio+Bomba+Tanque (**Solução**) - Simulação

<br>

[Circuit Verse](https://circuitverse.org/simulator)

---

# 2
Rio+Bomba+Tanque (**Solução**) - TV da simulação

| L | H | R | $B_s$ |
|---|---|---|-------|
| 0 | 0 | 0 | **0** |
| 0 | 0 | 1 | **1** |
| 0 | 1 | 0 | **0** |
| 0 | 1 | 1 | **0** |
| 1 | 0 | 0 | **0** |
| 1 | 0 | 1 | **1** |
| 1 | 1 | 0 | **0** |
| 1 | 1 | 1 | **0** |

---

# 2
Rio+Bomba+Tanque (**Solução**) - Conclusão

<br>

> Ambas TVs, da interpretação e da simulação, são coincidentes e mostram que solução para o problema.

<br>

> O problema poderia ser ainda mais simplificado utilizando apenas o sensor superior, $H$, e o sensor do rio, $R$, conforme mostra a expressão simplificada.

---
layout: fact
---

# Perguntas

---
layout: section
---

# Primeira Avaliação

---

# Primeira Avaliação
Alarme automotivo

> Um carro possui 3 sensores:
- Nas portas: Quando alguma porta estiver aberta este sensor envia nível lógico alto;
- Na ignição: Quando a ignição está ligada este sensor envia nível lógico alto;
- Nos faróis: Quando algum farol está ligado esse sensor envia 1;

> Projete um circuito lógico que faça acionar uma luz vermelha no painel do carro sempre que:
- As portas estiverem abertas com a ignição acionada;
- Os faróis estiverem acesos com a ignição desligada.

---

# Primeira Avaliação
Alarme automotivo

> Apresentar as seguintes etapas de desenvolvimento.

<br>

1. Tabela Verdade da interpretação do problema;
2. Equação que representa a TV, simplificada;
3. Circuito digital que implementa a equação (*printscreen* do *Circuit Verse* ou imagem do circuito);
4. Tabela Verdade obtida a partir da simulação do circuito e comparada com a TV do ítem 1.

---

# Primeira Avaliação
Alarme automotivo

- 50% da nota da N1
- Atividade individual
- Prazo de entrega: **19/10/2025**
- Entrega apenas via <logos-google /> Sala de Aula 


---
layout: fact
---

# Dúvidas

---

# Referências

- [Simulador Circuit Verse](https://circuitverse.org/simulator)

---
src: /src/end.md
---


