# Catatan Keuangan (aplikasi Android)

Aplikasi pencatatan keuangan yang dipasang di layar utama HP seperti aplikasi biasa. Data tersimpan di HP, struk dan voice note dibaca otomatis lewat API key Anthropic milik Anda.

## Memasang di HP Android

Aplikasi ini perlu "ditaruh" di alamat web (HTTPS) satu kali, lalu dipasang dari Chrome. Cara termudah tanpa menulis kode:

1. Ekstrak `catatan-keuangan-app.zip` di laptop sampai menjadi satu folder.
2. Buka <https://app.netlify.com/drop> di laptop, lalu seret folder tadi ke halaman itu. Buat akun gratis jika diminta, supaya alamatnya tidak hilang.
   (Alternatif: GitHub Pages atau Cloudflare Pages, caranya sama: unggah isi folder.)
3. Salin alamat yang muncul (misalnya `https://nama-acak.netlify.app`).
4. Di HP, buka alamat itu di **Chrome**.
5. Ketuk menu **⋮** → **Pasang aplikasi** (atau **Tambahkan ke layar utama**). Ikon "Keuangan" muncul di layar utama.

Setelah terpasang, aplikasi terbuka layar penuh dan tetap bisa dibuka tanpa internet (baca otomatis butuh internet).

## Pengaturan pertama kali
1. Buka aplikasi → tab **Pengaturan**.
2. Buat API key di <https://console.anthropic.com> (menu API Keys), isi saldo kecil, dan pasang batas pengeluaran bulanan di sana.
3. Tempel key di kolom **API key Anthropic** → **Simpan** → **Tes koneksi**. Harus muncul "Tersambung".

## Memakai
- **Foto struk:** tab Tambah → Foto struk → ambil foto → periksa hasil → Simpan.
- **Voice note:** tab Tambah → Voice note → **Rekam suara** (izinkan mikrofon) lalu bicara, atau pakai ikon mikrofon di keyboard → **Baca transaksi** → periksa → Simpan.
- **Manual:** tab Tambah → Manual.
- **Ringkasan:** saldo total, pemasukan, pengeluaran, selisih, pengeluaran per kategori, grafik 6 bulan, tabel bulanan.
- **Riwayat:** cari, ubah, hapus. Tombol **Unduh CSV** menghasilkan file yang bisa dibuka di Excel atau Google Sheets.

## Data dan keamanan
- Catatan disimpan di penyimpanan browser HP ini. **Menghapus data Chrome atau mencopot aplikasi menghapus catatan.** Unduh cadangan di tab Pengaturan secara berkala. Cadangan bisa dipulihkan di HP yang sama atau HP baru.
- API key disimpan hanya di HP ini dan dikirim hanya ke Anthropic. Jangan pasang di HP bersama, dan pasang batas pengeluaran di console.anthropic.com.
- Foto struk dikirim ke Anthropic hanya saat dibaca otomatis, dan tidak disimpan oleh aplikasi (yang tersimpan hanya hasil teksnya).

## Mengubah jadi file APK (opsional)
Setelah alamat web aktif, buka <https://www.pwabuilder.com>, masukkan alamatnya, lalu pilih paket Android. Hasilnya file APK yang bisa dipasang manual atau diunggah ke Play Store.
