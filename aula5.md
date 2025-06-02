---
theme: default
lineNumbers: true
layout: intro
title: Módulos
author: José Roberto Bezerra
---

# Módulos

Introdução a Programação

---
layout: section
---

# Módulos Embutidos

---
layout: quote
---

> Um módulo Python é um arquivo contendo um conjunto de funções e declarações que podem ser incluído na sua aplicação. Um módulo pode ser entendido como uma biblioteca de códigos. O Python disponibiliza diversos módulos embutidos e existem ainda módulos de terceiros.

---
layout: default
---

# Módulos embutidos
- Existem diversos módulos disponíveis
- Exemplos:
    - `platform`
    - `math`
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