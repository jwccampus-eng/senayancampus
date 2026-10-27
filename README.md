# Lucky Draw – Doorprize

Aplikasi undian doorprize satu file (`index.html`) dengan check-in peserta lewat QR.

Alamat publik (GitHub Pages): https://jwccampus-eng.github.io/senayancampus/

## Cara kerja check-in QR

1. Penyelenggara membuka alamat di atas di laptop/komputer layar utama.
2. Buka **Settings → Check-in**. Tunggu status berubah menjadi **Ready**, lalu tekan **Show QR fullscreen**.
3. Peserta memindai QR dengan HP. Form berisi **nama lengkap** dan **email** (plus kolom tambahan jika Anda tambahkan) akan terbuka.
4. Setelah peserta menekan **Check in**, namanya langsung masuk ke daftar peserta undian.

Catatan:
- Halaman penyelenggara harus tetap terbuka dan online selama check-in berlangsung. Data dikirim langsung dari HP ke halaman penyelenggara (WebRTC lewat PeerJS), tidak disimpan di server.
- Daftar peserta tersimpan di browser penyelenggara. Gunakan **Export participants (CSV)** untuk cadangan.
- Email yang sama tidak bisa check-in dua kali. Anda bisa membatasi domain email (misalnya `.edu` atau `binus.ac.id`) di tab Check-in.
- Selalu buka aplikasi dari satu alamat yang sama selama acara. Daftar peserta tersimpan per alamat, jadi membuka dari alamat lain akan terlihat kosong.

## Mengaktifkan GitHub Pages

Repo → **Settings → Pages → Build and deployment** → Source: *Deploy from a branch* → Branch: `main` / `(root)` → **Save**. Tunggu 1–2 menit sampai alamat publik aktif.

### Memakai domain sendiri (opsional)

Atur record DNS di tempat Anda membeli domain: 4 record **A** untuk host `@` ke `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`, dan satu **CNAME** `www` ke `jwccampus-eng.github.io`. Tunggu DNS menyebar, lalu isi domainnya di **Settings → Pages → Custom domain** dan centang **Enforce HTTPS** setelah bisa dipilih. Sebaiknya pasang domain hanya setelah DNS siap, karena alamat `github.io` bisa ikut dialihkan ke domain itu dan tidak terbuka selama DNS belum jalan. Setelah domain aktif, ubah `DEFAULT_PUBLIC_URL` di `index.html` ke alamat barunya.
