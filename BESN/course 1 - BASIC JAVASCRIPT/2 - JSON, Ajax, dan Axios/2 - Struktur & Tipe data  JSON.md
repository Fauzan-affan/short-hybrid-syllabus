# Struktur & Tipe Data JSON

Sebuah objek JSON adalah format data ***key:value*** yang biasanya dirender di dalam kurung kurawal. Saat kita bekerja dengan JSON, kita akan sering melihat objek JSON disimpan di dalam sebuah *file* `.json`, tapi mereka juga dapat disimpan sebagai objek JSON atau string di dalam sebuah program.

Sebuah objek JSON terlihat seperti berikut ini:

```json
{
  "first_name" : "Ade Hikma",
  "last_name" : "Tiana",
  "address" : "Jakarta",
  "online" : true,
}
```

Contoh di atas secara umum menggambarkan dua kurung kurawal `{}` di awal dan di akhir dengan pasangan ***key:value*** di antara ke dua tanda kurang. Sebagian besar data yang dipakai di JSON dienkapsulasi di dalam sebuah objek JSON.

Pasangan ***key:value*** memiliki tanda titik dua diantara mereka `"key" : "value"`. Setiap ***key:value*** dipisahkan oleh sebuah koma, sehingga ditengah isi sebuah JSON terlihat seperti in:

- `"key" : "value", "key" : "value", "key": "value"`

Pada contoh di atas, nilai pertama pasangan ***key:value*** kita adalah `"first_name" : "Sammy"`.

**Key JSON** berada di sebelah kiri tanda titik dua. Mereka perlu dibungkus oleh tanda petik dua seperti ini: "key", dan dapat berupa string apapun yang valid. Di dalam setiap objek, *key* haruslah unik. *Key* ini dapat memiliki spasi seperti di "first name", namun menambahkannya akan membuat kita lebih repot saat akan mengaksesnya di proses ngoding sehingga disarankan untuk menggunakna ***underscore*** seperti pada "first_name".

**Value JSON** ada di sebelah kanan tanda titik dua.

Ada enam tipe data dasar yang bisa dipakai untuk mengisinya yaitu:

1. Strings
2. Numbers
3. Objects
4. Arrays
5. Booleans (true atau false)
6. Null

Meskipun di dalam file `.json` kita sering melihat format ini ditulis dalam beberapa baris, JSON juga dapat ditulis disatu baris saja.

```json
{ "first_name" : "Ade", "last_name": "Tiana",  "online" : true, }
```
