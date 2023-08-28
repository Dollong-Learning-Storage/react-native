Dalam React Native, props adalah cara untuk mengirimkan data dari komponen induk (parent component) ke komponen anak (child component). Props memungkinkan komponen untuk menerima dan menggunakan data eksternal, membuat komponen menjadi lebih dinamis dan dapat digunakan ulang dengan lebih baik.

**Peran dan Fungsi Props:** Props digunakan untuk mengirimkan informasi dari komponen induk ke komponen anak. Ini memungkinkan kita untuk mengubah perilaku atau tampilan komponen anak berdasarkan data yang diterima dari induk. Props adalah salah satu cara utama untuk membuat komunikasi antara komponen dalam hierarki.

**Contoh Penggunaan Props:**

```jsx
import React from 'react';
import { View, Text } from 'react-native';

const Greeting = (props) => {
  return <Text>Halo, {props.name}!</Text>;
}

const App = () => {
  return (
    <View>
      <Greeting name="Ahmad" />
      <Greeting name="Budi" />
    </View>
  );
}

export default App;
```

Dengan props, kita bisa mengirimkan data dari komponen induk ke komponen anak, sehingga kita bisa menghasilkan variasi tampilan atau perilaku yang berbeda berdasarkan data yang dikirimkan. Hal ini membuat komponen kita menjadi lebih dinamis dan mudah digunakan kembali dalam berbagai konteks.