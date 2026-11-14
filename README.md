# Panduan Template Undangan Pernikahan Digital

Template ini terdiri dari **satu file** (`undangan.html`). Semua data pernikahan ada di satu blok bernama **PENGATURAN UNDANGAN** di bagian atas file. Anda cukup mengubah isi blok itu.

## 1. Cara membuka dan mengedit

1. Buka `undangan.html` dengan editor teks biasa (Notepad, VS Code, atau editor kode di HP).
2. Cari tulisan `PENGATURAN UNDANGAN`.
3. Ubah teks di antara tanda kutip `' '`. Jangan hapus tanda kutip, koma, atau kurung.
4. Simpan, lalu buka file di browser untuk melihat hasilnya.

## 2. Memilih tema

Ubah baris ini:

```js
tema: 'zamrud',
```

Pilihan: `'zamrud'` (hijau tua dan emas), `'sage'` (hijau lembut terang), `'anggur'` (merah anggur dan rose gold), `'embun'` (biru lembut terang).

Untuk pratinjau, biarkan `tampilkanPilihTema: true` agar muncul tombol warna di pojok kiri bawah. Untuk dipakai pelanggan, ganti menjadi `false`.

## 3. Mengganti data

| Bagian | Yang diubah |
| --- | --- |
| `whatsapp` | Nomor penerima RSVP, diawali 62 tanpa 0 dan tanpa + (contoh `6281234567890`) |
| `hitungMundur` | Waktu acara untuk hitung mundur, format `2027-02-20T08:00:00+07:00` |
| `pria`, `wanita` | Nama lengkap, panggilan, nama orang tua |
| `acara` | Daftar acara. Salin satu blok `{ ... }` untuk menambah acara |
| `lokasi` | Kartu lokasi dan tombol Google Maps |
| `rekening` | Amplop digital. Isi `[]` untuk menyembunyikannya |

## 4. Memasukkan foto

Taruh foto di folder `foto` di samping `undangan.html`, lalu tulis namanya:

```js
galeri: ['foto/1.jpg', 'foto/2.jpg', 'foto/3.jpg'],
```

Foto profil mempelai: isi `foto: 'foto/raka.jpg'` pada bagian `pria` dan `wanita`. Foto latar halaman pembuka: isi `fotoCover: 'foto/cover.jpg'`.

Saran: kecilkan foto ke lebar sekitar 1200 piksel dan ukuran di bawah 300 KB agar halaman cepat dibuka. Foto pertama galeri sebaiknya mendatar, sisanya tegak.

## 5. Google Maps

Isi `linkMaps` dengan link dari Google Maps (buka tempatnya, tekan Bagikan, salin link). Kalau dikosongkan, tombol mencari berdasarkan nama tempat dan alamat.

## 6. Link khusus untuk setiap tamu

Tambahkan `#` dan nama tamu di akhir alamat undangan, dengan tanda hubung sebagai pengganti spasi:

```
https://alamat-undangan-anda.com/#Budi-Santoso
```

Cover akan menyapa "Budi Santoso" dan kolom nama RSVP terisi otomatis. Gunakan huruf dan angka saja.

## 7. Musik

Bawaan: nada lembut yang dibuat langsung di browser. Untuk lagu sendiri, taruh file mp3 di folder `musik` lalu isi `fileMusik: 'musik/lagu.mp3'`. Pastikan Anda berhak memakai lagu tersebut. Lagu populer berhak cipta, jadi gunakan musik bebas royalti atau musik milik pembeli.

Untuk mematikan musik sama sekali, ubah `musik: false`.

## 8. RSVP

Formulir RSVP menyusun pesan lalu membukanya di WhatsApp, ditujukan ke nomor pada `whatsapp`. Jawaban tamu masuk ke chat mempelai. Template ini tidak menyimpan jawaban di server.

## 9. Memasang agar bisa dibuka lewat link

Pilih salah satu:

1. **Netlify Drop** (drop.netlify.com): seret folder yang berisi `undangan.html` dan folder `foto`. Ganti nama file menjadi `index.html` agar alamat utamanya langsung membuka undangan.
2. **GitHub Pages**: unggah file ke repository, lalu aktifkan Pages.
3. **Hosting biasa**: unggah lewat File Manager atau FTP.

## 10. Hal penting sebelum menjual

1. Ganti semua data contoh (nama, nomor WhatsApp, rekening, alamat) milik pembeli.
2. Pastikan foto dan musik yang dipakai milik pembeli atau bebas royalti.
3. Font memakai Google Fonts (Bodoni Moda, Cormorant Garamond, Playfair Display, DM Serif Display, Jost), berlisensi terbuka. Undangan butuh internet untuk memuat font. Tanpa internet, tampilan memakai font cadangan.
4. Template ini adalah kode buatan Anda sendiri. Periksa ketentuan platform tempat Anda menjual.
