NOTES

- masih ada beberapa yang sengaja tidak dimasukkan di lms, masih di pikirkan. terlalu banyak

## Easy - 5 Poin

1. Apa kegunaan dari komponen Image dalam React Native?
   a. Mengoptimalkan tampilan teks.
   b. Menampilkan gambar dari sumber lokal atau publik.
   c. Mengatur ukuran dan aspek rasio teks.
   d. Mengelola state dalam aplikasi.
2. Bagaimana cara mengambil gambar dari direktori proyek (sumber lokal) menggunakan komponen Image?
   a. source={require('./assets/local-image.jpg')}
   b. source={{ uri: 'https://example.com/public-image.jpg' }}
   c. source={{ './assets/local-image.jpg' }}
   d. source={import('./assets/local-image.jpg')}
3. Bagaimana cara mengambil gambar dari sumber eksternal seperti internet (URL) menggunakan komponen Image?
   a. source={require('./assets/local-image.jpg')}
   b. source={{ uri: 'https://example.com/public-image.jpg' }}
   c. source={{ './assets/local-image.jpg' }}
   d. source={import('./assets/local-image.jpg')}

Jawaban :

1. B
2. A
3. B

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
   A. { uri: 'https://example.com/image.jpg' }
   B. 'image.jpg'
   C. require('./image.jpg')
   D. 100x100
2. Bagaimana Kamu mengatur gambar placeholder untuk ditampilkan ketika gambar utama sedang dimuat?
   A. Menggunakan properti placeholder pada komponen Image
   B. Menggunakan komponen PlaceholderImage sebagai anak dari komponen Image
   C. Menggunakan properti defaultSource pada komponen Image
   D. Menggunakan properti loadingIndicatorSource pada komponen Image

Jawaban:

1. A
2. C

## Intermediate - 15 Poin

1. Apa yang terjadi ketika properti resizeMode pada komponen Image diatur sebagai 'cover'?
   A. Gambar akan diposisikan dan diubah ukuran sedemikian rupa sehingga seluruh area gambar tercakup tanpa merusak rasio aspeknya.
   B. Gambar akan diperbesar hingga mengisi seluruh area komponen Image tanpa memperhatikan rasio aspek.
   C. Gambar akan ditampilkan dengan ukuran aslinya tanpa perubahan.
   D. Gambar akan diposisikan di tengah area komponen Image tanpa mengubah ukuran atau merusak rasio aspeknya.
2. Bagaimana Kamu menangani kesalahan (error) saat mengambil gambar dari sumber eksternal, seperti URL yang tidak valid?
   A. Menyematkan gambar placeholder sebagai ganti gambar yang gagal dimuat.
   B. Menampilkan pesan kesalahan kepada pengguna dan memberikan opsi untuk mencoba memuat gambar lagi.
   C. Menyembunyikan komponen Image dan menampilkan pesan kesalahan secara terpisah.
   D. Menggunakan properti onError pada komponen Image untuk menangkap kesalahan dan mengambil tindakan yang sesuai.

Jawaban:

1. A
2. D
