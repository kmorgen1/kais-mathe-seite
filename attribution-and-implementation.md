---
layout: default
title: 'Attribution and Implementation'
---
This site uses the Jekyll Computer Modern Theme. It is a simple theme for publishing essays to GitHub Pages with Jekyll: [Github Link](https://github.com/kortina/jekyll-computer-modern-theme). It is 🆗 for a simple blog or academic paper.

## $$LaTex$$ Markup
For MathJax the following code has to be included in the page header:

```html
<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
   CommonHTML: {
    scale: 85
   }
  });
</script>
<script type="text/javascript" async src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>
```
### Scaling
The parameter `scale` above determines how big the $$LaTex$$ formulas are relative to the regular text. I found by trial and error that 85 is pretty close to a 1:1-ratio, as seen in the F$$Formula$$a. However, this is only true for a computer screen. On my mobile the ratio changes. 

### Delimiters
In $$LaTeX$$ code like this `\( \nabla_\boldsymbol{x} J(\boldsymbol{x}) \)` the markdown syntax uses `$$...$$` in stead of `\(...\)` as the delimiter: `$$ \nabla_\boldsymbol{x} J(\boldsymbol{x}) $$`.
and the code is rendered as $$ \nabla_\boldsymbol{x} J(\boldsymbol{x}) $$.

Formulas that are their own paragraph, in $$LaTex$$ delimited as `\[...\]` have to be delimited by <p>$$...$$</p>, otherwise the unrendered code will be repeated after the formula:

$$ \nabla_\boldsymbol{x} J(\boldsymbol{x}) $$

With the tags the superflous raw code disapears:

<p>$$ \nabla_\boldsymbol{x} J(\boldsymbol{x}) $$</p>

For some reason I have not figured out yet, this is caused by some combination a MathJax and the theme. I have tested this in other themes and there the <p> tags are not necessary.

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
