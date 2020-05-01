title: Membuat Blog di GitHub
date: 2020-05-10 19:57
category: Python
tags: python, github
author: msiahaan

# Membuat Blog dengan Pelican di Github

[GitHub](http://github.com) adalah penyedia layanan bagi pemrogram untuk berkolaborasi dalam pengembangan aplikasi. Tim pemrogram dapat meletakkan kode sumber di Github dalam sebuah *repository* dan pemrogram lain dapat berkolaborasi melalui *clone* dari *repository* tersebut.

Selain itu [GitHub](http://github.com) juga menyediakan layanan untuk membuat *website* dari repository yang ada: [GitHub Pages](http://pages.github.com). Dalam tulisan ini saya menuliskan bagaimana saya membuat blog menggunakan [Pelican](http://getpelican.com) (aplikasi membuat halaman web statis) yang kemudian dipublikasikan sebagai halaman web di [GitHub](http://github.com). Tulisan ini merujuk kepada [Run your blog on GitHub Pages with Python](https://opensource.com/article/19/5/run-your-blog-github-pages-python)

## Membuat  *Virtual Environment* untuk Projek Blog

Pertama, saya lebih suka membuat *virtual environment* tersendiri untuk projek blog ini agar tidak bercampur dengan projek lain.

```
$  python -m venv websites
```

## Instalasi Pelican, Markdown dan ghp-import

Kedua, setelah *install* paket yang diperlukan:
1.  [Pelican](http://getpelican.com)
2.  [Markdown](https://pypi.org/project/Markdown/)
3.  [ghp-import](https://pypi.org/project/ghp-import/)

Caranya, pakai ```pip``` dong!
```
$  cd websites
$  source bin/activate
$  pip install Pelican Markdown ghp-import
```

## Membuat Repository untuk Blog di GitHub

Nah, kini waktunya untuk membuat repository untuk projek blog. Sesuai dengan amanat [GitHub Pages](http://pages.github.com) maka repository untuk GitHub Pages harus dinamai ```username.github.io```
![Create Repository][create_repository]


## Membuat Clone dari Repository

Ini keempat ya. Setelah *repository* di GitHub ada, *clone* *repository* ```username.github.io``` di PC/laptop lokal:

```
$  git clone https://github.com/username/username.github.io blog
$  cd blog
```

Selanjutnya, ini tips ampuh yang dari penulis [Run your blog on GitHub Pages with Python](https://opensource.com/article/19/5/run-your-blog-github-pages-python): buat cabang terpisah untuk "bahan dasar" dan "barang jadi". "Bahan dasar" adalah berkas-berkas dalam format Markdown, berkas-berkas konfigurasi dari Pelican. "Barang jadi" adalah berkas-berkas halaman web (```*.html```).

```
$  git checkout -b content
Switch to a new branch 'content'
```
**content** adalah cabang tempat kerja dalam mengedit "barang mentah" sementara "barang jadi"/halaman-halaman web akan ditempatkan di cabang **master**.

## Menjalankan Pelican

Sampailah ke tahap lima: mengkonfigurasi isi dari halam web. Pelican menyediakan skrip untuk mengotomasi proses konfigurasi: ```pelican-quickstart```

```
$ pelican-quickstart
WWelcome to pelican-quickstart v4.2.0.

This script will help you create a new Pelican-based website.

Please answer the following questions so this script can generate the files
needed by Pelican.

    
> Where do you want to create your new web site? [.] 
> What will be the title of this web site? My Blog
> Who will be the author of this web site? username
> What will be the default language of this web site? [en] 
> Do you want to specify a URL prefix? e.g., https://example.com   (Y/n) n
> Do you want to enable article pagination? (Y/n) y
> How many articles per page do you want? [10] 10
> What is your time zone? [Europe/Paris] Asia/Kuala_Lumpur
> Do you want to generate a tasks.py/Makefile to automate generation and publishing? (Y/n) y
> Do you want to upload your website using FTP? (y/N) n
> Do you want to upload your website using SSH? (y/N) n
> Do you want to upload your website using Dropbox? (y/N) n
> Do you want to upload your website using S3? (y/N) n
> Do you want to upload your website using Rackspace Cloud Files? (y/N) n
> Do you want to upload your website using GitHub Pages? (y/N) y
> Is this your personal page (username.github.io)? (y/N) y
Done. Your new project is available /home/users/websites/blog
```

Beberapa hal yang perlu **dijawab**:

1.  Judul/title dari website
2. Penulis/author dari website
3.  Zona waktu, saya mengunakan Asia/Kuala_Lumpur
4.  Upload ke GitHub Pages, "y"


Pelican secara otomatis akan membuat struktur direktori dan berkas konfigurasi yang diperlukan.

```
$  ls

content  Makefile  output  pelicanconf.py  publishconf.py  tasks.py

```

Sampailah kita ke langkah ke-enam: tambahkan berkas-berkas konfigurasi dan direktori buatan Pelican ke cabang **content** , *commit* perubahan dan *push* perubahan di cabang lokal ke repo di GitHub.

```
$ git add .
$ git commit -m 'initial pelican commit to content'
$ git push origin content
```

## Membuat Post Pertama

Setelah melalui persiapan panjang, maka saatnya untuk membuat *post* pertama menggunakan *text editor* favorit: [SublimeText](https://www.sublimetext.com/). Anda bebas menggunakan *editor* yang Anda suka. Post saya tulis dalam format Markdown (Cek ulang: paket Markdown sudah terinstall atau belum).

![First Post][first_post]

Simpan!

## Publish!

Tentu saja selanjutnya adalah memublikasikan *post* perdana saya di [GitHub Pages](http://pages.github.com). Begini caranya:

* Jalankan Pelican untuk membuat halaman web statis di direktori **content**
```
$  pelican content -o output -s publishconf
```

* Gunakan **ghp-import** untuk memuat isi direktori **output** ke cabang **master**
```
$  ghp-import -m "Pelican site ku" --no-jekyll -b master output
```

* *Push* cabang **master** lokal ke repo di GitHub
```
$  git push origin master
```

* *Commit* dan *push* ke cabang **content**
```
$  git add content
$  git commit -m "buat post pertama: Zen of Python"
$  git push origin
```

## Enjoy Aja!

Nah, sekaran waktunya menikmati Blog baru. Buka browser 
```
https://username.github.io
```

Untuk membuat post baru, ulangi langkah-langkah pembuatan *post* serta *publis* di atas. Selamat blogging.


[create_repository]: {static}/images/github-pages-create.png
[first_post]: {static}/images/first-post.png