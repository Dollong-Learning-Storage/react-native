## Image

![Init React](<../../Assets/Materi/UI Native/image-explanation.png>)

Komponen Image digunakan dalam React Native untuk menampilkan gambar di antarmuka pengguna. Ini memungkinkan Kamu menampilkan gambar dari sumber lokal maupun publik / luar

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

**Dua cara menggunakan Image:**

1. **Local Image:** Menggunakan `require()` untuk mengambil gambar dari direktori proyek. Ini cocok untuk gambar yang ada di proyek kamu sendiri. Misalnya gambar tersebut di simpan di folder `/assets`
2. **Public Image (URL):** Menggunakan `source={{ uri: 'https://example.com/image.jpg' }}` untuk mengambil gambar dari URL. Ini digunakan untuk menampilkan gambar dari sumber eksternal seperti internet.

# Quiz

## Easy - 5 Poin

1. Apa kegunaan dari komponen Image dalam React Native?
   - A. Mengoptimalkan tampilan teks.
   - [x] B. Menampilkan gambar dari sumber lokal atau publik.
   - C. Mengatur ukuran dan aspek rasio teks.
   - D. Mengelola state dalam aplikasi.
2. Bagaimana cara mengambil gambar dari direktori proyek (sumber lokal) menggunakan komponen Image?
   - [x] A. source={require('./assets/local-image.jpg')}
   - B. source={{ uri: 'https://example.com/public-image.jpg' }}
   - C. source={{ './assets/local-image.jpg' }}
   - D. source={import('./assets/local-image.jpg')}
3. Bagaimana cara mengambil gambar dari sumber eksternal seperti internet (URL) menggunakan komponen Image?
   - A. source={require('./assets/local-image.jpg')}
   - [x] B. source={{ uri: 'https://example.com/public-image.jpg' }}
   - C. source={{ './assets/local-image.jpg' }}
   - D. source={import('./assets/local-image.jpg')}

## Medium - 10 Poin

```jsx
import React from 'react';
import { View, Image } from 'react-native';

const MyComponent = () => {
  return (
    <View>
      <Image
        style={{ width: 100, height: 100 }}
        source={???}
      />
    </View>
  );
};
```

1. Berikut adalah potongan kode. Pilih jawaban yang benar untuk mengganti tanda tanya ? agar kode berfungsi dengan baik:
   - [x] A. { uri: 'https://example.com/image.jpg' }
   - B. 'image.jpg'
   - C. require('./image.jpg')
   - D. 100x100
