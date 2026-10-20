# UI Security Checklist - Bab 2

| No | Pemeriksaan | Status | Catatan |
|---|---|---|---|
| 1 | Setiap data yang tampil diperlukan use case | [x] | Lihat ui-requirement-map.md |
| 2 | Hanya data dummy (Andi Saputra, andi@example.com, NIM 24010001) | [x] | Bukan data pribadi nyata |
| 3 | Tidak ada credential/API key/token/password di HTML & komentar | [x] | Dicek lewat View Source |
| 4 | Data sensitif tidak di URL; form memakai method="post" | [x] | Persiapan Bab 6 |
| 5 | Tidak ada hidden input berisi rahasia | [x] | Hidden input tetap terlihat di DevTools |
| 6 | HTML5 validation dipahami hanya sebagai lapisan usability | [x] | `required` bisa dihapus lewat DevTools; validasi server-side wajib (Bab 6) |
| 7 | Screenshot/repository publik tidak memuat data nyata | [x] | |

## Potensi paparan data client-side yang dicegah (min. 2)
1. Tidak menaruh credential/token di komentar HTML maupun atribut `data-*`.
2. Tidak mengirim data lewat URL (query string) karena tersimpan di history/log; form memakai POST.
3. Tidak mengumpulkan field yang tidak dibutuhkan (NIK, alamat, dll.).

---

# Pembaruan Bab 3 - CSS Security Checkpoint

| No | Pemeriksaan | Status | Catatan |
|---|---|---|---|
| 1 | Tidak ada elemen sensitif yang hanya disembunyikan dengan CSS | [x] | Tidak ada `display:none`/`visibility:hidden` untuk data sensitif |
| 2 | Stylesheet/pseudo-element tidak memuat token, password, atau data sensitif | [x] | `content:` hanya berisi ikon dan label status |
| 3 | Tombol/fitur administratif dipahami sebagai UI saja, bukan authorization | [x] | Belum ada fitur admin; otorisasi server-side direncanakan Bab 6+ |
| 4 | Focus state terlihat; status tidak hanya mengandalkan warna | [x] | Outline 3px; error = border tebal + teks/ikon |
| 5 | Layout responsif tidak menyembunyikan informasi penting | [x] | Tabel digeser dalam `.table-wrapper`, tidak disembunyikan |

Catatan: menyembunyikan elemen dengan CSS hanya keputusan UI. Pengguna tetap dapat mengubah CSS lewat DevTools atau mengirim request langsung, sehingga hak akses wajib diperiksa di server pada setiap request sensitif.
