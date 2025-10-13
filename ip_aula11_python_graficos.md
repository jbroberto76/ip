---
theme: default
lineNumbers: true
colorSchema: dark
layout: image
image: /layered-steps-right.svg
title: Visualização de Dados
description: Introdução a Programação
exportFilename: ip_aula11_python_graficos
author: José Roberto Bezerra
---

# {{ $slidev.configs.title }}
{{ $slidev.configs.description }}

---

# Objetivo de Aprendizagen
- Aplicar os módulos `matplotlib` e `seaborn` para visualização de dados

---

# Agenda
- Matplotlib <logos-matplotlib />
- Seaborn <logos-seaborn />

---
layout: section
---

# Matplotlib

---
layout: quote
---

> Matplotlib is a comprehensive library for creating static, animated, and interactive visualizations in Python. Matplotlib makes easy things easy and hard things possible.

---

# Instalação

- O Matplotlib (MPL) é um módulo externo, logo precisa ser instalado
    - `pip install matplotlib`
    - `!pip install matplotlib`

---

# Conceitos

- MPL desenha ('plota') um gráfico numa `Figure`
- `Figure` pode conter um ou mais eixos (`Axes`), ou seja uma área que pode conter pontos (x-y)
- `suplots` cria uma `Figure` com `Axes`

---

```python{*}{class:'!children:text-2xl'}
import matplotlib.pyplot as plt

fig, ax = plt.subplots()
ax.plot([1, 2, 3, 4], [1, 4, 2, 3])
plt.show()
```

---

# Artistas

- `Figure` pode conter ainda diversos `Artists`
    - Títulos
    - Legendas
    - Barras
    - Linhas

---
layout: image
backgroundSize: contain
image: https://matplotlib.org/stable/_images/anatomy.png
---

---

# `Figure`
Como criar

```python{*}{class:'!children:text-xl'}
fig = plt.figure()
fig, ax = plt.subplots()
fig, axs = plt.subplots(2, 2)
fig, axs = 
    plt.subplot_mosaic([['left', 'right_top'], ['left', 'right_bottom']])
```

---

# `Axes`

- É um *Artist* associado a uma `Figure`
- Contém uma área de plotagem
- Inclui dois ou mais eixos
- `Axes` pode conter:
    - Título (`set_title()`)
    - Rótulo do eixo X (`set_xlabel()`)
    - Rótulo do eixo Y (`set_ylabel()`)
    - etc

---

# `Axis`

- `Axes` contém eixos (`Axis`)
- `Axis` ajusta a escala e os limites de cada eixo
- A marcação (*ticks*)

---

# Exemplo
Função seno

```python{*}{class:'!children:text-xl'}
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 2 * np.pi, 200)
y = np.sin(x)

fig, ax = plt.subplots()
ax.set_title('Gráfico do Seno')
ax.set_xlabel('X')
ax.set_ylabel('sen(x)')
ax.plot(x, y)
plt.show()
```

---

# Exemplo

```python{*}{class:'!children:text-xl'}
x = np.linspace(0, 2, 100)
fig, ax = plt.subplots(figsize=(5, 2.7), layout='constrained')
ax.plot(x, x, label='linear')
ax.plot(x, x**2, label='quadratic') 
ax.plot(x, x**3, label='cubic')
ax.set_xlabel('x label')
ax.set_ylabel('y label')
ax.set_title("Simple Plot")
ax.legend()
```

---

# Exemplo
Legendas

```python{*}{class:'!children:text-xl'}
fig, ax = plt.subplots(figsize=(5, 2.7))
ax.plot(np.arange(len(data1)), data1, label='data1')
ax.plot(np.arange(len(data2)), data2, label='data2')
ax.plot(np.arange(len(data3)), data3, 'd', label='data3')
ax.legend()
```

---
layout: section
---

# Seaborn

---
layout: quote
---

# Quando usar o Seborn?

> Para criar gráficos com bom aspecto visual, porém utilizando configurações pré-definidas

---

# Exemplo

```python{*}{class:'!children:text-xl'}
# Import seaborn
import seaborn as sns

# Apply the default theme
sns.set_theme()

# Load an example dataset
tips = sns.load_dataset("tips")

# Create a visualization
sns.relplot(
    data=tips,
    x="total_bill", y="tip", col="time",
    hue="smoker", style="smoker", size="size",
)
```

---

# Exemplo

```python{*}{class:'!children:text-xl'}
import seaborn as sns
import matplotlib.pyplot as plt

sns.set_theme()
sns.lineplot(x=[1, 2, 3], y=[100, 200, 350])
plt.title("Minhas Economias ao Longo do Ano - Seaborn Style")
plt.show()
```

---
layout: fact
---

# Exercício

---

# 1
Criar um *script* em Python que plota equações do segundo grau personalizadas através dos coeficientes $a$, $b$ e $c$.

---

# Referências
- [Matplotlib](https://matplotlib.org/)
- [Seaborn](https://seaborn.pydata.org/)
- [Guia para iniciantes em visualização de dados](https://hub.asimov.academy/blog/matplotlib-visualizacao-de-dados/)

---
src: /snippets/end.md
---