# StackNavigator

StackNavigator adalah salah satu jenis navigator yang paling umum digunakan dalam pengembangan aplikasi React Native. Ini memungkinkan Kamu untuk membuat navigasi tumpukan (stack navigation) yang mengatur layar-layar dalam tumpukan, sehingga pengguna dapat berpindah antara layar-layar ini dengan mudah dan dapat kembali ke layar sebelumnya. Dalam tulisan ini, kita akan menjelaskan secara mendalam tentang StackNavigator dan bagaimana Kamu dapat menggunakannya dalam pengembangan aplikasi React Native.

## Apa itu StackNavigator?

StackNavigator adalah komponen utama dalam pustaka navigasi React Navigation yang memungkinkan Kamu untuk membuat tumpukan layar dalam aplikasi React Native. Ide dasarnya adalah setiap kali Kamu berpindah ke layar baru, layar tersebut ditumpuk di atas layar sebelumnya dalam urutan yang dapat diakses dengan mudah. Ini mirip dengan tumpukan buku, di mana Kamu dapat menambahkan buku baru (layar baru) di atas tumpukan dan menghapusnya dari tumpukan saat selesai membacanya.

## Mengapa StackNavigator Penting?

1. Pengalaman Pengguna yang Lancar: Dengan StackNavigator, pengguna dapat berpindah antara layar dengan cara yang intuitif dan nyaman. Mereka dapat kembali ke layar sebelumnya dengan mudah dengan menekan tombol kembali atau menggunakan fungsi navigasi yang disediakan.
2. Organisasi yang Baik: StackNavigator membantu Kamu mengorganisir kode Kamu dengan baik. Setiap layar memiliki tanggung jawabnya sendiri, sehingga memudahkan pemeliharaan dan pengembangan aplikasi.
3. Navigasi yang Fleksibel: Kamu dapat dengan mudah menambahkan berbagai jenis efek transisi antara layar, seperti animasi slide atau transparansi. Kamu juga dapat mengatur tajuk layar dan tindakan navigasi yang terkait dengan setiap layar.

## Contoh StackNavigator:

Mari kita lihat contoh penggunaan StackNavigator dalam React Native:

```jsx
import { createStackNavigator } from "@react-navigation/stack";
import HomeScreen from "./HomeScreen";
import DetailScreen from "./DetailScreen";

const Stack = createStackNavigator();

function App() {
  return (
    <Stack.Navigator initialRouteName="Home">
      <Stack.Screen name="Home" component={HomeScreen} />
      <Stack.Screen name="Detail" component={DetailScreen} />
    </Stack.Navigator>
  );
}
```

Dalam contoh ini, kita menginisialisasi StackNavigator dengan dua layar, yaitu **HomeScreen** dan **DetailScreen**. initialRouteName menunjukkan layar pertama yang akan ditampilkan saat aplikasi dimulai. Pengguna dapat berpindah antara layar ini dengan menggunakan fungsi navigasi yang disediakan oleh React Navigation.
