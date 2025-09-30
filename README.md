|                |                    |
| -------------- | ------------------ |
|      _Nama_    | Fitri Ramadhani |
|      _NIM_     |      312410085     |
|     _Kelas_    |      TI.24.A.1      |
|  _Mata Kuliah_ | Pemrograman Web 1 |

Pertanyaan dan Tugas
1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS
dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.
2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan
penjelasannya!
3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada
elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan
penjelasan dan contohnya!
4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut
terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser?
Berikan penjelasan dan contohnya! ( p id="paragraf-1" class="text-paragraf" )
Jawab:

## 1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.

## Hasil Output Program
<img width="1366" height="768" alt="pemweb1" src="https://github.com/user-attachments/assets/818d050f-6fa9-45e8-96fc-d86d46b52493" />

<img width="1366" height="768" alt="pemweb2" src="https://github.com/user-attachments/assets/0dfe14b5-55a1-41af-92c7-d5e37cbc6cae" />

<img width="1366" height="768" alt="pemweb4" src="https://github.com/user-attachments/assets/9ad3c8e9-5f1e-4f84-a8f0-aff85079045e" />

<img width="1366" height="768" alt="pemweb5" src="https://github.com/user-attachments/assets/700a4a18-cc32-45f9-9726-d48ce9942773" />

<img width="1366" height="768" alt="pemweb6" src="https://github.com/user-attachments/assets/c6e07d85-4f73-465a-825c-f23cb1828ddf" />

## 2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan penjelasannya!

 - h1 {...} adalah elemen selector yang berlaku untuk semua tag h1 di dalam dokumen HTML. Jadi, semua heading h1 akan mendapatkan style yang sama.
 - sedangkan #intro h1 {...} adalah ID selector yang lebih spesifik, artinya aturan CSS tersebut hanya berlaku pada elemen h1 yang berada di dalam elemen dengan id="intro". Dengan kata lain, style hanya diterapkan pada h1 yang merupakan turunan langsung dari elemen #intro. 
Contoh:
```python
h1 {
  color: blue;
}

#intro h1 {
  color: red;
}
```

Jika ada dua h1, satu di luar div id="intro" dan satu di dalamnya, maka h1 di luar akan berwarna biru, sedangkan h1 di dalam #intro akan berwarna merah.

## 3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!

Prioritas jika ada Internal, Eksternal, dan Inline CSS pada elemen yang sama CSS memiliki aturan prioritas (specificity). 
Urutannya:

Inline CSS → prioritas paling tinggi.
Internal CSS (dalam tag style di file HTML).
Eksternal CSS (file .css terpisah).

Jika ketiganya digunakan pada elemen yang sama, maka Inline CSS akan ditampilkan di browser, karena tingkat prioritasnya lebih tinggi dibanding internal maupun eksternal.

Contoh:
```python
HTML:

<p id="teks" style="color: green;">Ini contoh teks</p>


Eksternal CSS (style.css):

#teks {
  color: red;
}


Internal CSS:

<style>
#teks {
  color: blue;
}
</style>
```

Hasil di browser: teks akan berwarna hijau, karena inline CSS lebih diutamakan.

## 4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebutterdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya! ( p id="paragraf-1" class="text-paragraf" )

Dalam aturan CSS, ID memiliki prioritas lebih tinggi daripada Class. Jadi, jika sebuah elemen HTML memiliki id dan class sekaligus, maka style yang berasal dari ID-lah yang akan dipakai browser.

Contoh:
```python
HTML:

<p id="paragraf-1" class="text-paragraf">Belajar CSS Prioritas</p>


CSS:

.text-paragraf {
  color: blue;
}

#paragraf-1 {
  color: red;
}
```
Hasil di browser: teks akan berwarna merah, karena CSS dengan selector id lebih spesifik dibanding class.

# Pertemuan 3 - Pemrograman Web

Proyek ini merupakan latihan dasar HTML dan CSS pada mata kuliah Pemrograman Web di Universitas Pelita Bangsa.
Fokus utama dari tugas ini adalah mempelajari penerapan CSS Internal, CSS Inline, serta melakukan simulasi penggunaan CSS Eksternal dalam satu halaman website.

---

## Materi yang Dipelajari

1. **CSS Internal**  
   Menggunakan tag <style> yang ditulis langsung di dalam file HTML.
   
2. **Inline CSS**  
   Menyisipkan atribut `style`' secara langsung pada elemen HTML, misalnya:
   ```html
   <p style="text-align: center; color: #ccd8e4;">...</p>
   
3. **CSS Eksternal (Simulasi)**
Disimulasikan dengan menambahkan block <style> kedua, meskipun pada praktik sebenarnya diletakkan dalam file .css terpisah.

5. **Selector CSS**
   ID Selector → #intro
   
   Class Selector → .button, .btn-primary
   
   Tag Selector → h1, nav, p

# Input kodingan
```python
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Dasar</title>
    
    <!-- CSS Internal -->
    <style>
        body {
            font-family: 'Open Sans', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f5f5f5;
        }
        
        header {
            min-height: 80px;
            border-bottom: 1px solid #77CCEF;
            background-color: white;
        }
        
        h1 {
            font-size: 24px;
            color: #0F189F;
            text-align: center;
            padding: 20px 10px;
            margin: 0;
        }
        
        h1 i {
            color: #6d6a6b;
        }
        
        #intro {
            background: #418fb1;
            border: 1px solid #099249;
            min-height: 100px;
            padding: 10px;
            margin: 20px;
            border-radius: 5px;
        }
        
        #intro h1 {
            text-align: left;
            border: 0;
            color: #fff;
            padding: 10px 0;
        }
        
        #intro p {
            color: white;
            line-height: 1.5;
        }
        
        .button {
            padding: 15px 20px;
            background: #bebcbd;
            color: #fff;
            display: inline-block;
            margin: 10px;
            text-decoration: none;
            border-radius: 4px;
        }
        
        .btn-primary {
            background: #E42A42;
        }
        
        .btn-primary:hover {
            background: #c21830;
        }
    </style>
    
    <!-- CSS Eksternal (disimulasikan dalam style tag) -->
    <style>
        /* Simulasi CSS Eksternal */
        nav {
            background: #20A759;
            color: #fff;
            padding: 10px;
        }
        
        nav a {
            color: #fff;
            text-decoration: none;
            padding: 10px 20px;
            display: inline-block;
        }
        
        nav .active,
        nav a:hover {
            background: #08E8BA;
        }
    </style>
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
    
    <!-- CSS ID Selector -->
    <div id="intro">
        <h1>Hello World</h1>
        <!-- Inline CSS pada paragraf -->
        <p style="text-align: center; color: #ccd8e4;">
            Kami sedang belajar HTML dan CSS dasar, pada mata kuliah <b>Pemrograman Web</b> di <i>Universitas Pelita Bangsa</i>. 
            Pelajaran pertama yang kami dapat adalah membuat tampilan web sederhana dalam rangka mengenal tag-tag dasar HTML dan CSS.
        </p>
        <!-- CSS Class Selector -->
        <a class="button btn-primary" href="#intro">Informasi selengkapnya.</a>
    </div>
</body>
</html>
```
