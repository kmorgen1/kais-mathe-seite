---
layout: default
title: "Jekyll Computer Modern Theme"
---

# Jekyll Computer Modern Theme

Jekyll Computer Modern Theme is a simple theme for publishing essays to GitHub Pages with Jekyll: [Github Link](https://github.com/kortina/jekyll-computer-modern-theme). It is 🆗 for a simple blog or academic paper.

## $$LaTex$$ Markup
> The LaTeX code for this is `$ \nabla_\boldsymbol{x} J(\boldsymbol{x}) $`. The markdown syntax uses $ one more time in each delimiter: `$$ \nabla_\boldsymbol{x} J(\boldsymbol{x}) $$`.

In den Text eingesetzt ergibt das $$ \nabla_\boldsymbol{x} J(\boldsymbol{x}) $$.

## Existenzbeweis Determinante
Um zu beweisen, dass die Determinante einer oberen Dreiecksmatrix das Produkt der Diagonalelemente ist, betrachten wir eine beliebige obere Dreiecksmatrix $$ A $$ der Größe $$ n \times n $$:

$$ A = \begin{pmatrix}
a_{11} & a_{12} & a_{13} & \cdots & a_{1n} \\
0 & a_{22} & a_{23} & \cdots & a_{2n} \\
0 & 0 & a_{33} & \cdots & a_{3n} \\
\vdots & \vdots & \vdots & \ddots & \vdots \\
0 & 0 & 0 & \cdots & a_{nn} \\
\end{pmatrix} $$

Wir können die Determinante dieser Matrix $$ \text{det}(A) $$ durch Entwicklung nach der ersten Zeile berechnen:

$$ \text{det}(A) = a_{11} \cdot \text{det}(A_{11}) + a_{12} \cdot \text{det}(A_{12}) + \cdots + a_{1n} \cdot \text{det}(A_{1n}) $$

Wobei $$ A_{ij} $$ die Matrix ist, die aus $$ A $$ entsteht, wenn man die $$i$$-te Zeile und die $$j$$-te Spalte entfernt. Da alle Elemente unterhalb der Diagonale null sind, sind alle $$ A_{ij} $$ ebenfalls obere Dreiecksmatrizen. Wenn $$ i \neq j $$, dann hat $$ A_{ij} $$ mindestens eine Nullzeile und somit ist $$ \text{det}(A_{ij}) = 0 $$. 

Wenn $$ i = j $$, dann besteht $$ A_{ii} $$ aus einem Element (dem Diagonalelement) und ist daher eine 1x1-Matrix, deren Determinante einfach das Diagonalelement selbst ist. Also gilt $$ \text{det}(A_{ii}) = a_{ii} $$.

Daraus folgt:

$$ \text{det}(A) = a_{11} \cdot \text{det}(A_{11}) + a_{22} \cdot \text{det}(A_{22}) + \cdots + a_{nn} \cdot \text{det}(A_{nn}) $$

Da alle $$ \text{det}(A_{ij}) $$ für $$ i \neq j $$ null sind, bleibt nur der Ausdruck $$ a_{11} \cdot \text{det}(A_{11}) + a_{22} \cdot \text{det}(A_{22}) + \cdots + a_{nn} \cdot \text{det}(A_{nn}) $$ übrig, und das ist einfach das Produkt der Diagonalelemente der Matrix $$ A $$. Daher ist die Determinante einer oberen Dreiecksmatrix gleich dem Produkt ihrer Diagonalelemente.


## Posts List

{% for post in site.posts %}<p><a href="{{ site.url }}{{ post.url }}">{{ post.title }}</a></p>{% endfor %}

## Example Static Page (not a post)

[Example Static Page]({{site.url}}/example-static-page/)

## Style Guide

Here is a short paragraph of text.

> Here is what a blockquote would look like. Here is what a blockquote would look like.

<a name="lorem"></a>

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

Here's a list with 3 items:

- item numero
- second item, this one is long enough so that it will wrap onto another line of text so you can see how it aligns
- third item

A horizontal rule:

---

And here is a code block:

```python
some_int = 11
some_list = [12]
some_list.append(some_int)
print(f"Some python code {some_list}")
```

All the headings:

# h1 example

text.

## h2 example

text.

### h3 example

text.

#### h4 example

text.

##### h5 example

text.

###### h6 example

text.

And an aside:

<aside markdown="1">
Some markdown aside (with support for `markdown`)
</aside>

An image (from _Nightcrawler_) resized to same width as everything else (the default):

![nightcrawler](https://kortina.nyc/files/nightcrawler.jpg)

A full width image (from _Ghost in the Shell_) (using `<img class="full-width" ... />` via the `_includes/embed.html` helper):

{% include embed.html class="full-width" url="https://kortina.nyc/files/conscioussness-as-computation/ghost-in-the-shell-contructing-the-mind.jpg" %}

A vimeo embed (also via the `_includes/embed.html` helper):

{% include embed.html url="https://player.vimeo.com/video/389644389" autoplay="0" %}

A youtube embed (also via the `_includes/embed.html` helper):

{% include embed.html url="https://www.youtube.com/embed/CybARtyBHxI" %}
