Pada React Native, event handling adalah cara kita merespons aksi yang dilakukan oleh pengguna terhadap elemen UI. Salah satu event handling yang umum digunakan adalah `onPress`. Event `onPress` digunakan untuk menangkap ketika pengguna menekan (klik) elemen tertentu, seperti tombol.

**Fungsi dan Kegunaan onPress:**
Event `onPress` memberi Kamu kemampuan untuk merespons tindakan pengguna secara interaktif. Ketika pengguna menekan elemen dengan event `onPress`, Kamu dapat mengeksekusi kode tertentu, misalnya untuk memicu perubahan tampilan, memanggil fungsi, atau menavigasi antarmuka pengguna.

**Contoh Kode:**

<iframe src="https://snack.expo.dev/@doltons/handle-onpress" height="500" width="100%"></iframe>

```jsx
import { useState, useEffect } from "react";
import { View, Text, Button } from "react-native";

const FunctionalComponentExample = (props) => {
  const [count, setCount] = useState(0);

  const incrementCount = () => setCount(count + 1);

  useEffect(() => {
    console.log("Component did mount");
    return () => {
      console.log("Component will unmount");
    };
  }, []);

  useEffect(() => {
    console.log("Component did update");
  }, [count]);

  return (
    <View>
      <Text>Halo, ini adalah Functional Component!</Text>
      <Text>Count: {count}</Text>
      <Button title="+" onPress={incrementCount} />
    </View>
  );
};

export default FunctionalComponentExample;
```

**Penjelasan Kode:**

- Pada contoh di atas, komponen `TouchableOpacity` digunakan untuk membuat elemen yang bisa di-'tekan'.
- Properti `onPress` dari `TouchableOpacity` ditetapkan dengan fungsi `handlePress`.
- Fungsi `handlePress` akan dipanggil ketika pengguna menekan elemen.
- Dalam contoh ini, ketika tombol ditekan, kita memanggil fungsi `alert` untuk menampilkan pesan.
- Gaya (style) diterapkan pada elemen `TouchableOpacity` untuk memberikan tampilan tombol yang lebih menarik.

Event handling `onPress` memungkinkan Kamu untuk memberikan interaksi yang responsif kepada pengguna ketika mereka berinteraksi dengan elemen UI. Dalam contoh ini, pesan akan muncul ketika tombol ditekan.
