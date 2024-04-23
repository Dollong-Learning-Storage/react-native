## Button

![Init React](<../../Assets/Materi/Button & Touchable opacity/button-explanation.png>)

<!-- Komponen Button adalah salah satu komponen dasar dalam React Native yang digunakan untuk membuat tombol interaktif dalam antarmuka pengguna. Tombol ini memungkinkan pengguna untuk _melakukan tindakan tertentu_ saat ditekan. -->

Di website kita mempunya _tag_ `<button>` yang berperilaku sebagai component interaktif yang akan **melakukan tindakan tertentu ketika di tekan**. React Native memiliki beberapa component _native_ yang tujuannya kurang lebih sama. React Native punya `<Button>`, `<Pressable>` dan`<TouchableOpacity>`.

> Note! 📝
>
> Kita hanya akan membahas `<Button>` dan `<TouchableOpacity>`.

Contoh `<Button>`:

<div style="width: 800px;position:relative;overflow-x:auto">
<iframe src="https://snack.expo.dev/@doltons/button" height="500" width="1500" title="Button and TouchableOpacity Example"></iframe>
</div>

Contoh `<TouchableOpacity>`:

<div style="width: 800px;position:relative;overflow-x:auto">
<iframe src="https://snack.expo.dev/@doltons/touchableopacity" height="500" width="1500" title="Button and TouchableOpacity Example"></iframe>
</div>

Kalau di perhatikan keduanya sama ya?

TouchableOpacity adalah komponen React Native yang digunakan untuk membuat area yang _dapat ditekan (tappable)_ di dalam UI. Ketika user menekan nya, akan memberikan efek sentuhan (seperti efek transparansi atau perubahan warna) **ketika area tersebut ditekan**

> Note! 📝
>
> Perlu diingat bahwa `<TouchableOpacity>` ini hanya merupakan component `<View>` yang memiliki efek ketika di tekan.

<!-- **Fungsi dan Kegunaan:**

1. **Interaksi Pengguna:** Tombol memungkinkan pengguna untuk melakukan tindakan tertentu, seperti mengirim formulir, memulai proses, atau berpindah ke halaman lain.
2. **Tindakan Pemicu:** Kamu dapat menghubungkan fungsi atau tindakan khusus ke tombol yang akan dijalankan saat tombol ditekan.
3. **Tampilan Visual:** Tombol biasanya memiliki tampilan yang berbeda ketika dalam keadaan normal dan ketika dihover atau ditekan. -->

<!-- ## Touchable Opacity:

TouchableOpacity adalah komponen React Native yang digunakan untuk membuat area yang _dapat ditekan (tappable)_ di dalam UI. Ketika user menekan nya, akan memberikan efek sentuhan (seperti efek transparansi atau perubahan warna) **ketika area tersebut ditekan**

**Contoh Kode Button dan TouchableOpacity:**

<iframe src="https://snack.expo.dev/@doltons/touchableopacity" height="500" width="1500" title="Button and TouchableOpacity Example"></iframe>

<br />

> Note! 📝
>
> Perlu diingat bahwa `<TouchableOpacity>` ini hanya merupakan component `<View>` yang memiliki efek ketika di tekan. -->

<!-- ```jsx
import React from "react";
import { View, Text, Button, Alert } from "react-native";

const ButtonExample = () => {
  const handlePress = () => {
    Alert.alert("Tombol Ditekan", "Tindakan dilakukan saat tombol ditekan!");
  };

  return (
    <View>
      <Text>Selamat datang di contoh Button!</Text>
      <Button title="Click Here.." onPress={handlePress} />
    </View>
  );
};

export default ButtonExample;
``` -->

# Quiz

## Easy - 5 Poin

1. Apa fungsi dari `<Button>`
   - [x] A. melakukan tindakan tertentu ketika di tekan
   - B. Memberikan efek sentuhan
   - C. Mengorganisir styling pada React Native
   - D. Mengubah warna latar belakang suatu komponen
2. Dalam contoh kode yang diberikan, komponen mana yang digunakan untuk mengelompokkan elemen-elemen UI bersama?
   - A. <Text>
   - [x] B. <View>
   - C. <React>
   - D. <StyleSheet>

## Medium - 10 poin

1. Apa perbedaan `<Button>` dan `<TouchableOpacity>`?
   - A. Keduanya sama-sama component yang berperilaku sebagai component interaktif yang akan melakukan tindakan tertentu ketika di tekan
   - B. `<Button>` adalah komponen React Native yang digunakan untuk membuat area yang dapat ditekan (tappable) di dalam UI. TIdak seperti `<TouchableOpacity>` yang hanya merupakan `<View>`
   - [x] C. `<TouchableOpacity>` hanya merupakan `<View>` yang memiliki efek ketika di tekan bukan _button_ asli seperti `<Button>`
   - D. Keduanya tidak memiliki perbedaan, hanya nama yang berbeda
