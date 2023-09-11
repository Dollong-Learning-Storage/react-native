Komponen Image digunakan dalam React Native untuk menampilkan gambar di antarmuka pengguna. Ini memungkinkan Anda menampilkan gambar dari sumber lokal maupun publik.

**Fungsi dan Kegunaan:**

1. **Menampilkan Gambar:** Komponen Image digunakan untuk menampilkan gambar di dalam aplikasi.
2. **Optimalisasi Tampilan:** Anda dapat mengatur ukuran, aspek rasio, dan penggunaan caching untuk mengoptimalkan tampilan gambar.
3. **Sumber Gambar:** Image mendukung berbagai sumber gambar, termasuk gambar lokal di dalam proyek dan gambar yang diambil dari URL.

**Contoh Kode:**

<iframe src="https://snack.expo.dev/@doltons/image-component" height="500" width="100%" title="Image Example"></iframe>

<!-- ```jsx
import React from 'react';
import { View, Image, StyleSheet } from 'react-native';

const ImageExample = () => {
  return (
    <View>
      {/* Gambar dari sumber lokal */}
      <Image
        source={require('./assets/local-image.jpg')}
      />

      {/* Gambar dari sumber publik */}
      <Image
        source={{ uri: 'https://example.com/public-image.jpg' }}
      />
    </View>
  );
}

export default ImageExample;
``` -->

**Perbedaan Cara Menggunakan Image:**

1. **Local Image:** Menggunakan `require()` untuk mengambil gambar dari direktori proyek. Ini cocok untuk gambar yang ada di proyek kamu sendiri.
2. **Public Image (URL):** Menggunakan `source={{ uri: 'https://example.com/image.jpg' }}` untuk mengambil gambar dari URL. Ini digunakan untuk menampilkan gambar dari sumber eksternal seperti internet.
