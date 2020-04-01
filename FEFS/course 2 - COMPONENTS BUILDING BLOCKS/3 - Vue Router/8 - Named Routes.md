# Named Routes

Dengan menamai root yang kita punya di `index.js`. Kita juga bisa mengarahkan ke namanya pada `to` di `<router-link>`. Caranya seperti berikut:

* Buka `index.js` dan lihat name untuk route yang mau kita panggil. Misalkan kita ingin memanggil `path: /`, dengan `name: Home`. Pada `App.vue` tinggal kita ubah `to` menjadi seperti berikut:

    > ***Tips & trick:*** Untuk bisa menggunakan cara ini, kita harus membinding `to` menjadi `:to` dan sertakan `{}` didalam tanda petiknya. Sertakan `name: 'namaRoute'`

    ```html
    <router-link :to="{name: 'Home'}">Home</router-link>
    ```

    Save dan coba di browser! Ya, jika berhasil tidak akan ada yang berubah. Yang berbeda hanya penggunaan `name` pada `:to` di `<router-link>` saja.
