# Pendahuluan #

## Tentang JavaScript ##

## Penggunaan JavaScript di masa kini ##

### Penggunaan JavaScript di Browser ###

### Penggunaan JavaScript di Mobile ###

### Penggunaan JavaScript di Server ###

## Tentang Buku JavaScript ##


### Mengapa buku ini ditulis ###


### Siapa yang sebaiknya membaca ###


### Bagaimana urutan membacanya ###


### Format penulisan ###

Agar lebih enak dibaca, kita akan membedakan bentuk dan warna tulisan
sebagai berikut. Perintah yang kita berikan pada komputer ditulis
seperti ini.

`git --version`

Hasil yang ditampilkan komputer ditulis seperti ini.

    git version 1.7.4.1

Catatan khusus. Seringkali ada hal penting yang perlu mendapat perhatian
khusus. Ini ditulis di menjorok ke tengah seperti contoh berikut.

> **Note**
>
> Working folder Git mengandung repository lengkap mulai dari revisi
> pertama sampai terbaru.

Berikut contoh kode program HTML.

~~~~ {.xml}
<html>
    <head>
        <title>Halo Dunia</title>
    </head>
    <body>
        <h1>Halo Dunia</h1>
    </body>
</html>
~~~~

Dan ini cara penulisan file konfigurasi

    # Ignore file eclipse
    .settings
    .metadata
    .project
    .classpath
    bin

    # Ignore hasil kompilasi Maven
    target

## Lisensi ##

Buku ini memiliki lisensi Creative Commons Attribution Share Alike
(CC-BY-SA). Artinya, semua orang:

-   bebas menggunakan buku ini tanpa harus membayar, baik untuk
    keperluan non-profit maupun komersil. Anda boleh membuka pelatihan
    berbayar menggunakan buku ini.
-   bebas membagikan buku ini kepada siapa saja.
-   bebas membuat perubahan terhadap isi buku ini.

Semua kebebasan di atas hanya memiliki syarat yaitu tetap harus
menyebutkan nama pengarang yang aslinya. Ini disebut dengan istilah
attribution. Singkatnya, boleh dipakai dan dibagikan asal jangan diakui
sebagai karya sendiri. Selain itu, segala perubahan yang dibuat juga
harus dilisensikan sama dengan buku ini. Ini disebut dengan istilah
Share-Alike. Lebih lanjut tentang lisensi ini bisa dilihat di
[website Creative Commons](http://creativecommons.org/licenses/)

## Tools ##

Buku ini dibuat menggunakan perangkat pembantu :

-   Markdown
    : format text untuk menulis buku
-   Pandoc
    : aplikasi untuk mengkonversi markdown menjadi PDF atau HTML

## Kontribusi ##

Semua orang boleh dan dianjurkan untuk ikut membantu penulisan buku ini.
Bagaimana caranya? Gampang. Ada beberapa pekerjaan yang dapat dilakukan.

### Reviewer ###

Tugasnya adalah memeriksa isi buku dan memberikan koreksi. Apa saja
boleh dikoreksi, mulai dari tanda baca, salah ketik, contoh latihan
tidak bisa dijalankan, apa saja. Kalau ada penjelasan yang kurang jelas
juga boleh dikomentari. Apapun yang bisa membuat buku ini lebih baik.
Hasil review dapat dientri di [halaman Issue di
Github](https://github.com/endymuhardin/buku-js/issues).

### Penulis ###

Bagus sekali kalau Anda ingin menyumbangkan tulisan. Lebih banyak yang
mencerdaskan bangsa lebih baik. Begini caranya. Langsung saja fork repository
`buku-js` ini dan segeralah berkarya. Begitu dirasa sudah memadai,
kirimkan pull request ke saya. Nanti akan saya merge ke repository saya.

# Persiapan #

## Daftar Tools yang dibutuhkan ##

### Chrome Developer Tools

### Firebug ###

### Testacular ###

# Konsep Dasar JavaScript #

## Primitive Data Type ##

## Operators ##

## Arrays ##

## Conditional and Loop ##

# Object Oriented JavaScript #

## Function and Closure ##

Pemahaman _function_ pada JavaScript sangat penting. Perlu diingat bahwa
_function_ di JavaScript adalah _object_.

_Object_ pada JavaScript memiliki karakteristik sebagai berikut:
- dapat di-*assign* ke variabel, elemen array, atau ke properti milik _object_ lain
- dapat di-*pass* sebagai argumen ke _function_
- dapat dikembalikan (*return*) dari _function_
- dapat memiliki properti yang bisa dibuat secara dinamis
- dapat dibuat melalui literal (contohnya: {} adalah _object_ di JavaScript)

_Function_ mewarisi segala karakteristik _object_ tersebut, oleh karena itu 
_function_  disebut sebagai _first-class object_.

Selain karakteristik di atas, _function_ juga punya kelebihan yaitu bisa 
di _invoke_ (dipanggil untuk menjalankan rutin yang ada di dalam _function_).
Pemanggilan _function_ (*function invocation*) juga terkadang bisa dilakukan
dengan cara asinkron (*asynchronous*), misalnya dalam kasus menangani event AJAX
(AJAX *event handler*). Perhatikan contoh di bawah ini.

~~~~ {.js}
function getHandler(data, status, jqXHR){
  // ... detail handler disini
}

jQuery.ajax({
  async: true,
  url: 'http://example.com/ajax/resource/1',
  success: getHandler
});
~~~~


> **Referensi**
> Penjelasan tentang _function_ sebagai _first-class object_ bersumber dari
> buku Secret of the JavaScript Ninja, bab 3.

### Callback Pattern ###

### Returning Pattern ###

### `this` Scope ###

### Immediate Function ###

## Object ##

## Prototype ##

## Inheritance ##

# DOM Programming #

## DOM Structure, InnerHTML, InnerText, Attribute, etc ## 

## Finding Element ##

## Event ##

