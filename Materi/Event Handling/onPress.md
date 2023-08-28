Pada React Native, event handling adalah cara kita merespons aksi yang dilakukan oleh pengguna terhadap elemen UI. Salah satu event handling yang umum digunakan adalah `onPress`. Event `onPress` digunakan untuk menangkap ketika pengguna menekan (klik) elemen tertentu, seperti tombol.

**Fungsi dan Kegunaan onPress:** 
Event `onPress` memberi Anda kemampuan untuk merespons tindakan pengguna secara interaktif. Ketika pengguna menekan elemen dengan event `onPress`, Anda dapat mengeksekusi kode tertentu, misalnya untuk memicu perubahan tampilan, memanggil fungsi, atau menavigasi antarmuka pengguna.

**Contoh Kode:**

```jsx
import React from 'react';
import { View, Text, TouchableOpacity, StyleSheet } from 'react-native';

const ButtonExample = () => {
  const handlePress = () => {
    alert('Tombol telah ditekan!');
  };

  return (
    <View style={styles.container}>
      <TouchableOpacity onPress={handlePress} style={styles.button}>
        <Text style={styles.buttonText}>Tekan Saya</Text>
      </TouchableOpacity>
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    backgroundColor: '#ffffff',
  },
  button: {
    backgroundColor: '#3498db',
    padding: 10,
    borderRadius: 5,
  },
  buttonText: {
    color: '#ffffff',
    fontSize: 18,
  },
});

export default ButtonExample;
```

**Penjelasan Kode:**

- Pada contoh di atas, komponen `TouchableOpacity` digunakan untuk membuat elemen yang bisa di-'tekan'.
- Properti `onPress` dari `TouchableOpacity` ditetapkan dengan fungsi `handlePress`.
- Fungsi `handlePress` akan dipanggil ketika pengguna menekan elemen.
- Dalam contoh ini, ketika tombol ditekan, kita memanggil fungsi `alert` untuk menampilkan pesan.
- Gaya (style) diterapkan pada elemen `TouchableOpacity` untuk memberikan tampilan tombol yang lebih menarik.

Event handling `onPress` memungkinkan Anda untuk memberikan interaksi yang responsif kepada pengguna ketika mereka berinteraksi dengan elemen UI. Dalam contoh ini, pesan akan muncul ketika tombol ditekan.