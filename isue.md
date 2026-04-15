# Planning Aplikasi Backend

Dokumen ini berisi instruksi tingkat tinggi (high-level) untuk diimplementasikan oleh programmer junior dalam membangun aplikasi backend.

## Stack Teknologi
1. **Runtime**: Bun
2. **Framework Web**: ElysiaJS
3. **ORM**: Drizzle ORM
4. **Database**: MySQL

## Instruksi Implementasi

### 1. Persiapan Lingkungan & Dependensi
- Proyek dasar sudah diinisialisasi menggunakan Bun.
- Instal dependensi yang dibutuhkan:
  - Framework: `elysia`
  - Database & ORM: `drizzle-orm`, `mysql2`
  - Development tools: `drizzle-kit`

### 2. Konfigurasi Database (Drizzle & MySQL)
- Siapkan koneksi *connection pool* ke database MySQL.
- Buat file skema Drizzle (contoh: skema `users` dengan field id, name, email).
- Atur konfigurasi `drizzle.config.ts` untuk keperluan generate dan push migrasi.
- Lakukan migrasi skema ke database.

### 3. Pembuatan Server API (ElysiaJS)
- Siapkan entry point server (misalnya `src/index.ts`).
- Inisialisasi aplikasi ElysiaJS.
- Buat *endpoint* untuk *health check* dasar (`GET /` atau `GET /ping`).

### 4. Integrasi API dengan Database
- Kembangkan *endpoints* CRUD (Create, Read, Update, Delete) sederhana untuk skema yang sudah dibuat.
- Gunakan instance Drizzle ORM di dalam handler Elysia untuk berinteraksi dengan database MySQL.
- Jalankan dan uji endpoints menggunakan REST client.
