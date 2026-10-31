# WiraLib Assistant + Gemini (Vercel)

1. Upload semua file beserta folder `api/` ke root repository GitHub yang tersambung ke Vercel. `index.html` dan `Code.gs` dari versi ini sudah disertakan; `Code.gs` hanya untuk Google Apps Script, JANGAN upload ke Vercel (file bisa tetap disimpan lokal).
2. Buat API key di https://aistudio.google.com/apikey. Pastikan project memiliki akses model gratis yang dipilih.
3. Di Vercel, buka Project → Settings → Environment Variables. Tambahkan `GEMINI_API_KEY` (value = kunci rahasia), dan opsional `GEMINI_MODEL` = `gemini-3.5-flash-lite`. Jangan taruh API key di `index.html` atau GitHub.
4. Redeploy production di Vercel. Klik chatbot dan uji pertanyaan baru. Jika Gemini mengalami error atau kuota habis, chatbot otomatis menggunakan FAQ berbasis kata kunci.
5. Pengumpulan rating akhir chat dan Apps Script/Google Sheets tetap seperti sebelumnya; uji langsung apakah satu kunjungan dan rating masuk spreadsheet.

**Perhatian:** Paket ini adalah prototipe. Endpoint `/api/chat` terbuka untuk publik; tambahkan rate limiting/bot protection sebelum penyebaran luas untuk mencegah penyalahgunaan kuota. Pertanyaan mahasiswa dikirim ke Gemini, jadi perbarui pemberitahuan privasi dan jangan mengumpulkan data sensitif. Free tier punya batas kuota dan ketentuan penggunaan data. Teks FAQ dari versi WiraLib terakhir dijadikan basis model, perlu diverifikasi dengan kebijakan sebenarnya. Model Gemini bisa tetap menghasilkan kesalahan, tinjau sebelum digunakan secara resmi.
