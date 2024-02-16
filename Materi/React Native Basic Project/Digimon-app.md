Selamat untuk kalian semua yang sudah melewati semua tahapan belajar React Native!. Sekarang sudah waktunya kalian implementasi semua yang sudah di pelajari!.

Di akhir dari project ini kalian akan membuat aplikasi sederhana yang menampilkan list Film.

Pertama, install dulu project expo nya

- `npx create-expo-app --template`
- akan ada beberapa pilihan, bebas milih apa. untuk contoh kali ini kita **pilih yang blank saja**

Install navigation

- `npm install @react-navigation/native @react-navigation/native-stack`
- `npx expo install react-native-screens react-native-safe-area-context`

Buatlah folder /screen, /data dan /components di dalam /src.
![Struktur Folder](folder-structure.png)

pada file app.js ubah semua kode dengan kode di bawah

```jsx
function App() {
  return <></>;
}

export default App;
```

Sekarang kita perlu untuk init navigation

```jsx
import { NavigationContainer } from "@react-navigation/native";
import { createNativeStackNavigator } from "@react-navigation/native-stack";
import HomeScreen from "./src/screens/Home";
import DetailScreen from "./src/screens/Detail";

const Stack = createNativeStackNavigator();

function App() {
  return (
    <NavigationContainer>
      <Stack.Navigator>
        <Stack.Screen name="Home" component={HomeScreen} />
        <Stack.Screen name="Detail" component={DetailScreen} />
      </Stack.Navigator>
    </NavigationContainer>
  );
}
export default App;
```

Kita akan mencoba menampilkan semua list movie yang sudah kita simpan. Isi component
MovieList dengan kode di bawah

```jsx
// ./src/components/MovieList

import React from "react";
import { FlatList, Image, ScrollView, Text, View } from "react-native";
import MOVIES_DATA from "../../data/movies.json";
import styles from "./styles";

const MovieList = () => {
  const [moviesData] = useState(MOVIES_DATA);

  return (
    <View style={styles.container}>
      <FlatList
        data={moviesData}
        keyExtractor={(item) => item.imdbID}
        renderItem={({ item }) => (
          <View style={styles.cardContainer}>
            <Image style={styles.image} source={{ uri: item.Poster }} />
            <Text style={styles.title}>{item.Title}</Text>
          </View>
        )}
      />
    </View>
  );
};

export default MovieList;
```

Dari kode `MovieList` ternyata kita masih bisa buat lebih modular!

Kita bisa memisahkan component di `renderItem` ke suatu component `MovieItem`. Berikut kode untuk `MovieItem`

```jsx
// ./src/components/MovieItem

import React from "react";
import { Text, View, Image } from "react-native";
import styles from "./styles";

const MovieItem = ({ title, imgUrl }) => {
  return (
    <View style={styles.cardContainer}>
      <Image style={styles.image} source={{ uri: imgUrl }} />
      <Text style={styles.title}>{title}</Text>
    </View>
  );
};

export default MovieItem;
```

Sebelumnya kita menggunakan `item.title` dan `item.imgUrl` yang mana itu berasal properti `renderItem`. Ketika kita sudah di tahap membuat component lebih modular kita bisa..

Style untuk Movie Item. `./src/components/MovieItem/styles.js`

```jsx
import { StyleSheet } from "react-native";

const styles = StyleSheet.create({
  container: {
    borderRadius: 8,
    overflow: "hidden",
    marginBottom: 24,
    elevation: 3,
    shadowOffset: { width: 0, height: 2 },
    shadowOpacity: 0.2,
    shadowRadius: 2,
  },
  image: {
    width: "100%",
    height: 550,
  },
  title: {
    position: "absolute",
    bottom: 0,
    width: "100%",
    padding: 20,
    color: "#FFD605",
    fontSize: 16,
    fontWeight: "bold",
    backgroundColor: "rgba(48, 48, 48, 0.8)",
  },
  badgeText: {
    color: "#FFF",
    marginLeft: 5,
  },
});

export default styles;
```

Sekarang import `MovieItem` ke `MovieList` sehingga kode di `MovieList` akan seperti ini:

```jsx
import React, { useState } from "react";
import { FlatList, StyleSheet, View } from "react-native";
import MOVIES_DATA from "../../data/movies.json";
import MovieItem from "../MovieItem";

const MovieList = () => {
  const [moviesData] = useState(MOVIES_DATA);

  return (
    <View style={styles.container}>
      <FlatList
        data={moviesData}
        keyExtractor={(item) => item.imdbID}
        renderItem={({ item }) => (
          <MovieItem title={item.Title} imgUrl={item.Poster} />
        )}
      />
    </View>
  );
};

const styles = StyleSheet.create({
  container: {
    paddingTop: 12,
    paddingHorizontal: 16,
    backgroundColor: "#242424",
  },
});

export default MovieList;
```

## Navigate Ke screen detail

Sekarang tugas kita adalah navigate dari screen sekarang ke screen detail agar user mendapatkan informasi detail di screen tersebut.

Berikut yang akan kita lakukan

- Navigate ke screen detail
- Tampilkan lebih banyak data di screen detail

<!-- Kita akan menangkap *param* yang dikirim dari screen `Home` ke `Detail`.  -->

Di MovieItem, kita perlu menambahkan properti `onPress`. Niatnya adalah agar ketika `MovieItem` di tekan maka akan navigate ke halaman lain.

```jsx
import { Text, Image, TouchableOpacity } from "react-native";
import styles from "./styles";

const MovieItem = ({ title, imgUrl, onPress }) => {
  return (
    <TouchableOpacity
      onPress={onPress}
      activeOpacity={0.8}
      style={styles.container}
    >
      <Image resizeMode="cover" style={styles.image} source={{ uri: imgUrl }} />
      <Text style={styles.title}>{title}</Text>
    </TouchableOpacity>
  );
};
```

Kita juga mengubah container nya yang sebelumnya menggunakan `<View>` ke `<TouchableOpacity>`.

kita butuh function `navigate` untuk memungkinkan kita melakukan navigate.

```jsx
import { useNavigation } from "@react-navigation/native";

// di dalam MovieList
const navigation = useNavigation();
```

Kita akan navigate ke halaman detail ketika user menekan `<MovieItem>`. Jangan lupa untuk mengirimkan movieId juga karena kita akan butuh di halaman detail untuk memilih data spesifik **berdasarkan id**

```jsx
<MovieItem
  title={item.Title}
  imgUrl={item.Poster}
  onPress={() => navigation.navigate("Detail", { movieId: item.imdbID })}
/>
```

## Screen Detail

Halaman detail biasanya menampilkan data spesifik dan dengan informasi yang lebih banyak dari pada di homepage misalnya.

Karena yang ingin di tampilkan hanya data tertentu yang dipilih dari `<MovieList>`, Kita perlu menemukan data sesuai ID yang dikirim dari halaman sebelumnya

```jsx
const movieData = MOVIE_DATA.find((item) => item.imdbID == movieId);
```

Oke ide nya sudah dapat tinggal implementasi!.

```jsx
import { Image, Text, View, ScrollView } from "react-native";
import MOVIE_DATA from "../../data/movies.json";
import styles from "./styles";

const Detail = ({ route }) => {
  const { movieId } = route.params;

  const movieData = MOVIE_DATA.find((item) => item.imdbID == movieId);

  // Pencegahan apabila tidak ditemukan
  if (!movieData) return <Text>Movie Not Found!</Text>;

  return (
    <ScrollView style={styles.container}>
      <Image
        resizeMode="contain"
        style={styles.image}
        source={{ uri: movieData.Poster }}
      />
      <View style={styles.flexContainer}>
        <Text style={styles.boldText}>Title: </Text>
        <Text>{movieData.Title}</Text>
      </View>
      <View style={styles.flexContainer}>
        <Text style={styles.boldText}>Genre: </Text>
        <Text>{movieData.Genre}</Text>
      </View>
      <View style={styles.flexContainer}>
        <Text style={styles.boldText}>Year: </Text>
        <Text>{movieData.Year}</Text>
      </View>
      <View style={styles.flexContainer}>
        <Text style={styles.boldText}>Director: </Text>
        <Text>{movieData.Director}</Text>
      </View>
      <View style={styles.flexContainer}>
        <Text style={styles.boldText}>Actor: </Text>
        <Text>{movieData.Actors}</Text>
      </View>
      <Text style={styles.boldText}>Rating:</Text>
      <ScrollView horizontal>
        {movieData.Ratings.map((item) => (
          <View style={styles.ratingBadge} key={item.Source}>
            <Text style={styles.ratingText}>{item.Source}</Text>
            <Text style={styles.ratingText}>{item.Value}</Text>
          </View>
        ))}
      </ScrollView>
    </ScrollView>
  );
};

export default Detail;
```

Ini untuk styles nya

```jsx
// ./src/screens/Detail/styles.js
import { StyleSheet } from "react-native";

const styles = StyleSheet.create({
  container: {
    marginTop: 12,
    marginBottom: 24,
    paddingHorizontal: 16,
    backgroundColor: "#242424",
  },
  flexContainer: {
    flex: 1,
    flexDirection: "row",
    marginBottom: 12,
  },
  boldText: {
    color: "#FFD605",
    fontWeight: "bold",
  },
  image: {
    width: "100%",
    height: 550,
  },
  ratingSection: {
    paddingTop: 12,
  },
  ratingBadge: {
    paddingVertical: 12,
    paddingHorizontal: 16,
    backgroundColor: "#303030",
    marginRight: 8,
    marginTop: 8,
    borderRadius: 8,
  },
  ratingText: {
    color: "white",
  },
});

export default styles;
```

Selamat! Akhirnya kita sudah membuat aplikasi sederhana. Sudah cukup bangga belum dengan yang kamu lakukan hari ini!.
