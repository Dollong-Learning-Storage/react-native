## Easy - 5 Poin

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

Jawaban:

1. A
2. B
3. B

## Medium - 10 Poin

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

1. Apa yang akan dihasilkan dari contoh kode di atas?
   A. Tiga kotak merah dengan perataan vertikal.
   B. Tiga kotak merah dengan perataan diagonal.
   C. Tiga kotak merah dengan perataan horizontal.
   D. Satu kotak merah dengan dua kotak lain yang tidak terlihat.
2. Bagaimana Kamu akan mengatur dua elemen dalam satu baris dengan menggunakan Flexbox di React Native?
   A. Menggunakan properti flexDirection: 'row'.
   B. Menggunakan properti flexDirection: 'column'.
   C. Menggunakan properti alignItems: 'center'.
   D. Menggunakan properti justifyContent: 'space-between'.

Jawaban:

1. C
2. A

## Intermediate - 15 Poin

1. Bagaimana Kamu akan mengatasi masalah elemen yang saling tumpang tindih (overlap) dalam suatu layout Flexbox React Native?
   A. Menggunakan properti zIndex untuk mengatur tumpang tindih elemen.
   B. Menggunakan properti position: 'absolute' untuk mengatur posisi elemen secara eksplisit.
   C. Menggunakan properti flex: 1 untuk mengatur ruang elemen secara proporsional.
   D. Menggunakan properti overlap: 'hidden' untuk menyembunyikan tumpang tindih elemen.
2. Bagaimana cara mengatur elemen-elemen dalam suatu container menggunakan properti alignContent dalam Flexbox React Native?
   A. Mengatur posisi elemen di dalam container secara horizontal.
   B. Mengatur posisi elemen di dalam container secara vertikal.
   C. Mengatur ruang ekstra di sekitar elemen.
   D. Mengatur posisi elemen di dalam container ketika ada lebih dari satu baris.

Jawaban:

1. B
2. D

## Advanced - 20 Poin

1. Bagaimana Kamu akan membuat elemen-elemen Flexbox di React Native rata tengah secara horizontal dan vertikal dalam suatu container? Jelaskan dengan contoh kode.

Jawaban:
Kamu dapat menggunakan properti justifyContent: 'center' untuk meratakan elemen secara horizontal dan alignItems: 'center' untuk meratakan elemen secara vertikal dalam suatu container.

```jsx
import React from "react";
import { View, StyleSheet } from "react-native";

const App = () => {
  return (
    <View style={styles.container}>
      <View style={styles.centeredBox}>{/* Elemen Flexbox di sini */}</View>
    </View>
  );
};

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: "center",
    alignItems: "center",
  },
  centeredBox: {
    width: 100,
    height: 100,
    backgroundColor: "blue",
  },
});

export default App;
```
