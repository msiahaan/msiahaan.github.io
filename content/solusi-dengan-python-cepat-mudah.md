Title: Solusi dengan Python, Cepat Mudah Membuat CSV: modul CSV
Date: 2011-01-19 15:41
Author: mico@bisukmandiri
Tags: PyQt4, python
Slug: solusi-dengan-python-cepat-mudah
Status: published

Salah satu kelebihkan python yang sangat saya sukai adalah python memiliki koleksi modul yang lengkap dan mencakup berbagai jenis tugas sehingga saya dapat dengan cepat mencari solusi dari  permasalahan yang ada.\
\
Contohnya kemarin akuntan kantor bingung karena dia diminta oleh bank untuk mensubmit file csv yang berisikan data-data untuk transfer payroll/gaji karyawan. Bank mengirimkan template berkas csv yang dapat diimpor oleh sistem bank. Maka dia menerima file csv yang berisikan 41 field, sebagian harus diisi dan sebagian opsional. Setiap field dipisahkan oleh koma (,). Dia mengeluh karena format yang harus dia masukkan bagi dia terasa tidak 'user friendly'. Sudah coba impor dan ekspor file csv menggunakan Excel namun tetap kurang 'nyaman'.\
\
Akhirnya tadi malam berbekalkan modul csv serta PyQt4, saya buatkan antar muka untuk memasukkan data payroll yang kemudian disimpan dalam format csv.\
\
Screenshotnya:\

::: {.separator style="clear: both; text-align: center;"}
[![](http://1.bp.blogspot.com/_n6fub3mZ0JU/TTajLErGu-I/AAAAAAAAAEA/AKkO6CcKdxs/s320/payroll_csv_ui.png){width="320" height="258"}](http://1.bp.blogspot.com/_n6fub3mZ0JU/TTajLErGu-I/AAAAAAAAAEA/AKkO6CcKdxs/s1600/payroll_csv_ui.png)
:::

\
Potongan source codenya:\
\

```{=html}
<script src="https://gist.github.com/786137.js?file=payroll_csv_writer.py"></script>
```
\
\
\
 Sekali lagi, python membantu saya cepat menemukan solusi bagi problem di kantor.

```{=html}
</p>
```
