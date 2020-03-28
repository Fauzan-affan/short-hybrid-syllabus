# Adding Opacity Effect

Pada pembahasan kali ini, kita akan mencoba menambahkan sebuah efek-efek keren menggunakan CSS menggunakan `opacity`. Rencananya kita akan membuat semua image yang ada menjadi agak gelap sebelum `hover`, dan menjadi lebih terang ketika di-`hover`. Sebelum kita masuk ke pembahasan, pastikan teman-teman sudah merubah isi dari masing-masing images, dengan image yang berbeda. Pada contoh kali ini saya hanya menggunakan beberapa image yang sama supaya menghemat waktu pengerjaan reading ini, jadinya seperti ini:

![img](img/1.png)

## Adding New Class for Opacity

Okay, sekarang kita butuh menambahkan custom class untuk mentarget masing-masing foto yang ada, supaya bisa kita tambahkan `opacity` di dalamnya. Class ini teman-teman bebas mau kasih nama apa. Di sini saya menggunakan class dengan nama `item` saja. Selanjutnya, kita tambahkan di setiap `<div>` pembungukus element `<a>` kita. contohnya seperti berikut:

![img](img/2.png)

Contoh sintak untuk Front End Basic Specialization gallery:

```html
<div class="gallery px-6 mb-12">
    <h2 class="text-gray-500 mb-1">Front End Basic Specialization Gallery</h2>
    <div class="flex items-center">
        <div class="item shadow-xl mr-6">
            <a href="#"><img src="@/assets/gallery.jpg" alt="gallery"></a>
        </div>
        <div class="item shadow-xl mr-6">
            <a href="#"><img src="@/assets/gallery.jpg" alt="gallery"></a>
        </div>
        <div class="item shadow-xl mr-6">
            <a href="#"><img src="@/assets/gallery.jpg" alt="gallery"></a>
        </div>
        <div class="item shadow-xl mr-6">
            <a href="#"><img src="@/assets/gallery.jpg" alt="gallery"></a>
        </div>
        <div class="item shadow-xl mr-6">
            <a href="#"><img src="@/assets/gallery.jpg" alt="gallery"></a>
        </div>
    </div>
</div>
```

Lakukan hal yang sama pada bagian sisanya, yaitu **Front End Framework Specialization Gallery, Backend Specialization Gallery, Data Analytics Specialization, dan Machine Learning Specialization**.

> ***Tips & trick:*** Kamu bisa melakukan masive selection di vscode dengan cara: 1. Block satu kalimat yang mau kamu select 2. Tekan `command` + `d` pada macOs, atau `ctr` + `d` pada windows

Oya, biar lebih oke, kita tambahkan juga class `item` di bagian categori ya! Sama seperti sebelumnya kita akan tambahkan di setiap pembungkus element `<a>` untuk setiap kategori yang kita punya. Contohnya seperti ini:

![img](img/3.png)

```html
<div class="w-1/5 px-4 item">
    <a href="#" class="bg-gray-800 h-32 flex justify-center items-center rounded-lg border border-gray-700 p-4 hover:bg-gray-900 shadow-custom">
        <img src="@/assets/febs.svg" alt="FEBS">
    </a>
</div>
<div class="w-1/5 px-4 item">
    <a href="#" class="bg-gray-800 h-32 flex justify-center items-center rounded-lg border border-gray-700 p-4 hover:bg-gray-900 shadow-custom">
        <img src="@/assets/fefs.png" alt="FEFS">
    </a>
</div>
<div class="w-1/5 px-4 item">
    <a href="#" class="bg-gray-800 h-32 flex justify-center items-center rounded-lg border border-gray-700 p-4 hover:bg-gray-900 shadow-custom">
        <img src="@/assets/besn.png" alt="BESN">
    </a>
</div>
<div class="w-1/5 px-4 item">
    <a href="#" class="bg-gray-800 h-32 flex justify-center items-center rounded-lg border border-gray-700 p-4 hover:bg-gray-900 shadow-custom">
        <img src="@/assets/dasn.png" alt="DASN">
    </a>
</div>
<div class="w-1/5 px-4 item">
    <a href="#" class="bg-gray-800 h-32 flex justify-center items-center rounded-lg border border-gray-700 p-4 hover:bg-gray-900 shadow-custom">
        <img src="@/assets/mlsn.png" alt="MLSN">
    </a>
</div>
```

## Adding Opacity

Selanjutnya, buka file `main.css` yang terdapat pada folder `css`, dan tambahkan:

```css
.item {
    opacity: 0.5;
}

.item:hover {
    opacity: 1;
}
```

Setelah bagian terakhir dari `@tailwind utilities;`:

![img](img/4.png)

Save dan run, lalu coba lihat di browser:

Sebelum di-hover:

![img](img/5.png)

Ketika FEFS kategori di-hover:

![img](img/6.png)
