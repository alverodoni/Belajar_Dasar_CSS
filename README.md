# Belajar_Dasar_CSS
Nama: Doni Alvero <p>
Nim: 312410663 <P>
Kelas: TI.24.A.5 <P>
Jurusan: Teknik Informatika <p>
Mata Kuliah: Pemograman Web 1 <p>

### Link Web yang dibuat
file:///C:/xampp/htdocs/Lab2_css_dasar.html/CSS%20DASAR.html#

### Tahap 1: Struktur Dasar HTML
**Deskripsi:**
Menampilkan dokumen HTML awal tanpa CSS eksternal atau internal, hanya menggunakan tag dasar HTML (`<h1>`, `<p>`, `<a>`). Ini menunjukkan kerangka konten sebelum proses *styling* dimulai.
<img width="1912" height="967" alt="1  Membuat dokumen HTML" src="https://github.com/user-attachments/assets/82799f10-22b4-43a0-b631-24a7eebe2031" />

### Tahap 2: Mendeklarasikan CSS Internal
**Deskripsi:**
Implementasi CSS Internal. Menambahkan blok `<style>` (CSS Internal) di `<head>`. Hasilnya, elemen seperti `<h1>` berwarna biru dan Hello World sudah berada di tengah, menunjukkan penerapan selector elemen dasar.
<img width="1911" height="967" alt="2  Mendeklarasikan CSS Internal" src="https://github.com/user-attachments/assets/9b9aeee7-f9fa-45cc-975b-8cda4715ceab" />

### Tahap 3: Menambahkan Inline CSS
**Deskripsi:**
Styling Navigasi dan Inline CSS Lanjutan. Memperkenalkan styling navigasi (nav bar) menggunakan CSS Internal atau Eksternal. Terdapat elemen pemisah/border pada navigasi dan penggunaan inline style untuk penataan letak tombol atau link di bar navigasi.
<img width="1903" height="966" alt="3  Menambahkan Inline CSS" src="https://github.com/user-attachments/assets/01535975-43a4-4488-9fd8-020226cc1a0c" />

### Tahap 4: Membuat CSS Eksternal
**Deskripsi:**
Implementasi Navigasi dan Selector Class/ID. Desain mulai terbentuk: navigasi menggunakan background hijau, dan tombol Informasi selengkapnya. sudah menggunakan class selector dan berwarna biru tua, menunjukkan pemisahan style ke CSS Eksternal (asumsi).
<img width="1912" height="967" alt="4  Membuat CSS Eksternal" src="https://github.com/user-attachments/assets/8b8b759d-56fa-4b23-9f3e-430c73ad0eca" />

### Tahap 5: Menambahkan CSS Selector
**Deskripsi**
Finalisasi Tampilan dengan Selector Lanjutan. Ini adalah hasil akhir yang kompleks. Bagian #intro diberi background biru/teal penuh (menggunakan ID Selector) dan tombol (.button / .btn-primary) diubah menjadi merah, menunjukkan penggunaan class dan ID selector secara efektif untuk menciptakan section yang kontras dan menarik.
<img width="1912" height="968" alt="5  Menambahkan CSS Selector" src="https://github.com/user-attachments/assets/009a6a44-494e-4ed3-bdd2-2c0780cd8e6b" />

```html

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CSS Dasar</title>
<style>
/* 1. Styling Dasar */
body {
    font-family:'Open Sans', sans-serif;
    margin: 0; 
    padding: 0;
}
header {
    min-height: 80px;
    border-bottom: none;
}
/* The main page H1 (outside of the blue section) remains the primary blue */
h1 {
    font-size: 24px;
    color: #0F189F;
    text-align: center;
    padding: 20px 10px;
}
h1 i {
    color: #0F189F;
}
 
/* 2. Styling Navigasi - MATCHES IMAGE 2 & 3 */
nav {
    /* Solid Green Background */
    background: #20A759; 
    color: #fff; 
    padding: 0; 
    border-bottom: none; 
    max-width: 100%; 
    margin: 0;
}
nav a {
    color: #fff; /* White link text */
    text-decoration: none;
    padding: 10px 20px; 
    cursor: pointer;
    background: none; 
}
nav .active,
nav a:hover {
    background: #0B6B3A; 
    text-decoration: none; 
}
 
/* 3. ID Selector (#intro) - MODIFIED FOR BLUE BACKGROUND & FULL WIDTH */
#intro {
    /* Set background to the teal/blue color */
    background: #418fb1; /* A shade of blue/teal similar to the image */
    border: none;
    min-height: auto; 
    padding: 30px 10px; /* Increased padding for better look */
    margin-bottom: 0; /* Remove bottom margin */
    /* REMOVED max-width and margin: 20px auto; for full width */
    max-width: 100%;
    margin: 0;
}
#intro h1 {
    /* This CSS rule is now ignored because the H1 is centered via inline style/parent */
    text-align: left; 
    border: 0;
    /* Set color to white for visibility on blue background */
    color: #ffffff; 
    padding: 0 0 10px 0; /* Adjust padding */
    margin: 0 auto;
    max-width: 600px; /* Confine H1 to the content width */
}

/* 3.1 Styling the paragraph text inside #intro - MODIFIED FOR WHITE COLOR */
#intro p {
    /* Set color to a light gray/off-white for contrast */
    color: #f0f8ff; /* Almost white */
    font-size: 16px;
    text-align: left; /* Aligned left, matching the image */
    line-height: 1.6;
}
 
/* 4. Class Selector (.button, .btn-primary) - MODIFIED FOR RED BUTTON */
.button {
    padding: 15px 20px;
    /* Change default button to RED */
    background: #E42A42; /* Red color */
    color: #fff;
    display: inline-block;
    margin: 20px 0 0 0; /* Adjust margin above the button */
    text-decoration: none;
}
.btn-primary {
    /* Ensure the primary class is red */
    background: #E42A42;
}

/* 5. Styling for New Content Sections (Not visible in image) */
.materi-section {
    display: none;
    padding: 20px;
    margin: 20px auto;
    max-width: 900px;
    background-color: #f7f7f7;
    border: 1px solid #ddd;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.materi-section h2 {
    color: #0F189F;
    border-bottom: 2px solid #20A759;
    padding-bottom: 10px;
    margin-bottom: 15px;
}

.materi-section h3 {
    color: #0B6B3A;
    margin-top: 20px;
    margin-bottom: 5px;
}

.materi-section table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 10px;
}

.materi-section th, .materi-section td {
    border: 1px solid #ccc;
    padding: 8px;
    text-align: left;
}

.materi-section th {
    background-color: #e9e9e9;
}
</style>
</head>
<body>
<header>
    <h1>CSS Internal dan <i>Inline CSS</i></h1>
</header>
<nav style="display: flex; justify-content: center;"> 
    <a href="#" id="nav-css-dasar" data-target="materi-css-dasar">CSS Dasar</a>
    <a href="#" id="nav-css-eksternal" data-target="materi-css-eksternal">CSS Eksternal</a>
    <a href="#" id="nav-html-dasar" data-target="materi-html-dasar">HTML Dasar</a>
</nav>
 
<div id="intro" style="text-align: center;">
    <h1 style="text-align: center; margin-bottom: 20px;">Hello World</h1> 
 
    <div style="max-width: 600px; margin: 0 auto; text-align: left;">
        <p>Kami sedang belajar HTML dan CSS dasar, pada mata kuliah <b>Pemrograman
        Web</b> di <i>Universitas Pelita Bangsa</i>. Pelajaran pertama yang kami dapat
        adalah membuat tampilan web sederhana dalam rangka mengenal tag-tag dasar HTML
        dan CSS.</p>
        
        <div style="text-align: left;"> 
            <a class="button btn-primary" href="https://www.google.com" target="_blank">Informasi selengkapnya.</a>
        </div>
    </div>
</div>

<div id="materi-css-dasar" class="materi-section">
    <h2>CSS Dasar</h2>
    <p><strong>CSS (Cascading Style Sheets)</strong> adalah suatu style yang digunakan untuk mengatur dan mengontrol tampilan (presentasi) dari elemen-elemen HTML. Fungsi utama CSS adalah memisahkan tampilan (desain) dengan konten halaman web.</p>
    
    <h3>1. Struktur Dasar CSS</h3>
    <p>Perintah dasar CSS disebut <strong>rule</strong> dan terdiri atas dua komponen utama: <strong>Selector</strong> dan <strong>Declaration</strong>.</p>
    <ul>
        <li><strong>Selector:</strong> Berfungsi memberi tahu browser elemen HTML mana yang akan diberi style. Contoh: elemen HTML (h1, p), Class, atau ID.</li>
        <li><strong>Declaration:</strong> Merupakan aturan style yang diterapkan, yang terdiri atas <strong>Property</strong> dan <strong>Value</strong>.</li>
    </ul>
    <pre><code>h1 { color: blue; font-size: 20px; }</code></pre>
    <p>Setiap declaration diakhiri dengan titik koma (;).</p>
    
    <h3>2. Aturan Penulisan CSS (Tiga Cara)</h3>
    <table>
        <tr><th>Jenis Style</th><th>Penempatan Kode</th><th>Tag yang Digunakan</th><th>Keterangan</th></tr>
        <tr><td><strong>Internal Style</strong></td><td>Di dalam tag <code>&lt;head&gt;</code> dokumen HTML.</td><td>Menggunakan tag <code>&lt;style&gt;</code>.</td><td>Cocok untuk styling pada satu halaman HTML saja.</td></tr>
        <tr><td><strong>Inline Style</strong></td><td>Langsung di dalam tag pembuka elemen HTML yang bersangkutan.</td><td>Menggunakan atribut <code>style</code>.</td><td>Tidak disarankan untuk styling kompleks; hanya untuk elemen spesifik.</td></tr>
        <tr><td><strong>External Style</strong></td><td>Di dalam file .css terpisah.</td><td>Menggunakan tag <code>&lt;link&gt;</code> di dalam <code>&lt;head&gt;</code>.</td><td>Paling disarankan karena memisahkan total style dan konten, serta dapat dipakai untuk banyak halaman.</td></tr>
    </table>

    <h3>3. Jenis-Jenis Selector</h3>
    <table>
        <tr><th>Selector</th><th>Penanda CSS</th><th>Atribut HTML</th><th>Keterangan</th></tr>
        <tr><td><strong>Class Selector</strong></td><td>Diawali tanda titik (<code>.</code>).</td><td>Menggunakan atribut <code>class</code>.</td><td>Dapat digunakan berulang kali.</td></tr>
        <tr><td><strong>ID Selector</strong></td><td>Diawali tanda pagar (<code>#</code>).</td><td>Menggunakan atribut <code>id</code>.</td><td>Bersifat unik; satu elemen HTML hanya boleh menggunakan satu ID.</td></tr>
        <tr><td><strong>Grouping</strong></td><td>Dipisahkan dengan koma (misalnya: <code>h1, h2, p {...}</code>).</td><td>-</td><td>Mempersingkat penulisan untuk properti yang sama.</td></tr>
    </table>
    
    <h3>4. Properti Background CSS (Dasar)</h3>
    <table>
        <tr><th>Properti</th><th>Fungsi dan Nilai Penting</th></tr>
        <tr><td><code>background-color</code></td><td>Menentukan warna latar (nama, RGB, atau Heksa).</td></tr>
        <tr><td><code>background-image</code></td><td>Menentukan gambar sebagai latar (menggunakan <code>url(...)</code>).</td></tr>
        <tr><td><code>background-repeat</code></td><td>Mengontrol pengulangan gambar latar (<code>repeat-x</code>, <code>repeat-y</code>, <code>no-repeat</code>).</td></tr>
        <tr><td><code>background-position</code></td><td>Menentukan posisi awal gambar latar (<code>top left</code>, <code>center center</code>, dll.).</td></tr>
        <tr><td><code>background</code></td><td>Shorthand (singkatan) untuk menulis semua properti background dalam satu baris.</td></tr>
    </table>
</div>

<div id="materi-css-eksternal" class="materi-section">
    <h2>CSS Eksternal (External Style)</h2>
    <p>Metode ini paling direkomendasikan karena memisahkan secara total antara struktur dokumen HTML (konten) dengan tampilan visual (presentasi).</p>
    
    <h3>1. Konsep Dasar</h3>
    <p>Semua aturan CSS ditempatkan dalam sebuah file terpisah dengan ekstensi <strong><code>.css</code></strong> (contoh: <code>style.css</code>). File CSS ini kemudian dihubungkan (<strong>link</strong>) ke dokumen HTML.</p>
    <p><strong>Keuntungan Utama:</strong></p>
    <ul>
        <li><strong>Memisahkan Konten & Tampilan:</strong> Membuat kode HTML menjadi lebih bersih.</li>
        <li><strong>Efisiensi:</strong> Satu file CSS dapat digunakan untuk mengatur tampilan banyak halaman HTML sekaligus.</li>
    </ul>

    <h3>2. Implementasi Teknis</h3>
    <p>Digunakan tag <code>&lt;link&gt;</code> yang diletakkan di dalam tag <code>&lt;head&gt;</code>.</p>
    <p><strong>Atribut Wajib:</strong></p>
    <ul>
        <li><strong><code>href</code>:</strong> Lokasi atau path dari file CSS.</li>
        <li><strong><code>rel</code>:</strong> Harus <code>"stylesheet"</code>.</li>
        <li><strong><code>type</code>:</strong> Harus <code>"text/css"</code>.</li>
    </ul>
    <pre><code>&lt;link href="style.css" rel="stylesheet" type="text/css"&gt;</code></pre>
</div>

<div id="materi-html-dasar" class="materi-section">
    <h2>HTML Dasar</h2>
    <p><strong>HTML</strong> Adalah sebuah bahasa markup yang digunakan untuk membuat sebuah halaman web dan menampilkan berbagai informasi di dalam sebuah browser. HTML berupa kode-kode tag yang menginstruksikan browser untuk menghasilkan tampilan sesuai yang diinginkan.</p>
    
    <h3>1. Struktur Standar Dokumen HTML</h3>
    <table>
        <tr><th>Elemen</th><th>Tag</th><th>Keterangan</th></tr>
        <tr><td>Document Type Declaration</td><td><code>&lt;!DOCTYPE html&gt;</code></td><td>Mendefinisikan standar versi dokumen (HTML5).</td></tr>
        <tr><td>Root Element</td><td><code>&lt;html&gt;</code></td><td>Membungkus seluruh konten HTML.</td></tr>
        <tr><td>Document Header</td><td><code>&lt;head&gt;</code></td><td>Berisi metadata (seperti <code>&lt;title&gt;</code>, <code>&lt;meta&gt;</code>).</td></tr>
        <tr><td>Document Body</td><td><code>&lt;body&gt;</code></td><td>Berisi semua konten yang ditampilkan kepada pengguna.</td></tr>
    </table>

    <h3>2. Tag, Atribut, dan Elemen</h3>
    <table>
        <tr><th>Istilah</th><th>Definisi</th><th>Contoh</th></tr>
        <tr><td><strong>Tag</strong></td><td>Penanda awalan (<code>&lt;tag&gt;</code>) dan akhiran (<code>&lt;/tag&gt;</code>) suatu elemen.</td><td><code>&lt;p&gt;</code>, <code>&lt;img /&gt;</code>.</td></tr>
        <tr><td><strong>Atribut</strong></td><td>Informasi tambahan yang memberikan properti pada elemen, ditulis di dalam tag pembuka.</td><td><code>&lt;body bgcolor="blue"&gt;</code></td></tr>
        <tr><td><strong>Elemen</strong></td><td>Komponen penyusun dokumen, terdiri dari tag pembuka, isi, dan tag penutup (opsional).</td><td><code>&lt;p&gt;Ini adalah paragraf&lt;/p&gt;</code></td></tr>
    </table>

    <h3>3. Tag-Tag Dasar HTML</h3>
    <ul>
        <li><strong>Heading:</strong> <code>&lt;h1&gt;</code> hingga <code>&lt;h6&gt;</code> untuk judul dan sub judul.</li>
        <li><strong>Paragraf:</strong> Tag <code>&lt;p&gt;</code>.</li>
        <li><strong>Baris/Garis:</strong> <code>&lt;br&gt;</code> (Break-line), <code>&lt;hr&gt;</code> (Horizontal-line).</li>
        <li><strong>Pemformatan Teks:</strong> <code>&lt;b&gt;</code>/<code>&lt;strong&gt;</code> (tebal), <code>&lt;i&gt;</code>/<code>&lt;em&gt;</code> (miring).</li>
        <li><strong>Hyperlink:</strong> Tag <code>&lt;a&gt;</code> dengan atribut <code>href</code>.</li>
        <li><strong>Image:</strong> Tag <code>&lt;img&gt;</code> dengan atribut <code>src</code> (lokasi file) dan <code>alt</code> (deskripsi).</li>
    </ul>
</div>

<script>
    document.addEventListener('DOMContentLoaded', function() {
        const navLinks = document.querySelectorAll('nav a');
        const materiSections = document.querySelectorAll('.materi-section');

        navLinks.forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault(); // Stop default link navigation

                // Get the ID of the target section from the data-target attribute
                const targetId = this.getAttribute('data-target');
                
                // Hide all sections first
                materiSections.forEach(section => {
                    section.style.display = 'none';
                });

                // Remove 'active' class from all links
                navLinks.forEach(nav => {
                    nav.classList.remove('active');
                });

                // Show the target section and add 'active' class to the clicked link
                const targetSection = document.getElementById(targetId);
                if (targetSection) {
                    targetSection.style.display = 'block';
                    this.classList.add('active');
                }
            });
        });
        
        // Optional: Trigger a click on the first link (CSS Dasar) to show its content on page load
        // document.getElementById('nav-css-dasar').click();
    });
</script>

</body>
</html>

### Pertanyaan dan Tugas
1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini
jawaban
```html
/* 1. Styling Dasar */
body {
    font-family:'Open Sans', sans-serif;
    margin: 0;
    padding: 0;
    line-height: 1.6; /* Ditambahkan */
    background-color: #f4f4f4; /* Ditambahkan */
}
/* ... */
h1 {
    font-size: 24px;
    color: #0F189F;
    text-align: left; /* Diubah dari center */
    padding: 20px 10px;
    text-shadow: 1px 1px 2px rgba(0,0,0,0.2); /* Ditambahkan */
}
/* ... */
/* 2. Styling Navigasi */
nav {
    background: #20A759;
    color: #fff;
    padding: 0;
    /* ... */
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); /* Ditambahkan */
}
/* ... */
nav .active,
nav a:hover {
    background: #20A759; /* Diubah: warna tetap hijau */
    color: #ffeb3b; /* Ditambahkan: teks kuning */
    text-decoration: none;
    border-radius: 5px; /* Ditambahkan */
}

/* 3. ID Selector (#intro) */
#intro {
    background: #418fb1;
    border: none;
    /* ... */
    border-top: 5px solid #E42A42; /* Ditambahkan */
}
/* ... */
/* 3.1 Styling the paragraph text inside #intro */
#intro p {
    color: #f0f8ff;
    font-size: 18px; /* Diubah dari 16px */
    text-align: left;
    line-height: 1.6;
}
 
/* 4. Class Selector (.button, .btn-primary) */
.button {
    padding: 15px 20px;
    background: #E42A42;
    color: #fff;
    /* ... */
    text-decoration: none;
    transition: background 0.3s ease; /* Ditambahkan */
}
2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan 
penjelasannya!
Jawaban
Penggunaan #intro h1 {...} memungkinkan Anda untuk memberikan style khusus pada <h1> yang berada dalam suatu bagian tertentu (yang memiliki id="intro"), tanpa mengubah style <h1> lainnya yang berada di luar bagian tersebut.
3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!
Jawaban
Inline CSS memiliki prioritas tertinggi karena ia melekat langsung pada elemen yang bersangkutan, sehingga akan menimpa (meng-override) style dari Internal dan External CSS untuk properti yang sama.
Contoh
Misalkan terdapat tiga Deklarasi untuk elemen
     1. External CSS (di style.css):
        p { color: green; font-size: 14px; }
     2. Internal CSS (di <head>):
        p { color: red; font-size: 16px; }
     3. Inline CSS (pada elemen):
<p style="color: blue; text-align: center;">Ini adalah paragraf.</p>
4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!
jawaban
     1. Inline Style (Prioritas tertinggi, dihitung sebagai 1,0,0,0)
     2. ID Selector (Tingkat kekhususan tinggi, dihitung sebagai 0,1,0,0)
     3. Class Selector (Tingkat kekhususan menengah, dihitung sebagai 0,0,1,0)
     4. Element Selector (Tingkat kekhususan rendah, dihitung sebagai 0,0,0,1)
Contoh:
1. Misalkan terdapat elemen HTML:
<p id="paragraf-1" class="text-paragraf">Ini adalah paragraf dengan ID dan Class.</p>
2. Dan deklarasi CSS:
```html
/* Class Selector */
.text-paragraf {
    color: red; /* Properti A */
    font-size: 14pt; /* Properti B */
}

/* ID Selector */
#paragraf-1 {
    color: blue; /* Properti A (Menimpa) */
    text-align: justify; /* Properti C (Menambah) */
}



       
