# Tugas Individu 3 - Pengembangan Aplikasi Web

| | |
|---|---|
| Nama | Annisa Salsabila |
| NIM | 123140070 |
| Kelas | RA |

## Deskripsi

Website sederhana dua halaman untuk pendaftaran Pelatihan Web Dasar.

1. **Halaman pendaftaran** (`pendaftaran.html`): form dengan method **GET**.
2. **Halaman detail pendaftar** (`detail.html`): isinya dummy, ditulis manual di HTML.

Kedua halaman dihubungkan lewat query string. Sesuai instruksi tugas, query string hanya **didesain**, data dari form tidak ditangkap di halaman detail. Jadi isi tabel di halaman detail memang berbeda dengan data yang diisi di form.

## Struktur Folder

```
task_3/
├── pendaftaran.html
├── detail.html
├── style.css
├── README.md
└── RA-Annisa Salsabila-123140070-Tugas3-Pemweb.pdf
```

## Cara Menjalankan

Tidak butuh instalasi apa pun. Buka `pendaftaran.html` di browser, isi form, lalu klik **Daftar**. Browser akan pindah ke `detail.html` dan URL-nya berisi query string dari data form.

Kalau pakai VS Code, bisa juga lewat ekstensi Live Server.

## Desain Query String

Format: `detail.html?parameter1=nilai1&parameter2=nilai2`

| Parameter | Asal field |
|---|---|
| `nama` | input text |
| `nim` | input text (pattern 9 digit) |
| `tgl_lahir` | input date |
| `email` | input email |
| `no_hp` | input tel |
| `gender` | radio |
| `alamat` | textarea |
| `prodi` | select |
| `minat` | checkbox (bisa lebih dari satu) |
| `setuju` | checkbox |

Contoh hasil submit:

```
detail.html?nama=Budi+Santoso&nim=123140001&tgl_lahir=2005-03-14&email=budi.santoso%40mail.com&no_hp=081234567890&gender=laki-laki&alamat=Jl.+Merdeka+No.+10%2C+Bandar+Lampung&prodi=informatika&minat=frontend&minat=backend&setuju=on
```

Checkbox `minat` memakai `name` yang sama, jadi kalau dipilih lebih dari satu parameternya muncul berulang.

## Desain CSS (`style.css`)

- **Selector** yang dipakai: elemen, class, id, atribut, pseudo-class, dan gabungan (lebih dari 3 jenis).
- **Layout**: Flexbox (header, footer, tombol, pilihan radio/checkbox) dan Grid (form 2 kolom). Ada media query untuk layar kecil.
- **Box**: card dengan padding, margin, border, border-radius, dan box-shadow.
- **Tabel**: `border-collapse`, zebra stripes, dan efek hover pada baris.
- **Form**: fieldset, input dengan efek `:focus`, serta tombol dengan efek hover.

## Catatan

Field password sengaja tidak dipakai karena method GET menampilkan isi form di URL.
