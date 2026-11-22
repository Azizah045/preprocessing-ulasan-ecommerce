# Preprocessing Teks Ulasan Produk E-Commerce Berbahasa Indonesia

Repositori ini berisi implementasi tahapan *text preprocessing* pada dataset ulasan produk *e-commerce* berbahasa Indonesia untuk kebutuhan analisis sentimen.

## Identitas Mahasiswa
* **Nama:** Azizah
* **NIM:** 25146045

## Sumber Dataset
Dataset yang digunakan berasal dari Hugging Face:
* **Nama Dataset:** `dipawidia/ecommerce-product-reviews-sentiment`
* **Tautan:** https://huggingface.co/datasets/dipawidia/ecommerce-product-reviews-sentiment
* **Deskripsi Singkat:** Berisi 11.606 ulasan produk dari berbagai platform *e-commerce* Indonesia (Shopee, Tokopedia, Lazada, Bukalapak, Blibli, dan Zalora) dengan 3 kolom utama (`review`, `translate`, dan `sentimen`).

## Tahapan Preprocessing yang Diterapkan
1. **Case Folding:** Mengubah seluruh huruf menjadi huruf kecil (*lowercase*).
2. **Cleaning:** Menghapus URL, angka, tanda baca, emoji, karakter khusus, dan spasi berlebih.
3. **Tokenisasi:** Memecah kalimat menjadi daftar token kata.
4. **Stopword Removal:** Menghapus kata-kata umum tidak bermakna signifikan menggunakan daftar *stopword* bahasa Indonesia (`PySastrawi`).
5. **Stemming:** Mengubah kata berimbuhan menjadi kata dasar menggunakan algoritma Nazief & Adriani (`PySastrawi`).

## Struktur File dalam Repositori
* `preprocessing_ulasan_ecommerce.ipynb` — File Jupyter Notebook berisi kode eksplorasi dataset, pipeline 5 tahap *preprocessing*, 10 contoh hasil sebelum dan sesudah *preprocessing*, serta kesimpulan analisis.
* `README.md` — Dokumentasi identitas mahasiswa dan deskripsi proyek.

## Cara Menjalankan Notebook
1. Pastikan Python 3 telah terpasang.
2. Instal pustaka yang dibutuhkan:
   ```bash
   pip install datasets pandas nltk PySastrawi
   ```
3. Buka dan jalankan seluruh sel pada file `preprocessing_ulasan_ecommerce.ipynb` menggunakan Jupyter Notebook, JupyterLab, atau Google Colab.