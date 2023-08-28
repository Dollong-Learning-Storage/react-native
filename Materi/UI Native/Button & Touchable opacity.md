Komponen Button adalah salah satu komponen dasar dalam React Native yang digunakan untuk membuat tombol interaktif dalam antarmuka pengguna. Tombol ini memungkinkan pengguna untuk melakukan tindakan tertentu saat tombol ditekan.

**Fungsi dan Kegunaan:**

1. **Interaksi Pengguna:** Tombol memungkinkan pengguna untuk melakukan tindakan tertentu, seperti mengirim formulir, memulai proses, atau berpindah ke halaman lain.
2. **Tindakan Pemicu:** Anda dapat menghubungkan fungsi atau tindakan khusus ke tombol yang akan dijalankan saat tombol ditekan.
3. **Tampilan Visual:** Tombol biasanya memiliki tampilan yang berbeda ketika dalam keadaan normal dan ketika dihover atau ditekan.

**Contoh Kode:**

```jsx
import React from 'react';
import { View, Text, Button, Alert } from 'react-native';

const ButtonExample = () => {
  const handlePress = () => {
    Alert.alert('Tombol Ditekan', 'Tindakan dilakukan saat tombol ditekan!');
  };

  return (
    <View>
      <Text>Selamat datang di contoh Button!</Text>
      <Button title="Click Here.." onPress={handlePress} />
    </View>
  );
}

export default ButtonExample;
```

## Touchable Opacity:
Komponen Touchable Opacity digunakan untuk membuat area yang dapat diakses oleh sentuhan pengguna. Ini sering digunakan untuk membuat tindakan interaktif di luar dari tombol standar. Kamu dapat menggambarkan tombol kustom atau elemen lain sebagai elemen "sentuh".

Contoh Kode Touchable Opacity :

```jsx
import React from 'react';
import { View, Text, TouchableOpacity, Alert } from 'react-native';

const TouchableOpacityExample = () => {
  const handlePress = () => {
    Alert.alert('Elemen ditekan!', 'Anda berhasil mengklik elemen sentuh.');
  };

  return (
    <View>
      <TouchableOpacity onPress={handlePress}>
        <Text>Klik Saya</Text>
      </TouchableOpacity>
    </View>
  );
}

export default TouchableOpacityExample;

```