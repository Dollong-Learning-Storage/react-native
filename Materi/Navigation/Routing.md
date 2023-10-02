# Routing

Routing adalah salah satu aspek penting dalam pengembangan aplikasi React Native. Ini memungkinkan pengguna untuk berpindah antara layar atau komponen dalam aplikasi dengan lancar. Dalam tulisan ini, kita akan membahas konsep dasar routing dalam konteks aplikasi React Native, dan bagaimana Kamu dapat menggunakan pustaka navigasi seperti React Navigation untuk mencapainya.

## Apa itu Routing?

Routing, dalam konteks pengembangan aplikasi, adalah proses pengelolaan navigasi antara berbagai layar atau tampilan dalam aplikasi. Ini memungkinkan pengguna untuk berpindah dari satu bagian aplikasi ke bagian lainnya. Di React Native, routing membantu kita mengorganisir dan mengontrol tampilan yang ditampilkan kepada pengguna.

## Instalasi

```shell
npm install react-native-screens react-native-safe-area-context
```

**Note!**
Jika kamu menggunakan Mac dalam proses pembuatan aplikasi untuk IOS, kamu perlu install pods (via Cocoapods)
Berikut detailnya:
https://reactnavigation.org/docs/getting-started#installing-dependencies-into-a-bare-react-native-project

## Menggunakan React Navigation untuk Routing

Di React Native, salah satu pustaka navigasi yang paling umum digunakan adalah React Navigation. Pustaka ini menyediakan berbagai jenis navigator yang dapat Kamu gunakan untuk mengatur routing dalam aplikasi Kamu.

**Stack Navigator**
StackNavigator adalah jenis navigator yang paling umum digunakan untuk membuat tumpukan layar. Ini cocok untuk aplikasi dengan tampilan yang hierarkis, seperti aplikasi berita atau aplikasi e-commerce. Dalam Stack Navigator, setiap layar ditumpuk di atas layar sebelumnya, sehingga pengguna dapat kembali ke layar sebelumnya dengan mudah.

**Tab Navigator**
TabNavigator adalah jenis navigator yang digunakan untuk membuat navigasi tab. Ini berguna ketika Kamu memiliki beberapa bagian utama dalam aplikasi yang dapat diakses melalui tab di bagian bawah layar. Contoh penggunaan yang umum adalah tab navigasi untuk beranda, profil pengguna, dan pengaturan aplikasi.

## Contoh Penggunaan Routing

Mari kita lihat contoh sederhana penggunaan Stack Navigator dalam aplikasi React Native:

```jsx
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
```

Dalam contoh ini, kita menginisialisasi Stack Navigator dengan dua layar, yaitu HomeScreen dan DetailScreen. Pengguna dapat berpindah antara layar ini dengan menggunakan fungsi navigasi yang disediakan oleh React Navigation.
