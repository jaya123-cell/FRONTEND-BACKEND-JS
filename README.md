# Todo App Backend

Backend REST API sesuai Tugas #4: Express.js, TypeScript, MySQL, JWT, dan middleware.

## Persiapan
1. Pastikan Node.js sudah terpasang.
2. Jalankan layanan MySQL lokal (XAMPP, Laragon, atau MariaDB).
3. Buka database manager/phpMyAdmin, pilih tab SQL, lalu jalankan isi `database/schema.sql`.
4. Salin `.env.example` menjadi `.env`, lalu sesuaikan kredensial database.
5. Buka terminal di folder backend dan jalankan `npm install`.
6. Jalankan server dengan `npm run dev`.

Server: `http://localhost:5000`

## Endpoint
- `POST /api/auth/register` — JSON: `{"nama":"Nama Anda","email":"anda@example.com","password":"rahasia123"}`
- `POST /api/auth/login` — JSON: `{"email":"anda@example.com","password":"rahasia123"}`
- `POST /api/todos` — Bearer token; JSON: `{"task":"Belajar Express"}`
- `GET /api/todos` — Bearer token

Untuk endpoint todos, masukkan token login pada header:
`Authorization: Bearer TOKEN_ANDA`

## Catatan
- Modul menyebut kolom pengguna `nama`; validator juga menerima field `username` sebagai alternatif pada proses register.
- Jangan mengunggah file `.env` ke GitHub. File tersebut sudah dimasukkan ke `.gitignore`.
- Gunakan `http://localhost` (bukan https) untuk pengujian lokal.
