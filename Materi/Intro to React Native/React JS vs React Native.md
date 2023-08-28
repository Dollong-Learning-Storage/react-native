## **React JS vs React Native: Perbedaan dan Kesamaan**

**React JS (React)**

React JS adalah sebuah pustaka (library) JavaScript yang dikembangkan oleh Facebook. Tujuan utama dari React JS adalah memungkinkan pengembang untuk membangun antarmuka pengguna (UI) yang dinamis dan efisien. React JS fokus pada pembuatan komponen UI yang dapat diatur secara hierarkis. Komponen-komponen ini dapat digunakan kembali dan dikelola dengan lebih mudah, sehingga memudahkan dalam pengembangan aplikasi yang kompleks.

Beberapa fitur kunci dari React JS meliputi:

- **Virtual DOM**: React menggunakan konsep Virtual DOM untuk mengoptimalkan pembaruan tampilan. Perubahan pada tampilan diterapkan pada Virtual DOM terlebih dahulu, dan kemudian dibandingkan dengan tampilan real DOM untuk meminimalkan pembaruan yang sebenarnya diperlukan.
- **Component**: Aplikasi React dibangun dari berbagai komponen kecil yang dapat digunakan kembali. Ini membuat pengembangan lebih modular dan efisien.
- **JSX (JavaScript XML)**: JSX memungkinkan pengembang untuk menulis kode tampilan menggunakan sintaks yang mirip dengan HTML, tetapi pada akhirnya akan dikompilasi menjadi JavaScript.

**React Native**

React Native adalah kerangka kerja pengembangan aplikasi seluler yang juga dikembangkan oleh Facebook. Tujuan utama dari React Native adalah memungkinkan pengembang untuk membuat aplikasi mobile (iOS dan Android) menggunakan pengetahuan tentang React JS. Dengan React Native, Kamu dapat berbagi sebagian besar logika dan kode antarmuka pengguna antara platform iOS dan Android, sambil tetap memanfaatkan performa dan fungsionalitas native.

Perbedaan utama antara React JS dan React Native adalah:

1. **Platform Target**: React JS berfokus pada pembuatan antarmuka pengguna berbasis web, sedangkan React Native difokuskan pada pembuatan aplikasi mobile untuk platform iOS dan Android.
2. **Elemen UI**: React JS menggunakan elemen HTML untuk membangun tampilan, sedangkan React Native menggunakan komponen UI native seperti "View", "Text", dan "Image" yang disediakan oleh sistem operasi masing-masing.
3. **Styling**: Di React JS, Kamu menggunakan CSS untuk melakukan styling elemen. Di React Native, Kamu menggunakan stylesheet khusus yang meniru properti CSS namun diterjemahkan ke style native. Juga di React Native tidak ada konsep grid

**Kesamaan antara React JS dan React Native:**

1. **Sintaks**: Kode JavaScript dan konsep yang digunakan dalam React JS dapat dengan mudah diterapkan dalam React Native.
2. **Komponen**: Baik React JS maupun React Native mempromosikan pendekatan berbasis komponen dalam pembangunan UI.