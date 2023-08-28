Functional Component merupakan salah satu jenis komponen dalam React Native yang digunakan untuk membangun antarmuka pengguna (UI). Secara konsep, komponen ini adalah sebuah fungsi JavaScript yang mengembalikan tampilan yang akan ditampilkan di layar perangkat.

**Kelebihan Functional Component:**

1. **Sederhana dan Ringkas:** Functional Component lebih ringkas dibandingkan dengan Class Component, sehingga lebih mudah dibaca dan dipahami.
2. **Performa:** Functional Component cenderung lebih cepat dalam eksekusi dibandingkan dengan Class Component, karena memiliki overhead yang lebih rendah.
3. **Mudah untuk Dites:** Pengujian (testing) komponen ini lebih sederhana karena hanya berfokus pada input dan output fungsi.

**Contoh Kode Functional Component:**

```jsx
import React, { useState, useEffect } from 'react';
import { View, Text } from 'react-native';

const FunctionalComponentExample = (props) => {
  const [count, setCount] = useState(0);

  useEffect(() => {
    console.log('Component did mount');
    return () => {
      console.log('Component will unmount');
    };
  }, []);

  useEffect(() => {
    console.log('Component did update');
  }, [count]);

  return (
    <View>
      <Text>Halo, ini adalah Functional Component!</Text>
      <Text>Count: {count}</Text>
    </View>
  );
}

export default FunctionalComponentExample;

```

**Penggunaan dan Penjelasan Kode:**

- Import React dan komponen yang diperlukan dari 'react-native'.
- Deklarasikan sebuah fungsi bernama `FunctionalComponentExample` yang menerima parameter `props`.
- Fungsi ini mengembalikan elemen `<View>` yang berisi elemen-elemen `<Text>`. Ini adalah tampilan yang akan ditampilkan di layar.
- Dalam contoh ini, ada dua elemen `<Text>`. Yang pertama adalah pesan statis, dan yang kedua menampilkan nilai props yang diterima dari luar komponen.
- Terakhir, eksport komponen agar bisa digunakan di file lain.

Dalam Functional Component, kita hanya perlu mendefinisikan fungsi dan mengembalikan tampilan yang diinginkan. Props bisa diterima sebagai parameter fungsi untuk mengirim data dari komponen induk. Ini adalah cara sederhana untuk membuat komponen dalam React Native dengan fokus pada tampilan dan fungsi yang lebih terisolasi.