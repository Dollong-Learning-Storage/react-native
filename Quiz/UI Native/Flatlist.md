## Easy - 5 poin

1. Apa tujuan utama dari komponen FlatList di React Native?
   A. Mengatur list elemen dalam tampilan grid.
   B. Mengelola list elemen dalam tampilan list vertikal atau horizontal.
   C. Menggambar elemen dalam tampilan dalam bentuk grafik batang.
   D. Membuat list elemen dalam tampilan tabel.
2. Bagaimana cara mengimpor komponen FlatList dalam sebuah komponen React Native?
   A. import { FlatList } from 'react-native';
   B. import { List } from 'react-native';
   C. import FlatList from 'react-native/FlatList';
   D. import List from 'react-native/FlatList';
3. Apa properti yang digunakan untuk mengatur data yang akan ditampilkan dalam FlatList?
   A. items
   B. listData
   C. dataSource
   D. data
4. Bagaimana cara mengatur tampilan tiap elemen dalam FlatList?
   A. Dengan properti itemRenderer
   B. Dengan properti renderRow
   C. Dengan properti renderItem
   D. Dengan properti elementRenderer

Jawaban:

1. B
2. A
3. A
4. C

## Medium - 10 poin

1. Apa yang harus digunakan untuk mengidentifikasi setiap elemen dalam daftar dalam FlatList?
   A. keyExtractor
   B. elementIdentifier
   C. itemKey
   D. listKey
2. Bagaimana cara menggunakan properti data dan renderItem dalam komponen FlatList untuk menampilkan daftar nama produk dalam aplikasi React Native?
   A.

   ```jsx
   <FlatList
     productData={products}
     renderItems={({ productData }) => <Text>{productData.name}</Text>}
   />
   ```

   B.

   ```jsx
   <FlatList
     data={products}
     renderItem={({ item }) => <Text>{item.name}</Text>}
   />
   ```

   C.

   ```jsx
   <FlatList
     items={products}
     renderItem={(product) => <Text>{product.name}</Text>}
   />
   ```

   D.

```jsx
<FlatList items={products} render={(product) => <Text>{product.name}</Text>} />
```

Jawaban:

1. A
2. B

## Intermediate - 15 poin

1. Mengapa FlatList lebih efisien daripada menggunakan map untuk menampilkan daftar data dalam aplikasi React Native?
   A. Keduanya memiliki efisiensi yang sama dalam menangani daftar data besar.
   B. FlatList hanya merender elemen yang terlihat di layar, mengurangi beban render di aplikasi. Sementara map akan merender semua elemen sekaligus, bahkan yang tidak terlihat.
   C. FlatList hanya dapat menangani tata letak vertikal, sedangkan map dapat menangani tata letak vertikal dan horizontal.
   D. Penggunaan map dalam FlatList menghasilkan peringatan dan sebaiknya dihindari.
2. Bagaimana Kamu akan menangani ketika pengguna menggulir ke bagian bawah daftar data dan Kamu ingin memuat lebih banyak data secara otomatis dalam FlatList?
   A. Menggunakan properti onEndReached pada FlatList dan mengganti data daftar dengan data baru ketika mencapai bagian bawah.
   B. Menggunakan fungsi onScroll pada FlatList untuk mendeteksi pengguliran dan memuat lebih banyak data saat mencapai bagian bawah.
   C. Menggunakan properti onEndReachedThreshold pada FlatList untuk menentukan seberapa dekat ke bagian bawah sebelum memuat lebih banyak data.
   D. Tidak mungkin memuat lebih banyak data secara otomatis dalam FlatList.

Jawaban:

1. B
2. A

## Advanced - 20 Poin

1. Jelaskan case di mana Kamu akan menggunakan properti horizontal pada komponen FlatList dalam pengembangan aplikasi React Native.

Jawaban:
Properti horizontal pada komponen FlatList digunakan ketika Anda ingin menampilkan daftar data secara horizontal daripada vertikal. Situasi-situasi di mana Anda akan menggunakan properti horizontal meliputi:

Galeri Gambar: Menampilkan kumpulan gambar dalam bentuk galeri yang dapat digulir secara horizontal.
Menu Horizontal: Membuat menu aplikasi yang dapat digulir dari kiri ke kanan.
Slider: Membuat slider yang memungkinkan pengguna melihat konten dalam urutan horizontal.

Contoh Penggunaan:

```jsx
<FlatList
  data={items}
  horizontal
  renderItem={({ item }) => <Text>{item.name}</Text>}
  keyExtractor={(item) => item.id.toString()}
/>
```

2. Bagaimana Anda akan mengimplementasikan animasi masuk (entrance animation) pada elemen-elemen dalam FlatList saat tampilan dipasang pertama kali?

Jawaban:
Anda dapat menggunakan animasi dari modul React Native seperti Animated atau LayoutAnimation untuk menerapkan animasi masuk pada elemen-elemen dalam FlatList. Berikut adalah contoh penggunaan Animated untuk membuat animasi masuk ketika tampilan dipasang pertama kali:

```jsx
import React, { useEffect, useRef } from "react";
import { View, Text, FlatList, Animated } from "react-native";

const AnimatedFlatListExample = () => {
  const fadeAnim = useRef(new Animated.Value(0)).current;

  useEffect(() => {
    Animated.timing(fadeAnim, {
      toValue: 1,
      duration: 1000,
      useNativeDriver: true,
    }).start();
  }, [fadeAnim]);

  const data = [
    { id: "1", text: "Item 1" },
    { id: "2", text: "Item 2" },
    { id: "3", text: "Item 3" },
  ];

  const renderItem = ({ item }) => {
    return (
      <Animated.View style={{ opacity: fadeAnim }}>
        <Text>{item.text}</Text>
      </Animated.View>
    );
  };

  return (
    <FlatList
      data={data}
      renderItem={renderItem}
      keyExtractor={(item) => item.id}
    />
  );
};

export default AnimatedFlatListExample;
```

Dalam contoh di atas, `Animated.View` menggunakan fadeAnim untuk mengontrol opasitas elemen-elemen, menciptakan efek animasi masuk. Animasi ini dimulai ketika komponen pertama kali dipasang dan berlangsung selama 1 detik.
