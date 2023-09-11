1. Apa yang dimaksud dengan Flexbox dalam React Native?
   A. Sebuah komponen untuk membuat kotak input fleksibel.
   B. Pendekatan tata letak untuk mengatur posisi dan tata letak elemen-elemen UI.
   C. Library untuk mengelola data berbasis teks.
   D. Fitur untuk membuat animasi berbasis teks.
2. Apa yang dimaksud dengan "Container" dalam konsep Flexbox?
   A. Elemen-elemen dalam tampilan yang akan diatur.
   B. Komponen View yang digunakan untuk menempatkan elemen-elemen Flexbox.
   C. Jenis tata letak dalam React Native.
   D. Bagian dalam dari elemen Flexbox.
3. Manakah nilai default untuk properti flexDirection di React Native?
   A. row
   B. column
   C. wrap
   D. flex
4. Apa yang akan dihasilkan dari contoh kode di atas?
   A. Tiga kotak merah dengan perataan vertikal.
   B. Tiga kotak merah dengan perataan diagonal.
   C. Tiga kotak merah dengan perataan horizontal.
   D. Satu kotak merah dengan dua kotak lain yang tidak terlihat.

```jsx
import React from "react";
import { View, StyleSheet } from "react-native";

const FlexboxExample = () => {
  return (
    <View style={styles.container}>
      <View style={styles.box} />
      <View style={styles.box} />
      <View style={styles.box} />
    </View>
  );
};

const styles = StyleSheet.create({
  container: {
    flex: 1,
    flexDirection: "row",
    justifyContent: "space-between",
    alignItems: "center",
    padding: 20,
  },
  box: {
    width: 50,
    height: 50,
    backgroundColor: "red",
  },
});

export default FlexboxExample;
```

Jawaban:

1. A
2. B
3. B
4. C
