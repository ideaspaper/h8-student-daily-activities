# Pseudocode and Iterations

Sebuah bagian kode program dapat diulang sesuai dengan kebutuhan. Hal ini akan meningkatkan aspek DRY (Don't Repeat Yourself). Sebagai programmer, kita harus sebisa mungkin menghindari melakukan copy-paste kode program yang sama berkali-kali, karena hal tersebut meningkatkan faktor human error serta membuat kode program lebih susah untuk di maintain.

> Referensi: [Pseudocode Note 2](https://github.com/ideaspaper/class-notes/blob/master/phase-0/notes/pseudocode-note-2.md)

Agar lebih memahami iteration (pengulangan), buatlah implementasi algoritma, pseudocode serta kode program dari kasus berikut:

1. Kita diminta untuk menggambar sebuah garis sepanjang 1 meter. Adapun kita hanya memiliki sebuah penggaris dengan panjang 10 centimeter.

   ```javascript
   var penggaris = "--";

   // Your code here

   // Output: '--------------------'
   ```

1. Atlit lari memiliki jangkauan kaki yang berbeda-beda. Garis finish berjarak 100 meter dari atlit tersebut. Tampilkan `langkah 1`, `langkah 2`, `langkah 3`, dst. sampai atlit tersebut mencapai garis finish. Apabila atlit mencapai garis finish, tampilkan `FINISH`.

   ```javascript
   var jarak = 100;
   var jangkauan = 2; // Nilai dapat berubah-ubah

   // Your code here
   ```

1. Sebuah program akan menampilkan hasil input user. Input user disimulasikan sebagai angka random dari 1 hingga 20. Apabila user memberikan input angka 15, setelah program menampilkan angka 15, program akan berhenti.

   ```javascript
   var random = Math.floor(Math.random() * 20) + 1;

   // Your code here
   ```
