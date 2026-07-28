# NeonEQ Player — Music Player dengan Equalizer 3D Knobs

Website pemutar musik modern dengan:

- **Playlist** didefinisikan di file JavaScript (`player.js`)
- **Equalizer lengkap 10-band** (31 Hz – 16 kHz)
- **Knob 3D interaktif** (putar dengan mouse / touch)
- **Visualizer spektrum sirkular**
- **Support upload file lokal** + drag & drop
- **Shuffle** (acak urutan lagu)
- **Repeat**: Off → Repeat All → Repeat One
- **Preset EQ**: Flat, Bass Boost, Treble, Vocal, Rock

## Cara Pakai

1. Buka `index.html` di browser modern (Chrome / Edge / Firefox).
2. Klik **＋ Tambah Lagu** atau **drag & drop** file MP3 / WAV / OGG ke halaman.
3. Putar lagu, atur equalizer dengan memutar knob 3D.
4. Double-click knob untuk reset ke default.

## Menambah Track Permanen di JavaScript

Buka file `player.js`, cari bagian:

```js
const TRACKS = [
  {
    title: "Judul Lagu",
    artist: "Nama Artist",
    src: "path/ke/file.mp3",   // path relatif atau URL
    isDemo: false
  },
  // tambahkan lagi...
];
```

Jika `src` diisi path file lokal, letakkan file audio di folder yang sama dengan `index.html` (atau sesuaikan path-nya).

## Fitur Knob 3D

- Putar atas/bawah untuk mengubah nilai
- Range EQ: **-12 dB** sampai **+12 dB**
- Volume: 0 – 100%
- Double-click = reset

## Catatan

- Equalizer menggunakan **Web Audio API** (BiquadFilter peaking).
- Visualizer real-time dari AnalyserNode.
- Untuk file dari URL eksternal, pastikan server mengizinkan CORS.
- Demo tone otomatis muncul jika belum ada file audio yang di-upload.

Selamat menikmati! 🎧
