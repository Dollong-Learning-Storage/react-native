1. Apa yang dimaksud dengan state dalam konteks React Native?  
   A. State adalah representasi tampilan komponen.
   B. State adalah data yang dapat berubah dalam komponen yang memengaruhi tampilan.
   C. State adalah komponen yang dapat di-render ulang.
   D. State adalah data yang bersifat tetap dalam komponen.
2. Mengapa mengubah state penting dalam pengembangan aplikasi React Native?
   A. Agar komponen memiliki nama.
   B. Agar komponen bisa dirender satu kali saja.
   C. Agar komponen bisa merespons perubahan data dan interaksi pengguna.
   D. Agar komponen bisa memiliki properti.
3. Mengapa tidak boleh mengubah state secara langsung tanpa menggunakan fungsi yang disediakan oleh React?
   A. Karena mengubah state secara langsung lebih efisien.
   B. Karena itu adalah cara yang benar untuk mengubah state.
   C. Karena hal itu dapat menyebabkan masalah dalam siklus rendering dan tidak memicu re-rendering komponen.
   D. Karena komponen tidak perlu dirender ulang.
4. Apa yang terjadi setelah state berubah dalam komponen React Native?
   A. Komponen akan dirender ulang dengan data state yang baru.
   B. Komponen akan tetap dalam keadaan yang sama.
   C. Komponen akan otomatis keluar dari aplikasi.
   D. Komponen akan mengalami error.
5. Bagaimana cara mengubah state dalam contoh kode yang diberikan?

```jsx
const StateExample = () => {
  const [count, setCount] = useState(0);

  const increaseCount = () => {
    // Mengubah state count dengan menggunakan setCount
    setCount(count + 1);
  };

  return (
    <View>
      <Text>Hitungan: {count}</Text>
      <Button title="Tambah" onPress={increaseCount} />
    </View>
  );
};
```

A. Dengan mengubah variabel langsung, misalnya count = count + 1.
B. Dengan menggunakan fungsi setCount.
C. Dengan membuat state baru.
D. Dengan menggunakan console.log.

Jawaban :

1. A
2. C
3. C
4. A
5. B
