# Event onPress

<!-- ![Init React](../../Assets/Materi/State/calculator.gif). -->

Kalau sebelumnya kita hanya belajar cara membuat `<Button>`, pada materi ini kita akan mencoba membuat `<Button>` yang kita buat menjadi lebih berguna.

**Kebanyakan interaksi user ada pada button** yang ketika di klik akan entah mengarahkan kita ke halaman yang berbeda, melakukan kalkulasi, mengirim data ke Backend ketika user tekan 'login'.

Perhatikan contoh di bawah:

```jsx
<Button onPress={() => {}} title="Munculkan alert." />
```

Untuk implementasi penggunaan onPress usahakan menggunakan antara `Button`, `TouchableOpacity` ataupun `Pressable` yang memang tujuan elemen `<Button>` untuk melakukan interaksi ketika di tekan.

Ada dua cara menggunakan onPress, cara pertama adalah dengan langsung memasukkan interaksi yang akan terjadi ketika di tekan:

```jsx
<Button
  onPress={() => alert("Alert!, kamu sedang mempelajari event onPress")}
  title="Munculkan alert."
/>
```

Cara seperti ini sangat efisien untuk perintah yang hanya satu baris seperti contoh di atas.

Cara kedua adalah dengan membuat function terpisah:

<div style="width: 800px;position:relative;overflow-x:auto">
<iframe src="https://snack.expo.dev/@doltons/handle-onpress" height="500" width="1500"></iframe>
</div>

Cara seperti ini merupakan yang paling umum dan juga baik untuk di gunakan terutama ketika kalian memiliki banyak perintah dalam satu interaksi.

Mudah bukan? Kerjakan latihan dibawah untuk memastikan kamu benar-benar mengerti

# Quiz

## Easy - 5 Poin

1. Kenapa kita di sarankan menggunakan `<Button>` untuk implementasi `onPress`?

- [] Karena merupakan component yang mengembalikan `<View>`, berperilaku seperti `<TouchableOpacity>`
- [x] Tujuan elemen `<Button>` untuk melakukan interaksi ketika di tekan
- [ ] Tidak ada yang benar, Seharusnya menggunakan `onPress` pada component `<View>`
- [ ] Button merupakan component yang di buat untuk merender component yang interaktif

## Medium - 10 poin

1. Apa yang terjadi ketika kode di bawah ini di jalankan

```jsx
const isLogin = true;
const App = () => {
  const handleLogin = () => {
    if (isLogin) {
      return alert("Login berhasil!");
    }

    return alert("Login Gagal!, Pastikan username dan password sudah tepat");
  };

  return <Button onPress={alert("Alert Berhasil!")} title="Munculkan alert" />;
};
```

- [] Tidak ada yang terjadi, ketika button di tekan akan menampilkan alert dengan text "Alert Berhasil!"
- [] Memunculkan alert "Login Gagal!, Pastikan username dan password sudah tepat", ketika button di tekan tidak ada yang terjadi
- [x] Memunculkan alert "Alert Berhasil!", dan ketika menekan button akan menampilkan alert yang sama lagi
- [] Memunculkan alert "Login berhasil!", ketika menekan button akan menampilkan alert dengan text "Alert Berhasil!"
