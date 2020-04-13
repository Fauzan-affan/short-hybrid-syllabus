# Array Pada Javascript

**Array** merupakan tipe data bentukan yang berisi banyak data. Di dalam JavaScript, **array** juga termasuk ke dalam **Object** yang memiliki berbagai property dan method. Dalam bab ini kita akan fokus membahas tentang **Array** **Object** JavaScript.

Array bisa ditulis menggunakan **object constructor** dengan perintah _new Array()_, maupun dengan penulisan **array literal** menggunakan tanda kurung siku [ ]. Berikut contohnya:

```JS
var foo = new Array("a","b","c","d","e");
 console.log ( typeof foo ); // object
 console.log ( foo ); // Array [ "a", "b", "c", "d", "e" ]

var bar = ["a","b","c","d","e"];
 console.log ( typeof bar ); // object
 console.log ( bar ); // Array [ "a", "b", "c", "d", "e" ]
```

Terlihat kedua cara pembuatan _array_ ini tetap dianggap sebagai object oleh JavaScript. Namun karena lebih praktis dan efisien, cara pembuatan _array_ yang lebih disarankan adalah menggunakan **array literal**, yakni membuat _array_ menggunakan tanda kurung siku [ ].

## Kenapa Kita Butuh Array

Ilustrasi data mahasiswa diatas tersebut adalah salah satu alasan mengapa kita membutuhkan _array_, yaitu karena _array_ dapat menampung lebih dari sebuah nilai, alasan lain kenapa kita menggunakan _array_ adalah:

1. Mempermudah pengelolaan nilai / value/ data. Dengan _array_ kita dapat melakukan penulusuran dan pencarian.
2. Manajemen memori, karena kita tidak perlu lagi membuat variabel yang banyak, cukup dengan sebuah _array_ kita sudah dapat menampung banyak data sekaligus.

## Karakteristik Array

1. _Array_ itu adalah variabel jamak, yang mempunyai banyak elemen dan diacu dengan nama yang sama
2. Kumpulan pasangan key dan nilai / key and value pair. Key adalah index pada _array_ dengan tipe integer yang dimulai dari 0
3. _Array_ pada _JavaScript_ ini tipenya adalah Object, karena **array adalah Object** maka _array_ pada _JavaScript_ memiliki fungsi/method, salah satunya adalah length yang digunakan untuk menghitung jumlah elemen didalamnya.
4. Elemen pada _array_ boleh saja memiliki tipe data yang berbeda.

## Cara Membuat Array pada Javascript

Pada _javascript_, array dapat kita buat dengan tanda kurung siku **([...])**.

Contoh:

```js
var products = [];
```

Maka variabel products akan berisi sebuah array kosong.

Kita bisa mengisi data ke dalam array, lalu setiap data dipisah dengan tanda koma (,).

Contoh:

```js
var products = ["Flashdisk", "SDD", "Monitor"];
```

## Cara Mengambil Data dari Array

Seperti yang sudah kita kethaui, Array akan menyimpan sekumpulan data dan memberinya nomer indeks agar mudah diakses.

**Indeks array** selalu dimauli dari nol 0.

Misalkan kita punya array seperti ini:

```js
var aktivitas = ["Makan", "Minum", "Tidur"];
```

Bagaimana cara kita mengambil nilai "Tidur"?

Jawabannya seperti ini:

aktivitas[2] //-> "Tidur"
Kenapa bukan 3?

> **Ingat: indeks array selalu dimulai dari nol.**

## Array adalah Object

_Array_ pada JavaScript adalah bertipe objek, untuk membuktikannya, mari kita uji _array_ hewan yang telah kita buat pada contoh diatas, caranya adalah tulis tampilkan kedalam console sbb:

```js
console.log(typeOf(hewan));
```

maka yang muncul adalah : **Object**.

Karena _array_ adalah Object, maka akan memiliki memiliki _function_ didalamnya, _function_ yang ada pada _Object_ biasanya kita sebut dengan _method_ (nanti akan kita bahas lebih detil pada saat kita belajar tentang _Object_), salah satu _method_ pada _array_ adalah length yang dapat digunakan untuk mengetahui jumlah elemen yang ada pada _array_.

coba kita tuliskan kode berikut:

```js
console.log(hewan.length);
```

maka hasilnya adalah : **4**, dimana 4 adalah jumlah dari elemen pada _array_ hewan.

> Perhatikan!! Jumlah elemen tidak sama dengan index terakhir pada _array_ tersebut, index terakhir adalah 3, sedangkan jumlah elemennya adalah 4, ini karena nomor index diawali dari 0, bukan 1.

## Array Object Method

**Array Object Method** adalah method yang melekat ke _Array_ Object, bukan hasil instance-nya. Dari web* Mozilla Developer Network* terdapat 3 method dari _Array_ _Object_:

1. Array.from()
2. Array.isArray()
3. Array.of()

Kita hanya akan membahas **method Array.isArray()**, karena method yang lain cukup jarang dipakai.

## Method Array.isArray()

**Method isArray()** digunakan untuk mengecek apakah isi dari suatu variabel berupa _array_ atau tidak. Jika berupa _array_, hasil method ini adalah **boolean true**. Jika bukan _array_, hasilnya **boolean false**:

```js
var c = new Array("x", "y", "z");
var b = ["a", "b", "c", "d"];
var a = "qwerty";
var d = 098765;
var z = false;

console.log(Array.isArray(c)); //true
console.log(Array.isArray(b)); //true
console.log(Array.isArray(a)); //false
console.log(Array.isArray(d)); //false
console.log(Array.isArray(z)); //false
console.log(Array.isArray([4, 5, 6])); //true
```

Dari 5 _variabel_ yang kita buat, yang bernilai **true** hanya c, dan b saja. Karena hanya kedua _variabel_ itulah yang berisi array.

pada baris terakhir, kita juga telah menginput secara langsung **array literal** sebagai argumen method _isArray()_, dan bernilai **true**

## Method filter()

Method `filter()` berfungsi untuk menyaring data dari array.

Parameter yang harus diberikan pada method `filter()` sama seperti method `forEach()`,

yaitu: sebuah fungsi callback.

Contoh:

```js
const angka = [1, 2, 3, 4, 5, 6, 7, 8, 9];

// Kita ambil data yang hanya habis dibagi dua saja
const filteredArray = angka.filter(item => {
  return item % 2 === 0;
});

console.log(filteredArray); // -> [2, 4, 6, 8]
```

Pada contoh di atas, kita memberikan _arrow function_ sebagai fungsi callback yang akan melakukan penyaringan terhadap array.

Sebenarnya kita bisa buat lebih sederhana lagi seperti ini:

```js
const filteredArray = angka.filter(item => item % 2 === 0);
```

## Method forEach()

Salah satu method yang argumennya berupa function adalah _forEach()_. Method _forEach()_ sendiri berfungsi menjalankan sebuah function untuk setiap element array.

Pada bab tentang function, kita telah membahas bahwa function bisa diinput sebagai argumen. Dalam JavaScript, function yang diletakkan sebagai argument dikenal juga dengan istilah **Callback**.

Dikarenakan method pada dasarnya juga merupakan function, maka **Callback** ini adalah cara menginput function ke dalam function (mudah-mudahan anda tidak bingung dengan istilah ini).

Bagi saya pribadi, konsep ini memang sedikit rumit, karena itu kita akan membahasnya secara bertahap.

Method _forEach()_ mirip seperti perulangan _for of_, yakni akan dijalankan sebanyak jumlah element dari array. Namun yang dijalankan disini adalah sebuah function. Berikut contoh dasar penggunannya:

```js
const array = [1, 2, 3, 4, 5];

array.forEach(item => {
  console.log(item); // Output: 1 2 3 4 5
});
```

## Method Map()

Method map() mirip seperti forEach(), dalam artian method ini juga menjalankan sebuah function callback sebagai argument. Bedanya, method map() akan mengembalikan sebuah array baru sebagai hasil callback.
Berikut contoh penggunaannya:

```js
const angka = [1, 2, 3, 4, 5, 6, 7, 8, 9];

// membuat array baru dari array angka untuk memeriksa apakah setiap elemennya bernilai habis dibagi 2 atau tidak
const mapedArray = angka.map(item => item % 2 === 0);
console.log(mapedArray); // output: [false, true, false, true, false, true, false, true, false]

// membuat array baru dari array angka untuk melakukan operasi perkalian 2 pada setiap elemennya
const multipleOfTwo = angka.map(e => e * 2);
console.log(multipleOfTwo); // Output: [2, 4, 6, 8, 10, 12, 14, 16, 18]
```

## Method find()

_Method find()_ dan _findIndex()_ digunakan untuk mencari suatu nilai di dalam array berdasarkan syarat tertentu. Sama seperti method-method sebelumnya, syarat ini dibuat menggunakan **callback**.

Kedua method ini akan langsung berhenti dan mengembalikan nilai yang ditemukan pertama kali ( jika element yang memenuhi syarat lebih dari 1). Method _find()_ akan mengembalikan nilai element array tersebut, sedangkan method _findIndex()_ akan mengembalikan **index** dimana element tersebut ditemukan.
Berikut contoh penggunaanya:

```js
function genap(element) {
  return element % 2 === 0;
  3;
}
var foo = [5, 7, 14, 12, 16];
console.log(foo.find(genap)); // 14
console.log(foo.findIndex(genap)); // 2
var bar = [99, 75, 17, 29, 88];
console.log(bar.find(genap)); // 88
console.log(bar.findIndex(genap)); // 4
```

Disini saya menggunakan function **callback genap()**, yang akan mengembalikan nilai true jika angka yang diuji merupakan angka genap. Perintah foo.find(genap) artinya cari di dalam array foo, apakah ada angka yang memenuhi syarat callback genap() (menghasilkan **true**).

Proses pengujian dimulai dari index pertama hingga terakhir. Apakah 5 % 2 === 0? tidak, lanjut ke element berikutnya. Apakah 7 % 2 === 0? juga **tidak**. Apakah 14 % 2 === 0? benar, function callback genap() akan mengembalikan nilai **true** dan method _find()_ menghasilkan nilai 14.

## Method every()

Method _every()_ digunakan untuk mengecek apakah setiap element array memenuhi syarat tertentu. “Syarat” ini harus kita buat sendiri menggunakan function callback.

Jika seluruh element lolos pemeriksaan callback (hasilnya **true** semua), maka method _every()_ akan mengembalikan nilai **true**. Jika ada salah satu saja nilai element yang **false**, method _every()_ akan mengembalikan nilai **false**.

Sebagai contoh kasus, saya memiliki sebuah array foo. Saya ingin memastikan seluruh element di dalamnya genap. Untuk contoh seperti inilah method _every()_ bisa dipakai:

```js
function genap(element) {
  if (element % 2 === 0) {
    return true;
  } else {
    return false;
  }
}
var foo = [6, 8, 10, 12, 16];
console.log(foo.every(genap)); //true
var bar = [3, 8, 10, 12, 16];
console.log(bar.every(genap)); //false
```

Array bar tidak lolos seleksi karena terdapat angka 3. Angka 3 ini akan menghasilkan nilai **false** dari callback, itulah sebabnya hasil dari bar.every(genap) juga **false**.

## Method some()

Method _some()_ mirip seperti _every()_, tapi syaratnya terbalik. Method _some()_ akan mengembalikan nilai true jika salah satu element saja memenuhi syarat. Dan akan mengembalikan nilai false hanya ketika seluruh element tidak memenuhi syarat.
Mari kita pakai contoh kasus bilangan genap sebelumnya:

```js
const angka = [1, 2, 3, 4, 5];

// mengecek apakah dalam array angka terdapat elemen yang habis dibagi 2
const some = angka.some(item => item % 2);
console.log(some); // Output: true

// mengecek apakah dalam array angka terdapat elemen yang kurang dari 0
const thing = angka.some(item => item < 0);
console.log(thing); // Output: false
```

## Method reduce()

Method ini digunakan untuk memproses total seluruh element array dan menghasilkan 1 nilai akhir. Sebagai contoh, saya ingin menambahkan semua isi array foo, atau ingin mengu- rangkan hasil pangkat dua dari seluruh isi array foo. Inilah yang bisa diproses menggunakan method _reduce()_ dan _reduceRight()_.

Bedanya, pada method reduce() proses akan dimulai dari awal array, sedangkan method _reduceRight()_ di proses dari akhir element array. Hasil kedua method ini hanya 1 nilai akhir. Proses untuk method _reduce()_ dan _reduceRight()_ melibatkan sebuah function callback, dan satu nilai awal (opsional).

Sebagai argumen ke dalam function callback, bisa diisi dengan 4 nilai:

- **Argumen pertama**: sebagai accumulator, atau variabel penampung total.
- **Argumen kedua**: nilai array yang saat ini sedang di proses.
- **Argumen ketiga** (opsional): index array yang saat ini sedang di proses.
- **Argumen keempat** (opsional): berisi seluruh element array.

Sedangkan untuk nilai awal (opsional) diinput setelah penulisan **callback**.

Penjelasan argumen diatas terasa cukup rumit, sehingga ada baiknya kita langsung lihat contoh
kode program:

```js
function tambah(total, angka) {
  return total + angka;
}
var foo = [5, 7, 14, 12, 16];
console.log(foo.reduce(tambah)); // 54
console.log(foo.reduce(tambah, 10)); // 54
console.log(foo.reduceRight(tambah)); // 54
console.log(foo.reduceRight(tambah, 10)); // 64
```

Dalam contoh ini, saya hanya menggunakan 2 buah argumen untuk function callback _tambah()_. Argumen pertama (total) sebagai penampung nilai akumulasi, dan argumen kedua (angka) sebagai penampung element array yang saat ini sedang diproses.

Ketika perintah _foo.reduce(tambah)_ mulai diproses, nilai 5 akan masuk ke dalam argumen total, dan nilai 7 ke dalam argumen angka. Fungsi _tambah()_ akan mengembalikan nilai 5+7 = 12.
