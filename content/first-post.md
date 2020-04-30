title: Post Pertama di Bangmico Python Blog
date: 2020-04-30 19:57
category: Python
author: msiahaan

# Membuat Blog dengan Pelican di Github

[GitHub](http://github.com) adalah penyedia layanan bagi pemrogram untuk berkolaborasi dalam pengembangan aplikasi. Tim pemrogram dapat meletakkan kode sumber di Github dalam sebuah *repository* dan pemrogram lain dapat berkolaborasi melalui *clone* dari repository* tersebut.

Selain itu [GitHub](http://github.com) juga menyediakan layanan untuk membuat *website* dari repository yang ada. Dalam tulisan ini saya menuliskan bagaimana saya membuat blog menggunakan [Pelican](http://getpelican.com)(aplikasi membuat halaman web statis) yang kemudian dipublikasikan sebagai halaman web di GitHub](http://github.com). Tulisan ini merujuk kepada [Run your blog on GitHub Pages with Python](https://opensource.com/article/19/5/run-your-blog-github-pages-python)

## Membuat  *Virtual Environment* untuk Projek Blog

Pertama, saya lebih suka membuat *virtual environment* tersendiri untuk projek blog ini agar tidak bercampur dengan projek lain.

'''
$ python -m venv websites
'''

## Membuat Repository untuk Blog di GitHub