# Tutorial Running Script Xreign Bot (Protected Version)

Panduan ini menjelaskan cara menjalankan server Xreign Bot yang sudah terenkripsi ketat (obfuscated) yang berada di dalam folder `dist/server/`.

---

## 🛠️ Persyaratan System
- **Node.js**: Versi `v20.6.0` ke atas (Sangat direkomendasikan versi **`v22.14.0`** yang sedang Anda gunakan saat ini).

---

## 📝 Langkah-Langkah Penyiapan & Running

### Langkah 1: Jalankan Server (Langsung Tanpa .env)

Karena kredensial Telegram Bot Anda sudah **tertanam langsung (baked) dan terenkripsi** di dalam script, Anda **tidak memerlukan file `.env` lagi** untuk menjalankannya.

Pilih salah satu cara berikut untuk menjalankan server:

#### Cara A: Menggunakan NPM Script (Direkomendasikan)
Jalankan perintah berikut di terminal pada folder root project:
```bash
npm start
```
*(Atau `node dist/server/index.js`)*

#### Cara B: Menggunakan Override Kredensial (Opsional)
Jika di kemudian hari Anda ingin mengganti token Telegram secara dinamis tanpa mengenkripsi ulang script, Anda bisa membuat file `.env` di folder root project berisi:
```env
TELEGRAM_TOKEN=token_baru_anda
TELEGRAM_CHAT_ID=chat_id_baru_anda
```
Lalu jalankan dengan:
```bash
npm run start:prod
```

---

## 🔁 Cara Memperbarui File Enkripsi (Jika Ada Perubahan Kode)
Jika Anda melakukan modifikasi pada kode asli di folder `server/` dan ingin mengenkripsi ulang kodenya ke folder `dist/server/`, jalankan perintah berikut di root project:

```bash
npm run obfuscate
```
Perintah ini akan secara otomatis mengenkripsi ulang seluruh file Javascript di dalam folder `server/` ke dalam folder `dist/server/` dengan tingkat keamanan tinggi.
