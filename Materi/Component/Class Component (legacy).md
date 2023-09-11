Class Component merupakan salah satu tipe komponen dalam React Native yang digunakan untuk membangun antarmuka pengguna (UI). Pada awalnya, class component adalah pendekatan utama dalam pembangunan komponen dalam React, sebelum diperkenalkannya Functional Component. Namun, dengan perkembangan React, penggunaan Functional Component menjadi lebih disarankan.

**Kelebihan dan Kekurangan Class Component:** **Kelebihan:**

1. **Mempunyai State dan Lifecycle Methods:** Class Component memungkinkan penggunaan `state` untuk menyimpan data dinamis dan `lifecycle methods` untuk mengatur perilaku komponen pada berbagai fase siklus hidupnya.
2. **Legacy Codebase:** Jika Anda bekerja pada proyek lama yang menggunakan pendekatan class component, Anda akan menemukan lebih banyak contoh kode dalam format class component.

**Kekurangan:**

1. **Lebih Rumit:** Penulisan dan pemahaman kode Class Component cenderung lebih rumit dibandingkan dengan Functional Component.
2. **Lebih Banyak Boilerplate:** Diperlukan lebih banyak kode boilerplate untuk membuat sebuah class component.
3. **Kinerja dan Optimalisasi:** Class Component cenderung memiliki performa yang lebih rendah daripada Functional Component karena overhead yang lebih tinggi.

**Contoh Kode Class Component :**

<iframe src="https://snack.expo.dev/@doltons/class-component" height="500" width="100%"></iframe>

**Penggunaan dan Penjelasan Kode:**

- Import React dan komponen yang diperlukan dari 'react-native', serta `Component` dari 'react'.
- Deklarasikan sebuah class bernama `ClassComponentExample` yang extends dari `Component`.
- Definisikan `constructor` untuk menginisialisasi `state`. Dalam contoh ini, `count` diatur awalnya menjadi 0.
- Terdapat beberapa lifecycle methods, seperti `componentDidMount`, `componentDidUpdate`, dan `componentWillUnmount`, yang memungkinkan kita mengatur perilaku komponen pada berbagai tahap siklus hidupnya.
- Method `render()` diimplementasikan untuk mengembalikan tampilan yang akan ditampilkan di layar.
- Dalam contoh ini, tampilan mencakup elemen `<Text>` yang menampilkan pesan dan nilai `count` dari `state`.

Meskipun Class Component masih dapat digunakan, disarankan untuk lebih memilih Functional Component karena lebih sederhana, mudah dipahami, dan performanya lebih baik.
