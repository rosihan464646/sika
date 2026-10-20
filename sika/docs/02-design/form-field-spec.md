# Form Field Specification - form-mahasiswa.html

| Field (name) | Tujuan | Type HTML | Wajib | Batas | Klasifikasi Data |
|---|---|---|---|---|---|
| nim | Identitas unik mahasiswa | text | Ya | 8-15 karakter | Internal |
| nama | Nama lengkap | text | Ya | min 3 karakter | Pribadi |
| email | Kontak mahasiswa | email | Ya | format email | Pribadi |
| prodi | Program studi | select (TI/SI) | Ya | nilai dari daftar | Internal |
| angkatan | Tahun masuk | number | Ya | 2020-2030 | Internal |
| status | Status akademik | radio (aktif/nonaktif) | Ya (default aktif) | 2 pilihan | Internal |

## Data minimization
Hanya 6 field di atas yang dikumpulkan karena dibutuhkan FR-03. Tidak ada field tanggal lahir, alamat, NIK, atau no. HP karena belum ada kebutuhan pada fase ini.
