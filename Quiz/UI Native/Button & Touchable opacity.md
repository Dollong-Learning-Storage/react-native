## Easy (5 Poin)

1. Apa properti yang digunakan untuk menentukan teks yang akan ditampilkan pada tombol dalam komponen Button?
   A. label
   B. text
   C. title
   D. children

Jawaban :

1. C. title

## Medium (10 Poin)

1. Button dan TouchableOpacity adalah komponen yang digunakan untuk membuat tombol di React Native. Manakah pernyataan berikut yang benar?
   A. Button dan TouchableOpacity keduanya adalah komponen yang sama.
   B. Button adalah komponen bawaan React Native, sedangkan TouchableOpacity adalah komponen pihak ketiga.
   C. Button dan TouchableOpacity memiliki fungsi yang sama, yaitu untuk membuat tombol.
   D. Button dan TouchableOpacity memiliki fungsi yang berbeda, yaitu Button digunakan untuk membuat tombol dengan efek animasi, sedangkan TouchableOpacity digunakan untuk membuat tombol dengan efek transisi.

Jawaban :

1. C. Button dan TouchableOpacity memiliki fungsi yang sama, yaitu untuk membuat tombol.

## Intermediate (15 Poin)

```javascript
<TouchableOpacity onPress={() => alert("Tombol ditekan!")}>
  <Text>Tombol</Text>
</TouchableOpacity>
```

1. Berikut adalah kode untuk membuat tombol dengan TouchableOpacity:
   Apakah kode tersebut akan berfungsi dengan benar?
   A. Ya, kode tersebut akan berfungsi dengan benar.
   B. Tidak, kode tersebut tidak akan berfungsi dengan benar karena komponen TouchableOpacity tidak memiliki properti onPress.
   C. Tidak, kode tersebut tidak akan berfungsi dengan benar karena komponen Text tidak memiliki properti onPress.
   D. Tidak, kode tersebut tidak akan berfungsi dengan benar karena komponen TouchableOpacity dan komponen Text harus berada di dalam komponen View.

```jsx
<Button title="Tombol">
  <Text>Tombol</Text>
</Button>
```

2. Berikut adalah kode untuk membuat tombol dengan Button:
   Apakah kode tersebut akan berfungsi dengan benar?
   A. Ya, kode tersebut akan berfungsi dengan benar.
   B. Tidak, kode tersebut tidak akan berfungsi dengan benar karena properti title tidak tersedia untuk komponen Button.
   C. Tidak, kode tersebut tidak akan berfungsi dengan benar karena properti Text tidak tersedia untuk komponen Button.
   D. Tidak, kode tersebut tidak akan berfungsi dengan benar karena komponen Button dan komponen Text harus berada di dalam komponen View.

Jawaban :

1. A. Ya, kode tersebut akan berfungsi dengan benar.
2. A. Ya, kode tersebut akan berfungsi dengan benar.
