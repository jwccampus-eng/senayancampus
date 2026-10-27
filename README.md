# Lucky Draw – Doorprize

Aplikasi undian doorprize satu file (`index.html`) dengan check-in peserta lewat QR.

Alamat publik (GitHub Pages dengan domain sendiri): https://jwcfx.io/

## Cara kerja check-in QR

1. Penyelenggara membuka alamat di atas di laptop/komputer layar utama.
2. Buka **Settings → Check-in**. Tunggu status berubah menjadi **Ready**, lalu tekan **Show QR fullscreen**.
3. Peserta memindai QR dengan HP. Form berisi **nama lengkap** dan **email** (plus kolom tambahan jika Anda tambahkan) akan terbuka.
4. Setelah peserta menekan **Check in**, namanya langsung masuk ke daftar peserta undian.

Catatan:
- Halaman penyelenggara harus tetap terbuka dan online selama check-in berlangsung. Data dikirim langsung dari HP ke halaman penyelenggara (WebRTC lewat PeerJS), tidak disimpan di server.
- Daftar peserta tersimpan di browser penyelenggara. Gunakan **Export participants (CSV)** untuk cadangan.
- Email yang sama tidak bisa check-in dua kali. Anda bisa membatasi domain email (misalnya `.edu` atau `binus.ac.id`) di tab Check-in.
- Selalu buka aplikasi dari satu alamat yang sama selama acara (`https://jwcfx.io/`). Daftar peserta tersimpan per alamat, jadi membuka dari alamat lain akan terlihat kosong.

## Mengaktifkan GitHub Pages

Repo → **Settings → Pages → Build and deployment** → Source: *Deploy from a branch* → Branch: `main` / `(root)` → **Save**. Tunggu 1–2 menit sampai alamat publik aktif.

Domain sendiri diatur di **Settings → Pages → Custom domain** (file `CNAME` dibuat otomatis oleh GitHub, jangan dihapus). Setelah pengecekan DNS selesai, centang **Enforce HTTPS** supaya HP membuka situs lewat `https://`.
