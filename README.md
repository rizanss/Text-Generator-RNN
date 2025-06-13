# ✍️ The AI Poet: Character-Level Text Generator with LSTM

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python Version](https://img.shields.io/badge/python-3.10%2B-green.svg)
![TensorFlow Version](https://img.shields.io/badge/tensorflow-2.x-orange.svg)

## 📄 Project Overview

Proyek ini adalah eksplorasi **Natural Language Generation (NLG)** menggunakan **Recurrent Neural Network (RNN)**, secara spesifik dengan arsitektur **Long Short-Term Memory (LSTM)**. Model ini dilatih pada naskah lengkap karya William Shakespeare untuk mempelajari gaya bahasa, struktur kalimat, dan kosakata pada level karakter. Tujuannya adalah untuk menghasilkan teks baru yang meniru gaya penulisan Shakespeare.

Proyek ini mencakup:
1.  **Preprocessing Teks:** Mengubah naskah mentah menjadi sekuens data yang terstruktur untuk *training*.
2.  **Arsitektur Model:** Membangun dan melatih model LSTM bertumpuk (*stacked*) untuk menangkap dependensi jangka panjang dalam teks.
3.  **Text Generation:** Mengimplementasikan fungsi untuk menghasilkan teks baru, lengkap dengan *tuning* parameter **Temperature** untuk mengontrol kreativitas vs. koherensi.

---

## 🎯 Goal & Key Learnings

Tujuan utama dari proyek ini adalah untuk memahami dan mengimplementasikan dasar-dasar model generatif sekuensial. Fokus utamanya adalah pada proses, bukan kesempurnaan output.

**Temuan Kunci:**
* Model LSTM bertumpuk terbukti lebih efektif dalam menurunkan *loss* dibandingkan model dengan satu layer.
* Terdapat *trade-off* yang jelas antara koherensi dan kreativitas, yang dapat dikontrol menggunakan parameter `temperature` saat *inference*.
* Meskipun model berhasil mempelajari struktur kata dan kalimat dasar, pendekatan *character-level* memiliki keterbatasan dalam menghasilkan teks yang bermakna secara semantik.

---

## 📂 Project Structure
```
Text-Generator-RNN/
├── models/
│   └── shakespeare_lstm_v3_loss_1.69.keras  # Model terbaik yang sudah terlatih
│
├── notebooks/
│   └── LSTM_Text_Generator.ipynb            # Notebook untuk eksperimen & training
│
├── .gitignore
├── README.md
└── requirements.txt
```
---

## 🛠️ Tech Stack

* **TensorFlow & Keras:** Untuk membangun, melatih, dan mengevaluasi model LSTM.
* **NumPy:** Untuk manipulasi data dan *vectorization*.
* **Google Colab:** Digunakan untuk training dengan akselerasi GPU.

---

## 📈 Model Performance

Setelah melalui beberapa iterasi eksperimen, arsitektur terbaik (LSTM bertumpuk) berhasil mencapai **loss training serendah 1.69**. Hasil teks yang digenerate menunjukkan kemampuan model untuk membentuk kata-kata valid dan meniru struktur penulisan drama, meskipun masih kurang dalam koherensi kalimat panjang.

Eksperimen dengan parameter `temperature` menunjukkan:
* **Temp Rendah (0.2 - 0.5):** Menghasilkan teks yang lebih "aman", dengan kata-kata yang valid namun cenderung repetitif.
* **Temp Tinggi (1.0 - 1.2):** Menghasilkan teks yang lebih "kreatif" dan bervariasi, namun dengan banyak kata-kata yang tidak ada dalam kamus (halusinasi).

---

## 🚀 How to Run

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/rizanss/Text-Generator-RNN.git](https://github.com/rizanss/Text-Generator-RNN.git)
    cd Text-Generator-RNN
    ```
2.  **Setup Environment (Rekomendasi: Google Colab):**
    * Buka [Google Colab](https://colab.research.google.com/).
    * Upload notebook `notebooks/LSTM_Text_Generator.ipynb`.
    * Upload file model `models/shakespeare_lstm_v2_loss_1.69.keras`.
    * Aktifkan akselerator `GPU`.
3.  **Run The Notebook:** Jalankan sel-sel di notebook untuk men-download data, me-load model yang sudah ada, dan men-generate teks baru.

---

## 📬 Contact
* **Author:** Riza Nursyah
* **GitHub:** [rizanss](https://github.com/rizanss)
* **LinkedIn:** [Riza Nursyah](https://www.linkedin.com/in/riza-nursyah-31a6a7221/)