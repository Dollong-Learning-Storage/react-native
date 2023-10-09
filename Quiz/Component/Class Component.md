## Easy (5 Poin)

1. Apa itu komponen kelas (class component) dalam React Native?
   A. Komponen yang hanya bisa digunakan dalam kelas.
   B. Komponen yang ditulis dengan sintaks kelas ES6 dan memiliki state.
   C. Komponen yang hanya bisa digunakan dalam fungsi.
   D. Komponen yang hanya berisi fungsi.
2. Bagaimana Anda mendeklarasikan state dalam sebuah komponen kelas?
   A. this.state = { key: value };
   B. state = { key: value };
   C. setState({ key: value });
   D. this.setState({ key: value });

Jawaban:

1. B
2. A

## Medium (10 Poin)

1. Apa perbedaan utama antara komponen kelas dan komponen fungsional dalam React Native?
A. Komponen kelas tidak dapat memiliki metode khusus, sedangkan komponen fungsional dapat.
B. Komponen fungsional tidak dapat menerima prop, sedangkan komponen kelas dapat.
C. Komponen kelas dapat memiliki state, sedangkan komponen fungsional tidak.
D. Tidak ada perbedaan antara komponen kelas dan komponen fungsional.
<!-- 2. Bagaimana Anda mengakses prop dalam sebuah komponen kelas?
   A. this.props.key
   B. props.key
   C. this.key
   D. key -->

```jsx
class MyComponent extends Component {
  render() {
    return <Text>{this.props.data}</Text>;
  }
}
```

2. Manakah di antara opsi berikut yang menunjukkan cara menggunakan prop dalam sebuah komponen kelas?

A. this.data
B. props.data
C. this.props.data
D. data

Jawaban :

1. A
2. C

## Medium (10 Poin)

```jsx
class ExampleComponent extends Component {
  constructor(props) {
    super(props);
  }
}
```

1. Berikut adalah contoh kode untuk sebuah komponen kelas. Apa fungsi dari pernyataan super(props) dalam constructor?
   A. Menambahkan properti props ke dalam state komponen.
   B. Menginisialisasi state komponen dan memungkinkan akses ke properti dari parent component.
   C. Menambahkan props sebagai argumen untuk constructor dan memberikan akses ke metode super.
   D. Menghubungkan state dan props sehingga perubahan pada props akan mempengaruhi state secara otomatis.

Jawaban:

1. B

## Advanced

```jsx
class CounterComponent extends Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0,
    };
  }

  increaseCount = () => {
    // handle tambah count disini...
  };

  render() {
    return (
      <View>
        <Button title="Tambah" onPress={this.increaseCount} />
        <Text>Jumlah: {this.state.count}</Text>
      </View>
    );
  }
}
```

1. Berikut adalah contoh kode untuk sebuah komponen kelas. Bagaimana Anda akan mengubah nilai state count ketika tombol Tambah ditekan? Berikan contoh kode dan jelaskan prosesnya.

Jawaban :

```jsx
increaseCount = () => {
  this.setState({ count: this.state.count + 1 });
};
```

2. Dalam konteks pengembangan aplikasi React Native, berikan contoh situasi di mana penggunaan komponen fungsional (functional component) lebih disarankan daripada komponen kelas (class component). Jelaskan alasan mengapa komponen fungsional lebih cocok dalam situasi tersebut.
