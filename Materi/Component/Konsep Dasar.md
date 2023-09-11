Dalam React Native, semua elemen antarmuka pengguna (UI) direpresentasikan sebagai komponen. Komponen adalah blok bangunan dasar dari aplikasi Kamu, dan mereka dapat digunakan untuk menyusun tata letak, menangani interaksi pengguna, dan menampilkan informasi kepada pengguna. Dua jenis komponen utama dalam React Native adalah komponen functional dan class component (legacy).

```jsx
import React from "react";
import { View, Text } from "react-native";

const BasicComponent = () => {
  return (
    <View>
      <Text>Hello, ini adalah contoh komponen dasar!</Text>
    </View>
  );
};

export default BasicComponent;
```
