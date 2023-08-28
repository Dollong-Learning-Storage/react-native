Komponen View adalah salah satu komponen dasar dalam React Native yang digunakan untuk membungkus dan mengelompokkan elemen-elemen UI lainnya. Sebagai wadah (container), View membantu dalam mengatur tata letak dan struktur antarmuka pengguna.

**Fungsi dan Kegunaan:**

1. **Pengelompokan Elemen:** View digunakan untuk mengelompokkan elemen-elemen UI bersama, seperti teks, gambar, tombol, dan komponen lain.
2. **Pengaturan Tata Letak:** View memungkinkan untuk mengatur tata letak dan posisi elemen-elemen di dalamnya.
3. **Styling:** Anda dapat memberikan gaya (style) seperti warna latar belakang, margin, padding, dan lainnya kepada komponen View.

**Contoh Kode:** 
```jsx
import React from 'react';
import { View, Text } from 'react-native';

const ViewExample = () => {
  return (
    <View>
      <Text>Selamat datang di materi UI Native!</Text>
      <Text>Ini adalah contoh penggunaan komponen View.</Text>
    </View>
  );
}

export default ViewExample;
```

**Penjelasan Kode:**

- Import React dan komponen `View` serta `Text` dari 'react-native'.
- Deklarasikan komponen `ViewExample` sebagai sebuah fungsi.
- Dalam `return`, kita mengembalikan komponen View yang berisi dua elemen `<Text>`. Elemen ini diatur di dalam View untuk mengelompokkan mereka.
- Pada komponen View, kita memberikan style menggunakan properti `style`. Objek style didefinisikan dalam `styles` menggunakan `StyleSheet.create()`.
- Dalam contoh ini, style `container` memiliki flex 1 (mengisi seluruh ruang yang tersedia), posisi di tengah (`justifyContent` dan `alignItems`), serta warna latar belakang abu-abu muda.
- Style `text` digunakan untuk mengatur ukuran font dan margin bawah pada elemen teks.

Dengan menggunakan komponen View, Anda dapat mengatur tata letak dan pengelompokan elemen-elemen UI dengan lebih terstruktur dan mudah dikendalikan.