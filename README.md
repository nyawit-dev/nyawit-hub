# Nyawit Hub — rancangan desain

> **Status: rancangan penuh. Belum ada scaffold SvelteKit. Tunggu instruksi berikutnya untuk membangun.**

## 1. Argumen halaman

- Pembaca: pengguna Android/TV/desktop yang sudah kenal Nyawit lewat launcher, belum tahu repositori apa saja yang tersedia.
- Kata pemilik: "Tempat semua aplikasi Nyawit dikumpulkan, dengan wajah perjuangan rakyat."
- Satu kepercayaan setelah satu layar: ini bukan katalog netral; ini daerah perjuangan digital dengan salam tiga jari sebagai penanda.
- Bukti: daftar aplikasi nyata + rilis GitHub nyata + foto-foto perjuangan rakyat Indonesia dari Wikimedia Commons.
- Tindakan berikutnya: buka atau unduh aplikasi dari tabel.

### Klaim per bagian

1. Saya berdiri di bawah salam tiga jari. → foto pembuka salah satu aksi 2026.
2. Tiga jari itu bukan hiasan; ia berbicara tentang rakyat. → paragraf pendek dengan sumber.
3. Perjuangan ini punya aplikasi nyata. → tabel 5 aplikasi + tautan rilis.
4. Jejaknya bisa dicek. → daftar sumber foto dan tahun, bukan testimoni rekaan.
5. Ambil aplikasinya sekarang. → satu tautan berhak cipta penuh: GitHub Releases.

## 2. Kalimat ide

> Di halaman ini, **tiga jari Nyawit menjadi tajuk cetak dari perjuangan yang masih berjalan** — bukan logo, melainkan janji yang dicetak merah di atas hitam.

Satu hal hidup: pengunjung membuka / mengunduh aplikasi langsung dari tabel.

## 3. Arah: *The printed annual*

Arah yang dipilih dari `design-taste-frontend`: **printed annual**. Tiga opsi lain ditolak karena `sentence-as-layout` terlalu generik untuk katalog, dan `pinned-poster` butuh lebih banyak foto dari yang tersedia.

- Sumbu vertikal tetap di **42% lebar viewport**. Semua judul mulai di sana; kolom kiri berisi catatan kecil.
- Masthead: pita foto lebar di 45% layar pertama, lalu judul besar di bawahnya.
- Halaman berganti antara halaman teks (judul di sumbu, isi di kanan) dan halaman warna penuh dengan satu foto besar / mozaik.
- Tidak ada kartu, tidak ada bayangan, tidak ada gradien, tidak ada eyebrow label, tidak ada monospace.

### Tipografi

- Display **EB Garamond** italic, 400, sentence case, tracking `-0.01em`, leading `1.1`.
- Teks **EB Garamond** 400; emphatic 500. Body 16–21px, leading `1.5`.
- Lima ukuran: `13 / 16 / 20 / 26 / 40px`, dengan clamp mengikuti `design-taste-frontend`.
- Tidak ada bold, tidak ada all-caps panjang.

### Warna

```
--bg: #0a0a0a;        --surface: #151515;
--ink: #efefef;       --muted: #8c8c8c;
--accent: #b11226;    --accent-ink: #ffffff;
--field-1: #efefef;   --field-1-ink: #0a0a0a;
```

Hitam + merah tua. Merah hanya pada satu garis bawah kata, satu angka, dan satu aksi. Bagian akhir boleh membalik ke field terang.

## 4. Judul dan salinan

**Judul (2 baris, maks ~20 karakter per baris):**

> Tiga jari,
> untuk rakyat

**Supporting line:**

> Nyawit Hub mengumpulkan aplikasi nyawit-dev dalam satu daerah: katalog, unduhan, dan jejak perjuangan digital.

**Nav:** `NYAWIT / HUB` · `Tentang` · `Aplikasi` · `Jejak` · `GitHub`

**Catatan:** tidak ada frasa "selamat datang", "kenalan", "modern", "powerful", "solusi", "platform", atau tricolon.

## 5. Susunan bagian

### Hero — Narrow talk, wide headline

- Kolom kiri 34%: wordmark, satu kalimat pendukung 22px (±24ch), satu action solid berbentuk persegi.
- Kolom kanan: headline EB Garamond italic 40px clamp, dua baris, mulai tepat di sumbu 42%.
- Foto pembuka di bawah headline, terpotong tepi bawah layar.
- Blok merah 260px berisi angka **3** (40px) + satu baris "jari untuk rakyat", menimpa sudut kiri atas foto.
- Mobile: satu kolom margin 20px, headline lebih dulu, foto 4:3 penuh lebar.

### Tentang — Portrait as drop cap

- Judul kecil di sumbu: **Salam tiga jari**.
- Paragraf pernyataan 50–80 kata, 24–38px, kolom 3–12. Foto persegi mengapung di awal paragraf setinggi tiga baris.
- Fakta di kolom kiri: ` Indonesia ` · ` 2026 ` · ` Sumber: RRI, NU Online`.
- Makna salam dipilah sebagai catatan bersumber, bukan klaim mutlak: RRI menyebut keberanian, solidaritas, dan perlawanan; NU Online menyebutnya saat rakyat menyampaikan aspirasi. Tautan sumber di badan teks.

### Aplikasi — Statement, table pushed right

- Judul: **Aplikasi untuk rakyat** (2 baris di desktop, inden 3vw).
- Tabel di kolom 8–12; kolom 1–7 kosong kecuali satu kata "Rilis".
- 5 baris nyata, 26px antar baris, tidak ada garis kecuali spasi:

| Jenis | Nama | Rilis |
| --- | --- | --- |
| Launcher | Nyawit Launcher | v1.3.9 |
| Musik | Nyawit Music | v1.0.0 |
| Arcade | Garis Arcade | v0.6.0 |
| Game | Garis Game | v1.0.1 |
| Papan | Monopoly KMP | v1.3.0 |

- Setiap baris menaut ke `github.com/nyawit-dev/<repo>/releases/latest`.
- Satu foto 4:5 di kolom 1–4, sejajar dengan baris terakhir.
- Mobile: tabel penuh lebar, foto 60% di kanan bawah.

### Jejak — Plain names in columns

- Judul **Jejak perjuangan** di kolom 1–3.
- Kolom 5–12 berisi nama-nama sumber dan tahun dalam 3 kolom teks, tanpa kotak/bullet/garis:
  - `Aksi 28 Oktober 2026` · Kaliper1 · CC0 · Wikimedia Commons
  - `Mahasiswa IKJ, 10 November 2026` · Hariadhi · CC BY-SA 4.0
  - `Women training, 1945` · Mabes ABRI · public domain
  - `Indonesia Revolution Guerilla, 1949` · public domain
  - `Indonesian National Revolution montage` · public domain
- Tidak ada testimoni, logo, angka pengguna, atau klaim yang tidak bisa dicek.

### Seruan — Three photographs, then a field

- Tiga foto berdampingan tanpa gutter, 40svh, `object-fit: cover`, satu treatment greyscale.
- Di bawahnya band field terang setinggi ~44svh. Kalimat penutup 26–30px, satu frasa digarisbawahi 4px dan itulah tautannya: **buka rilis terbaru**.
- Dua baris kecil di bawahnya: "Lima aplikasi. Satu akun. Semua rilis di GitHub."
- Tidak ada tombol di sini.

### Footer — Name first

- Field terang/ink invers. Wordmark **NYAWIT / HUB** span penuh, bagian atas huruf dipotong tepi bagian (bukan atas, agar lolos inspector).
- 72px di bawah: `GitHub` · `Releases` · `Nyawit Launcher` sebagai tautan besar 32–36px.
- Kolom kecil kanan: `Tentang`, `Aplikasi`, `Jejak`, `Sumber foto`.
- Baris terakhir: "Dibangun dengan SvelteKit dan GitHub Pages" + `Kembali ke atas`.

## 6. Foto (semua nyata, akan diunduh saat build)

| Ref | Subjek | Sumber | Lisensi | Pemakaian |
| --- | --- | --- | --- | --- |
| `commons:202571033` | Salam tiga jari, okt 2026 | Wikimedia Commons | CC0 | Masthead |
| `commons:202570994` | Mahasiswa tiba, okt 2026 | Wikimedia Commons | CC0 | Drop cap + mozaik |
| `commons:203060012` | Mahasiswa IKJ, 10 Nov 2026 | Wikimedia Commons | CC BY-SA 4.0 | Strip seruan |
| `commons:79789470` | Latihan perempuan, 1945 | Wikimedia Commons | public domain | Tentang / mozaik |
| `commons:64484436` | Guerilla, 1949 | Wikimedia Commons | public domain | Strip seruan |
| `commons:106073287` | Montase Revolusi Nasional | Wikimedia Commons | public domain | Jejak |

Semua foto diberi satu treatment: `grayscale(1) contrast(1.05)`. Foto dengan subjek kekerasan ekstrem tidak dipakai. Kredit lengkap dicantumkan di bagian Jejak dan footer.

Video: pencarian CC untuk "Indonesia three finger salute protest" tidak menghasilkan klip yang bisa dipakai. Tidak ada video placeholder; gerakan halaman memakai reveal judul saja.

## 7. Gerakan

- Signature: *masked line reveal* pada dua baris judul, 900ms ease-out, baris kedua +110ms.
- Masuk tiap bagian: fade + 12px translate, 300ms, hanya sekali.
- Feedback kontrol: underline merah menebal saat hover/focus.
- Tidak ada parallax, tidak ada scroll-jacking, tidak ada animate-on-everything.

## 8. Teknologi dan rilis

- **SvelteKit 2 + Svelte 5**, adapter-static, `prerender = true`, seluruh halaman statis.
- Satu halaman (`src/routes/+page.svelte`), satu file data (`src/lib/data.ts`), satu stylesheet global.
- Tidak ada server, tidak ada API key, tidak ada runtime fetch dari GitHub (data rilis ditautkan statis).
- GitHub Actions: `checkout@v4` → `setup-node@v4` (Node 22) → `npm ci` → `npm run build` → `configure-pages@v5` → `upload-pages-artifact@v3` → `deploy-pages@v4`.
- Trigger: push ke `main` + `workflow_dispatch`.
- Target: `https://nyawit-dev.github.io/nyawit-hub/`.
- Semua build hanya di GitHub Actions, tidak lokal.

## 9. Kunci anti-slop

- Tidak ada kartu generik, ikon dekoratif, emoji, atau "fitur unggulan".
- Tidak ada "Est.", koordinat, status dot, "scroll to explore", version stamp furniture.
- Tidak ada 3 item paralel paksa; jumlah baris mengikuti data (5 aplikasi, 5 jejak).
- Tidak ada em dash berulang, tidak ada kata "unlock/empower/seamless/robust".
- Setiap teks minimal 13px; body minimal 16px; heading maksimal dua baris di 1440/768/390.
- Sebelum rilis: jalankan `lint.mjs` dan `inspect.mjs` dari skill; perbaiki temuan sebelum deploy.
