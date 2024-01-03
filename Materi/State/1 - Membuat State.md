Aplikasi yang dinamis dinilai dari konten nya yang dapat berubah dan menyesuaikan secara otomatis dengan interaksi user

![Login SKilvul](../../Assets/Materi/state/login-skilvul.png)
![Calculator](../../Assets/Materi/state/calculator.gif)

<!-- ![Count](../../Assets/Materi/state/count.gif) -->

Contohnya seperti gambar di atas, kalukator yang ketika di tekan angka 1 maka akan menampilkan 1 ke layar ataupun user ketika ingin login, tentu datanya perlu di tampung dulu untuk di cek apakah data user tersebut sudah ada di database atau belum

Untuk membuat state di dalam sebuah komponen, kamu perlu menggunakan hook `useState` (dalam functional component) atau mendefinisikan `this.state` (dalam class component).

**Contoh Kode :**

<iframe src="https://snack.expo.dev/@doltons/state" height="500" width="100%"></iframe>

Perhatikan pada bagian ini:

```jsx
const [count, _] = useState(0);
```

**useState** mengembalikan data array. Kita men-_destructure_ nilai kembalian dari useState dengan `[count, _]`. Yang terjadi di belakang layar kurang lebih seperti kalian membuat variabel. Masih ingat ga? kalau udah lupa boleh cek lagi materi **Javascript Dasar**.

`count` disitu memiliki nilai `0`. Kita memberikan nilai default untuk state tersebut dengan cara ini:

```jsx
useState(0);
```

Kalau dengan membuat variabel biasa:

```jsx
const count = 0;
```

Setelah membuat state nya kita bisa memanggil nya seperti ini:

```jsx
<Text>Nilai count: {count}</Text>
```

Mudah kan? pada materi selanjutnya kita akan membahas bagaimana meng-_update_ state

<!-- ```jsx
import React, { useState } from "react";
import { View, Text, Button } from "react-native";

const StateExample = () => {
  const [count, _] = useState(0);

  return (
    <View>
      <Text>Nilai count: {count}</Text>
    </View>
  );
};

export default StateExample;
``` -->
