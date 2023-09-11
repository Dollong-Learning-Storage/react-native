Dalam React Native, props adalah cara untuk mengirimkan data dari komponen induk ke komponen anak. Selain data, kita juga dapat mengirimkan komponen itu sendiri sebagai prop. Ini disebut "Passing Component". Passing component memungkinkan kita untuk menyusun komponen yang lebih dinamis dan dapat digunakan ulang.

**Passing Component:**
Passing component adalah ketika kita mengirimkan suatu komponen sebagai nilai prop ke komponen lain, sehingga komponen penerima bisa merender dan memanipulasi komponen tersebut.

**Contoh Kode:**

<iframe src="https://snack.expo.dev/@doltons/props-component" height="500" width="100%"></iframe>

Misalkan kita memiliki komponen `Header` yang akan ditampilkan di beberapa layar yang berbeda:

Path: `components/Header.js`

```jsx
import React from "react";
import { View, Text } from "react-native";

const Header = ({ title, children }) => {
  return (
    <View>
      <Text style={{ fontSize: 20 }}>{title}</Text>
      {children}
    </View>
  );
};

export default Header;
```

Di sini, kita memiliki prop `title` dan juga menggunakan `{props.children}` untuk merender elemen apa pun yang dilewatkan sebagai child dalam komponen.

Kemudian, kita dapat menggunakan komponen `Header` di beberapa layar dengan cara yang berbeda:

Path: `App.js`

```jsx
import React from "react";
import { View } from "react-native";
import Header from "./Header";

const ScreenA = () => {
  return (
    <View>
      <Header title="Halaman A" />
      {/* Konten layar lainnya */}
    </View>
  );
};

const ScreenB = () => {
  return (
    <View>
      <Header title="Halaman B">
        <Text>Ini adalah konten tambahan di header</Text>
      </Header>
      {/* Konten layar lainnya */}
    </View>
  );
};

const App = () => {
  return (
    <View>
      <ScreenA />
      <ScreenB />
    </View>
  );
};

export default App;
```

**Penjelasan Kode:**

- Kita mengimpor komponen `Header` yang telah kita buat sebelumnya.
- Di `ScreenA`, kita hanya meneruskan prop `title` ke komponen `Header`.
- Di `ScreenB`, kita meneruskan prop `title` serta menambahkan elemen teks sebagai child di dalam komponen `Header`.

Dengan cara ini, kita dapat menggunakan komponen `Header` secara dinamis di berbagai layar dengan konten yang berbeda-beda. Ini memungkinkan kita untuk merancang komponen yang dapat digunakan ulang dan lebih fleksibel dalam menyusun antarmuka pengguna.
