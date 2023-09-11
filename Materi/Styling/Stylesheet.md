Styling adalah aspek penting dalam pengembangan aplikasi React Native untuk menciptakan tampilan yang menarik dan intuitif. Di React Native, terdapat dua pendekatan utama untuk memberikan gaya pada komponen-komponen: **Inline Style** dan **StyleSheet**.

**StyleSheet dalam React Native:**
Pada saat mengembangkan aplikasi React Native, disarankan untuk menggunakan **StyleSheet**, yang merupakan cara yang lebih efisien dan dioptimalkan untuk mengatur gaya komponen. StyleSheet memanfaatkan caching untuk mempercepat proses styling.

**Contoh penggunaan:**

<iframe src="https://snack.expo.dev/@doltons/stylesheet-style" height="500" width="100%"></iframe>

<!-- ```jsx
import React from "react";
import { View, Text, StyleSheet } from "react-native";

const StylesheetExample = () => {
  return (
    <View style={styles.container}>
      <Text style={styles.title}>Selamat Datang!</Text>
      <Text style={styles.paragraph}>
        Ini adalah contoh penggunaan StyleSheet pada React Native. Gaya dapat
        didefinisikan dalam objek styles yang disediakan oleh StyleSheet.
      </Text>
    </View>
  );
};

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: "center",
    alignItems: "center",
    backgroundColor: "#ffffff",
    padding: 20,
  },
  title: {
    fontSize: 24,
    fontWeight: "bold",
    marginBottom: 10,
  },
  paragraph: {
    fontSize: 16,
    textAlign: "center",
  },
});

export default StylesheetExample;
``` -->

Menggunakan `StyleSheet` adalah praktik yang direkomendasikan untuk mengelola gaya pada komponen-komponen kamu dalam React Native. Ini membantu menjaga kode lebih terstruktur dan efisien, serta mengoptimalkan kinerja aplikasi kamu.
