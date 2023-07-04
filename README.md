# Virtual Environment di python3.12 (beta)
## Penjelasan Virtual Environment
Virtual Environment adalah sebuah lingkungan virtual yang terisolasi untuk menyimpan semua library atau configurasi yang kita inginkan. 
pahami ilustrasi berikut ini : Jika aplikasi A membutuhkan versi 1.0 dari modul tertentu tetapi aplikasi B membutuhkan versi 2.0, maka persyaratannya bertentangan dan menginstal versi 1.0 atau 2.0 akan membuat satu aplikasi tidak dapat berjalan.

## Cara Menggunakan 

### 1. Install Virtual Environment

lakukan instalasi dengan memanggil query di terminal/cmd kita saja.
```bash
pip install virtualenv
```

### 2. Membuat Folder Proyek

Selanjutnya kita harus membuat folder proyek yang akan digunakan untuk meletakkan script - script python kita nantinya

```bash
mkdir python-project
```
`mkdir` adalah sebuah perintah (buat folder) di cmd

### 3. Membuat Virtual Environment

buka file folder yang telah dibuat terlebih dahulu:
```bash
cd python-project
```
`cd` adalah sebuah perintah (buka folder)  di cmd

Selanjutnya kita dapat membuat virtual environment baru di dalam folder proyek yang sudah kita buat. 
jalankan modul `venv` sebagai skrip dengan jalur direktori:

```bash
python -m venv tutorial-env
```

Ini akan membuat direktori `tutorial-env` jika tidak ada, dan juga membuat direktori di dalamnya yang berisi salinan interpreter Python dan berbagai file pendukung.

### 4. Mengaktifkan Virtual Environment

Setelah Anda membuat lingkungan virtual, Anda dapat mengaktifkannya.

Di Windows, operasikan:

```bash
tutorial-env\Scripts\activate
```
Pada Unix atau MacOS, operasikan: 
```bash
source tutorial-env/bin/activate
```
(Skrip ini ditulis untuk `base shell`. Jika Anda menggunakan `csh` atau  `fish shells`, ada pilihan skrip `activate.csh` dan `activate.fish` alternatif yang dapat Anda gunakan.)
Setelah menjalankan script `bin/active` maka virtual environment yang kita buat sudah aktif sehingga ketika kita menginstall package baru menggunakan `pip` maka package tersebut akan terinstall ke virtual environment tersebut

### 5. Menonaktifkan Virtual Environment

Untuk menonaktifkan virtual environment kita dapat menggunakan perintah berikut

```bash
deactivate
```

Setelah perintah tersebut dijalankan maka virtual environment kita tidak akan aktif sehingga setiap kali kita menginstall package baru menggunakan `pip` maka package tersebut akan terinstall ke sistem OS kita
