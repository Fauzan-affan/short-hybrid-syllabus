# Pengenalan Tipe Data Javascript

Data itu sendiri terdiri dari beragam jenis, mulai dari angka, teks, hingga data yang kompleks seperti **array** dan **objek**.

Agar memudahkan pemrosesan, *Javascript* membedakan data menurut sifatnya atau dikenal sebagai tipe data. Secara garis besar, tipe data dalam *Javascript* terdiri dari 2 kelompok, yakni **tipe data primitif (*primitive type*)**, dan **tipe data objek**.

## Perbedaan Tipe Data Primitif dan Tipe Data Objek

Tipe data primitif disebut demikian karena tipe data ini “sederhana” dan hanya terdiri dari 1 nilai. Di dalam *Javascript* terdapat 6 tipe data primitif:

1. Number
2. String
3. Boolean
4. Null
5. Undefined
6. Symbol

Selain dari tipe data ini, adalah _object_. _Object_ bisa disebut sebagai tipe data “khusus” yang prilaku dan isinya bermacam-macam.
Adapun tipe data _object_ bawaan *Javascript* adalah:

1. Array
2. Date
3. RegExp
4. Map dan WeakMap
5. Set dan WeakSet

Pada kesempatan kali ini kita akan fokus kepada **tipe data primitif** khususnya _Number_, _String_, dan _Boolean_.

## Tipe Data Number

Tipe data _number_ adalah **tipe data yang berisikan angka**, baik itu angka bulat seperti 1, 5, 1000, -99, maupun angka pecahan seperti 1.55, 3.14, 0.0009.

JavaScript merupakan bahasa pemrograman yang cukup unik, karena tidak membedakan tipe data angka bulat dengan angka pecahan. Di dalam JavaScript, angka bulat dan pecahan digabung ke dalam tipe data number.

```js
var foo = 100;
var bar = -5000;
var baz = 0.66634;

console.log(foo); // 100
console.log(bar); // -5000
console.log(baz); // 0.66634
```

### Bilangan Desimal, Biner, Oktal, dan Heksadesimal

Angka yang kita gunakan sehari-hari menggunakan basis 10, atau dalam matematika dikenal sebagai **bilangan desimal**. Bilangan desimal adalah angka yang disusun dari 10 digit karakter, yakni angka 0, 1, 2, 3 sampai 9. Selain bilangan desimal, dikenal juga **bilangan biner** (basis 2), oktal (basis 8), dan **heksadesimal** (basis 16).

**Bilangan biner** adalah angka yang digitnya hanya 2 buah, yakni 0 dan 1. Sebagai contoh, angka 18 desimal jika dikonversi ke dalam bentuk angka biner menjadi 10010.

Bilangan oktal adalah angka yang digitnya hanya 8 buah, yakni 0, 1, 2, .. 7. Sedangkan bilangan heksadesimal adalah angka yang digitnya terdiri 16 digit, yakni angka 0 sampai 9, kemudian ditambah dengan huruf A, B, C, D, E, dan F.
JavaScript mendukung penulisan bilangan biner, oktal dan heksadesimal. Berikut contoh peng- gunaannya:

```js
var foo;
foo = 999; // angka desimal
console.log(foo); // 999

foo = 0b1111100111; // angka biner
console.log(foo); // 999

foo = 01747; // angka oktal
console.log(foo); // 999

foo = 0o1747; // angka oktal
console.log(foo); // 999

foo = 0x3e7; // angka heksadesimal
console.log(foo); // 999
```

Untuk membuat bilangan biner, diawali dengan angka 0, kemudian diikuti dengan huruf b, contohnya 0b1111100111, yang artinya saya ingin membuat angka biner 1111100111.

Untuk membuat bilangan oktal, diawali dengan angka 0, atau 0o (angka nol dan dengan huruf ‘o’ kecil) seperti 01747 atau 0o1747. Ini artinya saya ingin membuat bilangan oktal dengan angka 1747.
Untuk membuat bilangan heksadesimal, diawali dengan angka 0 dan huruf ‘x’, seperti 0x3E7, yang artinya angka 3E7 dalam format heksadesimal.

Sebagaimana yang terlihat, walaupun saya mengisi variabel foo dengan bilangan biner, oktal dan heksadesimal, ketika di tampilkan angka-angka ini dikonversi otomatis oleh JavaScript ke bentuk desimal. Dengan kata lain, ketiga sistem bilangan ini hanya diproses secara internal oleh JavaScript.

## Tipe Data String

Tipe data _string_ adalah sebutan untuk **data yang berisi teks**, seperti "hello", "nama kamu", "andi" atau "i". JavaScript mendukung pembuatan string menggunakan tanda kutip satu ( ' ) maupun tanda kutip dua ( " ). Berikut contohnya:

```js
var foo;
foo = "Hello World"; // Hello World
console.log(foo);

foo = "Sedang belajar JavaScript"; // Sedang belajar JavaScript
console.log(foo);

foo = "199";
console.log(foo); // 199 (string)
```

Contoh terakhir cukup menarik. Dengan menambahkan tanda kutip, variabel foo berisi string 199, bukan tipe data number 199. Jika yang dimaksud adalah angka 199, hapus tanda kutip dari string tersebut.

Kita juga bisa mencampur penggunaan tanda kutip untuk membuat string, seperti contoh berikut:

```js
var foo;
foo = "Hari Jum'at";
console.log(foo); // Hari Jum'at

foo = 'Dia berkata: "aku sedang belajar JavaScript"';
console.log(foo); // Dia berkata: "aku sedang belajar JavaScript"

foo = "Let's go!";
console.log(foo); // Let's go!
```

Syarat dari penulisan seperti ini adalah, tanda kutip yang digunakan sebagai penanda string tidak boleh muncul di dalam string. Jika saya menggunakan tanda kutip dua untuk membuat string, maka yang boleh muncul hanya tanda kutip satu. Begitu juga sebaliknya.
Saya tidak bisa membuat string berikut:

```js
var foo;
foo = 'Hari Jum'at';
console.log(foo); //error!

foo = "Dia berkata: "aku sedang belajar JavaScript"";
console.log(foo); //error!
```

## Tipe Data Boolean

Tipe data _Boolean_ adalah **tipe data yang hanya mempunyai dua nilai**, yakni **true (benar**) atau **false (salah)**. Tipe data *boolean* sering digunakan untuk membuat alur logika program. Struktur logika seperti _if_, _else_, _while_, dan _do while_, membutuhkan nilai *boolean* sebagai ‘pengontrol’ alur program. Struktur logika ini akan saya bahas dalam bab terpisah.

Berikut contoh pembuatan tipe data *boolean* di dalam JavaScript:

```js
var foo = true;
var bar = false;

console.log(foo); // true
console.log(bar); // false
```

Sama seperti penulisan *keyword* lain di dalam JavaScript, nilai *boolean* ini harus ditulis dalam huruf kecil, tidak boleh dengan huruf besar. Kode berikut akan menghasilkan error:

```js
var foo = TRUE;
var bar = False;

console.log(foo); // ReferenceError: TRUE is not defined
console.log(bar); // ReferenceError: False is not defined
```

Tipe data *boolean* juga bisa didapat dari hasil operasi perbandingan. Misalkan apakah variabel a sama dengan b, atau apakah a lebih besar dari b.
