# PaDyViR - Particle Dynamics Virtual Reality

## Tentang Aplikasi

PaDyViR adalah aplikasi Virtual Reality (VR) dan Augmented Reality (AR) yang dirancang untuk simulasi dinamika partikel dan pembelajaran fisika dalam lingkungan virtual. Aplikasi ini memungkinkan pengguna untuk berinteraksi dengan simulasi fisika secara real-time dalam ruang virtual yang dapat diakses secara multiplayer.

### Fitur Utama

- **Simulasi Fisika**: Berbagai scene untuk pembelajaran dinamika partikel dan konsep fisika lainnya
- **Multiplayer**: Berinteraksi dengan pengguna lain dalam ruang virtual yang sama
- **Avatar Realistis**: Menggunakan avatar 3D yang dapat dianimasi
- **Chat & Komunikasi**: Fitur chat dan video sharing untuk kolaborasi
- **Voting System**: Sistem voting untuk sesi diskusi dan pengambilan keputusan
- **Portal Teleportasi**: Berpindah antar scene menggunakan portal
- **VR Mode**: Dukungan penuh untuk perangkat VR headset

## Cara Penggunaan

### Prasyarat

- Node.js versi 16 atau lebih tinggi
- NPM (Node Package Manager)

### Instalasi

1. Clone atau download repository ini
2. Buka terminal/command prompt di folder project
3. Install dependencies dengan menjalankan:
```bash
npm install
```

### Menjalankan Aplikasi

#### Mode Development
Untuk menjalankan aplikasi dalam mode development:
```bash
npm run dev
```

#### Mode Production
Untuk menjalankan aplikasi dalam mode production:
```bash
npm run build
npm start
```

#### Mode Development dengan Webpack Dev Server
Alternatif lain untuk development:
```bash
npm run dev2
```

### Mengakses Aplikasi

Setelah server berjalan, buka browser dan akses:
- **URL utama**: `http://localhost:8080`
- **Halaman utama**: `http://localhost:8080/public/index.html`
- **Scene 1**: `http://localhost:8080/public/scene1.html`
- **Scene 2**: `http://localhost:8080/public/scene2.html`
- **VR Mode**: `http://localhost:8080/public/vr.html`
- **Voting Session**: `http://localhost:8080/public/vote.html`

### Catatan Penting

- Pastikan port 8080 tidak digunakan oleh aplikasi lain
- Untuk akses dari perangkat lain dalam jaringan yang sama, gunakan IP address server (contoh: `http://192.168.1.15:8080`)
- Untuk mode VR, pastikan browser mendukung WebXR
- Gunakan headset VR untuk pengalaman yang optimal

## Tim Developer

- **Sugeng Margono**
- **Muhammad Abdillah Thoha**
- **Kalisna Joharestama**
- **Annaufal Fadhil Musyafa**
- **Maheswara Rizal Hafidz**

---

## Teknologi yang Digunakan

- **A-Frame**: Framework untuk membuat pengalaman VR/AR berbasis web
- **Networked-AFrame**: Library untuk multiplayer VR
- **SolidJS**: Framework JavaScript untuk UI
- **Express.js**: Web server framework
- **Socket.IO**: Real-time communication
- **EasyRTC**: WebRTC untuk komunikasi video/audio
- **Three.js**: 3D graphics library

## Lisensi

MIT License
