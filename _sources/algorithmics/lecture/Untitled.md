---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.16.7
kernelspec:
  display_name: Python 3 (ipykernel)
  language: python
  name: python3
---

```{code-cell} ipython3
---
editable: true
slideshow:
  slide_type: ''
---
%%flowchart_magic -h 100 
```

```{code-cell} ipython3
---
editable: true
slideshow:
  slide_type: ''
---
%load_ext nb_js_diagrammers
```

```{code-cell} ipython3
---
editable: true
slideshow:
  slide_type: ''
---
%%flowchart_magic -h 1000
st=>start: Начало
in=>inputoutput: Ввод Доход, КоличествоДетей
cond=>condition: КоличествоДетей?

op1=>operation: 25% от дохода
op2=>operation: 33% от дохода
op3=>operation: 50% от дохода
out=>inputoutput: Вывод алиментов
e=>end: Конец

st->in->cond
cond()->op1->out->e
cond(2)->op2->out->e
cond(3)->op3->out->e
```

```{code-cell} ipython3
---
editable: true
slideshow:
  slide_type: ''
---

```
