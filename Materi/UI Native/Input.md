Komponen Input merupakan salah satu komponen yang penting dalam pembangunan antarmuka pengguna dengan React Native. Komponen ini memungkinkan pengguna untuk memasukkan teks atau data lainnya melalui keyboard perangkat.

**Fungsi dan Kegunaan:** Komponen Input memiliki beberapa kegunaan utama:

1. **Penerimaan Data:** Komponen Input digunakan untuk mengumpulkan data yang dimasukkan oleh pengguna, seperti teks, angka, atau informasi lainnya.
2. **Formulir:** Biasanya digunakan dalam formulir untuk mengizinkan pengguna memasukkan informasi seperti nama, alamat email, kata sandi, dan lainnya.
3. **Pengaturan State:** Data yang dimasukkan melalui komponen Input dapat digunakan untuk mengatur state komponen atau komponen lainnya.

**Contoh Kode:**

```jsx
import React, { useState } from 'react';
import { View, TextInput, Text } from 'react-native';

const InputExample = () => {
  const [inputText, setInputText] = useState('');

  const handleInputChange = (text) => {
    setInputText(text);
  };

  return (
    <View>
      <Text>Masukkan Nama Anda:</Text>
      <TextInput
        placeholder="Contoh: John Doe"
        onChangeText={handleInputChange}
        value={inputText}
      />
      <Text>Kamu memasukkan: {inputText}</Text>
    </View>
  );
}

export default InputExample;
```