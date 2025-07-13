---
theme: default
lineNumbers: true
colorSchema: dark
layout: image
image: ./img/layered-steps-right.svg
title: Visualização de Dados
exportFilename: ip_aula10_python_graficos
author: José Roberto Bezerra
---

# {{ $slidev.configs.title }}
Introdução a Programação

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
Criar um *script* em Python que plota equações do segundo grau personalizadas através dos coeficientes $$a, b$$ e $$c$$.

---

# Referências
- [Matplotlib](https://matplotlib.org/)
- [Seaborn](https://seaborn.pydata.org/)
- [Guia para iniciantes em visualização de dados](https://hub.asimov.academy/blog/matplotlib-visualizacao-de-dados/)

---
layout: image
image: ./img/layered-steps-down.svg
---

# {{ $slidev.configs.author }}
jbroberto@ifce.edu.br
<br><br><br><br><br><br>
<PoweredBySlidev />
[<svg xmlns="http://www.w3.org/2000/svg" width="96" height="40" fill="none" viewBox="0 0 96 40" style="width:auto;height:2rem"><path fill="currentcolor" d="M87.465 7.456c0-1.538 1.193-2.856 2.888-2.856 1.695 0 2.919 1.318 2.919 2.856 0 1.6-1.224 2.793-2.92 2.793-1.694 0-2.887-1.193-2.887-2.793zM7.623 13.607c1.224-1.255 2.856-1.977 4.865-1.977 3.64 0 6.088 2.605 6.088 6.56v9.665h-4.99v-8.599c0-1.852-1.098-3.107-2.73-3.107-1.946 0-3.233 1.35-3.233 4.394v7.313H2.602V5.258h5.021v8.348z"></path><path fill="currentcolor" fill-rule="evenodd" d="M33.552 13.356V12.1h5.021v15.754h-5.021V26.6c-1.224 1.099-2.856 1.726-4.896 1.726-4.174 0-7.69-3.358-7.69-8.348 0-4.959 3.516-8.348 7.69-8.348 2.04 0 3.672.627 4.896 1.726zm-7.658 6.622c0 2.51 1.6 4.08 3.798 4.08 2.008 0 3.86-1.57 3.86-4.08 0-2.48-1.852-4.08-3.86-4.08-2.197 0-3.798 1.6-3.798 4.08z" clip-rule="evenodd"></path><path fill="currentcolor" d="M47.472 12.1h-5.021v15.755h5.021V12.1zM68.123 12.1l-6.904 7.501 7.626 8.255h-6.434l-4.833-5.681h-1.193v5.68h-5.021V5.26h5.022v12.208h1.004l4.676-5.366h6.057z"></path><path fill="currentcolor" fill-rule="evenodd" d="M84.98 19.978c-.094-5.147-3.672-8.348-8.129-8.348-4.582 0-8.348 3.39-8.348 8.348 0 4.99 3.766 8.348 8.317 8.348 3.61 0 6.465-1.6 7.815-4.927l-4.457-.91c-.847 1.538-2.197 1.82-3.358 1.82-1.695 0-2.982-1.161-3.39-3.044h11.55v-1.287zM76.85 15.71c1.444 0 2.7.784 3.17 2.48h-6.496c.47-1.602 1.883-2.48 3.326-2.48z" clip-rule="evenodd"></path><path fill="currentcolor" d="M87.842 12.1h5.022v15.755h-5.022V12.1zM44.962 29.752c-1.695 0-2.887 1.318-2.887 2.856 0 1.6 1.192 2.793 2.887 2.793s2.919-1.192 2.919-2.793c0-1.538-1.224-2.856-2.919-2.856z"></path></svg>](https://haikei.app/)