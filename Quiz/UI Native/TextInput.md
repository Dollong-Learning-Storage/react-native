1. Apa fungsi utama dari komponen Input dalam React Native?
   a. Menampilkan teks
   b. Mengumpulkan data dari pengguna
   c. Mengatur tampilan aplikasi
   d. Menampilkan gambar
2. Apa yang harus digunakan untuk menangani perubahan teks dalam TextInput dalam kode React Native?
   a. onChange()
   b. onInputChange()
   c. onChangeText()
   d. onTextChange()
3. Apa yang akan ditampilkan di layar setelah pengguna memasukkan teks `Halo Dunia!` dalam TextInput pada contoh kode?

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

a. Nama pengguna
b. Angka acak
c. Tidak ada yang ditampilkan
d. Teks "Kamu memasukkan: Halo Dunia!"

4. Apa yang akan terjadi jika handleInputChange() tidak digunakan dalam contoh kode?
   a. Aplikasi akan menampilkan pesan kesalahan
   b. Pengguna tidak dapat memasukkan teks
   c. Nilai dalam TextInput tidak akan berubah
   d. Aplikasi akan crash
5. Apa komponen yang digunakan untuk menampilkan teks di layar dalam contoh kode?
   a. View
   b. Text
   c. TextInput
   d. Input

Jawaban:

1. b. Mengumpulkan data dari pengguna
2. c. onChangeText()
3. d. Teks "Kamu memasukkan: Halo Dunia!"
4. c. Nilai dalam TextInput tidak akan berubah
5. c. TextInput
