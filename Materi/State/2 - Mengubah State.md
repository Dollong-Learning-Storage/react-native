**useState** mengembalikan dua nilai dalam array, kita sebut aja `state` dan `setState`. `state` berperilaku seperti variabel pada umumnya, yang biasa kita pakai untuk isi data dan data nya itu yang di pakai.

```jsx
const [state, _] = useState("default value nya");
```

Sedangkan `setState` yang di gunakan untuk meng-_update_ `state` nya.

```jsx
const [state, setState] = useState("default value nya");

setState("update data");
```

Mari lihat contoh di bawah

<div style="width: 800px;position:relative;overflow-x:auto">
<iframe src="https://snack.expo.dev/@doltons/setstate" height="500" width="1500"></iframe>
</div>

Pada contoh tersebut kita mencoba _update_ `state` count yang sudah kita buat pada topik sebelumnya. Kemarin kita menggunakan _state count_ dan ketika perlu di update kita bisa menggunakan setState.

Pastikan dalam satu state berisi data yang pasti. Misal kalian punya case login. Di form kalian memiliki 2 input, **email** dan **password**. Maka sudah pasti kalian membutuhkan state `email` dan `password`.

```jsx
const [email, setEmail] = useState("");
const [password, setPassword] = useState("");
```

Kita mengisi nya dengan default value yaitu **string kosong**. Pastikan yang akan kalian update juga dalam string jangan tiba-tiba berubah menjadi array

```jsx
const [email, setEmail] = useState("");
const [password, setPassword] = useState("");

setEmail(["email satu", "email dua"]);
```

<!-- ```jsx
import React, { useState } from "react";
import { View, Text, Button, StyleSheet } from "react-native";

const StateExample = () => {
  const [count, setCount] = useState(0);

  const increaseCount = () => {
    setCount(count + 1);
  };

  return (
    <View>
      <Text>Hitungan: {count}</Text>
      <Button title="Tambah" onPress={increaseCount} />
    </View>
  );
};

export default StateExample;
``` -->

**Penjelasan Kode:**

- Dalam contoh ini, kita menggunakan React Hooks dengan `useState` untuk membuat state `count` dan fungsi `setCount` untuk mengubahnya.
- Pada `increaseCount`, kita menggunakan `setCount` untuk menambah nilai `count` setiap kali tombol ditekan.
- Saat `count` berubah, komponen akan dirender ulang dengan nilai `count` yang baru, sehingga tampilan akan selalu diperbarui sesuai dengan nilai state terbaru.

Mengubah state adalah cara utama untuk membuat komponen React Native berinteraksi dengan pengguna dan menyediakan pengalaman dinamis. Dengan menggunakan langkah-langkah di atas, kamu dapat mengelola dan mengubah state secara efektif dalam aplikasi kamu.
