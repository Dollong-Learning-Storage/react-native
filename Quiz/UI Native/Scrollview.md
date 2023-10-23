## Easy - 5 poin

1. ScrollView adalah komponen yang digunakan untuk membuat area yang dapat digeser. Manakah pernyataan berikut yang benar?
   A. ScrollView hanya dapat digunakan untuk menggeser konten secara vertikal.
   B. ScrollView dapat digunakan untuk menggeser konten secara horizontal atau vertikal.
   C. ScrollView dapat digunakan untuk menggeser konten hanya jika konten tersebut lebih besar dari ukuran ScrollView.
   D. ScrollView dapat digunakan untuk menggeser konten apa pun, terlepas dari ukurannya.
2. Apa tujuan utama penggunaan ScrollView di React Native?
   A. Membuat tampilan yang tidak dapat digulir.
   B. Membuat daftar item yang dapat digulir.
   C. Mengatur tata letak komponen di dalam aplikasi.
   d. Menambahkan gambar latar belakang ke layar.
3. Apa perbedaan utama antara ScrollView dan FlatList dalam React Native?
   A. ScrollView hanya mendukung tata letak vertikal, sementara FlatList mendukung tata letak vertikal dan horizontal.
   B. ScrollView lebih efisien dalam menampilkan daftar data besar dibandingkan FlatList.
   C. FlatList lebih fleksibel dan efisien dalam menangani daftar data besar, sementara ScrollView merender semua elemen sekaligus.
   D. Tidak ada perbedaan, keduanya dapat digunakan untuk menampilkan daftar data.

Jawaban :

1. B.
2. B.
3. C.

## Medium

1. Apa yang harus Kamu lakukan jika konten dalam ScrollView lebih panjang daripada area tampilan ScrollView itu sendiri?
   A. Menggunakan komponen ScrollView secara otomatis dapat menangani hal ini.
   B. Menambahkan prop scrollEnabled dan mengaturnya menjadi true.
   C. Menambahkan prop contentContainerStyle untuk mengatur ukuran konten yang lebih besar.
   d. Tidak mungkin membuat konten yang lebih panjang daripada area tampilan ScrollView.

Jawaban:

1. C.

## Intermediate - 15 poin

1. Bagaimana cara mengimplementasikan ScrollView dengan beberapa elemen Text di dalamnya dalam aplikasi React Native?
   A.

   ```jsx
   <ScrollView>
     <Text>Element 1</Text>
     <Text>Element 2</Text>
     <Text>Element 3</Text>
   </ScrollView>
   ```

   B.

   ```jsx
   <ScrollView>
     <ScrollViewElement>Element 1</ScrollViewElement>
     <ScrollViewElement>Element 2</ScrollViewElement>
     <ScrollViewElement>Element 3</ScrollViewElement>
   </ScrollView>
   ```

   C.

   ```jsx
   <ScrollView>
     {["Element 1", "Element 2", "Element 3"].map((element, index) => (
       <Text key={index}>{element}</Text>
     ))}
   </ScrollView>
   ```

   D.

   ```jsx
   <ScrollView>
     <Text key={1}>Element 1</Text>
     <Text key={2}>Element 2</Text>
     <Text key={3}>Element 3</Text>
   </ScrollView>
   ```

2. Bagaimana cara mengatur properti contentContainerStyle dalam komponen ScrollView untuk mengatur tata letak elemen-elemen di dalamnya?
   A. Menggunakan objek gaya CSS dalam properti contentContainerStyle.
   B. Menggunakan properti style langsung pada elemen-elemen di dalam ScrollView.
   C. Menggunakan properti contentContainerStyle dan memberikan nilai berupa objek gaya React Native.
   D. Tidak ada properti contentContainerStyle dalam komponen ScrollView.

Jawaban:

1. A
2. C

## Intermediate - 15 Poin:

1. Apa yang terjadi jika elemen-elemen di dalam ScrollView memiliki konten yang sangat panjang, melebihi tinggi layar perangkat?
   A. ScrollView akan secara otomatis menambahkan scrollbar untuk memungkinkan pengguna menggulir ke bawah.
   B. Pengguna tidak akan dapat melihat elemen-elemen yang berada di luar jangkauan layar, kecuali jika mereka menggulir.
   C. Elemen-elemen yang berada di luar jangkauan layar akan ditempatkan di halaman baru yang dapat diakses melalui tombol "Selanjutnya".
   D. Elemen-elemen yang berada di luar jangkauan layar akan secara otomatis dipangkas sehingga sesuai dengan tinggi layar perangkat.
2. Apa manfaat menggunakan nested properti dalam komponen ScrollView dalam pengembangan aplikasi React Native?
   A. Membuat ScrollView dapat ditempatkan di dalam komponen FlatList.
   B. Tidak ada properti nested dalam komponen ScrollView.
   C. Membuat elemen-elemen di dalam ScrollView dapat menggulir bersama dengan elemen-elemen di luar ScrollView.
   D. Membuat elemen-elemen di dalam ScrollView dapat menggulir terpisah dari elemen-elemen di luar ScrollView.

Jawaban:

1. B
2. D

## Advanced - 20 Poin:

1. Jelaskan situasi di mana penggunaan FlatList lebih disarankan daripada menggunakan ScrollView dalam pengembangan aplikasi React Native.

Jawaban:
Penggunaan FlatList lebih disarankan daripada menggunakan ScrollView dalam situasi-situasi berikut:

Daftar Data Dinamis: Ketika Anda memiliki daftar data yang dinamis dan besar, terutama data yang akan diambil dari sumber eksternal seperti API. FlatList akan memungkinkan Anda untuk menangani daftar data besar dengan efisien, hanya merender elemen-elemen yang terlihat di layar, sehingga menghemat memori dan meningkatkan kinerja aplikasi.

Optimasi Kinerja: Saat aplikasi Anda membutuhkan optimasi kinerja dan penggunaan memori yang efisien. FlatList menggunakan teknik pemberdayaan (virtualization) yang memungkinkan penggunaan memori yang minimal, terutama saat menangani daftar data yang sangat besar.

Pencarian dan Filter: Jika aplikasi Anda memungkinkan pengguna melakukan pencarian atau filter pada daftar data. FlatList memungkinkan Anda memperbarui data dinamisnya dengan mudah saat filter atau pencarian berubah, sementara di ScrollView, Anda harus
