---
layout: post
title: Text and Typography
author: Harsha S. Bhat
math: true
tags:
  - Website
hide: false
bibliography: /Users/bhat/Dropbox/Public/CollectedPapers/MasterBibliography.bib
csl: /Users/bhat/Dropbox/Public/CollectedPapers/csl/agu.csl

---

This post is to show Markdown syntax rendering.

## Titles
---
# H1 - heading

<h2 data-toc-skip>H2 - heading</h2>

<h3 data-toc-skip>H3 - heading</h3>

<h4>H4 - heading</h4>
---
<br>

## Paragraph

I wandered lonely as a cloud

That floats on high o'er vales and hills,

When all at once I saw a crowd,

A host, of golden daffodils;

Beside the lake, beneath the trees,

Fluttering and dancing in the breeze.

## Lists

### Ordered list

1. Firstly
2. Secondly
3. Thirdly

### Unordered list

- Chapter
	- Section
           - Paragraph

### Task list

- [ ] TODO
- [x] Completed
- Hold on
- [ ] Defeat COVID-19
  - [x] Vaccine production
  - [ ] Economic recovery
  - [ ] People smile again

### Description list

Sun
: the star around which the earth orbits

Moon
: the natural satellite of the earth, visible by reflected light from the sun


## Block Quote

> This line to shows the Block Quote.

## Tables

| Company                      | Contact          | Country |
|:-----------------------------|:-----------------|--------:|
| Alfreds Futterkiste          | Maria Anders     | Germany |
| Island Trading               | Helen Bennett    | UK      |
| Magazzini Alimentari Riuniti | Giovanni Rovelli | Italy   |

## Links

[I'm an inline-style link](https://www.google.com)

[I'm an inline-style link with title](https://www.google.com "Google's Homepage")

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[I'm a relative reference to a repository file](../blob/master/LICENSE)

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself].

URLs and URLs in angle brackets will automatically get turned into links.
http://www.example.com or <http://www.example.com> and sometimes
example.com (but not on Github, for example).

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[link text itself]: http://www.reddit.com


## Footnote

Click the hook will locate the footnote[^footnote], and here is another footnote[^fn-nth-2].


## Images

- Default (with caption)

![Desktop View](/images/posts/mockup.png "Title")
_Full screen width and center alignment_



## Video

{% include video.html id="hMHSsEobbz0" caption="Animation of a supershear rupture" %}

Embed youtube videos as below. You need to get the video id for this.

{% raw %}
```
{% include video.html id="hMHSsEobbz0" caption="Animation of a supershear rupture" %}
```
{% endraw %}


## Mathematics

The mathematics powered by [**MathJax**](https://www.mathjax.org/):

Use standard latex as below.

```latex
$$ \sum_{n=1}^\infty 1/n^2 = \frac{\pi^2}{6} $$
```

$$ \sum_{n=1}^\infty 1/n^2 = \frac{\pi^2}{6} $$

Or in-line latex as below

```
When $$ a \ne 0 $$, there are two solutions to $$ax^2 + bx + c = 0$$ and they are

 $$ x = {-b \pm \sqrt{b^2-4ac} \over 2a} $$
```

When $$a \ne 0$$ , there are two solutions to $$ax^2 + bx + c = 0$$ and they are

 $$ x = {-b \pm \sqrt{b^2-4ac} \over 2a} $$

You can use your personal latex macros by adding a them as below

```latex
$$
\newcommand{\pd}[2]{\dfrac{\partial #1}{\partial #2}}
\begin{equation}
\begin{cases}
\pd{H}{t} + \pd{(Hu)}{y} = 0 \\
\pd{(Hu)}{t}+\pd{(Hu^2)}{y}+gH\pd{\eta}{y} =0
\end{cases}, \quad \quad \quad 0\leq y \leq L, \quad t\geq 0.
\end{equation}
$$
```

$$
\newcommand{\pd}[2]{\dfrac{\partial #1}{\partial #2}}
\begin{equation}
\begin{cases}
\pd{H}{t} + \pd{(Hu)}{y} = 0 \\
\pd{(Hu)}{t}+\pd{(Hu^2)}{y}+gH\pd{\eta}{y} =0
\end{cases}, \quad \quad \quad 0\leq y \leq L, \quad t\geq 0.
\end{equation}
$$



## Inline code

This is an example of `Inline Code`.

## Citation

Citing my own paper [@bhat2004]. @amazigo1977


## Code block

### Common

```
This is a common code snippet, without syntax highlight and line number.
```

### Specific Languages

#### Console

```console
$ env |grep SHELL
SHELL=/usr/local/bin/bash
PYENV_SHELL=bash
```

#### Ruby

```ruby
def sum_eq_n?(arr, n)
  return true if arr.empty? && n == 0
  arr.product(arr).reject { |a,b| a == b }.any? { |a,b| a + b == n }
end
```

#### Shell

```shell
if [ $? -ne 0 ]; then
    echo "The command was not successful.";
    #do the needful / exit
fi;
```

#### Liquid

{% raw %}
```liquid
{% if product.title contains 'Pack' %}
  This product's title contains the word Pack.
{% endif %}
```
{% endraw %}

#### MATLAB

```matlab
% Simple script to plot a cosine
% vector x takes only 10 values
x = linspace(0, 2*pi, 10);
y = cos(x);
plot(x,y)
xlabel('x')
ylabel('cos(x)')
title('Plotting a cosine')
grid on
```

#### Fortran

```fortran
    PROGRAM Triangle
     IMPLICIT NONE
     REAL :: a, b, c, Area
     PRINT *, 'Welcome, please enter the&
              &lengths of the 3 sides.'
     READ *, a, b, c
     PRINT *, 'Triangle''s area:  ', Area(a,b,c)
    END PROGRAM Triangle
    FUNCTION Area(x,y,z)
     IMPLICIT NONE
     REAL :: Area            ! function type
     REAL, INTENT( IN ) :: x, y, z
     REAL :: theta, height
     theta = ACOS((x**2+y**2-z**2)/(2.0*x*y))
     height = x*SIN(theta); Area = 0.5*y*height
    END FUNCTION Area
```
## Reverse Footnote

[^footnote]: The footnote source
[^fn-nth-2]: The 2nd footnote source

# References
