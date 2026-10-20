# CSS Style Guide - SIKA Bab 3

## Design tokens (`:root` di `assets/css/style.css`)
| Token | Nilai | Kegunaan |
|---|---|---|
| --primary / --primary-dark | #1d4ed8 / #1e40af | Nav, judul header, tombol, hover |
| --surface / --background | #ffffff / #f3f4f6 | Kartu, form, tabel / latar halaman |
| --text / --muted | #1f2937 / #4b5563 | Teks utama / teks sekunder |
| --border | #d1d5db | Garis kartu, input, tabel |
| --focus | #f59e0b | Outline focus (3px) |
| --error / --success | #b91c1c / #166534 | Status (selalu disertai teks + ikon) |
| --radius / --radius-sm | .75rem / .4rem | Sudut kartu / kontrol |
| --space-1..4 | .5 / 1 / 1.5 / 2 rem | Skala spacing |

## Tipografi
Arial, Helvetica, sans-serif; line-height 1.6; h1 1.75rem, h2 1.25rem (kartu 1.1rem); ukuran memakai rem.

## Layout & breakpoint
| Breakpoint | Perubahan |
|---|---|
| base (mobile) | 1 kolom; nav tersusun vertikal sampai 640px |
| >= 640px | dashboard 2 kolom |
| >= 700px | profil: foto 180px + info |
| >= 768px | form 2 kolom (`.form-row`) |
| >= 960px | dashboard 3 kolom |

Flexbox: navigasi (`nav ul`), kelompok tombol (`.button-group`), opsi radio.
Grid: `.dashboard-grid`, `.profile`, `.form-row`.
Breakpoint dipilih saat layout mulai sempit/renggang, bukan berdasarkan nama perangkat.

## Komponen & penamaan class
`.container`, `.card`, `.dashboard-grid`, `.profile`, `.profile-info`, `.table-wrapper`, `.form-row`, `.form-group`, `.hint`, `.radio-option`, `.button-group`, `.btn-secondary`, `.alert`, `.alert-error`, `.alert-success`. Penamaan: huruf kecil, kata dipisah tanda hubung, berdasarkan fungsi.

## Aturan
- Hanya CSS eksternal; tanpa inline style.
- Status tidak hanya warna: error = border tebal + ikon/teks; menu aktif = `aria-current` + underline.
- Tidak ada rahasia di stylesheet (termasuk `content:` pseudo-element).
