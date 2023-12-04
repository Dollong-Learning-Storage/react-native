Kamu mungkin pernah mengalami halaman dengan konten yang panjang, seperti daftar yang memerlukan scroll untuk melihat semua itemnya.

ScrollView adalah komponen yang memberikanmu kemampuan untuk membuat tampilan yang bisa digulir (scrollable). Ini sangat berguna saat kamu memiliki konten yang tidak muat dalam satu layar, seperti daftar panjang atau halaman dengan konten bervariasi. ScrollView memastikan pengguna tetap dapat mengakses seluruh konten dengan menggulir layar.

**Contoh :**

<iframe src="https://snack.expo.dev/@doltons/scrollview-component" height="500" width="100%" title="Scrollview Example"></iframe>

<!-- ```jsx
import React from 'react';
import { View, Text, ScrollView, StyleSheet } from 'react-native';

const ScrollViewExample = () => {
  return (
	  <ScrollView>
		<View style={styles.box} />
		<View style={styles.box} />
		<View style={styles.box} />
	  </ScrollView>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    backgroundColor: '#ffffff',
    padding: 20,
  },
  box: {
    width: 100,
    height: 300
  },
});

export default ScrollViewExample;

``` -->
