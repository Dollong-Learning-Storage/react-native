## Text

![Init React](<../../Assets/Materi/Button & Touchable opacity/text-explanation.png>).

Komponen Text adalah salah satu komponen dasar dalam React Native yang digunakan untuk menampilkan teks di antarmuka pengguna. Kamu dapat menggunakan komponen Text untuk menampilkan berbagai pesan, judul, paragraf, dan lainnya

<div style="width: 800px;position:relative;overflow-x:auto">
<iframe src="https://snack.expo.dev/@doltons/text-component" height="500" width="1500" title="Text Example"></iframe>
</div>

<!-- ```jsx
import React from "react";
import { View, Text, StyleSheet } from "react-native";

const TextExample = () => {
  return (
    <View>
      <Text>Selamat datang di materi UI Native!</Text>
      <Text>
        Ini adalah contoh penggunaan komponen Text dalam React Native. Kamu
        dapat menambahkan paragraf dan pesan sesuai kebutuhan.
      </Text>
    </View>
  );
};

export default TextExample;
``` -->

<!-- **Pentingnya Menggunakan Tag `<Text>`:**

Ketika Kamu ingin menampilkan teks di React Native, Kamu harus menggunakannya dalam komponen `<Text>`. Ini adalah perbedaan fundamental antara **HTML** dan **React Native**. Pada **HTML**, Kamu bisa saja menulis teks tanpa wadah elemen tertentu, tetapi di **React Native**, setiap potongan teks harus ditempatkan di dalam komponen `<Text>`.

Contoh yang tidak benar :

```jsx
<View>Ini adalah teks yang ingin ditampilkan.</View>
```

Contoh yang benar :

```jsx
<Text>Ini adalah teks yang ingin ditampilkan.</Text>
```

Alasan utama di balik ini adalah cara **React Native** membangun antarmuka pengguna. Saat Kamu memasukkan teks ke dalam komponen `<Text>`, React Native tahu bagaimana mengelola dan merender teks dengan benar sesuai dengan sistem operasi dan perangkat yang berbeda. -->

# Quiz

## Easy (5 poin)

1. Apa yang bisa Kamu lakukan dengan komponen Text dalam React Native?
   - [x] A. Menampilkan teks
   - B. Menambahkan efek animasi
   - C. Menampilkan video
   - D. Menampilkan konten-konten yang berisi gambar
2. Apa yang akan terjadi jika Kamu mencoba untuk menampilkan teks tanpa menggunakan komponen <Text> dalam React Native?
   - A. Teks akan ditampilkan dengan benar.
   - B. Aplikasi akan mengabaikan teks tersebut.
   - [x] C. Aplikasi akan menghasilkan pesan error atau crash.
   - D. Teks akan muncul dengan style default.

## Medium (10 Poin):

1. Bagaimana Kamu memperbaiki kesalahan saat mencoba menampilkan teks tanpa komponen <Text> ?
   - A. Menghapus seluruh teks tersebut.
   - B. Mengubah semua komponen <Text> menjadi <View>.
   - [x] C. Membungkus teks dengan komponen <Text>.
   - D. Menambahkan atribut noError pada komponen <Text>.
2. Bagaimana cara menampilkan teks dengan format cetak tebal (bold) dalam komponen Text?
   - [x] A. Menggunakan properti fontWeight: 'bold' dalam properti style.
   - B. Menggunakan properti textStyle: 'bold' dalam properti style.
   - C. Menggunakan tag <Bold> di sekitar teks yang akan diformat cetak tebal.
   - D. Tidak mungkin menampilkan teks dengan format cetak tebal dalam komponen Text.
3. Apa yang akan terjadi jika Kamu mencoba untuk menampilkan teks tanpa menggunakan komponen <Text> dalam React Native?
   - A. Teks akan ditampilkan dengan benar.
   - B. Aplikasi akan mengabaikan teks tersebut.
   - [x] C. Aplikasi akan menghasilkan pesan error atau crash.
   - D. Teks akan muncul dengan style default.
