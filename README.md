# 🧠 Analisis Opini Publik terhadap RUU TNI di Twitter 🇮🇩

Proyek ini bertujuan untuk menganalisis opini publik di Twitter terkait pembahasan *Rancangan Undang-Undang Tentara Nasional Indonesia (RUU TNI)*. Proyek menggunakan pendekatan **Natural Language Processing (NLP)** dengan model sentimen Bahasa Indonesia berbasis transformer.

---

## 📌 Tujuan
- Mengambil data tweet dari Twitter menggunakan kata kunci seputar RUU TNI
- Membersihkan dan memproses teks dari tweet
- Menganalisis sentimen publik (positif, negatif, netral)
- Menampilkan kata-kata yang paling sering muncul dalam opini publik
- Membuat visualisasi seperti Wordcloud untuk masing-masing kategori sentimen

---

## 🛠️ Tools & Teknologi
- Python (Colab)
- 🐍 `pandas`, `numpy`
- 🧹 `re`, `string` (text cleaning)
- 🤗 `transformers` (Indonesian Roberta model for sentiment classification)
- 🧾 `scikit-learn` (frekuensi kata)
- ☁️ `wordcloud`
- 📊 `matplotlib`

---

## 🔍 Alur Analisis

### 1. Data Collection
Tweet diambil menggunakan `snscrape` dengan kata kunci seperti:
- `"RUU TNI"`
- `"revisi UU TNI"`
- `"militer sipil"`
- `"TNI ranah sipil"`

### 2. Preprocessing
- Lowercasing
- Hapus simbol, emoji, link
- Stopword removal (Bahasa Indonesia)
- Optional: stemming (tidak dilakukan dalam proyek ini)

### 3. Sentiment Classification
Model: [`w11wo/indonesian-roberta-base-sentiment-classifier`](https://huggingface.co/w11wo/indonesian-roberta-base-sentiment-classifier)

Klasifikasi ke dalam 3 label:
- `positive`
- `neutral`
- `negative`

### 4. Ringkasan Opini Publik
Menampilkan kata-kata yang paling sering muncul pada tweet `positif` dan `negatif`.

### 5. Wordcloud
Membuat wordcloud untuk masing-masing sentimen agar lebih mudah divisualisasikan.

---

## 📌 Hasil Utama

- Sentimen negatif mendominasi perbincangan publik terhadap RUU TNI.
- Tweet netral umumnya berupa berita atau informasi tanpa opini.

