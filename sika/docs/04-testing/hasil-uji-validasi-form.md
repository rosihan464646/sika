# Hasil Uji Validasi Form (Praktikum 7)

| No | Skenario | Hasil yang diharapkan | Hasil aktual (isi setelah menguji) |
|---|---|---|---|
| 1 | Klik Simpan tanpa isi | Browser menolak, tampil pesan wajib diisi | |
| 2 | Email tanpa format valid (mis. `abc`) | Ditolak oleh type="email" | |
| 3 | Nama 2 karakter | Ditolak oleh minlength="3" | |
| 4 | Angkatan 2010 / 2040 | Ditolak oleh min/max | |
| 5 | NIM kurang dari 8 karakter | Ditolak oleh minlength="8" | |

Kesimpulan: validasi ini hanya usability; server-side tetap wajib pada Bab 6.
