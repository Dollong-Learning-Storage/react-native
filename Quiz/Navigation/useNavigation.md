## Easy - 5 Poin

1. Apa fungsi dari hook useNavigation dalam React Navigation di React Native?
   A. Mengambil data dari API
   B. Mengelola state komponen
   C. Mengakses objek navigasi dari komponen fungsional
   D. Menggunakan animasi transisi halaman
2. Bagaimana useNavigation membantu dalam mengakses objek navigasi dalam komponen fungsional?
   A. Dengan membuat objek navigasi secara manual
   B. Dengan mengimport modul navigasi dari React Navigation
   C. Dengan menghubungkan komponen ke objek navigasi menggunakan properti
   D. Dengan menggunakan hook useNavigation untuk mendapatkan objek navigasi

Jawaban:

1. C
2. D

## Medium - 10 Poin (Application):

```jsx
import { useNavigation } from '@react-navigation/native';

const MyComponent = () => {
  const navigation = useNavigation();

  const goToScreen = (screenName) => {
    // Menggunakan objek navigasi untuk navigasi ke halaman lain
    navigation.navigate(???, { paramName: 'someValue' });
  };

  return (
    // Konten komponen...
  );
};

```

1. Berikut adalah potongan kode. Pilih jawaban yang benar untuk mengganti tanda tanya ? agar kode berfungsi dengan baik:
   A. navigation.to(screenName)
   B. navigation.go(screenName)
   C. navigation.navigate(screenName)
   D. navigation.push(screenName)
2. Kapan sebaiknya Anda menggunakan useNavigation daripada properti navigation yang diteruskan dari komponen induk?
   A. Saat komponen membutuhkan properti tambahan dari navigasi
   B. Saat komponen ingin mengakses riwayat navigasi secara langsung
   C. Saat komponen memiliki lebih dari satu objek navigasi
   D. Saat komponen tidak memerlukan akses ke objek navigasi

Jawaban:

1. C
2. B

## Intermediate - 15 Poin (Analyze):

1. Jelaskan perbedaan antara useNavigation dan useRoute hooks dalam React Navigation. Kapan sebaiknya Anda menggunakan masing-masing hook?
   A. useNavigation digunakan untuk navigasi antar layar, sedangkan useRoute digunakan untuk mendapatkan informasi tentang rute saat ini. Sebaiknya gunakan useNavigation saat memerlukan navigasi, dan useRoute saat memerlukan informasi rute seperti parameter.
   B. useNavigation digunakan untuk mengakses properti navigasi, sedangkan useRoute digunakan untuk mengakses parameter rute saat ini. Sebaiknya gunakan useNavigation saat memerlukan akses ke navigasi, dan useRoute saat memerlukan akses ke parameter rute.
   C. useNavigation dan useRoute adalah sama, hanya nama yang berbeda. Gunakan keduanya secara bergantian tergantung pada preferensi pengembang.
   D. useNavigation dan useRoute tidak ada perbedaan. Keduanya dapat digunakan untuk mengakses properti navigasi dan parameter rute.
2. Bagaimana Anda akan menangani situasi ketika objek navigasi yang diambil menggunakan useNavigation adalah undefined dalam komponen fungsional? Berikan beberapa solusi.
   A. Menggunakan hook useFocusEffect untuk memastikan objek navigasi selalu tersedia saat komponen mendapat fokus
   B. Menyembunyikan komponen sampai objek navigasi tersedia untuk penggunaan
   C. Menggunakan fungsi useCallback untuk menetapkan objek navigasi hanya jika objek tersebut tidak undefined
   D. Menggunakan try-catch statement untuk menangkap kesalahan dan menampilkan pesan kesalahan kepada pengguna

Jawaban:

1. A
2. D

## Advance - 20 Poin

1. Jelaskan proses internal yang terjadi saat hook useNavigation dipanggil dalam komponen fungsional React Native. Bagaimana objek navigasi terkait dengan tumpukan navigasi (navigation stack)?
   A. Hook useNavigation memanggil fungsi internal dari React Navigation untuk mencari objek navigasi yang sesuai dengan komponen fungsional yang sedang berjalan. Objek navigasi terkait dengan tumpukan navigasi melalui identifikasi unik dari rute yang sedang aktif.
   B. Hook useNavigation memanfaatkan konteks navigasi yang disediakan oleh komponen induk terdekat yang memiliki objek navigasi. Objek navigasi terkait dengan tumpukan navigasi melalui informasi rute yang diteruskan saat navigasi antar halaman.
   C. Hook useNavigation menggunakan properti konteks global yang dikelola oleh React Navigation. Objek navigasi terkait dengan tumpukan navigasi melalui pengenalan unik, seperti nama rute atau ID halaman.
   D. Proses internal hook useNavigation tidak tergantung pada tumpukan navigasi. Objek navigasi hanya memahami halaman yang saat ini aktif dan parameter yang terkait.

Jawaban:

1. A
