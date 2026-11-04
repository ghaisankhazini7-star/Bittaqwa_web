BITTAQWA — IPHONE 16 NETLIFY PREVIEW

Isi paket:
- index.html       : halaman pembungkus dengan frame iPhone 16
- app/             : hasil build Flutter Web asli dari file yang kamu kirim

Cara deploy ke Netlify Drop:
1. Ekstrak ZIP ini.
2. Buka folder hasil ekstrak yang berisi index.html dan folder app.
3. Drag folder tersebut ke https://app.netlify.com/drop
4. Buka URL Netlify hasil deployment.

Catatan:
- Jangan upload folder app saja; upload folder paling luar yang berisi index.html dan app/.
- Aplikasi Flutter internal tidak diubah. Hanya base href pada app/index.html disesuaikan ke /app/ agar file asset dapat dimuat dari subfolder.
- Frame iPhone adalah mockup responsif di halaman luar. Aplikasi berjalan di dalam iframe.
