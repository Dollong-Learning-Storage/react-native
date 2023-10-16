## Pengenalan Async Storage

Dalam teknologi Website, kita menggunakan

Async storage adalah teknik penyimpanan data asinkron yang digunakan dalam pengembangan aplikasi React Native. Dalam konteks pengembangan mobile, menyimpan data secara permanen sangat penting untuk memberikan pengalaman pengguna yang konsisten. Async storage memungkinkan aplikasi untuk menyimpan data dengan cara yang aman, efisien, dan mudah diakses.

**Keuntungan Async Storage:**

Persistensi Data: Data tetap ada meskipun aplikasi ditutup atau perangkat dimatikan.
Efisien: Menggunakan sistem penyimpanan lokal perangkat, yang memungkinkan akses data secara cepat.
Sederhana: Antarmuka yang mudah digunakan untuk menyimpan dan mengambil data.
Ringan: Tidak membebani kinerja aplikasi dengan beban besar.

### Instalasi Async Storage

Buka direktori proyek React Native Kamu, dan jalankan perintah berikut:

```bash
npm install @react-native-async-storage/async-storage
```

atau menggunakan yarn

```bash
yarn add @react-native-async-storage/async-storage
```

Untuk menyimpan data, kita bisa gunakan fungsi setItem():

```jsx
const simpanData = async () => {
  try {
    await AsyncStorage.setItem("key", "nilai");
    console.log("Data berhasil disimpan!");
  } catch (error) {
    console.error("Gagal menyimpan data: ", error);
  }
};
```

Untuk mengambil data, gunakan fungsi getItem():

```jsx
const ambilData = async () => {
  try {
    const nilai = await AsyncStorage.getItem("key");
    if (nilai !== null) {
      console.log("Nilai yang diambil dari AsyncStorage: ", nilai);
    } else {
      console.log("Tidak ada data dengan key tersebut.");
    }
  } catch (error) {
    console.error("Gagal mengambil data: ", error);
  }
};
```
