# ES6

Setiap bahasa pemrograman pasti berevolusi dengan tujuan untuk memudahkan user-nya, dalam hal ini adalah para programmer yang menggunakan bahasa pemrograman tersebut. Salah satu evolusi penting dari JavaScript adalah ditetapkannya standar ES6. Hal-hal yang berkaitan dengan ES6 dan perlu dipahami untuk saat ini adalah:

- hoisting
- scope
- var, let, const
- template literal

## Hoising

> Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their scope before code execution.

Agar lebih memahami hoisting, perhatikan contoh di bawah:

```javascript
console.log(hoist); // Output: undefined
var hoist = 'The variable has been hoisted.';
```

Program di atas berhasil dieksekusi, namun hasilnya adalah `undefined`. Hal tersebut dikarenakan kode program tersebut akan "diubah" menjadi seperti di bawah oleh JavaScript.

```javascript
var hoist; // Variable declaration
console.log(hoist); // Output: undefined
hoist = 'The variable has been hoisted.'; // Variable assignment
```

> Variable hoisting hanya terjadi pada `var`. Sering kali, variable hoisting merupakan perilaku dari JavaScript yang tidak dikehendaki. Hal tersebut dikarenakan hoisting akan membuat alur eksekusi program menjadi tidak jelas.

## Scope

Scope adalah ruang lingkup. Scope dapat dianggap sebagai suatu ketentuan yang mengatur aksesibilitas sebuah variable. Pada JavaScript sebuah scope dapat dibuat menggunakan `{}`. Sebagai contoh perhatikan kode program di bawah:

```javascript
{
  // Scope 1
}

{
  // Scope 2
}

{
  // Scope 3
}
```

Scope membantu kita untuk mengelompokkan bagian-bagian yang saling terkait pada kode program. Sebagai contoh, kode program untuk menghitung laba penjualan tidak perlu mengetahui biodata dari customer. Maka dari itu, akan lebih baik jika kode program perhitungan laba diletakkan pada scope tersendiri, yang berbeda dari kode program pengolah data customer.

Variable yang dideklarasikan pada `Scope 1` tidak dapat diakses oleh kode program yang ada pada `Scope 2`. Ketentuan ini tidak berlaku untuk variable yang dideklarasikan menggunakan `var`.

## `var`, `let`, `const`

### `var`

Seperti yang dijelaskan sebelumnya, bahwa `{}` tidak berlaku untuk `var`. Untuk lebih jelasnya, coba eksekusi kode program di bawah:

```javascript
if (10 > 5) {
  var output = 'Point 1';
}

console.log(output);
```

Setelah kode program dieksekusi, ternyata variable `output` dapat diakses di luar scope. Hal tersebut dikarenakan `var` memiliki sifat **function scoped**. Function akan dibahas lebih lanjut pada materi-materi yang akan datang. Namun contoh dari function scope adalah seperti di bawah:

```javascript
function fungsi1() {
  var output = 10;
}

console.log(output);
```

Apabila kode program di atas dieksekusi, maka akan terjadi error dengan pesan `ReferenceError: output is not defined`. Perilaku function scoped dari `var` adalah sesuatu yang tidak umum pada bahasa pemrograman lain.

Hal yang tidak umum lagi dari `var` adalah kita dimungkinkan untuk melakukan redeclaration. Contoh dari redeclaration adalah seperti di bawah:

```javascript
var output = 10;
var output = 20;
```

Sifat `var` ini juga tidak umum dan membingungkan. Bayangkan seorang programmer telah menggunakan nama variable `output`, kemudian programmer lain melakukan variable declaration dengan nama yang sama.

### `let`

> `let` is the new `var`.

Kalimat di atas merupakan kesimpulan yang sering didapatkan setelah melakukan searching dengan keyword "let vs var". `let` memiliki sifat **block scoped**, sama halnya seperti variable pada bahasa pemrograman lainnya. Variable yang dideklarasikan dengan `let` hanya akan dikenali di dalam scope `{}` di mana variable tersebut dideklarasikan. Coba eksekusi kode program di bawah, kemudian amati hasilnya.

```javascript
if (10 > 5) {
  let output = 'Point 1';
}

console.log(output);
```

Redeclaration tidak dapat dilakukan pada variable yang telah dideklarasikan menggunakan `let`.

### `const`

Sama seperti `let`, namun bedanya kita tidak dapat melakukan assignment ulang pada `const`. Coba eksekusi kode program di bawah, kemudian amati hasilnya.

```javascript
const value = 10;
value = 5;
```

## Template Literal

Contoh template literal adalah seperti di bawah:

```javascript
const jumlahSate = 10;
let pernyataan = `Saat ini saya memesan ${jumlahSate} tusuk sate.`;
console.log(pernyataan);
```
