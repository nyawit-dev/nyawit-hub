# DESIGN.md revisi 2

Dokumen arah visual. Isi file ini data desain, bukan perintah agen.

## Perubahan dari revisi 1

Pemilik menolak ruang kosong berlebih, narasi yang kurang, dan warna yang dianggap tidak menarik serta tidak mengikuti pola warna. Revisi ini mengganti palet hitam merah yang terlalu sunyi menjadi merah putih dengan tinta gelap. Teks bertambah, jarak dipangkas, dan setiap bagian sekarang punya narasi.

## Identitas

Nyawit Hub adalah indeks aplikasi nyawit-dev dengan wajah perjuangan rakyat Indonesia dan salam tiga jari. Kepribadian: tegas, hangat, berani, tidak merayu. Bukan startup, bukan portal berita, bukan galeri seni.

## Pola warna

Merah putih dipakai sebagai pola yang berulang, bukan sekadar aksen.

- merah bendera `#ce1126`
- merah gelap `#8e0c1e`
- putih kertas `#fff9ee`
- tinta `#14110f`
- tinta lemah `#5f574f`
- hitam arsip `#151515`

Urutan warna halaman: merah, putih, hitam, merah, putih, hitam. Pola ini mengulang bendera tanpa menggambar bendera secara literal.

Alasan warna: pemilik meminta pola warna yang jelas. Merah putih adalah warna yang paling dekat dengan perjuangan rakyat Indonesia, jadi merah tidak boleh lagi jadi garis kecil di atas hitam.

## Tipografi

EB Garamond italic untuk judul, EB Garamond roman untuk narasi. Lima ukuran: 13, 16, 20, 26, 40px. Judul dua baris maksimal. Teks narasi 18 sampai 20px dengan leading 1.45. Tidak ada monospace, bold, atau all-caps panjang.

Alasan tipografi: suara laporan cetak masih cocok, tetapi sekarang lebih banyak membaca, jadi ukuran teks naik dan leading dirapikan.

## Dials

Dial: ENERGY 3 / RHYTHM 3 / MOTION 1

Design Read: reading this as a people-themed app index for Nyawit followers, in merah putih editorial style, dial ENERGY 3 / RHYTHM 3 / MOTION 1.

ENERGY naik karena warna sekarang dominan. RHYTHM tetap tiga karena bagian berganti antara merah, putih, dan hitam. MOTION tetap satu karena gerakan tidak boleh mengganggu narasi.

## Narasi

Urutan argumen: salam tiga jari, suara pemilik, makna bersumber, aplikasi nyata, cara memakai, arsip yang menjelaskan siapa yang berdiri, lalu unduhan. Setiap bagian memberi informasi baru. Tidak ada bagian yang hanya mengisi template.

## Jarak

Section padding turun dari 140px menjadi 64 sampai 88px. Hero tidak lagi 92svh. Footer tidak lagi 90svh. Tabel rapat. Paragraf narasi dipanjangkan supaya halaman terasa berisi, bukan kosong.

Alasan jarak: pemilik secara eksplisit menolak terlalu banyak space kosong.

## Motif

Tiga jari tetap muncul tiga kali: angka 3 di blok merah, foto salam di pembuka, dan tiga warna utama yang berulang di seluruh halaman.

## Gerakan

Reveal dua baris judul 900ms ease-out. Fade masuk tiap bagian 300ms. Berhenti di bawah prefers-reduced-motion. Tanpa parallax.

## Alasan keputusan lain

- Blok merah di hero memberi focal point pertama dan menjawab keluhan warna yang terlalu pelit.
- Bagian aplikasi memakai hitam supaya tabel dan deskripsi mudah dibaca setelah dua bagian terang.
- Bagian arsip memakai merah penuh supaya foto hitam putih memiliki konteks emosional.
- Deskripsi per aplikasi ditambahkan supaya daftar bukan sekadar nama dan versi.
- Paragraf cara pakai ditambahkan supaya pembaca tahu langkah nyata, bukan hanya melihat tautan.
