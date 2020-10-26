# Advance Conditionals

Sebuah statement conditional dapat terdapat di dalam statement conditional lainnya. Hal ini disebut juga sebagai nested conditional. Sebagai contoh:

```
IF kondisiSatu EQUAL TRUE
  IF kondisiDua EQUAL TRUE
    ...
  ELSE IF kondisiTiga EQUAL TRUE
    ...
  END IF
ELSE IF kondisiEmpat EQUAL TRUE
  IF kondisiLima EQUAL TRUE
    ...
  ELSE IF kondisiEnam EQUAL TRUE
    ...
  END IF
END IF
```

Agar lebih memahami, buatlah implementasi algoritma, pseudocode dan kode program dari kasus berikut:

1. Sebuah klinik membuat kategori ruangan pasien sebagai berikut:
   - Pasien dengan umur di bawah 50 tahun akan masuk ke ruangan A. Apabila pasien memiliki riwayat penyakit ganas, maka tampilkan `pasien masuk ke ruangan A bilik 1`. Apabila pasien tidak memiliki riwayat penyakit ganas, maka tampilkan `pasien masuk ke ruangan A bilik 2`.
   - Pasien dengan umur 50 tahun ke atas akan masuk ke ruangan B. Apabila pasien memiliki riwayat penyakit ganas, maka tampilkan `pasien masuk ke ruangan B bilik 1`. Apabila pasien tidak memiliki riwayat penyakit ganas, maka tampilkan `pasien masuk ke ruangan B bilik 2`.
1. Sebuah perusahaan manufaktur akan membuat barang dengan jumlah yang proporsional terhadap permintaan yang ada. Jika permintaan banyak dan stock sedikit, maka tampilkan `karyawan produksi bekerja lembur`. Jika permintaan banyak dan stock banyak, maka tampilkan `karyawan produksi bekerja seperti biasa`. Apabila permintaan sedikit, maka tampilkan `sales bekerja lembur`.

> Referensi: [Pseudocode Note 2 (Switch-Case)](https://github.com/ideaspaper/class-notes/blob/master/phase-0/notes/pseudocode-note-2.md)
