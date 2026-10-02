# KRIPTOGRAFI-KLASIK
# Tugas Praktikum Kriptografi Klasik

Repositori ini berisi program web sederhana berbasis HTML & JavaScript untuk mensimulasikan proses **enkripsi** dan **dekripsi** menggunakan **Caesar Cipher** dan **Vigenère Cipher**[cite: 1]. 

Proyek ini dibuat untuk memenuhi tugas mata kuliah Kriptografi / Keamanan Informasi, dan di-hosting lewat **GitHub Pages**[cite: 1].

---

## 🔗 Link Demo

Webnya bisa langsung dicoba di sini:  
👉 `https://USERNAME_KAMU.github.io/NAMA_REPO_KAMU/`

---

## 📌 Fitur Web

- Bisa pilih algoritma: **Caesar Cipher** atau **Vigenère Cipher**[cite: 1].
- Pilihan mode: **Enkripsi** dan **Dekripsi**[cite: 1].
- Spasi, huruf kapital, huruf kecil, dan tanda baca tetap dipertahankan sesuai input[cite: 1].
- Tanpa backend/install apa-apa, tinggal buka via browser karena murni pakai HTML & JS.

---

## 📐 Rumus yang Dipakai

1. **Caesar Cipher**  
   Pergeseran huruf sejauh $k$ posisi[cite: 1]:
   - Enkripsi: $C = (P + k) \pmod{26}$[cite: 1]
   - Dekripsi: $P = (C - k) \pmod{26}$[cite: 1]

2. **Vigenère Cipher**  
   Pergeseran berbasis kata kunci (keyword) $K_i$[cite: 1]:
   - Enkripsi: $C_i = (P_i + K_i) \pmod{26}$[cite: 1]
   - Dekripsi: $P_i = (C_i - K_i) \pmod{26}$[cite: 1]

---

## 📝 Jawaban Pertanyaan Analisis

1. **Beda proses enkripsi & dekripsi kedua algoritma:**
   - **Caesar Cipher:** Menggunakan nilai pergeseran kunci ($k$) yang sama/tetap untuk semua huruf[cite: 1].
   - **Vigenère Cipher:** Nilai pergeserannya beda-beda tiap huruf, tergantung urutan huruf dari kata kunci (*keyword*) yang dipakai[cite: 1].

2. **Pengaruh perubahan kunci ke ciphertext:**
   - Di **Caesar Cipher**, kalau kunci diubah, semua huruf di ciphertext cuma bergeser secara sejajar/linier[cite: 1].
   - Di **Vigenère Cipher**, kalau 1 huruf saja di keyword diganti, seluruh hasil ciphertext-nya bakal berubah total dan pola acaknya langsung beda[cite: 1].

3. **Kenapa Caesar Cipher gampang dipecahkan?**
   - Kuncinya cuma ada 25 kemungkinan (sesuai jumlah alfabet A–Z)[cite: 1]. Jadi sangat gampang ditebak pakai teknik *brute force* atau analisis frekuensi kemunculan huruf.

4. **Kelemahan utama kriptografi klasik:**
   - Ruang kuncinya terlalu kecil, jadi gampang dicari pakai komputer zaman sekarang.
   - Pola/karakteristik dari bahasa aslinya masih sering kelihatan di ciphertext, jadi mudah dianalisis oleh penyerang.

5. **Apakah pesan yang dienkripsi sudah aman dari perubahan (*tampering*)?**
   - **Belum.** Kriptografi klasik cuma buat nyembunyiin isi pesan (*confidentiality*), tapi gak punya fitur untuk ngecek apakah pesannya udah diubah di tengah jalan atau belum (*integrity*)[cite: 1]. Kalau ciphertext-nya diubah orang lain, penerima bakal tetap mendekripsinya tanpa tahu kalau datanya sudah dirusak.
