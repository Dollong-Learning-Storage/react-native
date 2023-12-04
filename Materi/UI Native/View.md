Di HTML kita menggunakan `<div />` untuk **mengelompokkan element**. Pada React Native, kita punya `<View />` yang memiliki peran yang sama

![Init React](<../../Assets/Materi/UI Native/view-explanation.png>)

Komponen `<View>` adalah komponen utama React Native yang digunakan untuk membungkus dan mengelompokkan elemen antarmuka pengguna lainnya. Fungsinya sebagai wadah atau container membantu mengatur tata letak dan struktur antarmuka pengguna.

<!-- **Fungsi dan Kegunaan:** -->

<!--
1. **Pengelompokan Elemen:** View digunakan untuk mengelompokkan elemen-elemen UI bersama, seperti teks, gambar, tombol, dan komponen lain.
2. **Pengaturan Tata Letak:** View memungkinkan untuk mengatur tata letak dan posisi elemen-elemen di dalamnya. -->

**Contoh Kode:**

<iframe src="https://snack.expo.dev/@doltons/view-component" height="500" width="100%" title="View Example"></iframe>

<!-- ```jsx
import React from "react";
import { View, Text } from "react-native";

const ViewExample = () => {
  return (
    <View>
      <Text>Selamat datang di materi UI Native!</Text>
      <Text>Ini adalah contoh penggunaan komponen View.</Text>
    </View>
  );
};

export default ViewExample;
``` -->

<!-- **Penjelasan Kode:**

- Deklarasikan komponen `ViewExample` sebagai sebuah fungsi.
- Dalam `return`, kita mengembalikan komponen View yang berisi dua elemen `<Text>`. Elemen ini diatur di dalam View untuk mengelompokkan mereka.
- Pada komponen View, kita memberikan style menggunakan properti `style`. Objek style didefinisikan dalam `styles` menggunakan `StyleSheet.create()`.
- Dalam contoh ini, style `container` memiliki flex 1 (mengisi seluruh ruang yang tersediA., posisi di tengah (`justifyContent` dan `alignItems`), serta warna latar belakang abu-abu muda.
- Style `text` digunakan untuk mengatur ukuran font dan margin bawah pada elemen teks.

Dengan menggunakan komponen View, Kamu dapat mengatur tata letak dan pengelompokan elemen-elemen UI dengan lebih terstruktur dan mudah dikendalikan. -->

# Quiz

## Easy - 5 Poin

1. Apa fungsi utama dari komponen View di React Native?
   - A. Mengatur tata letak dan posisi elemen-elemen UI
   - B. Menampilkan teks dalam aplikasi
   - [x] C. Mengelompokkan elemen-elemen UI bersama
   - D. Memberikan style kepada `<Text>`
2. Dalam contoh kode yang diberikan, komponen mana yang digunakan untuk mengelompokkan elemen-elemen UI bersama?
   - A. <Text>
   - [x] B. <View>
   - C. <React>
   - D. <StyleSheet>

## Medium - 10 poin

```jsx
import { Text, StyleSheet } from "react-native";

export default function App() {
  return (
    <View style={styles.container}>
      <Text style={styles.paragraph}>Halo dunia</Text>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: "center",
    backgroundColor: "#ecf0f1",
    padding: 8,
  },
  paragraph: {
    margin: 24,
    fontSize: 18,
    fontWeight: "bold",
    textAlign: "center",
  },
});
```

1. Apa yang salah pada kode di atas?
   - [x] A. Komponen <View> tidak diimpor dari 'react-native'.
   - B. Tidak ada kesalahan dalam kode tersebut.
   - C. Variabel styles tidak digunakan dalam komponen.
   - D. Properti textAlign: 'center' tidak dapat digunakan dalam komponen <Text>.
