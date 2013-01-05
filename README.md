Buku JavaScript
--------

TODO : penjelasan tentang buku ini


Cara menggunakan
----------------

Buku ini dibuat dalam format markdown.

Walaupun format markdown didesain untuk bisa dibaca apa adanya, kadangkala kita butuh format lain seperti PDF agar buku ini bisa dicetak. Untuk mengkonversi Markdown menjadi PDF, kita menggunakan aplikasi yang bernama Pandoc.

Lebih lanjut tentang Markdown, Pandoc, dan cara konversinya bisa dibaca di [blog saya](http://software.endy.muhardin.com/aplikasi/membuat-dokumen-dengan-markdown-dan-pandoc/). Sedangkan tata cara penulisan dalam format Markdown bisa dibaca di [Buku Pandoc](http://software.endy.muhardin.com/aplikasi/buku-panduan-markdown-dan-pandoc/).

Cara konversi ke PDF
Untuk mengkonversi buku menjadi PDF, gunakan perintah berikut:

```
pandoc --template resources/artivisi-template.tex --toc -N -o output/buku-js.pdf content/*md
```


Cara kontribusi
---------------
Anda ingin menyumbangkan tulisan? Baguslah kalau begitu.
Caranya gampang,

1. Fork repository ini menjadi repository Anda sendiri
2. Clone ke local untuk diedit
3. Editlah sesuka hati
4. Commit dan push ke repository Anda sendiri
5. Kirim pull request ke saya supaya bisa saya merge ke repository saya

