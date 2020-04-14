# Final Project: Fitnes Companion API

## Final Project Overview

Pada Final Project: Fitnes Companion API,

1. Kamu akan membuat sebuah **endpoint yang dapat mengatur data workout Fitnes Companion yang terdari dari 2 file, yaitu heroesList.js dan personalsList.js**

2. **Mengetest endpoint yang telah dibuat menggunakan aplikasi Postman** untuk memastikan endpoint bekerja sesuai dengan apa yang diharapkan

3. Projek ini menitikberatkan **penggunaan Express.js untuk memaintain aspek backend** nya

## Starting from Scratch

**Kerjakan semuanya dari 0, kamu bisa mulai dengan membuat server menggunakan Express.js.**

Ada beberapa package atau dependency wajib yang harus kamu instal sebelum kamu mulai membuat server menggunakan Express.js, selain `npm` dan Node.js. Berikut adalah beberapa package yang wajib digunakan:

* [Express.js](https://expressjs.com/)

    Digunakan untuk membuat endpoint RESTful API

* [Cors Middleware](http://expressjs.com/en/resources/middleware/cors.html)

    Digunakan untuk mengatasi CORS issue

* [Body Parser Middleware](http://expressjs.com/en/resources/middleware/body-parser.html)

    Digunakan untuk memfasilitasi data yang masuk (request) dan keluar (respond) melalui routes

* [Nodemon](https://nodemon.io/)

    Digunakan untuk mengotomatisasi server setiap kali ada perubahan yang terjadi. Sehingga tidak membutuhkan *re-run server*

Selain itu, instal juga aplikasi [Postman](https://www.postman.com/) yang bertindak sebagai pengganti dari frontend untuk mencoba masing-masing endpoint yang sudah kamu buat.

## User Story

Sebelum masuk ke *user story,* berikut ini adalah contoh static data yang bisa digunakan untuk Final Project kali ini. Ada dua buah file yang digunakan untuk memudahkan membedakan mana data heroes workout dan mana data personal workout.

1. `heroesList.js`, isinya seperti berikut:

    ```js
    [
        {
            "heroId": 1,
            "name": "Bat Ability",
            "detail": "Batman often performs the action at night. Because of that, batman must have additional strength at night. Perform the workouts over a seven days period.",
            "training":
            [{
                "exerciseName": "Incline Barbell Bench Press",
                "wramUp": "2 x 10-15",
                "workingSet": "3 x 4-8",
                "restPeriod": "5 min"
            },
            {
                "exerciseName": "Barbell Bench Press",
                "wramUp": "2 x 10-15",
                "workingSet": "3 x 4-8",
                "restPeriod": "4 min"
            },
            {
                "exerciseName": "Bent Over Barbell Row",
                "wramUp": "5 x 10-15",
                "workingSet": "1 x 4-8",
                "restPeriod": "10 min"
            }]
        },
        {
            "heroId": 2,
            "name": "Bat Punch",
            "detail": "The enemy of batman often has a good body endurance. To damage the opponents defense, the batman must launch a powerful punch to the opponent. Perform the workouts over a three days period.",
            "training":
            [{
                "exerciseName": "Incline Barbell Bench Press",
                "wramUp": "2 x 10-15",
                "workingSet": "3 x 4-8",
                "restPeriod": "5 min"
            },
            {
                "exerciseName": "Barbell Bench Press",
                "wramUp": "2 x 10-15",
                "workingSet": "3 x 4-8",
                "restPeriod": "4 min"
            },
            {
                "exerciseName": "Bent Over Barbell Row",
                "wramUp": "5 x 10-15",
                "workingSet": "1 x 4-8",
                "restPeriod": "10 min"
            }]
        },
        {
            "heroId": 3,
            "name": "Steel Muscle",
            "detail": "Get ready to ramp up the intensity and really blow out the muscle.",
            "training":
            [{
                "exerciseName": "Incline Barbell Bench Press",
                "wramUp": "2 x 10-15",
                "workingSet": "3 x 4-8",
                "restPeriod": "5 min"
            },
            {
                "exerciseName": "Barbell Bench Press",
                "wramUp": "2 x 10-15",
                "workingSet": "3 x 4-8",
                "restPeriod": "4 min"
            },
            {
                "exerciseName": "Bent Over Barbell Row",
                "wramUp": "5 x 10-15",
                "workingSet": "1 x 4-8",
                "restPeriod": "10 min"
            }]
        }
    ]
    ```

2. `personalsList.js`, isinya seperti berikut:

    ```js
    [
        {
            "personalId": 1,
            "name": "Incline Barbell Bench Press"
        },
        {
            "personalId": 2,
            "name": "Barbell Bench Press"
        },
        {
            "personalId": 3,
            "name": "Bent Over Barbell Row"
        }
    ]
    ```

Selanjutnya, kita masuk ke *user story*. *User story* adalah deskripsi yang menjelaskan fungsionalitas aplikasi. Untuk melengkapi proyek ini, kamu harus membangun sebuah endpoint yang meliputi semua fungsionalitas dari *user story* di bawah ini:

✨ **Expressjs (backend) User Story**\
**User Story \# 1** - Fitness Companion API **setidaknya** memiliki route berikut:

* Route GET `/heroes` digunakan untuk mengambil data dari file heroesList.js.
* Route GET `/heroes/:heroId` digunakan untuk mengambil data spesifik berdasarkan ID dari file heroesList.js. Route ini akan digunakan untuk mendapatkan workout detail dan menampilkan datanya menggunakan modal atau page baru.
* Route POST `/heroes` digunakan untuk membuat data baru di dalam file heroesList.js.
* Route PUT `/heroes/:heroId` digunakan untuk mengupdate data di dalam file heroesList.js.
* Route DELETE `/heroes/:heroId` digunakan untuk menghapus data yang ada di dalam file heroesLis.js.

**User Story \# 2** - Fitness Companion API setidaknya memiliki route berikut:

* Route GET `/personals` digunakan untuk mengambil data dari file personalList.js.
* Route GET `/personals/:personalId` digunakan untuk mengambil data spesifik berdasarkan ID dari file personalsList.js.
* Route POST `/personals` digunakan untuk membuat data baru di dalam file personalsList.js.
* Route PUT `/personals/:personalId` digunakan untuk mengupdate data di dalam file personalsList.js.
* Route DELETE `/personals/:personalId` digunakan untuk menghapus data yang ada di dalam file personalsLis.js.

**User Story \# 3** -  Aplikasi ini harus berjalan pada port 5000.

## Final Project Submission

Sebelum mengumpulkan Final Project ini ada beberapa hal yang perlu diperhatikan, yaitu:

* Saya yakin semua user story yang ada telah sesuai dan Final Project saya akan lolos untuk di-review \(Jika tidak, saya akan berdiskusi dengan mentor via live chat sebelum men-submit.\)
* Final Project dibuat dengan benar tanpa error.
* Semua kebutuhan fungsional terpenuhi dan Final Project saya mampu berjalan sesuai dengan kebutuhan.

Jika semua hal di atas terpenuhi, Final Project kamu sudah bisa **di-submit ke: Platform**

### Project Rubric

| Application Setup |  |
| :--- | :--- |
| CRITERIA | SPECIFICATIONS |
| Apakah aplikasi ini mudah diatur? | Aplikasi ini dibuat dengan CSS dan JS terpisah di setiap folder. Index.html adalah entry point menuju website. Lebih baik lagi jika website ini berbebntuk SPA |
| Apakah aplikasi memiliki README dengan panduan instalasi dan penggunaan yang jelas? | README yang ter-update sudah termasuk pada aplikasi ini, di mana README ini menjelaskan proyek, serta memberikan instruksi untuk me-maintain dan memodifikasi proyek. |
| Apakah aplikasi menggunakan Express.js? | Aplikasi harus menggunakan Express.js framework untuk pembuatan API. |
| Apakah aplikasi menggunakan middleware CORS (Cross-origin resource sharing)? | CORS middleware digunakan untuk mengatasi perbedaan domain yang terjadi. Di mana jika tidak menggunakan CORS Middleware, ke dua aplikasi tidak bisa saling bertukar informasi. |
| Apakah aplikasi menggunakan middleware `body-parser`? | `body-parser` middleware digunakan untuk digunakan untuk memfasilitasi data yang masuk (request) dan keluar (respond) melalui routes |
| Apakah aplikasi menggunakan Nodemon di Express.js? | Nodemon menjadikan server otomatis direload setiap kali ada perubahan yang terjadi di sisi server. |

| Heroes Workout API |  |
| :--- | :--- |
| CRITERIA | SPECIFICATIONS |
| Apakah API dengan route GET `/heroes` menampilkan daftar Heroes Workout? | API dengan route GET `/heroes` harus menunjukkan daftar semua heroes workout. |
| Apakah API dengan route GET `/heroes/:heroId` menampilkan spesifik hero workout berdasarkan `heroId` yang diinginkan? | API dengan route GET `/heroes/:heroId` harus menunjukkan spesifik hero workout berdasarkan `heroId` yang diminta. |
| Apakah API dengan route POST `/heroes` bisa digunakan untuk memasukkan data baru? | API dengan route POST `/heroes` harus bisa memasukkan data ke dalam static data yang ada, yaitu file heroesList.js. |
| Apakah API dengan route PUT `/heroes/:heroId` bisa digunakan untuk mengupdate data berdasarkan `heroId` yang diinginkan? | API dengan route PUT `/heroes/:heroId` harus bisa mengupdate data berdasarkan `heroId` yang diminta. |
| Apakah API dengan route DELETE `/heroes/:heroId` bisa digunakan untuk menghapus data berdasarkan `heroId` yang diinginkan? | API dengan route DELETE `/heroes/:heroId` harus bisa menghapus data berdasarkan `heroId` yang diminta. |

| Personal Workout API |  |
| :--- | :--- |
| CRITERIA | SPECIFICATIONS |
| Apakah API dengan route GET `/personals` menampilkan daftar Personals Workout? | API dengan route GET `/personals` harus menunjukkan daftar semua personals workout. |
| Apakah API dengan route GET `/personals/:personalId` menampilkan spesifik personal workout berdasarkan `personalId` yang diinginkan? | API dengan route GET `/personals/:personalId` harus menunjukkan spesifik personal workout berdasarkan `personalId` yang diminta. |
| Apakah API dengan route POST `/personals` bisa digunakan untuk memasukkan data baru? | API dengan route POST `/personals` harus bisa memasukkan data ke dalam static data yang ada, yaitu file personalsList.js. |
| Apakah API dengan route PUT `/personals/:personalId` bisa digunakan untuk mengupdate data berdasarkan `personalId` yang diinginkan? | API dengan route PUT `/personals/:personalId` harus bisa mengupdate data berdasarkan `personalId` yang diminta. |
| Apakah API dengan route DELETE `/personals/:personalId` bisa digunakan untuk menghapus data berdasarkan `personalId` yang diinginkan? | API dengan route DELETE `/personals/:personalId` harus bisa menghapus data berdasarkan `personalId` yang diminta. |
