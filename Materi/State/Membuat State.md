Dalam React Native, state adalah cara untuk menyimpan dan mengelola data yang dapat berubah di komponen. State memungkinkan komponen Anda berinteraksi dengan data dan merespons perubahan data tersebut.

Untuk membuat state di dalam sebuah komponen, kamu perlu menggunakan hook `useState` (dalam functional component) atau mendefinisikan `this.state` (dalam class component).

**Contoh Kode :**

<iframe src="https://snack.expo.dev/@doltons/state" height="500" width="100%"></iframe>

<!-- ```jsx
import React, { useState } from "react";
import { View, Text, Button } from "react-native";

const StateExample = () => {
  const [count, _] = useState(0);

  return (
    <View>
      <Text>Nilai count: {count}</Text>
    </View>
  );
};

export default StateExample;
``` -->

Dengan menggunakan `useState`, kamu telah berhasil membuat state dalam functional component yang dapat menyimpan dan merepresentasikan data yang dapat berubah pada komponen tersebut.
