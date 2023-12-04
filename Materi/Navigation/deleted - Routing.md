<!-- Baik website maupun aplikasi, routing merupakan konsep utama dalam memungkinkan user berpindah halaman.

Pada website -->

Routing, dalam konteks pengembangan aplikasi, adalah proses pengelolaan navigasi antara berbagai layar atau tampilan dalam aplikasi. Kita menyediakan endpoint yang bisa diakses oleh pengguna, dan yang nantinya akan membimbing mereka melalui perjalanan yang terstruktur

<!-- ![Stack Navigator](../../Assets/Materi/Navigation/navigation-example.gif) -->

<!-- Pada video di atas terlihat kita memiliki dua _screen_, **Skilvul Course** dan **Detail Course**. -->

<!-- ## Instalasi

Di React Native, salah satu library yang memungkinkan kamu untuk mengelola navigasi adalah React Navigation. Sebelum lebih jauh mari kita install dulu.

1. Buka terminal kalian
2. Install React Native
3. Copy dan paste kode di bawah ke terminal kalian lalu enter untuk menginstall

```shell
npm install @react-navigation/native react-native-screens react-native-safe-area-context
```

> **Note!**
>
> Jika kamu menggunakan Mac dalam proses pembuatan aplikasi untuk IOS, kamu perlu install pods (via Cocoapods)
>
> Berikut detailnya:
> https://reactnavigation.org/docs/getting-started#installing-dependencies-into-a-bare-react-native-project -->

## Menggunakan React Navigation

React Navigation mempunyai dua fitur utama yaitu _Stack Navigator_ dan _Tab Navigator_

**Stack Navigator**
StackNavigator adalah jenis navigator yang paling umum digunakan untuk membuat tumpukan layar. Ini cocok untuk aplikasi dengan tampilan yang hierarkis, seperti aplikasi berita atau aplikasi e-commerce. Dalam Stack Navigator, setiap layar ditumpuk di atas layar sebelumnya, sehingga pengguna dapat kembali ke layar sebelumnya dengan mudah.

**Tab Navigator**
TabNavigator adalah jenis navigator yang digunakan untuk membuat navigasi tab. Ini berguna ketika Kamu memiliki beberapa bagian utama dalam aplikasi yang dapat diakses melalui tab di bagian bawah layar. Contoh penggunaan yang umum adalah tab navigasi untuk beranda, profil pengguna, dan pengaturan aplikasi.

Mari kita lihat contoh sederhana penggunaan Stack Navigator dalam aplikasi React Native:

![Stack Navigator](../../Assets/Materi/Navigation/navigation-example.gif)

<!-- ```jsx
import { NavigationContainer } from "@react-navigation/native";
import { createStackNavigator } from "@react-navigation/stack";
import HomeScreen from "./HomeScreen";
import DetailScreen from "./DetailScreen";

const Stack = createStackNavigator();

function App() {
  return (
    <NavigationContainer>
      <Stack.Navigator initialRouteName="Home">
        <Stack.Screen name="Home" component={HomeScreen} />
        <Stack.Screen name="Detail" component={DetailScreen} />
      </Stack.Navigator>
    </NavigationContainer>
  );
}
``` -->

<!-- Dalam contoh ini, kita menginisialisasi Stack Navigator dengan dua layar, yaitu HomeScreen dan DetailScreen. Pengguna dapat berpindah antara layar ini dengan menggunakan fungsi navigasi yang disediakan oleh React Navigation. -->
