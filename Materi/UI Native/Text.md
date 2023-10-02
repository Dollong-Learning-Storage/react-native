Komponen Text adalah salah satu komponen dasar dalam React Native yang digunakan untuk menampilkan teks di antarmuka pengguna. Kamu dapat menggunakan komponen Text untuk menampilkan berbagai pesan, judul, paragraf, dan lainnya.

**Fungsi dan Kegunaan:**

1. **Menampilkan Teks:** Komponen Text digunakan untuk menampilkan teks pada layar perangkat.
2. **Styling Teks:** Kamu dapat memberikan gaya (style) seperti ukuran font, warna, tebal, dan lainnya kepada teks yang ditampilkan.
3. **Penyusunan Teks:** Kamu dapat mengatur penyusunan teks seperti perataan (alignment), penjajaran (justification), dan pemutusan kata (line breaks).

<iframe src="https://snack.expo.dev/@doltons/text-component" height="500" width="100%" title="Text Example"></iframe>

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

**Pentingnya Menggunakan Tag `<Text>`:**

Ketika Kamu ingin menampilkan teks di React Native, Kamu harus menggunakannya dalam komponen `<Text>`. Ini adalah perbedaan fundamental antara **HTML** dan **React Native**. Pada **HTML**, Kamu bisa saja menulis teks tanpa wadah elemen tertentu, tetapi di **React Native**, setiap potongan teks harus ditempatkan di dalam komponen `<Text>`.

Contoh yang tidak benar :

```jsx
<View>Ini adalah teks yang ingin ditampilkan.</View>
```

Contoh yang benar :

```jsx
<Text>Ini adalah teks yang ingin ditampilkan.</Text>
```

Alasan utama di balik ini adalah cara **React Native** membangun antarmuka pengguna. Saat Kamu memasukkan teks ke dalam komponen `<Text>`, React Native tahu bagaimana mengelola dan merender teks dengan benar sesuai dengan sistem operasi dan perangkat yang berbeda.
