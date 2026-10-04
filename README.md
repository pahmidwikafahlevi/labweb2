Nama: Pahmi Dwika Fahlevi

NIM: 312510389 

Program Studi: Teknik Informatika 

Universitas: Universitas Pelita Bangsa

Deskripsi

Praktikum ini membuat satu halaman web Portal Mahasiswa (index.html) yang memakai HTML lanjutan: tabel, form, validasi form, semantic HTML, dan multimedia. Tampilan dibuat dengan CSS internal (di dalam tag <style>) dengan tema warna hijau, navigasi sticky, dan desain responsif.

Struktur Folder

Lab2Web/

├── gambar/

│   └── Logo-Universitas-Pelita-Bangsa-removebg-preview.png

├── WhatsApp Audio 2026-10-04 at 09.11.55.mp4

└── praktikum/               (folder file HTML)

    ├── index.html
    
    └── Video 2026-10-03 at 23.04.27.mp4

Sesuaikan struktur dengan folder proyek masing-masing. Path file gambar, audio, dan video pada HTML harus cocok dengan lokasi file sebenarnya.

Langkah-Langkah Praktikum

1. Membuat Kerangka Dasar HTML
   
Buat file index.html.

Tulis struktur dasar: <!DOCTYPE html>, <html lang="id">, <head>, dan <body>.

Di <head>, tambahkan <meta charset="UTF-8">, <meta name="viewport" ...> agar responsif, dan <title>.

2. Membuat Styling CSS

Tambahkan CSS di dalam <style> pada <head>:

Reset dasar (box-sizing: border-box) dan pengaturan body.

Gaya header, nav (sticky), main, section, footer.

Gaya tabel, form, tombol, dan kotak informasi (.info-box).


Media query (max-width: 700px) agar tampilan nyaman di layar kecil.

3. Membuat Header dan Navigasi

<header> berisi logo universitas dan judul "Portal Mahasiswa".
    
<nav> berisi tautan anchor (#beranda, #mahasiswa, #form, #multimedia, #biodata) yang mengarah ke id tiap section.
    
4. Membuat Tabel Data Mahasiswa (Section 1)
   
Gunakan <table>, <caption>, <thead>, <tbody>, dan <tfoot>.

Kolom: NIM, Nama, Program Studi.

Baris footer memakai colspan="2" untuk menggabungkan dua kolom.

5. Membuat Tabel Nilai Praktikum (Section 2)
Tabel dengan kolom No, Nama, Nilai.

Baris <tfoot> menampilkan rata-rata nilai dengan colspan="2".

Tambahkan .info-box sebagai penjelasan eksperimen colspan.

6. Membuat Form Registrasi (Section 3)

Form dengan action="#" dan method="post" yang berisi:

    Elemen	Tipe / Tag	Keterangan

    Nama Lengkap	input type="text"	required, minlength="3"

    Email	input type="email"	required

    Password	input type="password"	required, minlength="6"

        Tanggal Lahir	input type="date"	required

    Jenis Kelamin	input type="radio"	satu pilihan, name sama

    Keahlian	input type="checkbox"	boleh lebih dari satu

    Program Studi	<select> + <option>	dropdown

    Alamat	<textarea>	rows="5"

    Tombol	<button type="submit"> dan type="reset"	kirim dan reset

    Setiap <label> dihubungkan dengan input melalui atribut for yang sama dengan id input.

7. Membuat Validasi Form Dasar (Section 4)

Form dengan input nama (required, minlength), email (required), dan umur (type="number", min="17", max="60", required).
Uji dengan menekan tombol Kirim tanpa mengisi data. Browser akan menampilkan pesan peringatan otomatis.

8. Menerapkan Semantic HTML (Section 5)
Gunakan <header>, <nav>, <main>, <section>, <article>, <aside>, dan <footer> agar struktur halaman jelas dan bermakna.

9. Menambahkan Multimedia (Section 6)
Audio: <audio controls> dengan <source src="..." type="audio/mp4">.
Video: <video controls width="480"> dengan <source src="..." type="video/mp4">.
Tambahkan teks cadangan di dalam tag untuk browser yang tidak mendukung.

10. Membuat Proyek Mini Biodata (Section 7)
<article> pertama: tabel biodata (NIM, Nama, Program Studi, Jenis Kelamin, Email).
<article> kedua: form biodata (nama, email, program studi, alamat) dengan validasi required dan minlength.
    
11. Membuat Kesimpulan dan Footer
Tambahkan section kesimpulan yang merangkum materi.
Tutup halaman dengan <footer> berisi hak cipta dan nama praktikum.

12. Menjalankan dan Menguji
Buka index.html di browser (klik dua kali, atau gunakan ekstensi Live Server di VS Code).
Klik menu navigasi dan pastikan halaman berpindah ke section yang sesuai.
Coba kirim form kosong untuk menguji validasi.

Putar audio dan video untuk memastikan file terbaca.
Perkecil jendela browser untuk menguji tampilan responsif.
Catatan Perbaikan

Nilai rata-rata pada tabel nilai seharusnya 88.2, karena (85 + 90 + 88 + 92 + 86) / 5 = 441 / 5 = 88.2.
Pada kode tertulis 88.6.
NIM 312510389 muncul dua kali (Pahmi Dwika Fahlevi dan Andika). 
NIM seharusnya unik, jadi salah satunya perlu diperiksa.
Path audio memakai ../ sedangkan path video tidak.
Pastikan keduanya sesuai lokasi file agar media dapat diputar.



    
Jawaban Pertanyaan
1. Apa fungsi <table>, <tr>, <th>, dan <td>?
   
        <table>: membuat tabel, yaitu wadah utama untuk menampilkan data dalam baris dan kolom.
        <tr> (table row): membuat satu baris di dalam tabel.
        <th> (table header): membuat sel judul kolom atau baris. Teksnya biasanya tebal dan rata tengah.
        <td> (table data): membuat sel yang berisi data biasa.

    Contoh:

        html
        <table>
          <tr>
            <th>NIM</th>
            <th>Nama</th>
          </tr>
          <tr>
                <td>312510389</td>
        <td>Pahmi Dwika Fahlevi</td>
          </tr>
        </table>

2. Apa perbedaan <th> dan <td>?

    <th> adalah sel judul/header yang secara bawaan tampil tebal dan rata tengah, serta memberi makna bahwa isinya adalah label bagi kolom atau baris (berguna untuk aksesibilitas dan             screen reader).
    <td> adalah sel data biasa yang berisi isi tabel dan tampil dengan teks normal rata kiri.

3. Apa fungsi colspan pada tabel?

colspan menggabungkan beberapa kolom menjadi satu sel pada baris yang sama. 
Contohnya colspan="2" membuat sel memanjang menutupi dua kolom. 
Pada praktikum ini dipakai di <tfoot>, misalnya <td colspan="2">Rata-rata</td>, sehingga label "Rata-rata" menempati dua kolom dan nilainya berada di kolom ketiga.

4. Apa fungsi <form> dalam HTML?

<form> adalah wadah untuk mengumpulkan input dari pengguna dan mengirimkannya ke server atau halaman tertentu. 
    Atribut pentingnya:

    action: tujuan pengiriman data (pada praktikum # berarti halaman itu sendiri).
    method: cara pengiriman, yaitu get atau post.

Semua elemen input seperti teks, radio, checkbox, select, textarea, dan tombol submit ditempatkan di dalamnya.

5. Apa perbedaan radio button dan checkbox?
Aspek	Radio button	Checkbox
Jumlah pilihan	Hanya satu dalam satu grup	Boleh lebih dari satu
Pengelompokan	Beberapa radio dengan name yang sama menjadi satu grup	Setiap checkbox bisa berdiri sendiri
Membatalkan pilihan	Tidak bisa dibatalkan dengan klik ulang	Bisa dicentang dan dihapus centangnya
Contoh pada praktikum	Jenis Kelamin (Laki-laki / Perempuan)	Keahlian (HTML, CSS, JavaScript)

6. Mengapa <label> sebaiknya terhubung dengan id input melalui atribut for?

Karena hubungan tersebut memberi beberapa manfaat:

Klik label memfokuskan input. Mengklik teks label otomatis memilih atau mengaktifkan input terkait. Ini sangat membantu pada radio button dan checkbox yang area kliknya kecil.
Aksesibilitas. Screen reader dapat membacakan label saat pengguna berada pada input tersebut.
Struktur kode lebih jelas. Setiap input punya label yang tegas, sehingga mudah dipahami dan dipelihara.

Contoh: <label for="nama">Nama</label> dan <input type="text" id="nama">. Nilai for harus sama persis dengan id input.

7. Apa perbedaan <textarea> dengan input type text?
Aspek	<input type="text">	<textarea>
Jumlah baris	Satu baris	Banyak baris
Penggunaan	Data singkat (nama, email)	Teks panjang (alamat, komentar, pesan)
Penulisan tag	Tag tunggal (tidak punya penutup)	Punya tag pembuka dan penutup <textarea></textarea>
Nilai awal	Atribut value	Ditulis di antara tag
Ukuran	size / CSS	rows dan cols / CSS

8.     Apa fungsi semantic HTML seperti
           <header> <nav> <main> <section> <article> <aside>dan <footer>?

 Semantic HTML adalah elemen yang namanya menjelaskan makna isinya. 
 
 Manfaatnya: struktur halaman lebih mudah dibaca developer, 
 
lebih ramah mesin pencari (SEO), dan lebih mudah diakses oleh pembaca layar.

    <header>: bagian kepala halaman atau section, biasanya berisi logo dan judul.
    <nav>: kumpulan tautan navigasi utama.
    <main>: isi utama halaman (hanya satu per halaman).
    <section>: pengelompokan konten yang bertema sama, biasanya dengan judul sendiri.
    <article>: konten mandiri yang bisa berdiri sendiri, misalnya artikel atau postingan.
    <aside>: informasi tambahan atau sampingan yang berkaitan dengan konten utama.
    <footer>: bagian kaki halaman, biasanya berisi hak cipta dan info kontak.
    
9. Apa fungsi required, min, max, dan minlength?

Semuanya adalah atribut validasi form bawaan HTML5:

required: input wajib diisi. Form tidak bisa dikirim jika kosong.
min: nilai minimum yang diizinkan pada input angka atau tanggal (contoh: min="17").
max: nilai maksimum yang diizinkan (contoh: max="60").
minlength: jumlah karakter minimum pada input teks (contoh: minlength="3").

Pada praktikum, input umur memakai min="17" dan max="60", sedangkan nama memakai minlength="3".

10. Apa perbedaan elemen <audio> dan <video>?
Aspek	<audio>	<video>
Jenis media	Suara (musik, rekaman, podcast)	Gambar bergerak beserta suara
Tampilan	Hanya pemutar kontrol, tanpa area gambar	Memiliki area layar tampilan
Atribut ukuran	Tidak memakai width / height	Bisa memakai width, height, dan poster
Format umum	MP3, WAV, OGG, M4A	MP4, WebM, OGG

Keduanya sama-sama memakai atribut controls untuk menampilkan tombol putar, jeda, dan volume, serta tag <source> untuk menentukan file sumber dan tipenya.

Kesimpulan

Dari praktikum ini dipelajari cara membuat tabel dengan thead, tbody, tfoot, dan colspan; membuat form lengkap (text, email, password, date, radio, checkbox, select, textarea); menerapkan validasi form dengan required, minlength, min, dan max; menyusun halaman dengan semantic HTML; serta menambahkan multimedia audio dan video.
