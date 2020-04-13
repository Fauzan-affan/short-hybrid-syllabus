# Lockdown Preparation Data Assignment - COURSE 2

Baru-baru ini semua orang takut keluar rumah. Pemerintah menghimbau untuk semua kalangan masyarakat supaya **#DiRumahAja** untuk menghindari penyebarluasan virus Covid-19 yang memakan banyak korban jiwa. Tak jarang masyarakat juga tidak memiliki bahan pangan untuk mempersiapkan keadaan seperti ini.

Bahan pangan, masker, dan sanitizer menjadi langka. Banyak orang kesulitan untuk mendapatkanya. Sebagai seorang backend developer, kita bisa memberikan kontribusi untuk memperkecil gap antara si penjual bahan pangan, masker, dll dan masyarakat di luar sana, dengan **membuat struktur data yang berisi kebutuhan-kebutuhan selama lockdown berlangsung**.

Buatlah sebuah struktur data, yang mendeskripsikan **persediaan selama masa lockdown diberlakukukan**. Persediaan ini bisa dibeli oleh siapapun. Tentu data-data ini sifatnya masih statis kerena kita tidak membuat bagian frontendnya. Contoh data-data yang digunakan untuk lockdown preparation adalah sebagai berikut:

```js
export const data = [
    {
        "topup" : [
            { "icon" : "💸", "price" : 5000000},
            { "icon" : "💸", "price" : 10000000},
            { "icon" : "💸", "price" : 2500000},
            { "icon" : "💸", "price" : 7000000},
            { "icon" : "💸", "price" : 15000000},
            { "icon" : "Don't Want to Top Up", "price" : 0},
        ]
    },
    {
        "food" : [
            { "icon" : "🎁", "name" : "Indomie", "price" : 50000 },
            { "icon" : "🍕", "name" : "Pizza", "price" : 100000 },
            { "icon" : "🍔", "name" : "Hamburger", "price" : 75000 },
            { "icon" : "🥣", "name" : "Cereal", "price" : 75000 },
            { "icon" : "🍗", "name" : "Fried Chicken", "price" : 100000 },
            { "icon" : "🍣", "name" : "Sushi", "price" : 125000 },
        ]
    },
    {
        "essential" : [
            { "icon" : "💊", "name" : "Medicine", "price" : 200000 },
            { "icon" : "💾", "name" : "Data", "price" : 100000 },
            { "icon" : "👘", "name" : "Cloth", "price" : 300000 },
            { "icon" : "🖥️", "name" : "Computer", "price" : 13000000 },
        ]
    },
    {
        "maskandsanitizer" : [
            { "icon" : "😷", "name" : "Mask", "price" : 150000 },
            { "icon" : "👹", "name" : "Devil Mask", "price" : 300000 },
            { "icon" : "🧴", "name" : "Sanitizer", "price" : 150000 },
        ]
    },
    {
        "entertainment" : [
            { "icon" : "🍿", "name" : "Netflix", "price" : 375000 },
            { "icon" : "🏍️", "name" : "Bein Sport", "price" : 1000000 },
            { "icon" : "📻", "name" : "Spotify", "price" : 75000 },
            { "icon" : "🎮", "name" : "FIFA 2020", "price" : 300000 },
            { "icon" : "👨‍👩‍👧‍👦", "name" : "The Sims", "price" : 315000 },
        ]
    },
]
```

Kita bebas menambahkan key dan value lainnya selama data yang dibuat berhubungan dengan persiapan lackdown. Silahkan berimajinasi seperti teman-teman mempunyai sebuah website e-commerce yang menjual apapun untuk persiapan lockdown. Tentu, sebagai backend teman-teman yang merancang data-data apa saja yang digunakan. Jika sudah, save ke dalam file dengan nama `data_lockdown_preparation.js`.
