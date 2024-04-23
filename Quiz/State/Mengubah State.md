## Easy

1. Apa yang terjadi setelah state berubah dalam komponen React Native?
   A. Komponen akan dirender ulang dengan data state yang baru.
   B. Komponen akan tetap dalam keadaan yang sama.
   C. Komponen akan otomatis keluar dari aplikasi.
   D. Komponen akan mengalami error.
2. Manakah di bawah ini cara _mengupdate state_ yang benar?
   A.

   ```jsx
   const [setCounter] = useState(1);

   setCounter(2);
   ```

   B.

   ```jsx
   const [counter, setCounter] = useState(1);

   setCounter(2);
   ```

   C.

   ```jsx
   const { counter, setCounter } = useState(1);

   setCounter(2);
   ```

   D.

   ```jsx
   const setCounter = useState(1);

   setCounter(2);
   ```

Jawaban:

1. A
2. B

## Intermediate

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

1. Bagaimana cara mengubah state dalam contoh kode yang diberikan?
   A. Dengan mengubah variabel langsung, misalnya count = count + 1.
   B. Dengan menggunakan fungsi setCount.
   C. Dengan membuat state baru.
   D. Dengan menggunakan console.log.
2. Mengapa tidak boleh mengubah state secara langsung tanpa menggunakan fungsi yang disediakan oleh React?
   A. Karena mengubah state secara langsung lebih efisien.
   B. Karena itu adalah cara yang benar untuk mengubah state.
   C. Karena hal itu dapat menyebabkan masalah dalam siklus rendering dan tidak memicu re-rendering komponen.
   D. Karena komponen tidak perlu dirender ulang.

Jawaban :

1. B
2. C
