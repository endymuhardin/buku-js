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

~~~~ {.html}
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

Perhatikan conntoh dibawah ini :

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
4. Nama varaibel tidak boleh menggunakan kata - kata yang merupakan perintah atau kata kunci dalam JavaScript.

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

Pemahaman _function_ pada JavaScript sangat penting. Perlu diingat bahwa
_function_ di JavaScript adalah _object_.

_Object_ pada JavaScript memiliki karakteristik sebagai berikut:
- dapat di- _assigned_ ke variabel, elemen array, atau ke properti milik _object_ lain
- dapat di- _passed_ sebagai argumen ke _function_
- dapat dikembalikan ( _return_ ) dari _function_
- dapat memiliki properti yang bisa dibuat secara dinamis
- dapat dibuat melalui literal (contohnya: {} adalah object di JavaScript)

_Function_ mewarisi segala karakteristik _object_ tersebut, oleh karena itu 
_function_  disebut sebagai _first-class object_.

Selain karakteristik di atas, _function_ juga punya kelebihan yaitu bisa 
di _invoke_ (dipanggil untuk menjalankan rutin yang ada di dalam _function_).
Pemanggilan _function_ ( _function invocation_ ) juga terkadang bisa dilakukan
dengan cara asinkron ( _asynchronous_ ), misalnya dalam kasus menangani event AJAX
(AJAX _event handler_). Perhatikan contoh di bawah ini.

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

_Coba ingat lagi topik Context di http://ejohn.org/apps/learn/#22_

### Immediate Function ###

## Object ##

## Prototype ##

## Inheritance ##

# DOM Programming #

## Apa itu DOM? (sejarah-singkat-ngebut)

Document Object Model adalah API (Application Programming Interface) pada dokumen HTML dan XML. Representasi struktural pada dokumen yang memungkinan kita untuk memodifikasi konten dan penampilan visual (style document). Secara garis besar, DOM menjembatani interaksi pemrograman script dengan dokumen pada halaman web.  

Dibawah komunitas internasional W3C yang dibentuk tahun 1994, Netscape, Microsoft dan perusahaan lain mengimplementasi standard baku pemrograman pada browser. 

Versi awal "ECMAScript" dirilis pada 1997 menjadi standard untuk Javascript, JScript dan ActionScript. Tidak lama setelah itu, akhir 1998 W3C juga mulai mestandarkan DOM.

Tahap Awal standard DOM untuk web browser dikenal sebagai "DOM Level 1".

"DOM Level 2" diperkenalkan pada akhir tahun 2000. Mengusung *method* `getElementById` yang sangat terkenal dan juga *event model*.

"DOM Level 3" yang rilis sejak tahun 2004, masih menjadi kurikulum terkini bagi browser modern saat ini. Mengedepankan teknologi *XPath* dan *event handling* pada keyboard.

## Javascript dan DOM

> Masihh binun, kk.., Lalu apakah DOM adalah bahasa pemrograman yang baru?

Jelas, bukan; tahan disitu. Bukan juga artinya yang sudah lama; DOM bukanlah bahasa pemrograman, melainkan suatu model. Tanpa DOM, pemrograman script kehilangan model untuk mendapatkan dan memanipulasi elemen pada halaman web.

Lebih lanjut interaksi javascript dan DOM akan kita uraikan dalam pembahasan Manipulasi DOM.

## DOM Structure, InnerHTML, InnerText, Attribute, etc ## 

### DOM Structure

Setiap elemen pada dokumen web adalah suatu node yang terkait satu sama lain tergabung membentuk gugusan `object` dengan hirarki yang terstruktur seperti *pohon*.

Ketika kita menulis suatu kode HTML, konten yang kita buat adalah suatu `Node` yang akan termuat pada suatu `Node` lainnya.

Indentasi markup bisa diterapkan pada penulisan kode HTML,. Hal ini mempermudah pembacaan kode dan tidak memberikan pengaruh yang berarti dari output hasil render browser.


Untuk mengetahui bagaimana browser melakukan proses parsing membentuk model DOM silahkan cekidot di [mari](http://www.html5rocks.com/en/tutorials/internals/howbrowserswork/#Parsing_general), secara umum menjelaskan bagaimana markup HTML dibawah ini di terjemahkan:

~~~~ {.html}
<!DOCTYPE html>
<html lang="en">
<head>
<title>HALO DUNIA</title>
</head>
<body>
<!-- Isi kontent disini-->
</body>
</html>
~~~~

Saat kode HTML sederhana diatas diterima dan diproses oleh browser akan terbentuk sebuah dokumen berisi struktur `nodes` dalam format pohon. Dalam contoh ini, digunakan DOM Inspector dari browser Opera, Dragonfly.

![halo-dunia](./resources/images/bab5/pic1-halodunia-o "Halo Dunia")
Gambar 1

Seperti terlihat pada gambar, elemen-elemen pada dokumen yang terbentuk pada browser ditampilkan dalam struktur hirarki node dengan format pohon.

Node `document` disebut sebagai root yaitu *parent* teratas bagi semua elemen yang ada pada dokumen. 
Node `head` memiliki sebuah childNode yaitu `title`; Node `title` juga memiliki child yaitu node dengan tipe `Text` bernilai "*HALO DUNIA*", dst.

Object lain yang juga terlibat disini adalah DOM `window`. Object `window` merepresentasikan window itu sendiri. Object `window` dan `document` adalah variable global yang dapat diakses dari script pada dokumen.

Salah satu property dari `window` adalah `document` yang menunjuk kepada DOM  `document` yang sedang diload pada window tersebut.

Lebih detail perhatikan potongan kode HTML berikut:

~~~~ {.html}
<a id="link-google" class="links" href="http://www.google.co.uk/">google</a>
~~~~

Interface HTML diatas berupa tag __A__, menghasilkan sebuah link ketika diterima browser sebagai bagian dari sebuah dokumen.

Elemen node diatas memiliki sebuah child bertipe `Text` bernilai "google", juga dikenali memiliki beberapa attribute, diantaranya *id*, *class*, *href*. 



### Object `Node` types

Klasifikasi dari semua tipe node terdapat pada property object `Node`.

~~~~ {.html}
<script>
  for(tipe in Node)
    console.log(tipe + " = " + Node[tipe]);
/* # result from console #
ELEMENT_NODE = 1
ATTRIBUTE_NODE = 2
TEXT_NODE = 3
CDATA_SECTION_NODE = 4
ENTITY_REFERENCE_NODE = 5
ENTITY_NODE = 6
PROCESSING_INSTRUCTION_NODE = 7
COMMENT_NODE = 8
DOCUMENT_NODE = 9
DOCUMENT_TYPE_NODE = 10
DOCUMENT_FRAGMENT_NODE = 11
NOTATION_NODE = 12
DOCUMENT_POSITION_DISCONNECTED = 1
DOCUMENT_POSITION_PRECEDING = 2
DOCUMENT_POSITION_FOLLOWING = 4
DOCUMENT_POSITION_CONTAINS = 8
DOCUMENT_POSITION_CONTAINED_BY = 16
DOCUMENT_POSITION_IMPLEMENTATION_SPECIFIC = 32
toString = function toString() { [native code] }
*/
</script>
~~~~

Beberapa tipe node yang akan sering kira temui yaitu tipe ELEMENT_NODE dan TEXT_NODE. Konstanta bernilai integer ini dapat digunakan untuk mengindentifikasi tipe node elemen pada dokumen dengan mengembalikannya dari property `nodeType`.

Kita dapat perlihatkan bahwa `object document` adalah Node dengan tipe `DOCUMENT_NODE`.

~~~~ {.html}
<script>
  console.log(document.nodeType == Node.DOCUMENT_NODE);
</script>
~~~~

Setiap node yang ada pada dokumen, termasuk dokumen itu sendiri memperoleh sifat dasar turunan dari object `Node`. Property dan method yang diturunkan tergantung dari tipe elemen.

Berikut ini pewarisan dari beberapa node:

- `Object` &lt; `Node` &lt; `Element` &lt; `HTMLElement` &lt; `HTML[*]Element`
- `Object` &lt; `Node` &lt; `CharacterData` &lt; `Text`
- `Object` &lt; `Node` &lt; `Document` &lt; `HTMLDocument`

~~~~ {.html}
<a href="http://www.google.com/">Google</a>
~~~~


![Google-Link](./resources/images/bab5/pic2-lgoog-o "Halo Google")
Gambar 2

Pada contoh diatas kita miliki suatu link tag **A**. Melalui DOM inspector elemen node ini adalah turunan dari `HTMLAnchorElement`, `HTMLElement`, `Element`, `Node`, `Object`.

### Properties and Method of `Node`

Seperti telah disebutkan, bahwa elemen-elemen pada dokumen adalah suatu `Node` berikut *property* dan *method* yang juga diturunkan dari object `Node` tersebut. Property dan method ini menjadi nilai dan fungsi dasar yang relevan bagi tiap elemen dan dapat digunakan untuk manipulasi dan melakukan DOM programing.

Sub bab ini tidak akan menjelaskan semua *method* dan *properties*. Penjelasan serta penggunaan akan disinggung pada pembahasan selanjutnya, lagi-lagi setelah kita mendefiniskan suatu node.

Beberapa property dan method dari elemen Node yang umum digunakan.

Node properties

- element.`nodeValue`
- element.`nodeName`
- element.`innerHTML`
- element.`parentNode`
- element.`childNodes`
- element.`firstChild`
- element.`lastChild`
- element.`nextSibling`
- element.`previousSibling`

Node Method:

- element.`appendChild()`
- element.`insertBefore()`
- element.`cloneNode()`
- element.`removeChild()`
- element.`replaceChild()`
- element.`setAttribute()`
- element.`getAttribute()`
- element.`addEventListener()`

Document Method:

- `document`.`getElementById()`
- `document`.`getElementsByTagName()`
- `document`.`getElementsByClassName()`
- `document`.`createElement()`

Window Properties:

- `window`.`location`
- `window`.`navigator`
- `window`.`localStorage`

Window Method:

- `window`.`scrollTo()`


---



Beberapa catatan mengenai DOM:

- DOM merupakan hirarki terstruktur dari konten dokumen yang terdiri dari kumpulan nodes. Beberapa tipe DOM nodes diantaranya: `Element`, `Text`, `Document`.
    + Tipe node `Element` adalah setiap elemen yang terdapat pada dokumen. Misalnya suatu link pada halaman web, adalah elemen node dengan *interface* HTML \'&lt;a&gt;\'
    + Tipe node `Text` adalah text yang termuat pada node `Element` pada dokumen.
    + Tipe `Document` adalah dokumen itu sendiri. Ini adalah akar node (root) dari hirarki DOM / struktur pohon.
- Setiap Node DOM adalah suatu *object*.
- Object `window` bersifat sebagai *global object*, dan dapat diakses melalui script sebagai `window` dan selayaknya object, ia memiliki *property* dan *method*.

## Finding Element ##

Terdapat beberapa metode untuk memperoleh elemen node pada dokumen.
Satu hal yang perlu dicermati adalah hasil kembalian dari metode yang digunakan.

__Single Node__

Metode umum yang sering digunakan untuk memperoleh elemen node tunggal:

- `querySelector()`
- `getElementById()`

~~~~ {.html}
<!DOCTYPE html>
<html lang="en">
<head>
<title>HALO DUNIA</title>
</head>
<body>
  <p>Selamat datang</p>
  <a href="http://www.google.com">google</a>
  <p id="penutup">selamat tinggal</p>
<script>
  console.log(document.querySelector("p").textContent)
  console.log(document.getElementById("penutup").textContent)
</script>
</body>
</html>
~~~~

Method `querySelector()` mengembalikan node pertama yang cocok dengan query yang diberikan. Kelebihan yang dimiliki oleh method ini adalah kita dapat menggunakan format standar seperti pada [selector CSS 3](http://www.w3.org/TR/css3-selectors/#selectors).
Sehingga kita dapat memperoleh elemen seperti ini:

~~~~ {.html}
  console.log(document.querySelector("p:last-child").textContent)
~~~~

Lain halnya dengan `getElementById()`, method ini mencari elemen dengan attribut *id* spesifik yang ada pada suatu elemen. Idealnya attribut *id* bagi elemen adalah unik, namun apa yang terjadi jika secara tidak sengaja ataupun disengaja nilai *id* yang sama diberikan pada elemen berbeda? Dalam hal pencarian node dengan menggunakan `getElementById()`, maka node pertamalah yang akan dikembalikan.

Mungkin ada pertanyaan yang sedikit mengusik, mengapa `document`? Bagaimana jika...? Mungkinkah bila...?
Okay mari kita kupas sedikit lebih rinci.

Kita ketahui bahwa `document` adalah suatu `Node`, lebih spesifik boleh dikatakan `document` node merupakan root atau parent bagi semua elemen yang ada di dalam dokumen. Penetapan node parent seperti kita menetapkan lingkup daerah pencarian.
Dan seperti dijanjikan bahwa setiap elemen memiliki method dan property yang diturunkan dari `object Node`, maka

~~~~ {.html}
<!DOCTYPE html>
<html lang="en">
<body>
  <p>Selamat datang</p>
  <div id="kakikaku">
     <p>selamat tinggal</p>
  </div>
<script>
  // definisikan variable parent sebagai suatu node
  var parent = document.querySelector("div");
  console.log(parent.querySelector("p").textContent); // "selamat tinggal"
</script>
</body>
</html>
~~~~

Pencarian node `querySelector()` dengan query "p" diatas kita persempit pada parent node dengan *interface* HTML "div" pertama, sehingga kembalian node pertama yang sesuai untuk query ini memiliki property `textContent` bernilai "*selamat tinggal*", berbeda dengan yang dihasilkan oleh kode dibawah ini:

~~~~ {.html}
 console.log(document.querySelector("p").textContent);
~~~~

Bagaimana dengan method `getElementById()`? Sayangnya method ini tidak diturunkan untuk semua elemen, melainkan hanya node `document`.
Hal ini relevan dengan keadaan ideal yang diharapkan dalam pemberian attribute *id* unik untuk pencarian elemen dengan dengan method ini.

Namun jangan kuatir masih ada method turunan lain yang dinilai cukup powerfull dalam pencarian node.   



__NodeList__

Metode untuk pencarian node dengan kembalian berupa koleksi node:

- `querySelectorAll()`
- `getElementsByTagName()`
- `getElementsByClassName()`

Nilai yang dikembalikan dari method-method ini adalah berupa `NodeList`. 

Mengurai elemen yang dikembalikan berupa `NodeList` mirip seperti kita lakukan pada elemen-elemen dalam suatu `Array`, namun perlu diingat bahwa `NodeList` BUKAN sebuah `Array`. Sehingga method yang terdapat pada `Array` (seperti: forEach, map) tidak bisa diterapkan pada `NodeList`.

~~~~ {.html}
<!DOCTYPE html>
<html lang="en">
<head>
<title>HALO DUNIA</title>
</head>
<body>
  <p>Selamat datang</p>
  <a href="http://www.google.com">google</a>
  <p id="penutup">selamat tinggal</p>
<script>
  var paragraf = document.querySelectorAll("p");
  console.log(Array.isArray(paragraf)); // false
  console.log(paragraf[0].textContent);
</script>
</body>
</html>
~~~~

Kabar baiknya disini, method dengan kembalian berupa `NodeList` seperti diatas diwarisi untuk setiap elemen node. Sehingga pencarian spesifik dibawah parent node tertentu memungkinkan untuk dilakukan.




__XPathResult__

XPath bukanlah method dari constructor `Node`, namun kita akan sedikit bahas bagaimana kita bisa mencari elemen node menggunakan teknik ini. 

Jika `querySelector()` menggunakan query String, pada XPath istilah yang digunakan adalah ekspresi XPath String dengan standar format penulisan yang sedikit berbeda.

XPath (dari akronim XML Path Language) menggunakan sintaks non-XML yang sangat fleksibel menunjuk suatu atau beberapa node pada dokumen berbasis XML. Teknik pencarian dengan XPath merupakan alternatif yang cukup handal menavigasi elemen pada DOM dokumen selain fitur standar yang ada pada DOM Core.

Untuk mengeksekusi XPath memerlukan method `document` yaitu `evaluate()`. Kembalian method ini adalah berupa `object XPathResult`, dan kembalian ini bergantung dari parameter `resultType` yang diberikan.

~~~~ {.html}
<script>
var xpathResult = document.evaluate(
 xpathString, 
 contextNode, 
 namespaceResolver, 
 resultType, 
 result
);
</script>
~~~~

- `xpathString` string mewakili ekspresi xpath yang akan di evaluate
- `contextNode` node yang menentukan parent konteks pencarian. Jika tidak spesifik diberikan, `contextNode` umumnya bernilai `document`.
- `namespaceResolver` fungsi yang akan dilewatkan prefix namespace dan mengembalikan URI namespace yang diasosiasikan dengan prefix yang diberikan tersebut. `null` adalah nilai yang umum diberikan untuk dokumen HTML atau ketika tidak ada namespace spesifik yang diberikan.
- `resultType` integer mewakili tipe hasil yang akan dikembalikan. Beberapa konstan dari constructor `XPathResult` bernilai integer dari 0 s/d 9. 
Lebih lengkapnya silahkan cekidot [named result constant](https://developer.mozilla.org/id/docs/Template:XPathResultConstants)
Akses node yang umum digunakan bisa menggunakan tipe Result `NODE_SNAPSHOT` yang memungkinkan memodifikasi node lebih lanjut pada dokumen.

~~~~ {.html}
<!DOCTYPE html>
<html lang="en">
<body>
  <div>Pada suatu hari...</div>
  <div id="kakikaku">
     <p>selamat tinggal</p>
  </div>
<script>
var nodes = document.evaluate("/html/body//div",
  document,
  null,
  XPathResult.ORDERED_NODE_SNAPSHOT_TYPE,
  null);
/*
* cari pada parent node document, semua elemen DIV.
* hasil akan berupa snapshot koleksi node terurut
*/
var nodeLen = nodes.snapshotLength;
console.log(nodeLen);
for(var i=0; i<nodeLen; i++){
  var node = nodes.snapshotItem(i);
  console.log(node.innerHTML)
}
</script>
</body>
</html>
~~~~

Perlu diketahui `resultType` yang diberikan berupa `ORDERED_NODE_SNAPSHOT_TYPE`, variable `nodes` diatas bukanlah berupa Array melainkan koleksi snapshot (`object XPathResult`). Mengurai elemen pada hasil `XPathResult` dengan `resultType` ini menggunakan method `snapshotItem`.

Lebih ringkas, penulisan ekspresi xpath diatas dapat ditulis seperti dibawah ini:

~~~~ {.html}
<script>
var nodes = document.evaluate("//div",
  document,
  null,
  XPathResult.ORDERED_NODE_SNAPSHOT_TYPE,
  null);
</script>
~~~~

Tipe `resultType` lain bisa juga menggunakan `UNORDERED_NODE_ITERATOR_TYPE` atau `ORDERED_NODE_ITERATOR_TYPE`. Kembalian juga berupa koleksi nodes `XPathResult`, namun untuk mengurai setiap node pada hasil menggunakan metode `iterateNext`.

perhatikan potongan kode-script berikut:

~~~~ {.html}
<script>
nodes = document.evaluate("//div",
  document,
  null,
  XPathResult.ORDERED_NODE_ITERATOR_TYPE,
  null);
/*
* cari pada parent node document, semua elemen DIV.
* hasil akan berupa iterator node terurut
*/
while(node = nodes.iterateNext()){
  console.log(node.innerHTML);
}
</script>
~~~~

Perbedaan yang perlu diketahui disini hasil `XPathResult` dengan `resultType` berupa `ORDERED_NODE_ITERATOR_TYPE` tidak memiliki nilai property `snapshotLength`. Selain itu, sejak hasil ini dikembalikan apabila terjadi modifikasi pada dokumen, koleksi node pada hasil tersebut tidak lagi valid untuk diakses, (Exceptions raised).

perhatikan potongan kode-script berikut:

~~~~ {.html}
<script>
var nodes = document.evaluate("//div",
  document,
  null,
  XPathResult.FIRST_ORDERED_NODE_TYPE,
  null);
/*
* cari pada parent node document, elemen pertama DIV.
* hasil akan berupa snapshot node terurut
*/
var node = nodes.singleNodeValue;
console.log(node.innerHTML);
</script>
~~~~

Pada potongan kode diatas diberikan `resultType` berupa `FIRST_ORDERED_NODE_TYPE`, hasil yang dikembalikan ke nodes memungkinkan kita memiliki property `singleNodeValue` dari constructor `XPathResult`. Nilai ini adalah node pertama yang sesuai dengan pencarian xpath string.

Penggunaan ekspresi path lebih lanjut bisa juga kita melakukannya seperti dibawah ini:

~~~~ {.html}
<script>
var nodes = document.evaluate("//div[@class=\"konten\"]",
  document,
  null,
  XPathResult.ORDERED_NODE_SNAPSHOT_TYPE,
  null);
/*
* cari pada node document, semua elemen DIV
* yang memiliki attribute class "konten".
* hasil akan berupa snapshot koleksi node terurut
*/

</script>
~~~~

Atau cara lain seperti potongan kode berikut:

~~~~ {.html}
<script>
var nodes = document.evaluate("//a[contains(@href, \"google\")]",
  document,
  null,
  XPathResult.ORDERED_NODE_SNAPSHOT_TYPE,
  null);
/*
* cari pada node document, semua elemen A
* yang memiliki attribute href 
* yang mengandung potongan string "google"
* hasil akan berupa snapshot koleksi node terurut
*/

</script>
~~~~

Walau terlihat lebih rumit dari teknik yang ada pada DOM Core, teknik pencarian dengan XPath ini setidaknya memberikan secercah harapan dan keleluasaan dalam mencari dan menggali node elemen pada DOM dokumen.


## Manipulasi DOM

Berbekal pendefinisian node mengunakan beberapa cara dalam pencarian elemen node, kita akan sundul kembali properties dan method dari Node.

Berbagai hal yang memungkinkan kita melakukan perubahan pada DOM atau sekedar mendapatkan nilai tertentu, bahkan menghapus suatu node pada DOM.

### Mendapatkan dan Menetapkan Attribute elemen node

Attribute pada elemen memiliki arti dan tujuan tertentu yang memberikan efek secara langsung atau tidak langsung bagi elemen itu sendiri.

`Object Node` memiliki method `getAttribute()` dan `setAttribute()` untuk memberikan atau mendapatkan suatu attribute pada elemen node.

~~~~ {.html}
<!DOCTYPE html>
<html lang="en">
<body>
  <a title="Pergi ke bulan" href="http://www.google.co.uk">Google</a>
<script>
  var el = document.querySelector("a");
  console.log(el.getAttribute("title"));

  // modifying
  el.setAttribute("title", "Pergi ke Google");
  console.log(el.getAttribute("title"));
</script>
</body>
</html>
~~~~



### Membuat elemen node melalui script

Method yang berperan untuk tujuan kita disini diantaranya:

- `createElement()`
- `cloneNode()`

Okay kedua method diatas mungkin tidak seperti membandingkan apple to apple. Tetapi pada akhirnya kita mampu menghasilkan node baru dengan method-method diatas.

~~~~ {.html}
<!DOCTYPE html>
<html lang="en">
<body>
  <div id="hasil"></div>
<script>
  var parent = document.querySelector("div[id=\"hasil\"]");
  var link = document.createElement("a");
  link.setAttribute("href", "http://kask.us/");
  link.textContent = "Cekibrot!";
  parent.appendChild(link);
</script>
</body>
</html>
~~~~

Variable `parent` diatas ditetapkan sebagai wrapper node yang akan menampung elemen yang akan kita buat.
Elemen yang akan kita buat adalah sebuah link atau dalam interface HTML tag __A__, kita berikan sebagai parameter berupa String untuk method `createElement()`. Karena link ini akan ditujukan ke suatu alamat URL, penambahkan attribute *href* pada elemen menggunakan method `setAttribute()`. Property `textContent` pada elemen bertujuan menampilkan text mewakili child bertipe `Text` bagi elemen link. Langkah terakhir meletakkan elemen ini menggunakan method `appendChild()` relative dibawah `parent` node.

Property `textContent` diatas merupakan salah satu cara membuat child bagi elemen link yang sudah dibuat. Bagaimana dan apa yang membedakannya dengan property lain seperti `innerHTML`?

Perbedaan yang cukup berarti bisa dilihat dengan menggantikannya dengan sebaris kode berikut:

```
  link.innerHTML = "<b>Cekibrot!</b>";
```

Dengan property `innerHTML`, text dalam format markup HTML yang diberikan memungkinkan untuk diterjemahkan dan terbentuk menjadi suatu DOM. Dari potongan kode diatas, child node dari elemen link akan berupa elemen node __B__ yang memuat suatu child bertipe `Text`.

Penggunaan property ini dinilai cukup praktis membangkitkan DOM melalui script, namun perlu diperhatikan dan sangat ekstra hati-hati terlebih jika nilai String yang dilewatkan pada property ini bersifat Dinamis.

Potensi serangan [XSS](http://en.wikipedia.org/wiki/Cross-site_scripting) (*cross-site-scripting*) pada halaman web bisa saja berawal dari sini. Sekedar saran 2-sen, sebisa mungkin jika tidak sangat terdesak, hindari penggunaan `innerHTML`, kecuali tahu betul apa yang sedang dilakukan. :)




## Event ##

