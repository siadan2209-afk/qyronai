# QYRON — Engineer Your Imagination

Starter website/PWA premium untuk koleksi prompt AI. Dibuat dengan HTML, CSS, dan JavaScript murni agar mudah diedit lewat HP Android, GitHub, dan Vercel.

## Fitur yang tersedia
- UI dark premium dengan aksen biru-ungu dan layout responsif.
- Home, Discover, Prompt Studio, Library, Profile, dan halaman Pro.
- 10 template prompt untuk gambar, menulis, coding, dan bisnis; tersedia template Indonesia dan Inggris.
- Pencarian, filter kategori, detail prompt, salin prompt, favorit, dan koleksi buatan.
- Data favorit dan prompt buatan disimpan di localStorage perangkat.
- Ekspor koleksi ke JSON dan hapus data lokal.
- PWA manifest dan service worker untuk caching dasar.
- Halaman Pro dan placeholder slot iklan.

## Deploy ke Vercel melalui GitHub
1. Ekstrak `QYRON.zip`.
2. Buat repository baru di GitHub, misalnya `qyron-app`.
3. Unggah seluruh file dan folder yang ada di dalam ZIP langsung ke root repository. Pastikan `index.html`, `style.css`, dan `app.js` terlihat langsung di halaman utama repository, bukan berada di dalam folder `QYRON` bersarang.
4. Di Vercel pilih **Add New → Project**, impor repository GitHub tersebut.
5. Untuk proyek statis ini, biarkan Framework Preset sebagai **Other**, Build Command kosong, Output Directory kosong atau `.` lalu deploy.
6. Buka URL deployment. Jika mengubah kode, commit/push kembali ke GitHub untuk memicu deployment baru.

## Menjadikan website sebagai APK
- Cara sederhana: gunakan pembungkus WebView/PWA-to-APK yang tepercaya dan masukkan URL Vercel kamu.
- Untuk PWA, buka website melalui Chrome Android lalu menu browser → **Install app** atau **Tambahkan ke layar utama** jika opsi tersedia.
- APK hasil pembungkus pihak ketiga perlu diuji di perangkat dan ditinjau izinnya sebelum dibagikan.

## Monetisasi: status penting
**AdMob dan pembayaran Pro belum benar-benar diintegrasikan.** UI ini hanya menyediakan slot iklan dan halaman Pro. Jangan memasukkan ID palsu dan jangan menganggap tombol Pro sebagai transaksi aktif.

### AdMob
AdMob umumnya ditujukan untuk aplikasi Android/iOS yang memenuhi kebijakan Google. Untuk APK berbasis WebView, integrasi iklan harus dilakukan melalui implementasi native yang sesuai, atau gunakan solusi iklan web yang memang mendukung website. Jangan sekadar menempelkan Ad Unit ID ke HTML dan menganggap iklan sudah berjalan. Uji iklan dan patuhi kebijakan sebelum rilis.

### Paket Pro
Untuk mengaktifkan pembayaran sungguhan, pilih penyedia pembayaran dan bangun alur verifikasi server-side. Untuk langganan digital di aplikasi Android yang dipublikasikan melalui Google Play, periksa kebijakan Google Play Billing yang berlaku. Jangan menyimpan rahasia API di JavaScript frontend.

## Catatan teknis
- Tidak ada login atau database cloud.
- Data koleksi hanya tersimpan di browser/perangkat masing-masing; data tidak otomatis tersinkron antarperangkat.
- Google Fonts membutuhkan koneksi internet; font fallback tetap tersedia.
- Prompt bertanda PRO saat ini diberi label saja dan belum memiliki sistem entitlement/paywall sungguhan.
- Ini adalah starter yang dapat dikembangkan, bukan produk dengan backend pembayaran siap produksi.
