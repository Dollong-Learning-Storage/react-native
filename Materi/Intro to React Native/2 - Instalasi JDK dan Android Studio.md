Ada dua cara untuk mengembangkan aplikasi React Native, yaitu dengan online IDE seperti Snack Expo dan menggunakan emulator sendiri.

## Snack Expo

Snack Expo merupakan online Editor yang juga memungkinkan kamu melihat preview dari aplikasi kamu langsung tanpa perlu menggunakan emulator.

Kamu hanya perlu mengakses halaman ini, [Snack Expo](https://snack.expo.dev).
![Init React](<../../Assets/Materi/Intro to React Native/expo-snack-preview.png>)

Ketika kamu sudah mengakses halaman snack expo maka kamu akan di diberikan code editor juga emulator nya yang bisa _langsung kamu pakai_. Gimana? Mudah kan!

## Android Studio

Cara Lain yang bisa kamu gunakan untuk mengembangkan aplikasi React Native kamu ialah dengan menggunakan emulator punya kamu sendiri atau Android Studio secara lokal.

> **Note!** <br>
>
> - Kita hanya menjelaskan cara menggunakan emulator dari android studio
> - Pastikan

Langkah pertama yang perlu kamu lakukan adalah menginstal **JDK** (Java Development Kit) dan **Android Studio**. **JDK** diperlukan untuk menjalankan proses kompilasi dan eksekusi aplikasi React Native, sedangkan **Android Studio** digunakan untuk mengelola lingkungan pengembangan Android serta menyediakan emulator untuk menjalankan aplikasi pada berbagai perangkat virtual.

Link Dokumentasi: https://reactnative.dev/docs/environment-setup?platform=android

Berikut adalah langkah-langkah untuk menginstal JDK dan Android Studio:

### Instalasi JDK

#### 1. Unduh JDK

Kunjungi situs resmi Oracle untuk mengunduh versi terbaru JDK ([Link](https://www.oracle.com/id/java/technologies/javase/jdk11-archive-downloads.html)). Pilih sesuai OS kalian, jika menggunakan Windows boleh ikuti gambar di bawah
![Unduh JDK](<../../Assets/Materi/Intro to React Native/oracle-jdk-install-windows.png>)

#### 2. Mulai Instalasi

Buka file installer JDK kamu mak akan tampil seperti di gambar, selanjutnya cukup next2 saja sampai  
 ![JDK Install Windows](<../../Assets/Materi/Intro to React Native/jdk-install-windows.png>)

### Instalasi Android Studio

#### 1. Unduh Android Studio

Kunjungi situs resmi Android Studio ([Link](https://developer.android.com/studio))
![Download Android Studio](<../../Assets/Materi/Intro to React Native/android-studio-download.png>)
Buka berkas installer Android Studio yang telah kamu unduh. Ikuti instruksi instalasi yang muncul.

- Untuk Windows: https://developer.android.com/codelabs/basic-android-kotlin-compose-install-android-studio#2
- Untuk MAC: https://developer.android.com/codelabs/basic-android-kotlin-compose-install-android-studio#3
- Untuk Linux: https://developer.android.com/codelabs/basic-android-kotlin-compose-install-android-studio#5

#### 2. Konfigurasi Android SDK

Setelah instalasi Android Studio selesai, kamu perlu mengonfigurasi lokasi Android SDK. Buka env seperti gambar di bawah
![Init React](<../../Assets/Materi/Intro to React Native/open-env.png>)
Akan ada path untuk ANDROID_HOME, jika belum ada boleh tambahkan dan isi sesuai lokasi dari android sdk kamu

![Setup Android Studio](<../../Assets/Materi/Intro to React Native/android-home-env.png>)

Umumnya di windows pathnya berada di `C:\Users\TUF\AppData\Local\Android\Sdk`

#### 3. Instal Android Virtual Device (AVD)

AVD adalah emulator Android yang dapat kamu gunakan untuk menguji aplikasi React Native pada berbagai perangkat virtual. Dalam Android Studio, buka "AVD Manager" dan ikuti petunjuk untuk membuat dan mengonfigurasi emulator sesuai preferensimu.suai preferensimu.

## Instalasi React Native

1. Buka folder yang ingin kalian isi dengan project React Native kalian, buka terminal di folder tersebut lalu masukkan ini
   `npx react-native@latest init NamaProject`, dan tekan enter untuk eksekusi perintahnya
   ![Init React](<../../Assets/Materi/Intro to React Native/install-react-native.png>)
2. Kemudian Masuk ke folder project kalian, dan jalankan yarn/npm start
   contoh: `yarn start`
3. Otomatis jika setup dan instalasi kalian berjalan lancar sdan sudh benar, maka kalian akan melihat emulator kalian otomatis nyala dan menginstall aplikasi kalian
   ![Init React](<../../Assets/Materi/Intro to React Native/react-native-overview.png>)
