title: Sharing Python di PPKBI
date: 2020-05-16 10:09
category: Python
author: msiahaan

Kemarin, saya memberikan sesi pengenalan pemrograman Python kepada rekan-rekan Persekutuan Kaum Bapak GKBI Kuala Lumpur. *Demo Coding* dilakukan menggunakan *Jupyter Notebook*

# Mem-print output


```python
print('Hello, world')

```

    Hello, world


# Menanyakan Input


```python
nama = input('Siapa nama Anda? ')
print(f'Nama Anda {nama}')
```

    Siapa nama Anda? Mico Siahaan
    Nama Anda Mico Siahaan


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

```
