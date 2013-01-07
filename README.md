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

Panduan Umum Penulisan
----------------------

1. Sementara ini, semua isi buku ditulis dalam file `content/01-isi.md`. 
   Nantinya bila file ini sudah terlalu besar, akan dipecah sesuai babnya.

2. Gambar/screenshot diletakkan di folder `resources/images`

3. Untuk memudahkan merge, harap ikuti panduan workflow di bawah

Workflow Kontribusi
-------------------

1. Fork dulu repository ini ke akun Anda. Setelah itu clone ke local, 
   kemudian tambahkan remote repository yang mengarah ke repo saya.
   Link ke repo saya ini diperlukan untuk sinkronisasi dengan pekerjaan orang lain.

2. Jangan commit di `master` supaya mudah integrasi dengan orang lain. 
   
3. Buatlah branch baru sesuai topik yang Anda kerjakan, misalnya diberi nama `penjelasan-firebug`, `bab-2`, dsb.

4. Pisahkan edit untuk masing-masing topik pada branch masing-masing. 
   Edit untuk bab 3 jangan dicampur dengan edit untuk bab 4.

5. Bila Anda merasa pekerjaan sudah selesai, kirimkan pull request untuk branch yang memuat pekerjaan Anda.
   Nanti saya mungkin akan meminta revisi agar sesuai dengan aturan penulisan dan sebagainya. 
   Lakukan revisi tersebut di branch Anda sendiri, setelah selesai, kirim pull request lagi.

6. Bila ingin mengupdate repo Anda dengan pekerjaan orang lain, pindah ke master, lalu pull master dari repo saya.
   Setelah itu Anda bisa merge atau rebase semua branch lokal Anda dengan master yang baru 
   supaya pekerjaan orang lain bisa terlihat di repository Anda.
