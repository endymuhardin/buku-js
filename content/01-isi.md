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

### Callback Pattern ###

### Returning Pattern ###

### `this` Scope ###

Pada kebanyakan bahasa pemrograman berorientasi obyek, 
`this` digunakan di dalam _method_ untuk merujuk kepada _class_ dimana _method_
tersebut bernaung -- sederhananya: membangun konteks.

~~~~ {.php}
<?php

  abstract class MahlukHidup {
    abstract public function getType(); 
  }

  class Manusia extends MahlukHidup {
    private $_type = 'Manusia';

    public function getType() {
      return $this->_type;
    }
  }

  class Hewan extends MahlukHidup {
    private $_type = 'Hewan';

    public function getType() {
      return $this->_type;
    }
  }

  $manusia = new Manusia;
  echo $manusia->getType();
?>
~~~~

_Catatan: keknya code PHP-nya di atas ga bagus *dan* kurang bisa mewakili
contoh untuk membandingkan dengan pendekatan Javascript_

Javascript tidak mengadopsi pendekatan seperti di atas. Penggunaan `this` pada Javascript merujuk kepada _caller_ (pemanggil).

~~~~ {.js}
function type() {
  console.log(this.type);
}

function Manusia() {
  this.type = 'Manusia';
  this.getType = type;
}

function Hewan() {
  this.type = 'Hewan';
  this.getType = type;
}

var manusia = new Manusia();
manusia.getType();

var hewan = new Hewan();
hewan.getType();
~~~~

_Catatan: keknya code Javascript di atas juga ga bagus. LOL. Mungkin
harus ulang baca demo-nya jresig lagi_

### Immediate Function ###

## Object ##

## Prototype ##

## Inheritance ##

# DOM Programming #

## DOM Structure, InnerHTML, InnerText, Attribute, etc ## 

## Finding Element ##

## Event ##

