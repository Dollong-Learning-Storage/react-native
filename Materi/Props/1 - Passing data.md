# Props

_Props_ merupakan salah satu keunggulan dari React Native. Mari lihat gambar di bawah:
![List](../../Assets/Materi/Props/list.png)

Dalam contoh di atas kita bisa melihat kalau list "Belajar Mandiri" dan "Program Bootcamp" itu kurang lebih sama. Secara kode akan seperti ini:

```jsx
const Program = () => (
  <View>
    {/* title */}
    <Text>Belajar Mandiri</Text>
    {/* list konten */}
    <View>
      <Text>→ Kelas</Text>
      <Text>→ Skilpath</Text>
      <Text>→ Paket</Text>
    </View>

    {/* title */}
    <Text>Program Bootcamp</Text>
    {/* list konten */}
    <View>
      <Text>→ Product Management Immersive (PMI)</Text>
      <Text>→ Full-Stack UI/UX Design - JobReady</Text>
    </View>
  </View>
);
```

Wah beneran sama!, sama-sama memiliki title dan list konten.

Keunggulan React adalah memungkinkan kamu membuat component lebih modular seperti yang sudah di bahas di Intro To React Native. Berarti kode yang seperti ini, _bisa kita buat lebih efisien dengan membuat component nya sendiri_.

Melihat UI tadi, kita menyadari bahwa kedua list tersebut berpotensi bisa di buat _modular_ (bisa di pakai di beberapa case).

![List with Mark](../../Assets/Materi/Props/list-with-mark.png)

Berikut implementasinya:

```jsx
const ListProgram = () => {
  return (
    <>
      <Text style={styles.titleText}>Belajar Mandiri</Text>
      <View style={styles.listContent}>
        <Text>→ Kelas</Text>
        <Text>→ Skilpath</Text>
        <Text>→ Paket</Text>
      </View>
    </>
  );
};

const Program = () => (
  <View>
    <ListProgram />
    <ListProgram />
  </View>
);
```

Gimana? lebih simpel bukan. Eitss tunggu dulu, kita masih butuh satu proses lagi untuk benar-benar yakin. Kode kita saat ini memang sudah cukup _modular dan reusable_ tapi hasilnya belum seperti yang kita inginkan di awal.

![Result](../../Assets/Materi/Props/result.png)

Melihat dari yang sudah di buat sepertinya sudah tepat, tapi konsep _modular_ memungkinkan component yang di buat di mungkinkan di beberapa case dan _future proof_. Kita tau bahwa yang serupa itu ada di **title** dan **list konten**, maka pada component `ListProgram` kita perlu memastikan `title` dan `konten` nya bisa sesuai dengan kebutuhan .

> Note!
>
> Future proof merupakan istilah untuk apapun yang kita buat saat ini akan berguna untuk bukan hanya kebutuhan saat ini tetapi juga masih layak untuk di masa depan.

## Passing Data

Pada React ada satu cara untuk memungkinkan kebutuhan kita di atas yaitu dengan _props_. Mari intip sedikit cara penggunaan nya.

```jsx
const Greeting = (props) => {
  return <Text>Halo, {props.name}!</Text>;
};

const ListFriends = () => {
  return (
    <View>
      <Greeting name="Ahmad" />
      <Greeting name="Budi" />
    </View>
  );
};
```

Pada contoh di atas mungkin kamu akan sedikit familiar. Yap, props!. Sama seperti _attribute_ pada HTML. _Di React kamu di mungkinkan untuk membuat elemen mu sendiri dengan sebutan Component_.

Cara membuat props adalah dengan passing props sebagai parameter dari component kamu. Dari yang awalnya masih _hardcode_ seperti ini

```jsx
const Greeting = () => {
  return <Text>Halo, Ahmad!</Text>;
};
```

Kamu bisa tambahkan _props_ **untuk memungkinkan ga hanya Ahmad yang di sapa**

```jsx
const Greeting = (props) => {
  return <Text>Halo, {props.name}!</Text>;
};
```

> Note!
>
> Props bisa menyimpan tipe data apa saja

Mudah kan?. Materi berikutnya kamu akan belajar passing component

<!-- Dalam React Native, props adalah cara untuk mengirimkan data dari komponen induk (parent component) ke komponen anak (child component). Props memungkinkan komponen untuk menerima dan menggunakan data eksternal, membuat komponen menjadi lebih dinamis dan dapat digunakan ulang dengan lebih baik.

**Peran dan Fungsi Props:** Props digunakan untuk mengirimkan informasi dari komponen induk ke komponen anak. Ini memungkinkan kita untuk mengubah perilaku atau tampilan komponen anak berdasarkan data yang diterima dari induk. Props adalah salah satu cara utama untuk membuat komunikasi antara komponen dalam hierarki. -->

<!-- **Contoh Penggunaan Props:**

<iframe src="https://snack.expo.dev/@doltons/props-data" height="500" width="1500"></iframe>

```jsx
import React from "react";
import { View, Text } from "react-native";

const Greeting = (props) => {
  return <Text>Halo, {props.name}!</Text>;
};

const App = () => {
  return (
    <View>
      <Greeting name="Ahmad" />
      <Greeting name="Budi" />
    </View>
  );
};

export default App;
``` -->
