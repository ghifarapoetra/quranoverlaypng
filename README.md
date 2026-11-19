# Quran Overlay — Affiliate Landing Page

Landing page statis (HTML/CSS/JS) untuk promosi affiliate Overlay PNG Quran Vertical. Bisa dipasang langsung di GitHub Pages atau Netlify. Tidak membutuhkan framework, build step, database, atau backend.

## Isi folder

- `index.html` — halaman utama, copywriting, layout responsif, FAQ, lightbox, dan event klik affiliate.
- `assets/` — poster promosi yang dioptimalkan ke WebP, dua video promosi yang dikompresi, poster video, favicon, dan gambar Open Graph.
- Semua tautan paket sudah dipasang ke tiga link affiliate Lynk.id yang diberikan.

## Deploy paling mudah (Netlify)

1. Download ZIP dan ekstrak di komputer.
2. Buka [Netlify Drop](https://app.netlify.com/drop).
3. Seret folder `overlay-quran-lp` (folder yang berisi `index.html` dan `assets/`) ke area upload.
4. Netlify akan memberi URL website. Buka URL itu dan tes seluruh tombol paket serta video.

### Deploy dari GitHub

1. Buat repository baru di GitHub, misalnya `overlay-quran-lp`.
2. Upload **isi folder** ini (`index.html`, `README.md`, dan folder `assets`) ke root repository. Jangan upload folder induk ekstra yang membuat `index.html` berada satu tingkat lebih dalam.
3. Di Netlify pilih **Add new project → Import an existing project → GitHub**, pilih repository tadi, lalu deploy.
4. Build command kosong dan publish directory isi dengan `.` (titik), karena ini situs statis tanpa proses build.

## Sebelum iklan berjalan

### 1. Perbarui domain untuk preview WhatsApp/Facebook

Di bagian `<head>` file `index.html`, ganti dua nilai berikut:

- `https://YOUR-DOMAIN/assets/og-cover.webp` → URL publik gambar `assets/og-cover.webp` setelah deploy.
- `https://YOUR-DOMAIN/` → URL publik landing page setelah deploy.

### 2. Pasang Meta Pixel (opsional)

Di bagian `<head>` cari:

```js
window.OVQ_META_PIXEL_ID = "";
```

Isi string kosong dengan Meta Pixel ID milik akun iklan, misalnya:

```js
window.OVQ_META_PIXEL_ID = "123456789012345";
```

Pixel akan mencatat `PageView` dan event khusus `AffiliateOutboundClick` saat tombol menuju Lynk.id diklik. **Event ini hanya mencatat klik keluar, bukan pembelian.** Karena checkout berlangsung di halaman pihak ketiga, jangan menganggap Pixel pada landing page ini otomatis bisa mengukur Purchase. Pelacakan pembelian membutuhkan integrasi/event yang disediakan pihak checkout atau akses tracking resmi.

### 3. Cek harga dan penawaran secara berkala

Harga yang ditampilkan di LP ini diambil dari halaman Lynk.id saat penyusunan:

- Indonesia Edition — Rp59.000
- Dual Language Edition — Rp79.000
- Complete Bundle — Rp149.000

Harga final, ketersediaan, detail isi, dan aturan lisensi mengikuti halaman checkout penjual. Ubah harga di tiga kartu paket jika penjual mengubahnya.

## Catatan materi dan lisensi

Poster dan video yang digunakan berasal dari folder `BAHAN IKLAN` dalam materi yang diberikan. File sampel PNG Al-Mulk dari folder `SAMPLE PNG-AL MULK` **sengaja tidak disalin ke website/repository**. Materi sumber memuat ketentuan yang melarang menjual kembali atau mendistribusikan ulang file PNG mentah. Halaman ini hanya menggunakan materi promosi yang disediakan, bukan membagikan aset produk.

Copy halaman juga menjelaskan batas penggunaan: file PNG mentah tidak boleh dijual atau dibagikan ulang. Pembeli perlu membaca lisensi edisi yang dipilih; jangan mengasumsikan ketentuan semua varian persis sama.

## Prinsip halaman

- Mobile-first, gambar WebP, video tidak autoplay dan memakai `preload="none"`.
- Tidak memakai countdown, stok terbatas, testimoni, angka penjualan, atau klaim yang belum didukung materi produk.
- Perbedaan paket dan harga ditampilkan sebelum pengunjung menuju checkout.
- CTA utama menuju bagian pilihan paket; setiap tombol paket menuju link affiliate yang sesuai.
- Tidak ada form atau data pribadi yang dikumpulkan di landing page.

Meta tetap melakukan review terhadap iklan dan destination page. Halaman yang berfungsi dengan baik tidak menjamin iklan pasti disetujui; pastikan copy dan materi iklan tetap sesuai kebijakan terbaru dan sama dengan penawaran di halaman ini.

## Sumber produk dan referensi

- [Complete Bundle — Lynk.id](https://lynk.id/ghifarapoetra/le7mll2e4lo0)
- [Indonesia Edition — Lynk.id](https://lynk.id/ghifarapoetra/j7qnj89vyv5d)
- [Dual Language Edition — Lynk.id](https://lynk.id/ghifarapoetra/ng991wyjp1m3)
- [Meta Blueprint — Understanding Meta Advertising Standards](https://storage.googleapis.com/understanding_meta_advertising_standards/Understanding_Meta_Advertising_Standards.pdf)
- [Stripe — Ecommerce landing page best practices](https://stripe.com/en-ch/resources/more/ecommerce-landing-page-best-practices)
- [Shopify — Landing page optimization strategies](https://www.shopify.com/blog/improving-landing-page-performance)
