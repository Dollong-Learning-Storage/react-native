Pada materi `onPress` sebelumnya, kita sudah berhasil membuat `<Button>` menjadi interaktif. Tapi kalau perhatikan contoh yang kemarin, komponen `<Input>` tidak bisa di isi alias _tidak interaktif_.

Berikut contoh yang di maksud:

<div style="width: 800px;position:relative;overflow-x:auto">
<iframe src="https://snack.expo.dev/@doltons/handle-onpress" height="500" width="1500"></iframe>
</div>

Kalau kamu coba jalankan di `snack.expo` dan mencoba mengisi Input tidak ada yang terjadi. Ini dikarenakan kita sama sekali belum meng-_handle_ **event onChange**.

<!-- Ketika pengguna memasukkan pada form input lalu mencoba submit, hal tersebut akan memungkinkan aplikasi Kita untuk merespons dan mengelola input dengan dinamis. Data yang di isi lewat input tersebut akan di proses lebih lanjut. Hal ini dimungkinkan dengan onChange

Event "onChange" adalah event yang terjadi ketika nilai suatu elemen berubah. Dalam konteks React Native, ini berarti ketika pengguna mengetikkan sesuatu dalam TextInput atau memilih sesuatu dalam Picker, event "onChange" akan aktif dan memungkinkan Kita untuk merespons perubahan tersebut.

Dalam TextInput, event "onChange" memungkinkan kita untuk mengakses nilai yang dimasukkan oleh pengguna dan menggunakannya dalam logika aplikasi. Berikut adalah contoh penggunaan "onChange" pada TextInput:

<iframe src="https://snack.expo.dev/@doltons/onchange" height="500" width="1500"></iframe>

Dalam contoh ini, "onChangeText" menerima fungsi "handleInputChange", yang akan dijalankan setiap kali nilai dalam TextInput berubah. Fungsi tersebut kemudian mengubah state "inputValue", dan nilai ini ditampilkan di bawah TextInput. -->
