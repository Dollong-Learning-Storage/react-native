1. Apa fungsi dari props dalam React Native?
   A. Menyimpan data dalam komponen anak.
   B. Mengirim data dari komponen anak ke komponen induk.
   C. Mengirim data dari komponen induk ke komponen anak.
   D. Menyimpan data dalam komponen induk.

```jsx
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
```

2. Pada contoh kode yang diberikan, apa yang akan ditampilkan oleh komponen <Greeting name="Ahmad" />?
   A. "Halo, Ahmad!"
   B. "Halo, Budi!"
   C. "Halo, Ahmad"
   D. Error karena properti nama tidak ada pada Component Greeting
3. Mengapa props sangat berguna dalam pengembangan aplikasi React Native?
   A. Props memungkinkan komponen anak mengubah perilaku komponen induk.
   B. Props memungkinkan komponen induk mengubah perilaku komponen anak.
   C. Props membuat komunikasi antara komponen menjadi lebih rumit.
   D. Props hanya bisa digunakan dalam satu komponen.

Jawaban :

1. C
2. A
3. B
