Flexbox adalah pendekatan tata letak yang kuat yang digunakan dalam React Native untuk mengatur posisi dan tata letak elemen-elemen UI. Dengan menggunakan prinsip Flexbox, Kamu dapat membuat tampilan yang responsif dan mudah diatur, terutama pada berbagai ukuran layar.

**Konsep Dasar Flexbox:**
Flexbox bekerja berdasarkan konsep Container dan Child Element. Kamu menempatkan Child element dalam container (biasanya dalam komponen `View`), dan kemudian mengatur tata letak dan perataan elemen-elemen tersebut.

**Beberapa Properti Flexbox:**

- `flexDirection`: Menentukan arah tata letak (row atau column).
- `justifyContent`: Mengatur perataan elemen sepanjang sumbu utama.
- `alignItems`: Mengatur perataan elemen sepanjang sumbu silang.
- `flex`: Mengalokasikan ruang fleksibel untuk elemen dalam Container.

**Contoh Kode:**

<iframe src="https://snack.expo.dev/@doltons/flatlist-component" height="500" width="100%"></iframe>

<!-- ```jsx
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
``` -->
