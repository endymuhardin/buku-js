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

## Variabel ##

Perhatikan conntoh berikut ini :

~~~~javascript
var x = 2;
var y = 4
var z = x - y;
~~~~

Ingat pelajaran aljabar? dalam aljabar kita menggunakan huruf (seperti x) untuk menyimpan sebuah nilai (seperti 4) dan dari ekspresi matematika z = x - y kita bisa mengetahui bahwa nilai z adalah -2. Lalu apa hubungannya dengan JavaScript, dalam bahasa pemrograman huruf x, y dan z disebut variabel sedangkan 2, 4 dan x -y adalah value atau nilai dari sebuah variabel. Seperti halnya dalam aljabar, variabel juga dapat digunakan untuk menampung nilai - nilai (x = 4) dan sebuah ekspresi (z = x - y) hanya saja memang sebuah variabel tidak hanya bisa menampung nilai atau ekspresi matematika. Jadi dari sini kita dapat menyimpulkan bahwa variabel adalah mekanisme untuk menampung suatu nilai tertentu pada sebuah bahasa pemrograman yang memiliki nama dan nilai.

### Aturan Nama Variabel ###

Dalam penamaan sebuah variabel kita dapat menggunakan huruf seperti x, y, z, w, dll atau sesuatu yang lebih deskriptif seperti nama, umur, alamat, dll. Dalam JavaScript sendiri memiliki sebuah aturan yang baku digunakan dalam penamaan sebuah variabel. Adapun aturannya adalah sebagai berikut :

1. Nama variabel harus diawali dengan huruf
2. Nama variabel bisa juga diawali dengan tanda dolas ($) dan garis bawah (_)
3. Nama varaibel bersifat case sensitif artinya antara Huruf (H besar) dengan huruf (h kecil) adalah kata berbeda.
4. Nama varaibel tidak boleh menggunakan kata-kata yang merupakan perintah atau kata kunci dalam JavaScript.

### Deklarasi Variabel ###

Pada JavaScript secara umum pendeklarasian sebuah variabel adalah sebagai berikut :

~~~~
var nama_variabel = value;
~~~~ 

atau

~~~~
var nama_variabel;
nama_variabel = value;
~~~~

Contohnya adalah sebagai berikut :

~~~~javascript
var kendaraan = "Kijang Innova";

// Atau bisa juga

var cc;
cc = 1989;
~~~~

Selain pada contoh diatas, kita juga dapat mendeklarasikan banyak variabel dalam satu statement seperti berikut :

~~~~javascript
var nama="Nana", age=23, job="administrasi";

// Atau bisa juga

var nama="Nana",
age=23,
job="administrasi";
~~~~

## Primitive Data Type ##

Sama seperti pada pemrograman PHP, JavaScript tidak memiliki tipe data secara eksplisit hal ini karena JavaScript kita bisa mendeklarasikan sebuah variabel tanpa menentukan tipe data yang digunakan. Tetapi meski demikian, terdapat empat tipe data implisit pada JavaScript, antara lain :

1. Numerik, untuk menampung nilai bertipe bilangan,
2. String, untuk menampung nilai bertipe string,
3. Boolean, untuk nilai *true* dan *false*
4. Null, adalah variabel yang tidak di inisialisasi

### Tipe Numerik ###

Pada JavaScript, kita hanya mengenal satu tipe untuk numerik, tetapi bisa ditulis dengan menggunakan koma (decimal) atau tidak. Contohnya adalah sebagai berikut :

~~~~javascript
var x1 = 12.45; // Menggunakan tanda koma (desimal)
var x2 = 1200; // Tidak menggunakan tanda koma (desimal)
~~~~

Selain penulisan seperti diatas, kita  juga bisa menuliskan tipe numerik di JavaScript dengan menggunakan notasi ilmiah atau exponential. Contohnya adalah sebagai berikut :

~~~~javascript
var x1 = 1e6; // 1000000
var x2 = 5e-4; // 0.00005
~~~~

### Tipe String ###

Perhatikan contoh variabel dibawah ini :

~~~~javascript
var nama = "Nama saya Noor Adiana";
var alamat = 'Kramat Jati';
var hari = "Sekarang hari jum'at";
var kalimat = 'Saya sering di panggil "Dulloh"';
~~~~

Dari contoh diatas, kita dapat melihat bahwa tipe string digunakan untuk menampung serangkaian karakter seperti "Noor Adiana" , 'Saya sering di panggil "Dulloh"' , dll. Kita juga melihat bahwa, untuk pendefinisian sebuah string dapat menggunakan tanda kutip ganda ("...") atau juga tanda kutip tunggal ('...'), selain itu kita juga bisa menggunakan tanda kutip dalam rangkaian string selama tidak sama dengan yang mengapit string tersebut, seperti pada "Sekarang hari jum'at" dan 'Saya sering di panggil "Dulloh"'.

### Tipe Boolean ###

Tipe data boolean, seperti halnya pada pemrograman lain, hanya dapat menampung dua buah nilai, yaitu true dan false. Tipe boolean biasanya digunakan pada uji kondisional seperti pada *if*. Contoh tipe data boolean :

~~~~javascript
// bernilai true karena 10 memang lebih besar dari 5
var nilai_true = (10 > 5);

// bernilai false karena 100 tidak sama dengan 10
var nilai_false = (100 == 10);
~~~~ 

### Tipe Null ###

Tipe ini adalah sebuah variabel yang belum di inisiallisaikan atau di beri sebuah nilai, baik itu string, numerik atau boolean. Contohnya adalah sebagai berikut :

~~~~javascript
var nama;
var alamat;
// variabel lainnya disini
~~~~

## Operators ##

## Arrays ##

## Conditional and Loop ##

# Object Oriented JavaScript #

## Function and Closure ##

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

