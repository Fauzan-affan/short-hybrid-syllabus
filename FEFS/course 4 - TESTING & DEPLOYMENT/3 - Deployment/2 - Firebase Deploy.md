# Firebase Deploy

Selain heroku, kita juga masih memiliki banyak opsi untuk membaut website yang sudah kita buat menjadi online. Salah satunya lewat [firebase.google.com](https://firebase.google.com/). Firebase merupakan salah satu produk google yang sedang naik daun. Firebase merupakan SaaS (Software as a Service) yang menggantikan peran backend. Selain itu, firebase juga mempunyai fitur hosting, yang dapat digunakan untuk mengonlinekan webstite yang sudah kita buat. Dan tentunya yang sama-sama kita cintai, **firebase ini gratis!** Pastikan teman-teman mempunyai akun google sebelum menggunakan firebase atau bisa juga menggunakan akun gmail. Jika belum punya silahkan buat terlebih dahulu [di sini](https://accounts.google.com/signup/v2/webcreateaccount?flowName=GlifWebSignIn&flowEntry=SignUp). Okay langsung saja kita mulai step by stepnya.

![img](img/1.png)

> ***Tips & trick:*** Banyak opsi-opsi untuk mendeploy website kita, jika teman-teman ingin tahu lebih banyak, silahkan kunjungi ekstrakulikuler **Melakukan Deployment dengan Nodejs**

## Step 1: Login

Silahkan login di pojok kanan atas halaman firebase.google.com yang bertulikan `sign in`. Jika sudah klik `go to console` untuk menuju console dari firebase pada account kita.

![img](img/2.png)

Di bawah ini adalah console saya. Karena saya sudah pernah membuat project firebase sebelumnya, makanya ada banyak project di sana. Jika teman-teman belum pernah membuat project apapun, tampilannya akan bersih.

![img](img/3.png)

## Step 2: Add New Project

Selanjutnya buat project baru dengan mengklik `+ add project`.

![img](img/4.png)

![img](img/5.png)

Isikan nama dari project baru yang mau teman-teman deploy. Dalam kasus kali ini saya akan mendeploy Vue `vue-router-project`, oleh karena itu saya akan namakan project di firebase dengan nama yang sama, yaitu `vue-router-project`. Teman-teman bisa pisahkan antara kalimat satu dengan yang lainnya menggunakan `-` (strip). Jika sudah klik `continue`.

![img](img/6.png)

Proses selanjutnya, kita akan ditanyakaan apakah ingin menggunakan google analytics? Untuk saat ini kita belum membutuhkannya, oleh karena itu kita klik saja bagian `Enable Google Analytics for this project` untuk mematikannya. Jika sudah klik `create project`, dan tunggu hingga project selesai dibuatkan, lalu klik `continue`.

![img](img/7.png)

![img](img/8.png)

![img](img/9.png)

Selanjutnya kita akan diarahkan ke bagian dasboard atau `project overview` dari firebase. Ada banyak sekali fitur yang firebase punya di bagian sidebarnya, tetapi kita akan fokus pada satu fitur saja, yaitu `Hosting`.

![img](img/10.png)

![img](img/11.png)

![img](img/12.png)

## Step 3: Hosting

Deployment sering disebut juga dengan hosting, ini yang membuat website kita bisa diakses lewat internet. Langsung saja klik bagian `Hosting` di sidebar bagian kiri layar, dan klik button `get started` yang berwarna putih.

![img](img/13.png)

![img](img/14.png)

Langkah selanjutnya adalah buka termial atau command promp, lalu copy perintah `npm install -g firebase-tools` yang ada di layar kedalam terminal untuk menginstal firebase CLI terlebih dahulu.

![img](img/15.png)

Jika sudah terinstal cek versi firebase dengan menggunakan `firebase --version`. Pada komputer saya versinya adalah 7.3.2, bisa saja versi teman-teman lebih baru pada saat mencoba.

![img](img/16.png)

Selanjutnya, firebase butuh otentikasi buat mengenali akun firebase mana yang akan melakukan hosting, oleh karena itu silahkan login menggunakan akun masing-masing menggunakan `firebase login`. Akan muncul tulisan *Allow Firebase to collect CLI usage and error reporting information?* kita jawab saja dengan `N` atau *No* lalu `enter`. Lalu kita akan diarahkan ke halam login dari google.

![img](img/17.png)

Jika berhasil akan di redirect ke halam di bawah ini dan tampilan terminal menunjukkan kita sudah login dengan akun google masing-masing. Pada contoh kali ini saya menggunakan akun google fauzanaffan780@gmail.com.

![img](img/18.png)

![img](img/19.png)

Selanjutnya, pastikan kita sudah mengarahkan terminal pada folder project Vue yang mau kita deploy. Saya sudah berada pada folder `vue-router-project` di terminal. Jika sudah inisialisai folder tersebut menjadi folder firebase dengan cara mengetikkan `firebase init`.

![img](img/20.png)

![img](img/21.png)

Tandai bagian hosting menggunakan keypad `spasi`, lalu `enter`.

![img](img/22.png)

Akan muncul pertanyaan *Please select an option:* karena kita sudah mempunyai project, pilih yang *Use an existing project* dan `enter`.

![img](img/23.png)

Pilih nama project yang tadi dibuat. Nama project saya `vue-router-project-88f7f` lalu tekan `enter`.

> ***Tips & trick:*** Terkadang firebase suka memberikan tambahan karakter pada nama project yang kita buat, contohnya `88f7f` pada `vue-router-project-88f7f`

Selanjutnya akan muncul pertanyaan *What do you want to use as your public directory? (public)*, karena kita ingin mengupload Vue yang konsepnya SPA, maka kita akan men-*generate* semua aset-aset yang dibutuhkan oleh project Vue kita ke dalam folder yang bernama `dist`. Oleh karena itu, ketikkan `dist` lalu `enter`.

![img](img/25.png)

Selanjutnya akan muncul pertanyaan *Configure as a single-page app (rewrite all urls to /index.html)? (y/N)* kita isikan `Y` atua `Yes` karena project Vue SPA atau Single Page Application.

![img](img/26.png)

Kita sudah selesai melakukan insialiasasi folder project Vue menjadi folder firebase.

![img](img/27.png)

## Step 4: Deployment

Masih pada folder yang sama, sekarang kita akan men-*generate* project Vue kita ke ***mode production*** namanya. Mode ini yang akan kita deploy ke hosting firebase. Caranya cukup mudah, tinggal ketikkan `npm run build` di temrinal, dan tunggu prosesnya hingga selesai.

![img](img/28.png)

Selanjutnya kita coba jalankan dulu di lokal server menggunakan `firebasae serve` sebelum mendeploynya ke hosting firebase. Buka `localhost:5000` di browser.

![img](img/29.png)

![img](img/30.png)

Klik button `next` pada `Set up Firebase Hosting` di browser:

![img](img/31.png)

![img](img/32.png)

Jika tampilan websitenya sudah sesuai dengan tampilan ketika kita jalankan pada mode development menggunakan `npm run serve`, hentikan lokal server menggunakan `control + c`. Lalu silahkan deploy ke hosting firebase menggunakan `firebase deploy`. Lalu klik `Continue to console` pada setup firebase di browser.

![img](img/33.png)

![img](img/34.png)

Klik salah satu domain dari 2 domain yang ada. Ini adalah domain yang bisa diakses lewat internet dan congratulation website kita sudah online sekarang :)

![img](img/35.png)

![img](img/36.png)
