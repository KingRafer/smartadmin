# SMARTAI Admin Panel

Panel admin Smart AI — kelola member, akun trading, komisi, referral, dan activity log.

## Akses demo

Halaman login (`index.html`) sudah **terisi otomatis** dengan akun demo:

- Email: `admin@smartai.id`
- Password: `admin123`

Untuk mengganti akun demo, edit `DEMO_ADMIN` di `js/auth-admin.js`.

## Struktur project

```
index.html            <- login
dashboard.html · members.html · accounts.html
commissions.html · referrals.html · activity.html · settings.html

css/
  admin.css           <- style semua halaman dashboard
  login.css           <- style halaman login
js/
  theme-init.js       <- terapkan tema sebelum render
  guard.js            <- redirect ke login jika belum masuk
  icons.js            <- pustaka ikon SVG (pakai <i data-icon="nama">)
  auth-admin.js       <- login / logout / session
  admin.js            <- core: data, toast, modal, sidebar
  pages/              <- satu file JS per halaman
```

HTML hanya berisi markup, CSS hanya di `css/`, JS hanya di `js/` (tanpa `<style>` / `<script>` inline).

## Deploy

Import ke Vercel (static site, tanpa build).
