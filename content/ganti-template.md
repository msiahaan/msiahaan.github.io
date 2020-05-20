title: Mengganti Template Blog
date: 2020-05-20 15:42
category: Python
author: msiahaan

Dalam membuat *blog*, sebagai blogger saya ingin menggunakan template yang berbeda untuk *blog* saya.

Pelican menyediakan beberapa template yang siap untuk digunakan. Koleksi template yang tersedia untuk Pelican dapat ditemukan di [Pelican Themes](http://pelicanthemes.com). Tersedia 127 template yang sedia untuk digunakan.

## Clone Template Repository

Mula-mula saya me-download koleksi template Pelican dari repositori dengan cara melakukan *clone* repositori [Pelican Themes GitHub](https://github.com/getpelican/pelican-plugins). Template saya letakkan di /home/micosiahaan/staticwebsite/websites

Saya pindah ke direktori /home/micosiahaan/staticwebsite/websites

```
$  git clone https://github.com/getpelican/pelican-plugins.git pelican-themes
```

Maka di direktori /home/micosiahaan/staticwebsite/websites akan terbentuk direktori pelican-themes. Direktori pelican-themes berisikan direktori-direktori yang berisikan template.

Kemudian pindah ke direktori yang berisikan projek *blog*. 

## Membuat Link ke Direktori Template

Lanhkah selanjutnya adalah membuat link dari template yang akan saya gunakan. Saya memilih template *bootstrap2* yang berada dalam direktori pelican-themes/bootstrap2

```
$  mkdir -p content/themes
$  ln -s home/micosiahaan/staticwebsite/websites/pelican-themes/bootstrap2 content/themes/bootstrap2
```

## Edit pelicanconf.py

Cari baris yang berisikan variable THEME, dan isikan alamat direktori template

```
#Use other theme
THEME = 'content/themes/bootstrap2'
```
Save, pelicanconf.py dan *VOILA!* template yang baru siap digunakan