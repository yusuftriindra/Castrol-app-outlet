# Castrol - GitHub Pages + Google Apps Script

## File
- `index.html` = frontend GitHub Pages
- `Code.gs` = backend Apps Script
- `ApiBridge.html` = bridge Apps Script

## URL backend
https://script.google.com/macros/s/AKfycbwZHD6DhhUjweqk8CgIrj81hMQOZOp2glKfa0C8hkpOsMdxwT8X8EDSTkcTUiY6oOzZ/exec

## Deploy Apps Script
1. Buka project Apps Script yang terhubung ke Google Sheet Castrol.
2. Pertahankan `Index.html` lama di project jika masih dipakai oleh `doGet()` normal.
3. Tambahkan file HTML baru bernama **ApiBridge.html**, lalu paste isi file yang disediakan.
4. Ganti `Code.gs` dengan versi di paket ini.
5. Deploy > Manage deployments > Web app > **New version / Edit deployment** lalu deploy ulang pada deployment yang sama.
6. Pastikan akses Web App sesuai kebutuhan aplikasi (umumnya Anyone).
7. Gunakan URL Web App yang sudah tertanam di `index.html`.

## GitHub Pages
Upload `index.html` ke repository. Aktifkan GitHub Pages dari branch/folder yang digunakan.

## Catatan login
Bridge memakai antrian + handshake `ready`, sehingga klik Masuk sebelum iframe Apps Script selesai dimuat tidak lagi kehilangan request. Login tetap memakai CUST.CODE tanpa password.
