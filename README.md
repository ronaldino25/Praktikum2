# Praktikum2
# Lab-2-Web-Praktikum-Dasar-CSS
Repositori ini berisi latihan dan tugas yang telah diselesaikan sebagai bagian dari Lab 2: CSS Dasar untuk mata kuliah Pemrograman Web di Universitas Pelita Bangsa. Praktikum ini mencakup dasar-dasar penggunaan CSS, seperti penerapan CSS internal, eksternal, dan inline, serta penggunaan selector, properti, dan nilai CSS.
# Daftar Isi
## Daftar Isi
1. [Pendahuluan](#bagian-1)
2. [Langkah-Langkah](#bagian-2)
   - [Langkah 1: Membuat Dokumen HTML](#sub-bagian-21)
   - [Langkah 2: Menambahkan CSS Internal](#sub-bagian-22)
   - [Langkah 3: Menambahkan CSS Inline](#sub-bagian-32)
   - [Langkah 4: Menambahkan CSS Eksternal](#sub-bagian-42)
   - [Langkah 5: Menggunakan Selector CSS](#sub-bagian-42)
3. [Hasil Eksperimen](#bagian-3)
4. [Kesimpulan](#bagian-4)
5. [Screenshot](#bagian-5)

# Pendahuluan
Tujuan dari praktikum ini adalah untuk memperkenalkan dasar-dasar CSS kepada mahasiswa. Dengan latihan ini, mahasiswa akan mempelajari cara menggunakan CSS secara internal, eksternal, dan inline, serta bagaimana memilih elemen HTML yang akan diubah tampilannya menggunakan berbagai jenis selector CSS.

# Langkah-Langkah
## Langkah 1: Membuat Dokumen HTML
Langkah pertama adalah membuat struktur dasar HTML seperti berikut:
### Langkah 1: Membuat Dokumen HTML

Langkah pertama adalah membuat struktur dasar HTML seperti berikut:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Dasar</title>
</head>
<body>
  <header>
    <h1>CSS Internal dan <i>Inline CSS</i></h1>
  </header>
  <nav>
    <a href="lab2_css_dasar.html">CSS Dasar</a>
    <a href="lab2_css_eksternal.html">CSS Eksternal</a>
    <a href="lab1_tag_dasar.html">HTML Dasar</a>
  </nav>
  <div id="intro">
    <h1>Hello World</h1>
    <p>Kami sedang belajar HTML dan CSS dasar, pada mata kuliah Pemrograman Web.</p>
    <a class="button btn-primary" href="#intro">Informasi selengkapnya</a>
  </div>
</body>
</html>
```

## Langkah 2: Menambahkan CSS Internal
Selanjutnya, tambahkan CSS internal di dalam tag `<head>`:
```
<style>
    body {
        font-family: 'Open Sans', sans-serif;
    }
    header {
        min-height: 80px;
        border-bottom: 1px solid #77CCEF;
    }
    h1 {
        font-size: 24px;
        color: #0F189F;
        text-align: center;
    }
    h1 i {
        color: #6d6a6b;
    }
</style>
```


## Langkah 3: Menambahkan CSS Inline
CSS inline diterapkan langsung di elemen `<p>`:
```
<p style="text-align: center; color: #ccd8e4;">Teks ini diatur menggunakan CSS inline.</p>
```
## Langkah 4: Menambahkan CSS Eksternal
Buat file eksternal (`assets/css/style.css`) dan hubungkan ke dokumen HTML:
```
<link rel="stylesheet" href="assets/css/style.css" type="text/css">
```
Isi dari `assets/css/style.css`:
``` 
nav {
    background: #20A759;
    color: #fff;
    padding: 10px;
}

nav a {
    color: #fff;
    text-decoration: none;
    padding: 10px 20px;
}

nav a:hover {
    background: #0B6B3A;
}
```
## Langkah 5: Menggunakan Selector CSS
Gunakan selector CSS seperti ID dan class:
``` 
#intro {
    background: #418fb1;
    padding: 10px;
}

.button {
    padding: 15px 20px;
    background: #bebcbd;
    color: #fff;
}

.btn-primary {
    background: #E42A42;
}
``` 
# Screenshot
1. **Tampilan Sebelum CSS Diterapkan:**
  - Tangkapan layar ini menunjukkan tampilan dasar halaman HTML sebelum ada gaya CSS yang diterapkan.
   ![image](https://github.com/user-attachments/assets/23289274-c23b-4b23-a873-3e7ada57246a)
2. **Tampilan Dengan CSS Internal dan Inline:**
   - Tangkapan layar ini menunjukkan perubahan tampilan setelah CSS internal dan inline diterapkan, seperti perubahan warna teks dan tata letak.
     ![image](https://github.com/user-attachments/assets/8463aa45-1a2f-4ac3-b8d8-840e8aa4a2e8)
3. **Tampilan Setelah Menambahkan CSS Eksternal:**
   - Di tangkapan layar ini, file CSS eksternal telah diterapkan, sehingga gaya pada navigasi dan elemen lainnya menjadi lebih terstruktur
   ![image](https://github.com/user-attachments/assets/1baf5cd8-80d7-4c8a-b7f3-5384304714c4)
4. **Tampilan Final Setelah Semua CSS Diterapkan:**
   - Ini adalah hasil akhir setelah semua jenis CSS (internal, inline, dan eksternal) diterapkan, termasuk penggunaan selector ID, class, dan elemen.
     ![image](https://github.com/user-attachments/assets/728f0df2-7101-4dba-829f-5cad1d8f3679)
# Hasil Eksperimen
1. **Perbedaan Selector Elemen (`h1 {...}`) vs. Selector ID (`#intro h1 {...}`):**
   - Selector elemen menerapkan gaya ke semua elemen `<h1>`, sedangkan selector ID hanya akan mempengaruhi elemen `<h1>` di dalam elemen dengan ID `#intro`.
2. **Urutan Prioritas CSS Internal, Eksternal, dan Inline:**
   - Jika ketiga jenis CSS ini diterapkan pada elemen yang sama, **inline CSS** memiliki prioritas tertinggi, diikuti **CSS eksternal**, dan terakhir **CSS internal**. Misalnya:
     ```
     <h1 style="color: red;">Judul ini akan berwarna merah karena CSS inline.</h1>
     ```
3. **Prioritas Selector ID dan Class:**
   - Selector ID memiliki prioritas lebih tinggi dibandingkan selector class, karena ID lebih spesifik.
     ```
     <p id="paragraf-1" class="text-paragraf">Gaya teks akan mengikuti selector ID.</p>
     ```
# Kesimpulan
Praktikum ini memberikan pengalaman dalam menggunakan berbagai metode deklarasi CSS dan menunjukkan bagaimana aturan CSS diterapkan dengan berbagai selector dan urutan prioritasnya.
