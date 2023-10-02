Dalam React Native, Kamu dapat menerapkan gaya (style) ke elemen-elemen UI menggunakan dua metode utama: Inline Style dan StyleSheet. Inline Style adalah cara langsung menetapkan gaya ke komponen melalui properti. Ini cocok untuk kasus-kasus sederhana, tetapi untuk proyek yang lebih besar dan kompleks, penggunaan StyleSheet lebih direkomendasikan.

**Inline Style:**
Inline Style adalah cara menerapkan style langsung ke komponen melalui properti `style`. Kamu mengirimkan objek gaya langsung ke properti `style` dan mendefinisikan properti style seperti `backgroundColor`, `fontSize`, dan lainnya.

**Contoh Kode:**

<iframe src="https://snack.expo.dev/@doltons/inline-style" height="500" width="100%"></iframe>

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

**Kelebihan dan Kekurangan:** **Kelebihan Inline Style:**

- Sederhana: Cocok untuk kasus-kasus sederhana dan cepat.
- Tidak Memerlukan Import Tambahan: Tidak perlu mengimpor `StyleSheet` dari 'react-native'.

**Kekurangan Inline Style:**

- Tidak Efisien untuk Pengulangan: Jika banyak elemen dengan gaya yang sama, ini bisa menjadi kurang efisien dan membingungkan.
- Sulit Dikelola: Pada proyek besar, manajemen gaya bisa menjadi rumit dan sulit dikelola.
- Kurang Reusable: Gaya tidak dapat digunakan kembali pada komponen lain.

Meskipun Inline Style bisa digunakan, lebih direkomendasikan untuk menggunakan `StyleSheet` ketika Kamu menghadapi proyek yang lebih besar dan kompleks.
