Salah satu cara melakukan styling di React Native adalah Inline Style

# Inline Style

<!-- Inline Style adalah cara menerapkan style langsung ke komponen melalui properti `style`. Kamu mengirimkan objek gaya langsung ke properti `style` dan mendefinisikan properti style seperti `backgroundColor`, `fontSize`, dan lainnya. -->

Inline Style adalah cara menerapkan style langsung ke komponen melalui _prop_ `style`. Kamu mengirimkan objek gaya langsung ke properti `style`.

Mari lihat contoh di bawah:

```jsx
const App = () => {
  return (
    <View>
      <Text>Ini adalah teks dengan gaya inline.</Text>
    </View>
  );
};
```

Di atas merupakan component biasa yang ada `view` sebagai container dan `text`. Jika kita ingin menghiasi text nya menjadi berwarna biru dan memiliki sedikit ruang misalnya. Kita bisa membuat seperti di bawah

<iframe src="https://snack.expo.dev/@doltons/inline-style" height="500" width="100%"></iframe>

Mudah bukan? sangatlah mudah dan langkah yang efisien jika kamu ingin menghiasi component kamu **apabila style yang di tambahkan hanya sedikit**.

_prop_ `style` menerima object, kalau kita lihat pada kode di atas, text nya kita beri warna dan _padding_ dengan cara seperti ini

```jsx
<Text style={{ backgroundColor: "lightblue", padding: 10 }}>
  Ini adalah teks dengan inline style.
</Text>
```

Kita mengisi style dengan object seperti `{ backgroundColor: "lightblue", padding: 10 }`. Keliatannya sama ya dengan _inline-style_ di css? yang membedakan adalah bahwa di React Native setiap kata yang terpisah seperti `background-color` di ganti dengan `backgroundColor`.

Ada dua cara membuat inline style, Yang pertama adalah dengan melakukan styling langsung seperti yang sudah di contohnya sebelumnya.

```jsx
const App = () => {
  return (
    <View style={{ backgroundColor: "#A52A2A", maxWidth: 400 }}>
      <Text>Text kamu disini...</Text>
    </View>
  );
};
```

Cara kedua adalah dengan membuat styling nya di dalam variable

```jsx
const titleStyle = { backgroundColor: "lightblue", padding: 10 };

const App = () => {
  return (
    <View>
      <Text style={titleStyle}>Ini adalah teks dengan inline style.</Text>
    </View>
  );
};
```

Atau

```jsx
const styles = {
  title: { backgroundColor: "lightblue", padding: 10 },
};

const App = () => {
  return (
    <View>
      <Text style={styles.title}>Ini adalah teks dengan gaya inline.</Text>
    </View>
  );
};
```

<!-- ```jsx
import React from "react";
import { View, Text } from "react-native";

const InlineStyleExample = () => {
  return (
    <View style={{ backgroundColor: "lightblue", padding: 10 }}>
      <Text style={{ fontSize: 18, color: "black" }}>
        Ini adalah teks dengan gaya inline.
      </Text>
    </View>
  );
};

export default InlineStyleExample;
``` -->

<!-- **Kelebihan dan Kekurangan:** **Kelebihan Inline Style:**

- Sederhana: Cocok untuk kasus-kasus sederhana dan cepat.
- Tidak Memerlukan Import Tambahan: Tidak perlu mengimpor `StyleSheet` dari 'react-native'.

**Kekurangan Inline Style:**

- Tidak Efisien untuk Pengulangan: Jika banyak elemen dengan gaya yang sama, ini bisa menjadi kurang efisien dan membingungkan.
- Sulit Dikelola: Pada proyek besar, manajemen gaya bisa menjadi rumit dan sulit dikelola.
- Kurang Reusable: Gaya tidak dapat digunakan kembali pada komponen lain.

Meskipun Inline Style bisa digunakan, lebih direkomendasikan untuk menggunakan `StyleSheet` ketika Kamu menghadapi proyek yang lebih besar dan kompleks. -->
