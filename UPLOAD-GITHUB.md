# Update GitHub — MPI Jelajah Gaya Patch v9

Patch ini dibuat agar asset lama di repository GitHub tidak perlu diunggah ulang.

## File yang perlu ditambahkan

- `patch-v9-github.js` — patch orientasi Portrait/Landscape + contoh soal kontekstual + style v9.
- `assets/bg-portrait-v9.webp` — background baru khusus mode Portrait.

## Perubahan pada `index.html` GitHub yang sekarang

Tambahkan satu baris berikut **tepat sebelum `</body>`**, setelah semua script aplikasi lama:

```html
<script src="./patch-v9-github.js?v=9"></script>
```

Tidak perlu menambahkan `patch-v9.css` dan `patch-v9.js` jika memakai `patch-v9-github.js`, karena CSS sudah digabung ke file tersebut. Dua file itu disertakan hanya sebagai versi terpisah/opsional.

## Struktur repository

```text
mpi-jelajah-gaya/
├─ index.html                 ← index GitHub lama, tambahkan 1 tag script
├─ patch-v9-github.js         ← BARU
└─ assets/
   └─ bg-portrait-v9.webp     ← BARU
```

## Yang tidak perlu diunggah ulang

Asset gambar/karakter/simulasi/mini-game yang sudah ada pada versi GitHub sebelumnya tetap digunakan. Berdasarkan perbandingan source sebelum dan sesudah Patch v9, hanya satu asset gambar baru yang ditambahkan oleh v9, yaitu background Portrait.

## Setelah upload

1. Commit perubahan.
2. Tunggu GitHub Pages selesai deploy.
3. Buka situs dengan hard refresh / incognito.
4. Cek pilihan Portrait dan Landscape, lalu buka Materi sampai setelah Rangkuman untuk memastikan halaman Contoh Soal muncul.

## Catatan penting

Patch harus dimuat setelah script aplikasi lama. Jangan menaruh tag `patch-v9-github.js` di `<head>` tanpa `defer`, karena patch membutuhkan fungsi dan data aplikasi utama yang sudah terbentuk.
