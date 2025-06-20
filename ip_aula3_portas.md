---
theme: default
lineNumbers: true
colorSchema: dark
ayout: image
image: ./img/layered-steps-right.svg
title: Portas Lógicas
exportFilename: ip_aula3_portas
author: José Roberto Bezerra
---

# {{ $slidev.configs.title }}
Introdução a Programação<br>

---

# Objetivos de Aprendizagem
- Conhecer circuitos que representam funções booleanas elementares
- Escrever circuitos a partir de expressões

---

# Agenda
- Portas lógicas
- Conversão de expressões lógicas em circuitos digitais

---
layout: section
---

# Portas Lógicas

---

# Funções Booleanas

São representadas de várias formas:
- Tabelas verdade
- Expressões
- Formato Gráfico, circuitos eletrônicos ou **portas lógicas**

---

# Portas Lógicas

- Representam mais do que simplesmente símbolos dos operadores lógicos

- Recursos físicos são associados

- Base da **eletrônica digital**

---

# Eletrônica Digital

- Existem dois estados
    - Nível lógico 0 (Ausência de tensão)
    - Nível lógico 1 (Tensão 5V ou 12V)

---

# Portas Lógicas (*Gates*)

> Circuitos eletrônicos que, de alguma maneira (circuito analógicos), realizam as funções booleanas existentes

---
layout: image-right
image: https://media.geeksforgeeks.org/wp-content/uploads/20220607101553/orgate.jpg
backgroundSize: contain
---

# Porta OR

---
layout: image-right
image: https://media.geeksforgeeks.org/wp-content/uploads/20220607100724/andgate.jpg
backgroundSize: contain
---

# Porta AND

---
layout: image-right
image: https://cdn.makecode.com/blob/f543c51cd05c07fa101886eecadd07a1ddc0052b/static/courses/logic-lab/logic-gates/not-gate.png
backgroundSize: contain
---

# Porta NOT

---
layout: image-right
image: https://redpitaya-knowledge-base.readthedocs.io/en/latest/_images/2000px-Nand-gate-en.png
backgroundSize: contain
---

# Porta NAND
NOT + AND

---
layout: image-right
image: https://redpitaya-knowledge-base.readthedocs.io/en/latest/_images/1200px-NOR_ANSI_Labelled.svg.png
backgroundSize: contain
---

# Porta NOR
NOT + OR

---
layout: image-right
image: https://electronicaonline.net/wp-content/uploads/2020/10/que-son-los-circuitos-integrados.jpg
backgroundSize: contain
---

# Circuitos Integrados

> Um circuito integrado (CI), também conhecido como chip ou microchip, é um componente eletrônico que contém vários componentes eletrônicos, como transistores, resistores e capacitores, integrados em um único substrato semicondutor, geralmente silício. 

---
layout: image-right
image: https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse1.mm.bing.net%2Fth%3Fid%3DOIP.dOx9BNoJTkJYSg1FwR8sOwHaHa%26pid%3DApi&f=1&ipt=e2a37f8123e7adc2b2b0f688b2e1cd13eb9c180d01dd55e65e502a7b5c02d111&ipo=images
---

# Circuitos Integrados

> São utilizados em uma vasta gama de dispositivos, desde computadores e *smartphones* até eletrodomésticos

---

# Portas Lógicas em CIs

> Integra diversas portas lógicas em um único circuito integrado. Facilita a implementação de aplicações reais. A mais comum atualmente é a TTL.

---

# Circuitos TTL

> TTL (*Transistor-Transistor Logic*) é um tipo de tecnologia de circuito digital que utiliza transistores bipolares para implementar funções lógicas. Foi amplamente utilizado em computadores e outros dispositivos eletrônicos antes da popularização de tecnologias mais avançadas, como CMOS (*Complementary Metal-Oxide-Semiconductor*).

---
layout: image-right
image: https://avelectronics.cc/wp-content/uploads/2018/09/7408-1.png
---

# TTL 7408
4 ANDs de duas entradas

---
layout: image-right
image: https://avelectronics.cc/wp-content/uploads/2018/09/7432.png
---

# TTL 7432
4 ORs de duas entradas

---
layout: image-right
image: https://avelectronics.cc/wp-content/uploads/2018/09/7404.png
---

# TTL 7404
6 NOTs

---
layout: center
---

# Portas TTL


[Lista Completa](https://blog.novaeletronica.com.br/lista-circuitos-integrados-ttl-serie-7400-eletronica-digital/)

---
layout: section
---

# Escrever Circuitos a partir de Expressões

---

# Circuito Lógico
Circuito Digital

- Dada uma equação Booleana qualquer, é possível desenhar o circuito lógico que a implementa
- O circuito lógico é composto das portas lógicas relacionadas às operações que são realizadas sobre as variáveis de entrada
- Os resultados das operações, as entradas e os valores intermediários são conduzidos por fios, os quais, no desenho, são representados por linhas simples

---
layout: fact
---

# Como desenhar o circuito a partir de uma expressão?

---

# Como desenhar o circuito a partir de uma expressão?

1. Identificar as variáveis independentes
2. Desenhar as portas lógicas que representam cada uma das subexpressões, seguindo a prioridade:
    1. Parênteses
    2. Operações AND
    3. Operações OR
3. Ligar com linhas as variáveis e as portas

---
layout: fact
---

# Exemplos

---

# $W = X + Y \cdot \overline{Z}$

---

# $S = A \cdot B + C \cdot \overline{D}$

---
layout: fact
---

# Perguntas

---
layout: fact
---

# Exercícios

---
layout: image-right
image: img/gates.png
---

# 1
Escreva a expressão booleana executada pelos circuitos mostrados.

---

# 2
Dada a expressão booleana $Z = ABC + (A\overline{B}) \cdot \overline{(\overline{A}\overline{B})}$, qual o circuito lógico que a representa?

---

# 3
Simplifique a expressão da questão anterior. Qual o circuito lógico que a representa agora?

<!-- ---

# 4
Use o simulador *Circuit Verse* para comparar os circuitos das questões 2 e 3 e verificar que são realmente equivalentes. Para isso, monte a Tabela Verdade de cada circuito e compare-as. -->

<!-- # Referências

--> 
---
layout: image
image: ./img/layered-steps-down.svg
---

# {{ $slidev.configs.author }}
jbroberto@ifce.edu.br
<br><br><br><br><br><br>
<PoweredBySlidev />