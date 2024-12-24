# Implementasi Chatbot Mahasiswa Baru UNIB

## Deskripsi Proyek
Proyek ini bertujuan untuk membangun chatbot berbasis deep learning yang akan membantu mahasiswa baru Universitas Bengkulu (UNIB) mendapatkan informasi terkait kampus dengan lebih efisien dan cepat. Chatbot ini dapat menjawab berbagai pertanyaan terkait registrasi, jadwal kuliah, lokasi gedung, prosedur administrasi, dan informasi umum lainnya di kampus UNIB.

Proyek ini dibuat untuk memenuhi tugas **Ujian Akhir Semester (UAS)** dalam mata kuliah **Deep Learning**.

## Anggota Kelompok
- **Yulia Pratiwi** – G1A021029
- **Zabrila Amrina Zadia Putri** – G1A021053
---
### 1. **Business Understanding**
- **Tujuan:**
  - Membuat chatbot yang dapat menjawab berbagai pertanyaan mahasiswa baru terkait kampus, seperti jadwal, lokasi gedung, prosedur administrasi, dan lain-lain.
- **Manfaat:**
  - Mengurangi beban layanan informasi manual.
  - Menyediakan akses informasi 24/7 untuk mahasiswa baru.

---

### 2. **Data Understanding**
- **Dataset:**
  - Dataset berbentuk JSON yang dikumpulkan melalui informasi pada laman unib.ac.id
- **Fitur Utama Dataset:**
  - **Patterns:** Kalimat input dari pengguna.
  - **Tags:** Label kategori intent.
  - **Responses:** Jawaban chatbot untuk setiap intent.

---

### 3. **Data Preparation**

#### **Teknik Pemrosesan Data:**
1. **Pembersihan Data:** Menghapus tanda baca dan karakter khusus dari teks.
2. **Lematisasi:** Mengubah kata menjadi bentuk dasar untuk konsistensi.
3. **Tokenisasi & Padding:**
   - Memecah kalimat menjadi token.
   - Menggunakan padding agar setiap input memiliki panjang yang sama.
4. **Encoding:**
   - Mengonversi label teks menjadi format numerik untuk diproses oleh model deep learning.

---

### 4. **Modeling**

#### **Arsitektur Model:**
- **Embedding Layer:** Untuk merepresentasikan kata sebagai vektor numerik.
- **Bidirectional LSTM & GRU:**
  - Digunakan untuk menangkap konteks sekuensial dari teks input.
- **Dense Layer:**
  - Mengklasifikasikan intent ke dalam kategori output.

#### **Parameter Model:**
- Optimizer: Adam.
- Loss Function: Sparse Categorical Crossentropy.
- Dropout: 0.5 (untuk mencegah overfitting).

#### **Hasil :**
- **Akurasi Pelatihan:** 97.3% setelah 200 epoch.
- **Grafik Pelatihan:**
  - **Loss:** Menurun konsisten selama pelatihan.
  - **Akurasi:** Meningkat stabil hingga mendekati 1.
![grafik](https://github.com/user-attachments/assets/cec2aa36-860a-425c-b320-e89090a66dcd)
---

### 5. **Evaluation**

#### **Kelebihan Model:**
- Mampu mengklasifikasikan intent pengguna dengan akurasi tinggi.
- Menangkap konteks teks input dengan baik menggunakan LSTM dan GRU.

#### **Kekurangan Model:**
- Masih membutuhkan pengujian pada data real-world untuk memastikan kemampuan generalisasi.
- Belum dilakukan evaluasi mendalam menggunakan metrik seperti precision, recall, dan F1-score.

---
### 5. **Pengujian**

## Hasil Pengujian Model
![Screenshot 2024-12-24 221949](https://github.com/user-attachments/assets/846072f1-3ee7-4005-927a-07c8b98ae07d)
![Screenshot 2024-12-24 222008](https://github.com/user-attachments/assets/7a84d672-e069-4f85-b0cb-35d6a3cf66bc)
![Screenshot 2024-12-24 222023](https://github.com/user-attachments/assets/15e4b3cd-d3b5-44e3-8e01-f21bd4ac27d4)

