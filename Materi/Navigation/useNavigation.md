# useNavigation

Dari course sebelumnya kita sudah belajar bagaimana membuat routing. Pada course kali ini kalian akan belajar bagaimana berpindah dari satu halaman ke halaman lain melalui route yang sudah kita pelajari.

useNavigation adalah salah satu fitur yang kuat dalam React Navigation yang memungkinkan Kamu mengakses objek navigasi dari komponen mana pun dalam aplikasi React Native Kamu. Kita akan membahas penggunaan useNavigation dan bagaimana fitur ini dapat membantu Kamu dalam pengembangan aplikasi yang lebih canggih dengan navigasi yang lebih baik.

## Apa itu useNavigation?

useNavigation adalah hook yang disediakan oleh React Navigation. Ini memungkinkan Kamu untuk mengakses objek navigasi yang terkait dengan komponen saat ini. Objek navigasi ini mengandung berbagai fungsi dan properti yang memungkinkan Kamu untuk mengendalikan navigasi dalam aplikasi Kamu.

## Menggunakan useNavigation

Berikut adalah contoh penggunaan useNavigation dalam sebuah komponen React Native:

```jsx
import React from "react";
import { View, Text, Button } from "react-native";
import { useNavigation } from "@react-navigation/native";

function HomeScreen() {
  const navigation = useNavigation();

  const goToProfileScreen = () => {
    navigation.navigate("Profile");
  };

  return (
    <View>
      <Text>Ini adalah halaman Beranda</Text>
      <Button title="Go to halaman Profile" onPress={goToProfileScreen} />
    </View>
  );
}

export default HomeScreen;
```

Dalam contoh ini, kita mengimpor useNavigation dari @react-navigation/native dan menggunakannya untuk mendapatkan objek navigasi. Kemudian, objek navigasi tersebut digunakan untuk melakukan navigasi ke layar Detail ketika tombol ditekan.
