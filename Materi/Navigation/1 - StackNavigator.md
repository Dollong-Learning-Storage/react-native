Routing, dalam konteks pengembangan aplikasi, adalah proses pengelolaan navigasi antara berbagai layar atau tampilan dalam aplikasi. Kita menyediakan endpoint yang bisa diakses oleh pengguna, dan yang nantinya akan membimbing mereka melalui perjalanan yang terstruktur

# StackNavigator

<video>
<source src="https://www.loom.com/share/9aa44530612545fda7055e36075ed8e5?sid=ba81e1fa-3fea-47ab-b8b1-bbc6afbdd538"></source>
</video>

![Stack Navigator](../../Assets/Materi/Navigation/stack-navigator.png)

StackNavigator adalah salah satu jenis **navigator** (_yang ngatur routing_). StackNavigator memungkinkan Kamu untuk membuat **navigasi tumpukan** (_stack navigation_), yang akan mengatur tiap layar dalam tumpukan sehingga pengguna dapat berpindah antara layar-layar ini dengan mudah dan dapat kembali ke layar sebelumnya.

Kayaknya keliatan rumit ya? mari lihat video di bawah untuk mempermudah pemahamanmu.

![Stack Navigator](../../Assets/Materi/Navigation/navigation-example.gif)

Dari video tersebut, terlihat kita memiliki 2 _screen_ yaitu screen Skilvul Course dan Detail Course. Dua halaman ini jelas mempunyai UI yang berbeda. Ketika user menekan salah satu card, user di **arahkan** (_navigate_) ke halaman Detail Course

Apa yang terjadi sebenarnya?

![Stack Navigator](../../Assets/Materi/Navigation/skilvul-course-app-ver.jpg)

<!-- Kita melakukan navigasi dari Skilvul Course ke Detail Course dengan *Stack Navigator*. -->

<!-- ## Apa itu StackNavigator?

StackNavigator adalah komponen utama dalam pustaka navigasi React Navigation yang memungkinkan Kamu untuk membuat tumpukan layar dalam aplikasi React Native. Ide dasarnya adalah setiap kali Kamu berpindah ke layar baru, layar tersebut ditumpuk di atas layar sebelumnya dalam urutan yang dapat diakses dengan mudah. Ini mirip dengan tumpukan buku, di mana Kamu dapat menambahkan buku baru (layar baru) di atas tumpukan dan menghapusnya dari tumpukan saat selesai membacanya. -->

<!-- ## Mengapa StackNavigator Penting?

1. Pengalaman Pengguna yang Lancar: Dengan StackNavigator, pengguna dapat berpindah antara layar dengan cara yang intuitif dan nyaman. Mereka dapat kembali ke layar sebelumnya dengan mudah dengan menekan tombol kembali atau menggunakan fungsi navigasi yang disediakan.
2. Organisasi yang Baik: StackNavigator membantu Kamu mengorganisir kode Kamu dengan baik. Setiap layar memiliki tanggung jawabnya sendiri, sehingga memudahkan pemeliharaan dan pengembangan aplikasi.
3. Navigasi yang Fleksibel: Kamu dapat dengan mudah menambahkan berbagai jenis efek transisi antara layar, seperti animasi slide atau transparansi. Kamu juga dapat mengatur tajuk layar dan tindakan navigasi yang terkait dengan setiap layar. -->

## Contoh StackNavigator:

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
