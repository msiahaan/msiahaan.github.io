title: Sesi Sharing PPKBI - Pemrograman Python
date: 2020-05-16 10:53
category: Python
author: msiahaan


Tadi malam, saya memmberikan pengenalan pemrograman Python kepada kaum Bapak Gereja Kristen Berbahasa Indonesia (GKBI) Kuala Lumpur. Demo *coding* menggunakan *Jupyter Notebook*. Notebook kemudian saya *Save As* sebagai file *markdown* sehingga mudah untuk dikonversi menjadi blog.

# Mem-print output

```python
print('Selamat pagi!')

```

    Selamat pagi!


# Menanyakan Input


```python
nama = input('Siapa nama Anda? ')
print('Nama Anda {0}'.format(nama))
```

    Siapa nama Anda? Ando Silaen
    Nama Anda Ando Silaen


# Variabel


```python
nama = 'Mico Siahaan' # string
jumlah_anak = 2    # bilangan bulat
bunga_bank = 0.05  # bilangan float
nama_anak = ['Mathias Siahaan', 'Malakhias Siahaan'] # list
array = (1 , 5, 6, 8, 10)  # tuple
daftar_kata = {'tabo': 'enak', 'mangan': 'makan', 'biang': 'anjing'} # dictionary

print(nama)
print(jumlah_anak)
print(bunga_bank)
print(nama_anak)
print(array)
print(daftar_kata)

```

    Mico Siahaan
    2
    0.05
    ['Mathias Siahaan', 'Malakhias Siahaan']
    (1, 5, 6, 8, 10)
    {'tabo': 'enak', 'mangan': 'makan', 'biang': 'anjing'}


# Angka/Numbers


```python
harga = 1000
diskon = 0.1 #diskon 10%
dibayar = harga * (1-diskon) # dibayar = harga - (1-diskon)

print(f'Jumlah yang perlu dibayar {dibayar}')

```

    Jumlah yang perlu dibayar 900.0



```python
pokok = 1000
bunga_pertahun = 0.04
dibayar = pokok * (1 + bunga_pertahun) ** 3

print(f'Jumlah dibayar setelah 3 tahun {dibayar}')
```

    Jumlah dibayar setelah 3 tahun 1124.864



```python
print(100 / 6)
print(100 % 6)
print(100 + 6)
print(100 - 6)
```

    16.666666666666668
    4
    106
    94


# Strings


```python
nama = 'Mico '
marga = 'Siahaan '
nama_lengkap = nama + marga
print(nama_lengkap)
print(nama * 3)
```

    Mico Siahaan 
    Mico Mico Mico 


# List 


```python
list_anak = ['Mathias', 'Malakhias']
list_keponakan = ['Jojo', 'Ivana']
list_anak_anak = list_anak + list_keponakan
print(list_anak_anak)
list_anak_anak[2] = 'Jonathan'
print(list_anak_anak)
```

    ['Mathias', 'Malakhias', 'Jojo', 'Ivana']
    ['Mathias', 'Malakhias', 'Jonathan', 'Ivana']



```python
anak_sulung = list_anak[0]
print(anak_sulung)
anak_kandung = list_anak_anak[0:2]
print(anak_kandung)
```

    Mathias
    ['Mathias', 'Malakhias']


# Tuples


```python
tuple_anak = ('Mathias', 'Malakhias')
tuple_keponakan = ('Jojo', 'Ivana')
tuple_anak_anak = tuple_anak + tuple_keponakan
print(tuple_anak_anak)
tuple_anak_anak[2] = 'Jonathan'
print(tuple_anak_anak)
```

    ('Mathias', 'Malakhias', 'Jojo', 'Ivana')



    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-13-d216d0a934f0> in <module>
          3 tuple_anak_anak = tuple_anak + tuple_keponakan
          4 print(tuple_anak_anak)
    ----> 5 tuple_anak_anak[2] = 'Jonathan'
          6 print(tuple_anak_anak)


    TypeError: 'tuple' object does not support item assignment


# Dictionary


```python
dict_batak = {'mangan': 'makan', 'tabo': 'enak', 'jabu': 'rumah'}
print(dict_batak['jabu'])

print(dict_batak.keys())
print(dict_batak.values())

dict_batak['tabo'] = 'lezat'
dict_batak
```

    rumah
    dict_keys(['mangan', 'tabo', 'jabu'])
    dict_values(['makan', 'enak', 'rumah'])





    {'mangan': 'makan', 'tabo': 'lezat', 'jabu': 'rumah'}



# Set


```python
list_buah = ['apel', 'jeruk', 'semangka', 'jeruk']
set_buah = {'apel', 'jeruk', 'semangka', 'jeruk'}

print(list_buah)
print(set_buah)
```

    ['apel', 'jeruk', 'semangka', 'jeruk']
    {'jeruk', 'semangka', 'apel'}



```python
buah_favorit = set_buah[1]
print(buah_favorit)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-25-3bfdf3d116bf> in <module>
    ----> 1 buah_favorit = set_buah[1]
          2 print(buah_favorit)


    TypeError: 'set' object does not support indexing


# For


```python
list_angka = [1, 2, 3, 4, 5, 6]
for angka in list_angka:
    print(angka, end=' ')
```

    1 2 3 4 5 6 


```python
tuple_anak_anak = ('Mathias', 'Malakhias', 'Jonathan', 'Ivana')
for anak in tuple_anak_anak:
    print('Nama anak: {0}'.format(anak))
```

    Nama anak: Mathias
    Nama anak: Malakhias
    Nama anak: Jonathan
    Nama anak: Ivana



```python
list_angka = [1, 2, 3, 4, 5, 6]

list_kuadrat = [kucing ** 2 for kucing in list_angka]

print(list_kuadrat)
```

    [1, 4, 9, 16, 25, 36]


# While


```python
angka_awal = 0
angka_akhir = 10
angka = angka_awal
while angka <= angka_akhir:
    print('Angka: {0}'.format(angka))
    angka = angka + 1
```

    Angka: 0
    Angka: 1
    Angka: 2
    Angka: 3
    Angka: 4
    Angka: 5
    Angka: 6
    Angka: 7
    Angka: 8
    Angka: 9
    Angka: 10


# Function


```python
def print_nama(nama):
    print('Selamat pagi {0}'.format(nama))
    print('Sudah makankah?')
    
def luas_kotak(sisi):
    print(sisi*4)
    
    
nama = input('Nama: ')
print_nama(nama)

sisi = int(input('Sisi: '))
print(luas_kotak(sisi))
```

    Nama: Ando Silaen
    Selamat pagi Ando Silaen
    Sudah makankah?
    Sisi: 2
    8
    None



```python
from math import pi

def luas_lingkaran(radius):
    """
    Fungsi untuk menghitung luas lingkaran
    
    Parameter:
    ----------
    radius    : radius/jari-jari dari lingkaran
    """
    return (pi * radius ** 2)

radius = input('Radius lingkaran (cm): ')
luas = luas_lingkaran(int(radius))
print('Luas lingkaran (cm2): {0}'.format(luas))

```

    Radius lingkaran (cm): 5
    Luas lingkaran (cm2): 78.53981633974483



```python
help(luas_lingkaran)
#help(print)
#help(string)

import math

print(math.factorial(20))
```

    Help on function luas_lingkaran in module __main__:
    
    luas_lingkaran(radius)
        Fungsi untuk menghitung luas lingkaran
        
        Parameter:
        ----------
        radius    : radius/jari-jari dari lingkaran
    
    2432902008176640000


# Class 


```python
class Anak:
    """
    Class untuk definisi Anak
    
    Attributes:
    -----------
    nama     : nama anak
    
    Methods:
    ------
    print_nama    : return nama anak
    """
    
    def __init__(self, nama, nama_belakang):
        #inisiasi nama
        self._nama = nama
        self._belakang = nama_belakang
    
    def print_nama(self):
        # Method: nama 
        # return nama
        return self._nama + ' ' + self._belakang

mathias = Anak('Mathias', 'Siahaan')
print(mathias.print_nama())

help(Anak)

```

    Mathias Siahaan
    Help on class Anak in module __main__:
    
    class Anak(builtins.object)
     |  Anak(nama, nama_belakang)
     |  
     |  Class untuk definisi Anak
     |  
     |  Attributes:
     |  -----------
     |  nama     : nama anak
     |  
     |  Methods:
     |  ------
     |  print_nama    : return nama anak
     |  
     |  Methods defined here:
     |  
     |  __init__(self, nama, nama_belakang)
     |      Initialize self.  See help(type(self)) for accurate signature.
     |  
     |  print_nama(self)
     |  
     |  ----------------------------------------------------------------------
     |  Data descriptors defined here:
     |  
     |  __dict__
     |      dictionary for instance variables (if defined)
     |  
     |  __weakref__
     |      list of weak references to the object (if defined)
    


# String Methods


```python
nama = 'mico siahaan'
print(nama.capitalize())
print(nama.title())
print(nama.upper())

list_char = nama.split()
print(list_char)
```

    Mico siahaan
    Mico Siahaan
    MICO SIAHAAN
    ['mico', 'siahaan']


Nice to read [https://docs.python.org/3/library/stdtypes.html#string-methods]

# Errors/Exceptions


```python
list_anak = ['Mathias', 'Malakhias']
list_anak[1] = 'Jojo'
list_anak
```




    ['Mathias', 'Jojo']




```python
int_utang = int(input('Utang pokok: '))
float_bunga = 0.03
float_bayar = int_utang * (1 + float_bunga) ** 2
print("Dibayar: {0}".format(float_bayar))
```

    Utang pokok: 1000
    Dibayar: 1060.8999999999999



```python
class Anak:
    def __init__(self, nama):
        self._nama = nama
    def nama(self):
        return self._nama
    
mathias = Anak('Mathias Siahaan')
mathias.nama()
```




    'Mathias Siahaan'




```python
list_angka = range(200)
for angka in list_angka:
    plus_one = angka + 1
    print(plus_one)
```

    1
    2
    3
    4
    5
    6
    7
    8
    9
    10
    11
    12
    13
    14
    15
    16
    17
    18
    19
    20
    21
    22
    23
    24
    25
    26
    27
    28
    29
    30
    31
    32
    33
    34
    35
    36
    37
    38
    39
    40
    41
    42
    43
    44
    45
    46
    47
    48
    49
    50
    51
    52
    53
    54
    55
    56
    57
    58
    59
    60
    61
    62
    63
    64
    65
    66
    67
    68
    69
    70
    71
    72
    73
    74
    75
    76
    77
    78
    79
    80
    81
    82
    83
    84
    85
    86
    87
    88
    89
    90
    91
    92
    93
    94
    95
    96
    97
    98
    99
    100
    101
    102
    103
    104
    105
    106
    107
    108
    109
    110
    111
    112
    113
    114
    115
    116
    117
    118
    119
    120
    121
    122
    123
    124
    125
    126
    127
    128
    129
    130
    131
    132
    133
    134
    135
    136
    137
    138
    139
    140
    141
    142
    143
    144
    145
    146
    147
    148
    149
    150
    151
    152
    153
    154
    155
    156
    157
    158
    159
    160
    161
    162
    163
    164
    165
    166
    167
    168
    169
    170
    171
    172
    173
    174
    175
    176
    177
    178
    179
    180
    181
    182
    183
    184
    185
    186
    187
    188
    189
    190
    191
    192
    193
    194
    195
    196
    197
    198
    199
    200



```python
angka = 10
if angka > 5:
    print('Lebih dari 5')
else:
    print('Kurang dari 5')

```

    Lebih dari 5



```python

```
Happy Pythoning!