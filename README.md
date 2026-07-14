# Lexicon-Based Sentiment Analysis on Indonesian Social Media Comments with Advanced Text Preprocessing

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/USERNAME/NAMA_REPOSITORI/blob/main/notebooks/sentiment_analysis_lexicon.ipynb)

## 📌 Project Overview
Lembaga riset dan inovasi sering kali membutuhkan analisis sentimen publik untuk memahami tren atau respons masyarakat. Proyek ini berfokus pada **implementasi analisis sentimen berbasis leksikon (*Lexicon-Based Approach*)** pada data komentar media sosial berbahasa Indonesia. 

Tantangan utama dari data media sosial adalah tingginya penggunaan bahasa non-formal (*slang*), singkatan, dan emoji. Proyek ini menyelesaikan tantangan tersebut dengan mengintegrasikan penanganan emoji ke dalam pipa pra-pemrosesan teks (*text preprocessing pipeline*) serta memperluas korpus *stopword* agar sesuai dengan konteks percakapan digital di Indonesia.

## 🛠️ Key Features & Methodology
1. **Advanced Text Preprocessing Pipeline:**
   * **Emoji-to-Sentiment Tokenization:** Mengonversi emoji positif dan negatif menjadi token khusus (`EMO_POS` / `EMO_NEG`) sebelum proses *cleaning* untuk mempertahankan konteks emosi tekstual.
   * **Custom Stopword Removal:** Menggabungkan *stopword* standar (NLTK & Sastrawi) dengan korpus kata *slang* media sosial Indonesia yang disesuaikan secara manual (seperti: *yg, gak, aja, bgt, wkwk*).
   * **Bilingual Stemming & Lemmatization:** Menggunakan `PySastrawi` untuk *stemming* bahasa Indonesia dan `WordNetLemmatizer` untuk kata serapan bahasa Inggris.
2. **Enhanced Lexicon-Based Labeling:**
   * Pembobotan ekstra untuk token emoji (+2).
   * Aturan penanganan khusus (*default fallback*) untuk komentar pendek ($\le$ 3 kata) guna meminimalkan ambiguitas klasifikasi pada teks media sosial.
3. **Rich Data Export:** Integrasi dengan `openpyxl` untuk menghasilkan laporan *spreadsheet* (.xlsx) dengan visualisasi berbasis warna otomatis (*conditional styling*) untuk efisiensi interpretasi data.

## 📊 Dataset & Metrics Summary
* **Source:** Komentar Media Sosial (TikTok/@therealgitasav).
* **Total Data:** 71 baris komentar.
* **Average Initial Tokens:** 5.66 token per kalimat.
* **Average Processed Tokens:** 3.56 token per kalimat (reduksi noise $\approx$ 37%).

### Sentiment Distribution Results:
| Label | Jumlah Data | Persentase |
| :--- | :---: | :---: |
| **Positif** | 63 | 88.7% |
| **Negatif** | 8 | 11.3% |
| **Total** | **71** | **100%** |

## 🚀 How to Use
1. Clone repositori ini:
   ```bash
   git clone [https://github.com/USERNAME/NAMA_REPOSITORI.git](https://github.com/USERNAME/NAMA_REPOSITORI.git)