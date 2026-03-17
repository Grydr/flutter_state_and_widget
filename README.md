# Widget Explanation
---

## Widgets Tree:
```
main()
  └─ MyApp
    └─ MaterialApp
      └─ RowColumnPage
          └─ Scaffold
            ├─ AppBar
            └─ SingleChildScrollView
              └─ Column
                ├─ AspectRatio
                │  └─ Container
                │     └─ Center
                │        └─ Image.network("https://picsum.photos/200")
                ├─ Container
                │  └─ Text("What image is that")
                ├─ Container
                │  └─ Row
                │     ├─ Column
                │     │  ├─ Icon(food_bank)
                │     │  └─ Text("Food")
                │     ├─ Column
                │     │  ├─ Icon(landscape)
                │     │  └─ Text("Scenery")
                │     └─ Column
                │        ├─ Icon(people)
                │        └─ Text("People")
                └─ CounterCard
                    └─ _CounterCardState.build
                      └─ Container
                          └─ Row
                            ├─ Text("Counter here: $_counter")
                            └─ Container
                                └─ IconButton
                                  └─ Icon(add)
```

### Material Widgets
- **MaterialApp:**
Root aplikasi berbasis Material Design. Mengatur hal seperti title, theme, dan halaman awal (home).

- **ThemeData:**
Konfigurasi tema aplikasi. Dipakai oleh MaterialApp.

- **ColorScheme.fromSeed:**
Membuat skema warna otomatis dari seedColor (di sini Colors.deepPurple).

- **Scaffold:**
Kerangka halaman: menyediakan struktur umum seperti appBar dan body.

- **AppBar:**
Bagian header di atas halaman. Background warna oranye muda, dan judul di tengah.

- **Text:**
Menampilkan teks.

- **SingleChildScrollView:**
Membuat isi halaman bisa di-scroll jika konten melebihi tinggi layar.

- **Column:**
Menyusun widget anak secara vertikal. Dipakai untuk menyusun semua section di body.

- **Row:**
Menyusun widget anak secara horizontal. Dipakai pada bar menu icon (“Food/Scenery/People”) dan pada CounterCard (teks counter + tombol).

- **AspectRatio:**
Memaksa child memiliki perbandingan lebar:tinggi tertentu (di sini 1:1). Dipakai untuk area gambar agar kotak.

- **Container:**
Widget “kotak serbaguna” untuk styling/layout: margin, padding, width, color, dsb. Banyak dipakai di halaman ini.

- **Center:**
Memusatkan child di tengah area yang tersedia. Dipakai untuk memusatkan gambar.

- **Image.network:**
Mengambil dan menampilkan gambar dari internet (https://picsum.photos/200).

- **Icon:**
Menampilkan ikon

- **IconButton:**
Tombol berbentuk ikon. Di sini dipakai untuk tombol “+” yang memanggil _incrementCounter.

- **EdgeInsets (fromLTRB / all):**
Mengatur jarak:

    margin = jarak luar container
    padding = jarak dalam container

- **MediaQuery.of(context).size.width:**
Mengambil lebar layar untuk membuat container selebar layar (dikurangi efek margin).

- **setState():**
Khusus StatefulWidget, dipakai untuk memberi tahu Flutter bahwa state berubah sehingga UI perlu dibangun ulang.


### Created Widgets
- **MyApp (StatelessWidget):**
Widget root aplikasi. Menyediakan MaterialApp dan menetapkan home: RowColumnPage().

- **RowColumnPage (StatelessWidget):**
Halaman utama. Menyusun beberapa container (gambar, teks, row ikon) dan menampilkan CounterCard.

- **CounterCard (StatefulWidget):**
Komponen counter yang bisa bertambah saat tombol ditekan.

- **_CounterCardState (State):**
Menyimpan state _counter dan fungsi _incrementCounter() untuk menambah nilai counter.
