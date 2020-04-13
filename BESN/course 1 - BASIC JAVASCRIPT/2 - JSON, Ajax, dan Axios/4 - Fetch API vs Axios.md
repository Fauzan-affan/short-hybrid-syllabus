# Fetch API vs AXIOS

Fetch merupakan (API) atau fungsi dasar untuk meminta sumber daya melalui jaringan Secara dasar berhubungan dengan request & response (permintaan/tanggapan) yang dapat digunakan hampir di semua jenis browser.

## Fetch API

Fetch ini adalah native web API untuk melakukan HTTP Calls dari external network. Saya tidak menyarankan referensi ke Fetch di MDN karena sama sekali dokumentasi yang buruk. Untuk memperdalam Fetch silahkan perbanyak googling karena ngegoogle itu hal yang paling gampang dan gratis. Di sini saya bakalan kasih sedikit contoh simple implementasi AJAX Reques menggunakan Fetch API untuk mendapatkan data yang kita mau:

```js
const url = "https://icanhazdadjoke.com/";
fetch(url, {
  headers: {
    Accept: "application/json"
  }
})
  .then(res => res.json())
  .then(data => console.log(data)); //
```

## Axios

Axios adalah sebuah library open source yang saat ini paling booming untuk melakukan request HTTP karena memiliki banyak kelebihan namun dengan penggunaan yang tidak lebih sulit dibanding yang lain.

Untuk menggunakan Axios, ada dua cara untuk menambahkannya ke project kita.

Pertama, menggunakan npm:

```js
npm install axios --save
```

Lalu di impor menggunakan perintah

```js
import axios from "axios";
```

Kita bisa melakukan request HTTP GET maupun HTTP POST dengan Axios.

### GET

```js
const axios = require("axios");
const Url = "https://jsonplaceholder.typicode.com/posts/";
axios
  .get(url)
  .then(data => console.log(data))
  .catch(err => console.log(err));

// dengan parameter

const U = (url = "https://jsonplaceholder.typicode.com/posts/");
const params = {
  name: "Said",
  id: 21
};
axios
  .get(Url, params)
  .then(data => console.log(data))
  .catch(err => console.log(err));
```

### POST

```js
const Url = "https://jsonplaceholder.typicode.com/posts/";
const user = {
  name: "Said",
  id: 21
};
axios({
  method: "post",
  url: Url,
  data: {
    user
  }
})
  .then(data => console.log(data))
  .catch(err => console.log(err));
```

Perbedaan saat melakukan POST, kita menambahkan property data untuk data yang ingin dikirim ke server.
