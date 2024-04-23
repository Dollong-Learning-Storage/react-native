<!-- Cara berikutnya melakukan styling di React Native adalah dengan menggunakan cara bawaan dari  -->

React Native menyediakan cara nya sendiri untuk melakukan _styling_.

# StyleSheet

Melihat dari materi sebelumnya, kita bisa memisahkan _styling_ kita ke suatu variabel lalu mengisi nya sebagau _value dari prop style_.

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

React Native menyediakan cara nya sendiri yaitu dengan **StyleSheet**.

```jsx
import { View, Text, StyleSheet } from "react-native";

// menggunakan method .create dari StyleSheet
const styles = StyleSheet.create({
  title: {
    backgroundColor: "lightblue",
    padding: 10,
  },
});

const App = () => {
  return (
    <View>
      <Text style={styles.title}>Ini adalah teks dengan inline style.</Text>
    </View>
  );
};
```

Contoh di atas merupakan cara menghiasi component kita dengan _StyleSheet_. Keliatannya sama aja ya? benar, bedanya adalah kita menggunakan cara yang disiapkan React Native.

<!-- React Native, disarankan untuk menggunakan **StyleSheet**, yang merupakan cara yang lebih efisien dan dioptimalkan untuk mengatur gaya komponen. StyleSheet memanfaatkan caching untuk mempercepat proses styling. -->

<!-- **Contoh penggunaan:**

<div style="width: 800px;position:relative;overflow-x:auto">
  <iframe src="https://snack.expo.dev/@doltons/props-component" height="500" width="1500"></iframe>
</div>

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

Menggunakan `StyleSheet` adalah praktik yang direkomendasikan untuk mengelola style pada komponen-komponen kamu dalam React Native. Ini membantu menjaga kode lebih terstruktur dan efisien, serta mengoptimalkan kinerja aplikasi kamu.
