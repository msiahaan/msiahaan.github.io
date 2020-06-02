Title: Menghitung Pi
Date: 2014-02-02 06:54
Author: msiahaan
Tags: python
Category: Python
Slug: menghitung-pi
Status: published


Wah, lama tidak menggunakan Python, otak terasa buntu. Soal yang perlu dipecahkan sederhana: hitunglah *Pi* menggunakan [Wallis Formula](https://en.wikipedia.org/wiki/Wallis_product)setelah 1 jam mencoba, maka saya menemukan potongan kode yang saya rasa betul:


``` 
In [50]: pi = 2 * reduce(lambda x,y: x*y, [(4.0*i**2)/(4.0*i**2-1) for i in xrange(1,1000)])
In [51]: pi
Out[51]: 3.1408069608284657
```

Wah, ternyata lebih ribet dari yang saya kira pada awalnya. Namun *cool*... kita dapat menghitung *Pi* hanya dengan **satu baris kode** yang melibatkan *fungsi built-in reduce*, *lambda*, serta *list comprehension*. Yang baru saya pelajari dan gunakan adalah fungsi *reduce*. Potongan penjelasan mengenai fungsi *reduce* dari *help* Python:

Apply function of two arguments cumulatively to the items of iterable, from left to right, so as to reduce the iterable to a single value. For example, reduce(lambda x, y: x+y, [1, 2, 3, 4, 5]) calculates ((((1+2)+3)+4)+5). The left argument, x, is the accumulated value and the right argument, y, is the update value from the iterable. If the optional initializer is present, it is placed before the items of the iterable in the calculation, and serves as a default when the iterable is empty. If initializer is not given and iterable contains only one item, the first item is returned.

