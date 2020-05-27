Title: Menghitung Pi
Date: 2014-02-02 06:54
Author: mico
Tags: belajar, python
Slug: menghitung-pi
Status: published

<div>

Wah, lama tidak menggunakan Python, otak terasa buntu. Soal yang perlu dipecahkan sederhana: hitunglah *Pi* menggunakan [Wallis Formula]{.underline}:

</div>

<div>

\

</div>

::: {.separator style="clear: both; text-align: center;"}
\
:::

<div>

setelah 1 jam mencoba, maka saya menemukan potongan kode yang saya rasa betul:

</div>

<div>

\

</div>

<div>

``` {style="text-align: left;"}
In [50]: pi = 2 * reduce(lambda x,y: x*y, [(4.0*i**2)/(4.0*i**2-1) for i in xrange(1,1000)])
In [51]: pi
Out[51]: 3.1408069608284657
```

Wah, ternyata lebih ribet dari yang saya kira pada awalnya. Namun *cool*... kita dapat menghitung *Pi* hanya dengan **satu baris kode** yang melibatkan *fungsi built-in reduce*, *lambda*, serta *list comprehension*. Yang baru saya pelajari dan gunakan adalah fungsi *reduce*. Potongan penjelasan mengenai fungsi *reduce* dari *help* Python:\
\
```{=html}
<dt id="reduce" style="background-color: #fbe54e; font-family: sans-serif; font-size: 16px;">
```
`reduce`{.descname style="background-color: transparent; font-size: 1.2em; font-weight: bold; padding: 0px 1px;"}`<big>`{=html}(`</big>`{=html}*function*, *iterable*[\[]{.optional style="font-size: 1.3em;"}, *initializer*[\]]{.optional style="font-size: 1.3em;"}`<big>`{=html})`</big>`{=html}[](http://docs.python.org/2/library/functions.html#reduce "Permalink to this definition"){.headerlink}
```{=html}
</dt>
```
[Apply]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}[ ]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}*function*[ ]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}[of two arguments cumulatively to the items of]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}[ ]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}*iterable*[, from left to right, so as to reduce the iterable to a single value. For example,]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}`reduce(lambda x, y: x+y, [1, 2, 3, 4, 5])`{.docutils .literal style="background-color: #ecf0f3; font-size: 0.95em; line-height: 20.8px; padding: 0px 1px; text-align: justify;"}[ ]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}[calculates]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}[ ]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}`((((1+2)+3)+4)+5)`{.docutils .literal style="background-color: #ecf0f3; font-size: 0.95em; line-height: 20.8px; padding: 0px 1px; text-align: justify;"}[. The left argument,]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}[ ]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}*x*[, is the accumulated value and the right argument,]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}[ ]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}*y*[, is the update value from the]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}[ ]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}*iterable*[. If the optional]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}[ ]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}*initializer*[ ]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}[is present, it is placed before the items of the iterable in the calculation, and serves as a default when the iterable is empty. If]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}[ ]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}*initializer*[ ]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}[is not given and]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}[ ]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}*iterable*[ ]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}[contains only one item, the first item is returned.]{style="background-color: white; font-family: sans-serif; font-size: 16px; line-height: 20.8px; text-align: justify;"}\
\

</div>

```{=html}
</p>
```
