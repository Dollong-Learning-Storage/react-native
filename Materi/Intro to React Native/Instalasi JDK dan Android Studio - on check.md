Ada dua cara untuk mengembangkan aplikasi React Native, yaitu dengan online IDE seperti Snack Expo dan menggunakan emulator sendiri.

## Snack Expo

Snack Expo merupakan online Editor yang juga memungkinkan kamu melihat preview dari aplikasi kamu langsung tanpa perlu menggunakan emulator,

Kamu hanya perlu mengakses halaman ini, [Snack Expo](https://snack.expo.dev).
![Init React](<../../Assets/Materi/Intro to React Native/expo-snack-preview.png>).

Ketika kamu sudah mengakses halaman snack expo maka kamu akan di diberikan code editor juga emulator nya yang bisa langsung kamu pakai. Gimana? Mudah bukan!

## Android Studio

Cara Lain yang bisa kamu gunakan untuk mengembangkan aplikasi React Native kamu ialah dengan menggunakan emulator punya kamu sendiri atau Android Studio secara lokal

Langkah pertama yang perlu kamu lakukan adalah menginstal JDK (Java Development Kit) dan Android Studio. JDK diperlukan untuk menjalankan proses kompilasi dan eksekusi aplikasi React Native, sedangkan Android Studio digunakan untuk mengelola lingkungan pengembangan Android serta menyediakan emulator untuk menjalankan aplikasi pada berbagai perangkat virtual.

Link instalasi
[https://reactnative.dev/docs/environment-setup?platform=android](https://reactnative.dev/docs/environment-setup?platform=android)

Berikut adalah langkah-langkah untuk menginstal JDK dan Android Studio:

**Langkah 1: Instalasi JDK**

1. **Unduh JDK**: Kunjungi situs resmi Oracle untuk mengunduh versi terbaru JDK ([Link](https://www.oracle.com/id/java/technologies/javase/jdk11-archive-downloads.html))
2. **Mulai Instalasi**: Buka berkas installer JDK yang telah kamu unduh.
3. **Setup Enviroment**: Setelah instalasi selesai, kamu perlu menambahkan jalur instalasi JDK ke dalam variabel lingkungan sistem. Ini memungkinkan sistemmu untuk menemukan perintah-perintah yang terkait dengan JDK. Petunjuk konfigurasi variabel lingkungan dapat berbeda tergantung pada sistem operasi yang kamu gunakan.

**Langkah 2: Instalasi Android Studio**

1. **Unduh Android Studio**: Kunjungi situs resmi Android Studio ([Link](https://developer.android.com/studio)) dan unduh versi terbaru sesuai dengan sistem operasi kamu.
2. **Instalasi**: Buka berkas installer Android Studio yang telah kamu unduh. Ikuti instruksi instalasi yang muncul. Pilih komponen yang ingin kamu instal, seperti Android SDK dan Android Virtual Device.
3. **Konfigurasi Android SDK**: Setelah instalasi Android Studio selesai, kamu perlu mengonfigurasi lokasi Android SDK. Buka env seperti gambar di bawah
   ![Init React](<../../Assets/Materi/Intro to React Native/install-react-native.png>)
   Akan ada path untuk ANDROID_HOME, jika belum ada boleh tambahkan dan isi sesuai lokasi dari android sdk kamu
4. **Instal Android Virtual Device (AVD)**: AVD adalah emulator Android yang dapat kamu gunakan untuk menguji aplikasi React Native pada berbagai perangkat virtual. Dalam Android Studio, buka "AVD Manager" dan ikuti petunjuk untuk membuat dan mengonfigurasi emulator sesuai preferensimu.

## Instalasi React Native

1. Buka folder yang ingin kalian isi dengan project React Native kalian, buka terminal di folder tersebut lalu masukkan ini
   `npx react-native@latest init NamaProject`, dan tekan enter untuk eksekusi perintahnya
   ![Init React](<../../Assets/Materi/Intro to React Native/install-react-native.png>)
2. Kemudian Masuk ke folder project kalian, dan jalankan yarn/npm start
   `yarn start`
3. Otomatis jika setup dan instalasi kalian berjalan lancar sdan sudh benar, maka kalian akan melihat emulator kalian otomatis nyala dan menginstall aplikasi kalian
   ![Init React](<../../Assets/Materi/Intro to React Native/react-native-overview.png>)
