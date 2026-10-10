# Ervan Projek — siap deploy ke Vercel

## Deploy cepat
1. Ekstrak ZIP ini.
2. Unggah isi folder ke repository GitHub baru, misalnya `ervan-projek`.
3. Di Vercel pilih **Add New → Project**, impor repository tersebut.
4. Framework akan terdeteksi sebagai **Vite**. Gunakan:
   - Build Command: `npm run build`
   - Output Directory: `dist`
   - Install Command: `npm install`
5. Klik **Deploy**.

Tidak memerlukan environment variable untuk build awal.

## Jalankan di komputer
```bash
npm install
npm run dev
```

## Catatan penting sebelum dipakai publik
- Kode sumber awal memiliki kata sandi admin yang ditanam langsung di browser. Itu bukan keamanan sungguhan; pengguna dapat melihatnya dari kode hasil build. Ganti dengan autentikasi server-side sebelum memakai fitur admin untuk mengubah data penting.
- Edit katalog pada versi ini hanya mengubah state di browser selama halaman terbuka; data belum tersimpan permanen ke database.
- Harga dan angsuran berasal dari data hardcoded di file sumber. Verifikasi semua angka sebelum dipublikasikan.
- Tailwind CSS dimuat melalui CDN agar proyek sumber ini sederhana. Untuk produksi skala besar, sebaiknya pasang Tailwind sebagai dependency build.
