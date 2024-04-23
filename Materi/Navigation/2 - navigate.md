Kemarin kita sudah meng-_init_ routing kita dengan _Stack Navigation_. Tentu, kurang komplit kalau belum bisa melakukan _navigasi_ nya.

<div style="width: 800px;position:relative;overflow-x:auto">
<iframe src="https://snack.expo.dev/@doltons/stack-navigation" height="500" width="1500"></iframe>
</div>

# Navigate

Di react JS kalian sudah familiar dengan kode ini

```jsx
<a href="detail.html">Go to Details</a>
```

Tujuan dari kode tersebut ialah untuk berpindah dari halaman saat ini ke halaman `/detail`.
Di React Native, Ada dua cara untuk _navigate_ dari satu screen ke screen lain. Pertama adalah dengan memanfaatkan _props navigation_.

```jsx
const HomeScreen = (props) => {
  return (
    <View style={styles.container}>
      <Text>Homepage</Text>
      <Button
        title="Ke halaman detail"
        onClick={() => props.navigation.navigate("Detail")}
      />
    </View>
  );
};
```

Semenjak Kamu _inisialisasi_ stack screen nya, dari situ screen kamu mendapatkan _privilege_ untuk menggunakan **navigation**.

```jsx
function App() {
  return (
    <>
      <NavigationContainer>
        <Stack.Navigator initialRouteName="Home">
          {/* HomeScreen akan mempunyai props navigation */}
          <Stack.Screen name="Home" component={HomeScreen} />

          {/* DetailScreen akan mempunyai props navigation */}
          <Stack.Screen name="Detail" component={DetailScreen} />
        </Stack.Navigator>
      </NavigationContainer>
      <View>
        {/* Footer tidak mempunyai props navigation */}
        <Footer />
      </View>
    </>
  );
}
```

Keren ya, di React Native juga _mendang mending_.

Kita ingin melakukan _navigate_ ke detail, Kita sebelumnya sudah membuat -->

Cara kedua untuk melakukan navigate adalah dengan menggunakan hook dari `react navigation`, yaitu `useNavigation`

```jsx
const DetailScreen = () => {
  const navigation = useNavigation();

  return (
    <View style={styles.container}>
      <Text>Homepage</Text>
      <Button
        title="Kembali ke Home"
        onClick={() => navigation.navigate("Home")}
      />
    </View>
  );
};
```

Baik dengan hook ataupun lewat props, keduanya sama-sama berguna untuk melakukan navigasi. Yang membedakan hanya apakah kamu mau menggunakan hook atau props.

> Note! 📝
>
> Lewat props ataupun hook tidak ada yang lebih baik atau lebih buruk, kebanyakan menggunakan hooks karena lebih familiar dengan useNavigate di React JS

Pastikan kamu memberikan _route_ yang sesuai dengan case kamu. Pastikan `Stack.Screen` nya sudah di buat karena **kamu ga akan bisa navigate ke route yang belum di inisialisasi**.

```jsx
// ./DetailScreen.js
navigation.navigate("Home")

// App.js
<NavigationContainer>
    <Stack.Navigator initialRouteName="Home">
        <Stack.Screen name="Home" component={HomeScreen} />
        <Stack.Screen name="Detail" component={DetailScreen} />
    </Stack.Navigator>
</NavigationContainer>
```
