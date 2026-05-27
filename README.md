# 📷 Agoy.net QR Code Scanner

> QR Code scanner berbasis web untuk login hotspot MikroTik — ringan, cepat, dan bisa langsung diakses dari browser HP.

![GitHub deployments]([https://img.shields.io/github/deployments/yogaariyanto312/QR-SCANER-VOCERAN/github-pages?label=GitHub%20Pages&style=flat-square](https://yogaariyanto312.github.io/QR-SCANER-VOCERAN/))
![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

---

## ✨ Fitur

- 📸 Scan QR Code langsung dari kamera HP
- 🎨 Tampilan modern dengan dark UI + glassmorphism
- ⚡ Ringan — tidak butuh instalasi, cukup buka di browser
- 📱 Responsive, optimal di perangkat mobile
- 🔍 Animated scan line untuk pengalaman scanning lebih intuitif

---

## 🚀 Demo

🔗 **Live:** [https://yogaariyanto312.github.io/QR-SCANER-VOCERAN](https://yogaariyanto312.github.io/QR-SCANER-VOCERAN)

> ⚠️ Kamera hanya bisa aktif jika halaman dibuka lewat **HTTPS**. GitHub Pages sudah mendukung HTTPS secara otomatis.

---

## 🛠️ Cara Pakai di MikroTik Hotspot

### 1. Tambahkan tombol di `login.html`

```html
<button onclick="window.location='https://yogaariyanto312.github.io/QR-SCANER-VOCERAN';">
  Scan QR Code
</button>
```

### 2. Whitelist domain di MikroTik (via Terminal)

```
/ip hotspot walled-garden ip
add action=accept comment="QR Code Scanner" disabled=no dst-host=yogaariyanto312.github.io
```

### 3. Generate QR Code untuk voucher

Buat QR Code dari URL voucher hotspot kamu, lalu pelanggan tinggal scan untuk login otomatis.

---

## 📁 Struktur Proyek

```
QR-SCANER-VOCERAN/
├── index.html          # Halaman utama scanner
├── llqrcode.js         # Library decode QR Code
├── mikhmon_webqr.js    # Logic kamera & scanning
├── arc-sw.js           # Service worker
├── font/               # Icon font (fontello)
└── README.md
```

---

## 🧰 Tech Stack

| Teknologi | Kegunaan |
|-----------|----------|
| HTML5 + CSS3 | Tampilan & animasi UI |
| JavaScript | Logic kamera & QR scanning |
| WebRTC `getUserMedia` | Akses kamera browser |
| [webqr.com](http://www.webqr.com) | Engine decode QR |

---

## 📋 Persyaratan Browser

- ✅ Chrome / Chromium (Android & Desktop)
- ✅ Firefox
- ✅ Safari (iOS 11+)
- ❌ Tidak support HTTP (harus HTTPS)

---

## 📄 Lisensi

Proyek ini menggunakan lisensi **MIT**. Silakan digunakan dan dimodifikasi sesuai kebutuhan.

---

<p align="center">Made with ❤️ by <a href="https://github.com/yogaariyanto312">yogaariyanto312</a> &nbsp;|&nbsp; Powered by <a href="http://www.webqr.com">webqr.com</a></p>
