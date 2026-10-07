# LAB3WEB

## Laporan Praktikum Pemrograman Web

**Nama:** Bagus Rigen Hermanta
**NIM:** 312510145
**Mata Kuliah:** Pemrograman Web

---

## 1. Membuat Dokumen HTML

Pada langkah pertama dibuat sebuah dokumen HTML sebagai dasar untuk latihan CSS. Dokumen HTML digunakan untuk membuat struktur halaman yang nantinya akan diberikan style menggunakan CSS.

### Tampilan Dokumen HTML

<img width="1917" height="408" alt="Screenshot 2026-10-07 083300" src="https://github.com/user-attachments/assets/70b3f252-9499-4f92-bfd8-cbf70048f8e7" />


---

## 2. Mendeklarasikan CSS Internal

Pada langkah kedua ditambahkan CSS secara internal menggunakan tag `<style>` yang berada di dalam bagian `<head>` pada dokumen HTML.

CSS internal digunakan untuk memberikan tampilan pada elemen HTML tanpa membuat file CSS terpisah.

### Hasil Penambahan CSS Internal

<img width="1847" height="450" alt="Screenshot 2026-10-07 084435" src="https://github.com/user-attachments/assets/6d154c70-a1b8-4d42-b2d3-f77dc2a8ad64" />

---

## 3. Menambahkan Inline CSS

Selanjutnya ditambahkan **Inline CSS**, yaitu CSS yang dituliskan langsung pada atribut `style` di dalam elemen HTML.

Contohnya:

```html
<p style="color: red;">Belajar CSS</p>
```

Inline CSS dapat digunakan untuk memberikan style secara langsung pada elemen tertentu.

### Hasil Penambahan Inline CSS

<img width="1881" height="422" alt="Screenshot 2026-10-07 084839" src="https://github.com/user-attachments/assets/69dc54c5-5e96-4b38-ab9c-c18913d181a3" />

---

## 4. Membuat CSS Eksternal

Pada langkah ini dibuat file CSS terpisah dari file HTML. CSS eksternal digunakan agar kode HTML dan CSS lebih terstruktur serta lebih mudah dikelola.

File CSS kemudian dihubungkan dengan HTML menggunakan tag:

```html
<link rel="stylesheet" href="style.css">
```

### Tampilan Setelah Menggunakan CSS Eksternal

<img width="1917" height="455" alt="Screenshot 2026-10-07 085540" src="https://github.com/user-attachments/assets/e12ac247-b395-4bc4-b1db-23ff7056c1af" />

---

## 5. Menambahkan CSS Selector

Pada langkah terakhir ditambahkan beberapa CSS selector, yaitu **ID Selector** dan **Class Selector**.

Contoh ID selector:

```css
#intro {
    background: #418fb1;
    border: 2px solid #099249;
    padding: 20px;
    border-radius: 10px;
}
```

Contoh selector untuk heading di dalam ID `intro`:

```css
#intro h1 {
    color: white;
    text-align: center;
    font-size: 28px;
}
```

Penambahan properti tersebut membuat tampilan menjadi lebih rapi, seperti background, border, ukuran tulisan, dan posisi judul.

### Hasil CSS Selector

<img width="1917" height="535" alt="Screenshot 2026-10-07 090328" src="https://github.com/user-attachments/assets/f234e7f7-a4bb-44f8-9118-d7e3eacde7cf" />

---

# Pertanyaan dan Tugas

## 1. Eksperimen Mengubah dan Menambah CSS

Saya melakukan eksperimen dengan mengubah dan menambahkan beberapa properti CSS, seperti:

* `background`
* `border`
* `padding`
* `border-radius`
* `color`
* `text-align`
* `font-size`

Contohnya:

```css
#intro {
    background: #418fb1;
    border: 2px solid #099249;
    padding: 20px;
    border-radius: 10px;
}

#intro h1 {
    color: white;
    text-align: center;
    font-size: 28px;
}
```

Perubahan tersebut membuat tampilan halaman menjadi lebih rapi. Background menjadi lebih menarik, sudut elemen menjadi melengkung, ukuran tulisan berubah, dan judul berada di tengah.

### Screenshot Hasil Eksperimen



---

## 2. Perbedaan `h1 { ... }` dengan `#intro h1 { ... }`

Selector:

```css
h1 {
    color: red;
}
```

digunakan untuk memberikan style kepada semua elemen `<h1>` yang terdapat pada halaman.

Sedangkan:

```css
#intro h1 {
    color: white;
}
```

hanya berlaku untuk elemen `<h1>` yang berada di dalam elemen yang memiliki `id="intro"`.

Contoh:

```html
<h1>Judul 1</h1>

<div id="intro">
    <h1>Judul 2</h1>
</div>
```

CSS `h1` akan memengaruhi kedua judul, sedangkan `#intro h1` hanya memengaruhi **Judul 2**.

---

## 3. Perbedaan CSS Internal, External, dan Inline

CSS dapat ditulis dalam tiga cara, yaitu:

1. **Internal CSS**
2. **External CSS**
3. **Inline CSS**

Contohnya:

### External CSS

```css
p {
    color: blue;
}
```

### Internal CSS

```html
<style>
    p {
        color: green;
    }
</style>
```

### Inline CSS

```html
<p style="color: red;">Belajar CSS</p>
```

Pada contoh tersebut, teks akan ditampilkan dengan warna **merah** karena Inline CSS memiliki prioritas lebih tinggi dibandingkan CSS internal dan external pada kondisi tersebut.

Secara umum:

```text
Inline CSS > Internal/External CSS
```

---

## 4. ID dan Class pada Elemen yang Sama

Sebuah elemen HTML dapat memiliki ID dan Class secara bersamaan.

Contohnya:

```html
<p id="paragraf-1" class="textparagraf">
    Ini adalah paragraf.
</p>
```

Kemudian diberikan CSS:

```css
#paragraf-1 {
    color: red;
}

.textparagraf {
    color: blue;
}
```

Hasilnya teks akan berwarna **merah** karena selector ID (`#`) memiliki specificity yang lebih tinggi dibandingkan selector class (`.`).

Namun, apabila ID dan class mengatur properti yang berbeda, keduanya tetap dapat digunakan secara bersamaan.

Contohnya:

```css
#paragraf-1 {
    color: red;
}

.textparagraf {
    font-size: 20px;
}
```

Dengan demikian, paragraf akan memiliki warna merah dan ukuran font 20px.

---

# Kesimpulan

Pada praktikum ini telah dilakukan latihan penggunaan CSS pada dokumen HTML, mulai dari CSS internal, inline CSS, CSS eksternal, hingga penggunaan ID dan Class Selector.

Praktikum ini juga menunjukkan bahwa setiap jenis CSS memiliki cara penggunaan dan tingkat prioritas yang berbeda. Dengan menggunakan CSS, tampilan halaman HTML dapat dibuat lebih terstruktur dan menarik.

---

## Struktur Repository

Struktur repository yang digunakan:

```text
Lab3Web/
│
├── README.md
├── index.html
├── style.css
│
└── screenshots/
    ├── 01-dokumen-html.png
    ├── 02-css-internal.png
    ├── 03-inline-css.png
    ├── 04-css-eksternal.png
    ├── 05-css-selector.png
    └── 06-eksperimen-css.png
```

> **Catatan:** Nama file screenshot pada bagian README harus disesuaikan dengan nama file screenshot yang kamu upload ke repository GitHub.
