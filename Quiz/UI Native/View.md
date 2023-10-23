## Easy - 5 Poin

1. Apa fungsi utama dari komponen View di React Native?
   a. Mengatur tata letak dan posisi elemen-elemen UI
   b. Menampilkan teks dalam aplikasi
   c. Mengelompokkan elemen-elemen UI bersama
   d. Memberikan gaya (style) kepada tombol
2. Dalam contoh kode yang diberikan, komponen mana yang digunakan untuk mengelompokkan elemen-elemen UI bersama?
   a. <Text>
   b. <View>
   c. <React>
   d. <StyleSheet>

Jawaban:

1. C
2. B

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
   A. Komponen <View> tidak diimpor dari 'react-native'.
   B. Tidak ada kesalahan dalam kode tersebut.
   C. Variabel styles tidak digunakan dalam komponen.
   D. Properti textAlign: 'center' tidak dapat digunakan dalam komponen <Text>.

Jawaban :

1. A
