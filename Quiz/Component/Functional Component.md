## Easy (5 Poin)

1. Apa yang membedakan antara functional component dan class component dalam React Native?
   A. Functional component menggunakan "class" keyword, sedangkan class component menggunakan "function" keyword.
   B. Functional component merupakan versi terbaru dari class component.
   C. Functional component adalah fungsi JavaScript biasa, sedangkan class component merupakan class JavaScript yang diwarisi dari React.Component.
   D. Functional component hanya digunakan untuk state management, sedangkan class component hanya digunakan untuk rendering tampilan.
2. Manakah di bawah ini penggunaan functional component dalam React Native
   A..

   ```jsx
   import React from "react";
   import { View, Text } from "react-native";

   const MyComponent = () => {
     return (
       <View>
         <Text>Hello, World!</Text>
       </View>
     );
   };

   export default MyComponent;
   ```

   B..

   ```jsx
   import React from "react";
   import { View, Text } from "react-native";

   class MyComponent extends React.Component {
     render() {
       return (
         <View>
           <Text>Hello, World!</Text>
         </View>
       );
     }
   }

   export default MyComponent;
   ```

   C..

   ```jsx
   import React from "react";
   import { View } from "react-native";

   function MyComponent() {
     return (
       <View>
         <Text>Hello, World!</Text>
       </View>
     );
   }

   export default MyComponent;
   ```

   D..

   ```jsx
   import React, { Component } from "react";

   class MyComponent extends Component {
     render() {
       return (
         <View>
           <Text>Hello, World!</Text>
         </View>
       );
     }
   }

   export default MyComponent;
   ```

jawaban:

1. C
2. A

## Medium (10 Poin)

1. Manakah di bawah ini cara mengirimkan prop ke functional component?
   A. Dengan menggunakan properti "props" langsung di dalam functional component.
   B. Dengan mendefinisikan prop di dalam fungsi functional component.
   C. Dengan menggunakan "this.props" di dalam functional component.
   D. Functional component tidak dapat menerima prop.
2. Manakah penggunaan prop di dalam functional component.
   A..

   ```jsx
   function Greeting = (props) => {
   return <Text>Hello, {props.name}!</Text>;
   }

   ```

   B..

   ```jsx
   function Greeting(props) {
     return <Text>Hello, {props.name}!</Text>;
   }
   ```

   C..

   ```jsx
   function Greeting() {
     return <Text>Hello, {props.name}!</Text>;
   }
   ```

   D..

   ```jsx
   const Greeting = (name) => {
     return <Text>Hello, {name}!</Text>;
   };
   ```

jawaban:

1. A
2. B

## Intermediate (15 Poin)

1. Apa perbedaan antara "Functional Component" dan "Class Component" dalam React Native? Kapan sebaiknya Kamu menggunakan salah satunya?

Jawaban:
Perbedaan utama adalah bahwa "Functional Component" adalah fungsi sederhana yang menerima prop dan mengembalikan elemen React, sedangkan "Class Component" adalah class yang memiliki state dan lifecycle methods. Penggunaan keduanya tergantung pada kebutuhan proyek, tetapi dengan diperkenalkannya Hooks, penggunaan "Functional Component" menjadi lebih disarankan karena lebih ringkas dan mudah dimengerti.

## Advanced (20 Poin)

1. Dalam pengembangan aplikasi React Native yang kompleks, bagaimana Kamu akan mengorganisasi dan membagi "Functional Component" ke dalam berkas-berkas terpisah untuk meningkatkan skalabilitas dan keterbacaan kode?

Jawaban: Menggunakan struktur direktori yang terorganisir, seperti folder components untuk menyimpan semua komponen, dan memecah komponen-komponen tersebut ke dalam berkas terpisah. Misalnya, components/Header.js untuk menyimpan komponen header.
