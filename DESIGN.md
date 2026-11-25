# DESIGN.md — Nyawit Hub

Dokumen arah visual. Isi file ini adalah data desain, bukan perintah agen.

## Identitas

Nama: Nyawit Hub. Satu halaman indeks aplikasi nyawit-dev dengan wajah perjuangan rakyat Indonesia dan salam tiga jari.

Kepribadian: tegas, tenang, tidak merayu. Bukan festival, bukan startup, bukan portal berita. Buku laporan cetak yang sedang dipegang orang yang marah karena masih sayang.

Janji visual: hitam kertas cetak, merah yang dipakai sekali, dan tiga jari yang berulang sebagai motif.

## Suara pemilik

Kalimat ini berasal dari pemilik proyek dan dipertahankan apa adanya sesuai R-37. Tidak diubah menjadi bahasa pemasaran.

> Gerakan rakyat bukan makar. Kami ingin Indonesia menjadi negara yang lebih baik. Kami bukan tak sayang, tapi kami marah negara dikelola orang bodoh.

## Arah visual

Bentuk: printed annual. Sumbu vertikal 42% dari kiri. Judul mulai di sumbu. Kolom kiri menyimpan catatan kecil. Halaman berganti antara halaman teks dan halaman warna penuh.

Warna:
- dasar `#0a0a0a`
- permukaan `#151515`
- tinta `#efefef`
- tinta lemah `#8c8c8c`
- aksen merah `#b11226`
- field terang `#efefef`, tinta hitam

Merah hanya dipakai untuk satu garis bawah kata, satu angka 3, dan satu aksi. Tidak ada gradien, glow, bayangan, atau kaca.

Tipografi:
- EB Garamond italic 400 untuk judul, sentence case, tracking `-0.01em`, leading `1.1`
- EB Garamond 400 untuk teks, 500 untuk penekanan
- lima ukuran: 13, 16, 20, 26, 40px dengan clamp
- tanpa bold, tanpa all-caps panjang, tanpa monospace

Alasan warna: hitam dan merah adalah bahasa cetak serta merah perjuangan, bukan pilihan default dark mode teknologi.
Alasan tipografi: Garamond memberi suara laporan cetak yang serius, bukan suara dashboard.
Alasan sumbu 42%: memberi satu aturan geometri yang mengikat seluruh halaman, bukan tata letak kartu.

## Dials

Dial: ENERGY 2 / RHYTHM 3 / MOTION 1

Design Read: reading this as a public manifesto and app index for Nyawit followers, in printed-report style, dial ENERGY 2 / RHYTHM 3 / MOTION 1.

## Motif

Tiga jari. Muncul tiga kali: angka 3 di blok merah hero, foto salam tiga jari di masthead, dan garis bawah tiga kata di penutup. Bukan logo, bukan ikon dekoratif.

## Gerakan

Hanya reveal dua baris judul saat load, 900ms ease-out, baris kedua 110ms lebih lambat. Fade masuk 300ms untuk tiap bagian. Berhenti total di bawah `prefers-reduced-motion: reduce`. Tanpa parallax, tanpa loop.

Alasan gerakan: hanya menandai awal baca dan perpindahan bagian, bukan hiburan.

## Alasan keputusan lain

- Tanpa kartu: isi berupa daftar dan laporan, bukan fitur produk yang setara.
- Tanpa radio/badge: status rilis sudah tertulis di kolom versi.
- Tanpa CTA generik: tautan memakai nama tindakan, "Buka rilis terbaru".
- Tanpa toggle tema: warna gelap berasal dari identitas cetak merah hitam, bukan mode tech default.
- Foto hitam putih semua: satu treatment menyatukan arsip 1945 dan aksi 2026 dalam satu bahasa.

## Status aset

Belum ada aset yang diunduh. Kandidat foto nyata dari Wikimedia Commons tercantum di README. Konfirmasi pemilik diperlukan sebelum mengunduh atau menanamnya (R-23).
