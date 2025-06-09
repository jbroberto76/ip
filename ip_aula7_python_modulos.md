---
theme: default
lineNumbers: true
colorSchema: dark
layout: image
image: ./img/layered-steps-right.svg
title: Módulos
exportFilename: ip_aula7_python_modulos
author: José Roberto Bezerra
---

# {{ $slidev.configs.title }}
Introdução a Programação

---

# Objetivo de Aprendizagen
- Conhecer módulos de uso geral do Python

---

# Agenda
- Módulos embutidos
- `math`
- `platform`
- `os`


---
layout: section
---

# Módulos Embutidos

---
layout: quote
---

> Um módulo Python é um arquivo contendo um conjunto de funções e declarações que pode ser incluído em um *script*. Um módulo pode ser entendido como uma biblioteca de códigos. O Python disponibiliza diversos módulos embutidos e existem ainda módulos de terceiros.

---

# Módulos embutidos
- Existem diversos módulos disponíveis
- Exemplos:
    - `math`
    - `platform`
    - `os`
    - Dentre muitos outros

---
layout: default
---

# Como usar um módulo?

- Vamos utilizar como exemplo o módulo `math`
- O primeiro passo é a importação do módulo: `import math`

```python{*}{class:'!children:text-2xl'}
import math
print(math.pi)
```

---
layout: default
---

# O que acontece ao executar os códigos?

```python{*}{class:'!children:text-2xl'}
import math
print(math.ceil(1.45))
print(math.floor(1.45))
print(math.factorial(3))
print(math.fabs(-1))
print(math.pow(2,3))
print(math.sqrt(2))
```

---
layout: default
---

# Referências
- [W3 Schools](https://www.w3schools.com/python/python_modules.asp)
- [Python Math](https://docs.python.org/3/library/math.html)

---
layout: image
image: ./img/layered-steps-down.svg
---

# Prof. {{ $slidev.configs.author }}
jbroberto@ifce.edu.br
<br><br><br><br><br><br>
<PoweredBySlidev />