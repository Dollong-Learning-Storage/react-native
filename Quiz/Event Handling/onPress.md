1. Kapan menggunakan event onPress dalam pengembangan React Native?
   A. Untuk mengubah jenis elemen UI.
   B. Untuk mengatur posisi elemen UI.
   C. Untuk merespons tindakan pengguna terhadap elemen UI.
   D. Untuk mengatur tampilan latar belakang elemen UI.

```jsx
const FunctionalComponentExample = (props) => {
  const [count, setCount] = useState(0);

  const incrementCount = () => setCount(count + 1);

  useEffect(() => {
    console.log("Component did mount");
    return () => {
      console.log("Component will unmount");
    };
  }, []);

  useEffect(() => {
    console.log("Component did update");
  }, [count]);

  return (
    <View>
      <Text>Halo, ini adalah Functional Component!</Text>
      <Text>Count: {count}</Text>
      <Button title="+" onPress={incrementCount} />
    </View>
  );
};
```

2. Pada contoh kode yang diberikan, kapan pesan "Component did update" akan ditampilkan di konsol?
   A. Setiap kali tombol "+" ditekan.
   B. Setiap kali tombol "-" ditekan.
   C. Saat komponen berfungsi pertama kali dimuat.
   D. Saat komponen diperbarui dengan perubahan properti tertentu.
3. Pada contoh kode yang diberikan **pada nomor **2, kapan pesan "Component did mount" akan ditampilkan di konsol?
   A. Setiap kali tombol "+" ditekan.
   B. Setiap kali tombol "-" ditekan.
   C. Saat komponen berfungsi pertama kali dimuat.
   D. Saat komponen dihapus dari tampilan.
4. Pada contoh kode yang diberikan, apa yang akan terjadi ketika tombol "+" ditekan?
   A. Elemen UI akan menghilang.
   B. Pesan akan muncul dalam jendela peringatan.
   C. Elemen UI akan berubah warna.
   D. Kode tertentu akan dihapus dari komponen.

Jawaban :

1. C
2. A
3. C
4. B
