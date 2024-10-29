Berikut adalah panduan singkat untuk membuat eBook tentang cara membuat todo app menggunakan Python, yang akan berisi langkah-langkah lengkap dari persiapan hingga deployment di internet.

> Paling pertama adalah setelah membuat folder project adalah setup Virtual Environment untuk melindungi file lain komputer anda dari proses setup & instalasi yang akan dilakukan dalam project ini dengan cara:

Buka terminal / cmd ketikkan:
```
python -m venv myenv
```
Kemudian aktifkan dengan perintah:
```
myenv\Scripts\activate
```
Untuk non aktifkan:
```
deactivate
```


### 1. Persiapan Lingkungan
   - **Bahasa Pemrograman**: Python 3.x
   - **Framework**: Flask (untuk membuat aplikasi web sederhana)
   - **Database**: SQLite (untuk penyimpanan lokal yang mudah dikelola)
   - **Library Tambahan**: 
     - Flask SQLAlchemy (ORM untuk interaksi dengan database)
     - Flask WTForms (untuk membuat form input data)
     - Flask Bootstrap atau CSS sederhana (untuk styling)
   - **Tool Lain**:
     - Editor Kode: Visual Studio Code, PyCharm, atau editor lain
     - Command Line atau Terminal untuk menjalankan server lokal

### 2. Struktur dan File yang Harus Dibuat
   - **File utama (`app.py`)**: Mengatur server, route, dan logic utama aplikasi
   - **Folder `templates`**: Menyimpan file HTML (misalnya `index.html`, `create.html`, `edit.html`)
   - **Folder `static`**: Menyimpan file CSS atau gambar (optional)
   - **Database File (`todo.db`)**: Berfungsi sebagai penyimpanan tugas yang diinput user

   Struktur dasar folder bisa terlihat seperti ini:
   ```
   todo_app/
   ├── app.py
   ├── todo.db
   ├── static/
   │   └── style.css
   └── templates/
       ├── index.html
       ├── create.html
       └── edit.html
   ```

### 3. Langkah-Langkah Membuat Kode Program
   - **Langkah 1**: Setup Project
     - Instalasi Flask (`pip install flask`), dan membuat file `app.py`.
     - Instalasi Flask SQL Alchemy (`pip install flask-sqlalchemy`), dan membuat file `app.py`.
     - Konfigurasi basic route untuk homepage dan koneksi dengan database.

   - **Langkah 2**: Membuat Database Model
     - Buat class `Todo` yang mewakili tabel dalam database SQLite.
     - Kelas ini akan berisi atribut seperti `id`, `title`, dan `completed`.

   - **Langkah 3**: Membuat Tampilan dan Template HTML
     - `index.html`: Menampilkan daftar semua todo items.
     - `create.html`: Form untuk menambahkan todo baru.
     - `edit.html`: Form untuk mengedit todo yang sudah ada.

   - **Langkah 4**: Logic Tambah, Edit, Hapus Todo
     - Buat fungsi untuk setiap action: menambah, mengedit, menghapus, dan menandai selesai.
     - Implementasikan di route masing-masing, misalnya `/create`, `/edit/<id>`, `/delete/<id>`.

   - **Langkah 5**: Styling
     - Gunakan CSS di dalam folder `static` untuk tampilan yang lebih menarik.

   - **Langkah 6**: Test dan Run
     - Jalankan aplikasi lokal dengan `python app.py`.
     - Pastikan setiap fungsi berjalan sesuai kebutuhan.

### 4. Menyajikan App di Browser dan Membuatnya Online
   - **Menjalankan di Browser**: Flask otomatis menjalankan server lokal di `http://localhost:5000`.
   - **Menyebarkan secara Online**: Gunakan platform seperti Heroku, Vercel, atau PythonAnywhere.
     - Buat akun dan install Heroku CLI.
     - Deploy aplikasi dengan command `git push heroku main`.

### 5. Gambaran Bentuk Todo App
   - **Tampilan Homepage**: List todo items dengan opsi untuk edit dan delete.
   - **Tampilan Form**: Form sederhana untuk menambah atau mengedit item.