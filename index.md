---
layout: slides
title:  A title for this block of slides
---

{% include title_slide.md %}

# Slide deck

To create a new **slide deck**, create a file with extension `.md`
and the following YAML header:

``` md
---
layout: slides
title:  ...deck title...
---
```

Within that file, each slide consists of a level 1 header (`#`,
optional) followed by the content of the slide.

Different slides are **separated** by a line beginning with `---`.

---
# First slide

The first slide is usually different, as it provides information
about the collection it belongs to and the slide deck it begins. To
include this slide in a slide deck use

``` md
{% raw %}{% include title_slide.md %}{% endraw %}
```

As we have seen, the `title` field in the YAML header of the slide
deck can be used to specify the title of the deck. Further
customization is possible by editing the file `title_slide.md` in
the `_includes` folder.

---
# Inline math

**Mathematical formulas** such as $\sin\alpha^2$ can be used in the
text by enclosing the corresponding `LaTeX` markup within `$`.

``` tex
**Mathematical formulas** such as $\sin\alpha^2$ can be
used in the text by enclosing the corresponding `LaTeX`
markup within `$`.
```

---
# Displayed math

**Displayed formulas** must occur in a paragraph of their own
enclosed by `` `$$ `` and `` $$` `` (note the *extra backtick*
before and after the `$$`).

For example, the formula

`$$
  \int_0^\infty f(x)
$$`

is obtained with

``` tex
`$$
  \int_0^\infty f(x)
$$`
```

---
# Code

Displayed code must be enclosed by three backticks. The opening
sequence of backticks is followed by the name of the programming
language in which the code is written.

## Example of Java method

```java
public static int fibo(int n) {
	return n <= 1 ? n : fibo(n - 1) + fibo(n - 2);
}
```

## Example of Haskell function

``` haskell
fibo :: Int -> Int
fibo 0 = 0
fibo 1 = 1
fibo n = fibo (n - 1) + fibo (n - 2)
```
