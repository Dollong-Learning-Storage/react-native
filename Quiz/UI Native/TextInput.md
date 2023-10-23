## Easy - 5 Poin

1. Apa tujuan dari komponen TextInput dalam React Native?
   A. Menampilkan teks statis
   B. Mengumpulkan input pengguna dalam bentuk teks
   C. Menampilkan gambar
   D. Memutar video
2. Apa yang harus digunakan untuk menangani perubahan teks dalam TextInput dalam kode React Native?
   A. onChange()
   B. onInputChange()
   C. onChangeText()
   D. onTextChange()

## Medium - 10 Poin

```jsx
import React, { useState } from "react";
import { View, TextInput } from "react-native";

const MyComponent = () => {
  const [inputValue, setInputValue] = useState("");

  const handleInputChange = (text) => {
    // Mengatur nilai state 'inputValue' dengan nilai input pengguna
    // CODE HERE
  };

  return (
    <View>
      <TextInput
        value={inputValue}
        onChangeText={handleInputChange}
        placeholder="Masukkan teks di sini"
      />
    </View>
  );
};
```

1. Berikut adalah potongan kode React Native. Pilih jawaban yang benar untuk mengisi bagian yang kosong agar TextInput menerima input pengguna dan menyimpannya dalam state 'inputValue':
   A. setInputValue(text)
   B. setInputValue({ text })
   C. setInputValue(inputValue + text)
   D. setInputValue({ inputValue: text })
2. Apa fungsi properti secureTextEntry dalam komponen TextInput?
   A. Menampilkan teks dalam format terenkripsi
   B. Menyembunyikan teks yang dimasukkan oleh pengguna
   C. Memvalidasi apakah teks merupakan kata sandi
   D. Mengunci TextInput sehingga tidak dapat diedit

```javascript
import React, { useState } from "react";
import { View, TextInput, Text } from "react-native";

const InputExample = () => {
  const [inputText, setInputText] = useState("");

  const handleInputChange = (text) => {
    setInputText(text);
  };

  return (
    <View>
      <Text>Masukkan Nama Kamu:</Text>
      <TextInput
        placeholder="Contoh: John Doe"
        onChangeText={handleInputChange}
        value={inputText}
      />
      <Text>Kamu memasukkan: {inputText}</Text>
    </View>
  );
};

export default InputExample;
```

3. Apa yang akan ditampilkan di layar setelah pengguna memasukkan teks `Halo Dunia!` dalam TextInput pada contoh kode?
   a. Nama pengguna
   b. Angka acak
   c. Tidak ada yang ditampilkan
   d. Teks "Kamu memasukkan: Halo Dunia!"
