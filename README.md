# 📜 Dataset Putusan Pengadilan: Kasus Narkotika & Psikotropika (2023)

Selamat datang di repositori yang penuh dengan wawasan tentang **putusan pengadilan** dalam kasus **Narkotika dan Psikotropika** di **Pengadilan Negeri Kendari**! 🎉

Dataset ini bukan hanya sekadar kumpulan data hukum, tetapi sebuah jendela untuk memahami lebih dalam mengenai **perjalanan hukum** dan **pertimbangan peradilan** dalam menangani kasus narkotika dan psikotropika. Mari kita jelajahi bersama data yang telah diproses dan siap untuk dianalisis!

## 🔍 Apa itu Dataset Ini?

**50 putusan pengadilan** yang diambil langsung dari **Direktori Putusan Mahkamah Agung RI** diambil dari kategori **PIDANA KHUSUS** dan klasifikasi **NARKOTIKA DAN PSIKOTROPIKA** yang berasal dari **PENGADILAN NEGERI KENDARI** pada tahun **2023**. 

Tujuan dari dataset ini adalah untuk memberikan gambaran mengenai bagaimana sistem peradilan Indonesia menangani kasus narkotika, serta memberikan data yang berguna untuk analisis **tekstual**, **pencarian dokumen terkait**, dan **pengindeksan** dokumen hukum.

### Fitur Dataset

Dataset ini terdiri dari **empat kolom utama** yang sangat relevan untuk analisis lebih lanjut:

| **No**  | **Fitur**            | **Deskripsi**                                                                                             |
|---------|----------------------|-----------------------------------------------------------------------------------------------------------|
| 1       | **No Putusan**        | Nomor identifikasi putusan pengadilan yang unik.                                                         |
| 2       | **Lembaga Peradilan** | Nama lembaga peradilan yang mengeluarkan putusan, yaitu Pengadilan Negeri Kendari.                        |
| 3       | **Barang Bukti**      | Deskripsi tentang barang bukti yang ditemukan dalam perkara yang diadili, baik narkotika maupun psikotropika. |
| 4       | **Amar Putusan**      | Ringkasan keputusan atau amar putusan yang dijatuhkan oleh pengadilan, termasuk hukuman yang diberikan.    |

### **Contoh Baris Dataset**

| No Putusan | Lembaga Peradilan        | Barang Bukti                   | Amar Putusan                                  |
|------------|--------------------------|---------------------------------|-----------------------------------------------|
| 108/Pid.Sus/2023/PN Kdi        | Pengadilan Negeri Kendari | Menetapkan barang bukti berupa: 5 (lima) paket Narkotika jenis Shabu dengan berat netto 0,3258 gram. 1 (satu) klik sachet kosong, 9 (sembilan) sachet kosong 1 (satu) timbangan digital, 1 (satu) alat press, 1 (satu) kaleng rokok Gudang Garam, 1 (satu) sendok Shabu dari pipet, 1 (satu) sendok plasti warna putih, 1 (satu) korek api gas, 1 (satu) buah bong dengan pireks kaca, 1 (satu) kotak putih, 4 (empat) potongan kertas, 1 (satu) unit handphone dengan no sim card 082349531336. Dirampas untuk dimusnahkan. Membebankan kepada terdakwa untuk membayar biaya perkara sejumlah Rp. 5.000,- (lima ribu rupiah) ;           | - Menyatakan Terdakwa SARDIN EKO PUTRA Bin SAINUDDIN, telah terbukti secara sah dan meyakinkan bersalah melakukan tindak pidana ?Tanpa Hak Menguasai Narkotika Golongan I Bukan Tanaman? sebagaimana dakwaan Jaksa Penuntut Umum pada dakwaan alternatif kedua;                   |                     |
| ...        | ...                      | ...                             | ...                                           |

## 🧠 Tujuan & Aplikasi

Data ini bukan hanya untuk sekadar melihat kasus hukum, tetapi juga untuk digunakan dalam berbagai aplikasi analisis teks, seperti:

- **Analisis Teks Hukum**: Memahami pola keputusan pengadilan pada kasus narkotika dan psikotropika.
- **Pencarian Dokumen Terkait**: Mencari putusan yang relevan dengan menggunakan **cosine similarity** dan **TF-IDF** untuk menemukan putusan serupa.
- **Pengindeksan Dokumen**: Menggunakan teknik **Information Retrieval** untuk mengorganisir dan mempermudah pencarian dokumen hukum di masa depan.

## 🔧 Proses Data

Kamu tidak hanya akan melihat data mentah, tetapi juga proses yang telah kami lakukan untuk mempersiapkan data ini agar siap digunakan:

1. **Preprocessing Teks**: 
   - Menghilangkan stop words dan tanda baca.
   - Melakukan **stemming** dengan bantuan **Sastrawi** untuk Bahasa Indonesia.
   - Mengubah teks ke dalam bentuk yang lebih sederhana agar mudah dianalisis.

2. **Vektorisasi dengan TF-IDF**:
   - Teks dalam kolom **Amar Putusan** diubah menjadi **vektor numerik** dengan menggunakan **TF-IDF** (Term Frequency-Inverse Document Frequency).
   - Ini membantu untuk melihat bobot kata-kata yang paling relevan di seluruh dataset.

3. **Pencarian Dokumen Terkait**:
   - Menggunakan **Cosine Similarity** untuk mencari putusan yang paling mirip dengan dokumen yang diberikan.
   - Membantu dalam menemukan keputusan hukum yang relevan berdasarkan kesamaan isi Amar Putusan.

# Pencarian Dokumen Terkait Berdasarkan Cosine Similarity pada Putusan Pengadilan

Proyek ini bertujuan untuk membantu dalam mencari dokumen terkait berdasarkan **Amar Putusan** dalam dataset putusan pengadilan menggunakan metode **Cosine Similarity** dan **TF-IDF** (Term Frequency - Inverse Document Frequency). Ini sangat berguna dalam menganalisis tren keputusan hukum dan menemukan kasus serupa yang relevan untuk penelitian lebih lanjut.

## Hasil Pencarian Dokumen Terkait

Berdasarkan **cosine similarity**, kamu dapat menemukan dokumen yang paling mirip dengan dokumen yang dipilih. Hasil pencarian ini sangat berguna untuk:

- Memahami lebih dalam tentang tren atau pola dalam keputusan hukum.
- Menemukan kasus serupa yang mungkin relevan dalam penelitian lebih lanjut.
- Mengidentifikasi hubungan antara putusan-putusan terkait dengan klasifikasi **Narkotika dan Psikotropika**.

Hasil pencarian dokumen terkait ini dapat disimpan dalam file CSV yang berbeda:

- **dokumen_terkait.csv**: Berisi putusan yang paling relevan beserta skor similarity.
- **dataset_preprocessed.csv**: Menyimpan dataset yang telah diproses dengan teks yang telah dibersihkan.
- **dokumen_indices_scores.csv**: Menyimpan indeks dan skor similarity dari pencarian dokumen terkait.

## 🛠️ Instalasi

Untuk menjalankan kode ini, pastikan kamu menginstal semua dependensi yang dibutuhkan:

```bash
pip install pandas nltk scikit-learn Sastrawi


## 🚀 Contoh Kode

Berikut adalah contoh langkah-langkah yang digunakan dalam kode untuk memproses dan mencari dokumen terkait:

```python
# Memuat dataset dari URL
df = pd.read_excel(url)

# Preprocessing teks
df['processed_text'] = df['Amar Putusan'].apply(preprocess_text)

# Vektorisasi teks dengan TF-IDF
tfidf_matrix = vectorizer.fit_transform(df['processed_text'])

# Menyimpan hasil TF-IDF
tfidf_df.to_csv('tfidf_indexed_dataset.csv', index=False)

# Pencarian dokumen terkait menggunakan cosine similarity
related_docs, similarity_scores = get_related_documents(doc_index, tfidf_matrix, top_n=10)

