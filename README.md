# TaniKira: Rekod Kebun Petani Muda

TaniKira ialah aplikasi telefon (Progressive Web App) untuk petani muda sawah padi, kebun getah dan kelapa sawit. Petani merekod kos dan hasil, menyemak kesihatan pokok, mengurus stok baja dan racun, dan melihat untung bersih setiap bulan. Aplikasi boleh dipasang ke skrin utama telefon dan berfungsi tanpa internet selepas dibuka kali pertama.

Dibangunkan oleh **Ir. Ts. Dr. Muhammad Hafiz HASSAN**, Pusat Pengajian Kejuruteraan Mekanik, Universiti Sains Malaysia.

## Kandungan repositori

| Fail | Fungsi |
|---|---|
| `index.html` | Aplikasi penuh (antara muka, logik, data contoh) |
| `manifest.webmanifest` | Nama, ikon, warna dan pintasan aplikasi untuk dipasang di telefon |
| `sw.js` | Service worker supaya aplikasi dibuka tanpa internet |
| `icons/` | Ikon aplikasi (192, 512, maskable, Apple) |
| `assets/usm-apex.png` | Logo USM APEX |
| `.nojekyll` | Memastikan GitHub Pages menghidangkan fail apa adanya |

## Terbitkan di GitHub Pages

1. Log masuk ke akaun GitHub `mhh-ppkm` dan cipta repositori baharu bernama `tanikira` (Public).
2. Tekan **Add file > Upload files**, seret semua fail dan folder dalam pakej ini (termasuk `.nojekyll`), kemudian **Commit changes**.
3. Pergi ke **Settings > Pages**. Di bahagian *Build and deployment*, pilih **Deploy from a branch**, branch `main`, folder `/ (root)`, kemudian **Save**.
4. Selepas satu hingga dua minit, aplikasi tersedia di `https://mhh-ppkm.github.io/tanikira/`.

## Pasang di telefon petani

- **Android (Chrome):** buka pautan, tekan butang **Pasang** dalam aplikasi atau menu ⋮ > *Pasang aplikasi*.
- **iPhone (Safari):** buka pautan, tekan butang Kongsi > *Tambah ke Skrin Utama*.

Tekan lama ikon TaniKira di Android untuk pintasan terus ke *Catat kos*, *Catat hasil* dan *Semak pokok*. Pautan yang sama boleh dijadikan kod QR untuk diedarkan semasa taklimat Jabatan Pertanian.

## Di mana data disimpan

Rekod setiap petani disimpan dalam telefon petani itu sendiri dan tidak dihantar ke mana-mana pelayan. Petani boleh memuat turun rekod sebagai CSV dari tab **Lagi** untuk sandaran atau untuk ditunjukkan kepada pegawai. Jika aplikasi dipadam atau data pelayar dikosongkan, rekod turut hilang, jadi galakkan eksport CSV secara berkala.

Jawapan **Tinjauan keperluan petani** dihantar melalui emel kepada penyelaras projek (`mhafizhassan@usm.my`). Untuk menukar alamat, sunting baris `var CONFIG={emelTinjauan:"..."}` dalam `index.html`.

Panel pegawai (ringkasan tinjauan secara langsung) dan *Tanya pakar AI* hanya berfungsi dalam versi Claude artifact. Dalam versi GitHub, bahagian AI disembunyikan secara automatik.

## Mengemas kini aplikasi

Selepas menukar `index.html` atau fail lain, naikkan nombor `VERSION` dalam `sw.js` (contoh `tanikira-v1.0.1`). Telefon petani akan menerima versi baharu apabila aplikasi dibuka semasa ada internet.

## Hak cipta

© 2026 Universiti Sains Malaysia. Logo USM ialah tanda dagangan Universiti Sains Malaysia. Prototaip ini disediakan untuk pembentangan dan perintis bersama Jabatan Pertanian Malaysia; sebarang penggunaan komersial memerlukan kebenaran bertulis daripada pembangun dan universiti.
