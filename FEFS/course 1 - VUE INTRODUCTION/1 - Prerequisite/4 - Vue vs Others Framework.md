# Vue vs Others Framework

Saat membicarakan *web development*, ada dua pemain besar mendominasi, yaitu **React** dan **Angular.** Bagaimana caranya Vue memposisikan dirinya diantara dua pemain besar dan terkenal tersebut?

Vue dibuat oleh [Evan You](https://github.com/yyx990803) yang bekerja di Google dengan Angular (1.0). Vue lahir dari keinginan Evan untuk membuat framework yang unggul di sisi ***performance.***

Vue mengadopsi ***sistem templating*** yang ada pada Angular, tetapi menghilangkan [*opinionated*](https://dev.to/heroku/opinionated-or-not-choosing-the-right-framework-for-the-job-4e9f)-nya, yaitu tempat peyimpanan data kompleks yang Angular gunakan, dan membuat performa Vue lebih kencang.

Angular (2.0) menyelesaikan issues yang terjadi pada Angular (1.0), namun dengan sintaks yang sangat berbeda dari pendahulunya (Angular 2.0), dan harus menggunakan bahasa pemrograman [Typescript](https://www.typescriptlang.org/) yang mana tidak setiap developers mau mempelajarinya.

Bagaimana dengan React? Vue mengambil banyak ide-ide cemerlang yang React gunakan, terutama virtual DOM. Namun, Vue menerapkan virtual DOM dengan *automation dependency management,* di mana **hanya component yang berhubungan dengan state saja yang dire-render ulang** ketika *state property* melakukan perubahan. Sedangkan di React, ketika ada perubahan state, maka **semua isi component yang berhubungan dengan state, akan dire-render**. Untuk menghindari hal seperti ini terjadi di React, kita harus menggunakan salah satu lifecycle method yang ada di React, yaitu `shouldComponentUpdate`. Hal ini menjelaskan betapa mudahnya penggunaan Vue, dan performa yang luar biasa yang Vue tawarkan.

Satu hal lagi yang berbeda antara Vue dan React, yaitu JSX di React. *Well*, kita bisa aja menggunakan JSX di Vue sebenernya, tapi jarang sekali developers yang menggunakannya di Vue. Vue menggunakan `<template>` untuk membungkus sintak HTML, sementara JSX berbeda sehingga membutuhkan proses belajar lagi bagi developer yang belum mengetahuinya.

React JSX:

```js
const element = (
  <h1 className="greeting">
    Hello, world!
  </h1>
);
```

Vue Template:

```html
<template>
    <h1 class="greeting">
        Hello, world!
    </h1>
</template>
```

Banyak lagi yang Vue adopsi dari React:

React:

* Management state dengan [Redux](https://redux.js.org/)
* Router dengan [React-router-dom](https://www.npmjs.com/package/react-router-dom) atau [@Reach/router](https://reach.tech/router)

Vue:

* Management state dengan [Vuex](https://vuex.vuejs.org/)
* Router dengan [Vue-router](https://router.vuejs.org/)

Terakhir, yang paling membedakan Vue dengan framework-framework lain, yaitu Vue merupakan ***indie project,*** artinya Vue tidak di backup oleh perusahaan besar seperti Facebook ataupun Google. Sebagai gantinya, Vue dibackup oleh komunitas yang sangat besar, pengembangannya melalui donasi dan sponsor.
