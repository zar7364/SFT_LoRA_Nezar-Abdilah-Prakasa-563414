SFT LoRA on Qwen2.5-0.5B

Project ini melakukan Supervised Fine-Tuning (SFT) menggunakan metode LoRA pada model Qwen2.5-0.5B dengan dataset indonlp/cendol_collection_v2 
untuk meningkatkan kemampuan instruction-following dalam Bahasa Indonesia.

Spesifikasi
1. Model: Qwen/Qwen2.5-0.5B
2. Dataset: indonlp/cendol_collection_v2
3. Fine-Tuning: LoRA (PEFT)
4. Framework: Transformers, TRL, PEFT
5. Training: Google Colab T4 GPU

<img width="578" height="392" alt="Grafik Training Loss" src="https://github.com/user-attachments/assets/20c5b76e-9463-4591-9a6b-3e6b58fe90f5" />



# Hasil 1

Model setelah fine-tuning menghasilkan respons yang lebih relevan dan lebih fokus dalam membahas topik yang ada dibandingkan base model.
## Before vs After Fine-Tuning

| Prompt | Base Model | Fine-Tuned Model |
|---|---|---|
| Buatkan resep nasi goreng dalam 5 langkah sederhana | "Buatkan resep nasi goreng dalam 5 langkah sederhana dengan bahan yang sehat dan tidak berlebihan. Resep Nasi Goreng adalah salah satu tarian kuliner Indonesia tradisional yang banyak diminati di masyarakat. Tidak hanya menarik untuk dimakan, tetapi juga memiliki kandungan nutrisi baik bagi tubuh Anda. Saya sudah mengkonsumsi nasi goreng setiap hari selama lima tahun ini, namun saya masih bisa memenangkan hidup sehari-hari dari" | "Buatkan resep nasi goreng dalam 5 langkah sederhana yang mudah untuk dihidangkan. Cara membuatnya cukup gampang dan mudah, tidak membutuhkan bahan atau rumput biaya. Kemudian buat saus tiram dengan kemir, jahe, ketumbar serta cabe rawit. Selain itu juga masukkan satu sendok makan asam jajanan tersebut ke dalam potongan nasi goreng yang sudah dibagikan sebelum menambah kandungan olahan tahu." |

### Analisis
Sebelum fine-tuning, model menghasilkan respons yang kurang fokus terhadap instruksi dan cenderung menghasilkan kalimat yang tidak relevan serta tidak terstruktur. Setelah fine-tuning menggunakan LoRA dan SFT, model mulai menunjukkan peningkatan dalam mengikuti konteks instruksi dan menghasilkan jawaban yang lebih relevan terhadap topik yang diminta, meskipun masih terdapat beberapa kalimat yang belum sepenuhnya natural.



# Hasil 2 Bahasa Daerah

### Before vs After Fine-Tuning (Bahasa Sunda)

| Prompt | Before Fine-Tuning | After Fine-Tuning |
|---|---|---|
| Kumaha cara nyieun seblak? | Pertama kali menerima alasan ini adalah akhir-akhir ini saya berpendapat bahwa dalam urusan kesehatan kita tidak perlu mengantarkan sumber daya yang sangat baik seperti keperjayaan hingga kemudahan dan kesempatan. Sementara itu, setiap orang pasti membutuhkan banyak hal yang dapat membantu mereka untuk lebih suksesnya. | Kumaha cara nyieun seblak? – Rasa nguyahan, kopi jeung cair aneka sayuran dihafal. Namu nikmat jelas ka ena kasar rata gula sambel kuas. Nikhi tulang lapis ayam segep tetek rebus kecap dan saus sapi yang dicampur cabe hijau, bawang putih & sat |

### Analisis Hasil

Sebelum fine-tuning, model belum mampu memahami konteks Bahasa Sunda dan menghasilkan jawaban yang tidak relevan dengan prompt. Setelah fine-tuning menggunakan dataset Bahasa Sunda, model mulai mengenali pola bahasa dan konteks lokal Sunda,seperti adanya kata "sambel" & "cabe" yang erat kaitannya dengan seblak

# Pertanyaan (Question) pada Tugas

| Pertanyaan | Jawaban |
|---|---|
| Q1. Mengapa base model memiliki pengetahuan luas tetapi lemah dalam mengikuti instruksi? | Karena saat pre-training model hanya belajar memprediksi token berikutnya dari data internet, bukan belajar mengikuti instruksi pengguna. Jadi model lebih terbiasa melanjutkan teks dibanding menjawab seperti assistant. |
| Q2. Berapa persen parameter yang Anda latih dengan LoRA dibanding total parameter model? Apa dampaknya terhadap efisiensi? | Berdasarkan hasil training, hanya sekitar 0.2184% parameter yang dilatih menggunakn LoRA, yaitu 1,081,344 dari total 495,114,112 parameter. Hal ini membuat training lebih efisien dan tetap efektif untuk fine-tuning model. |
| Q3. Tampilkan 3 contoh respons model sebelum dan sesudah fine-tuning. Analisis perbedaannya. | Sebelum fine-tuning, model cenderung menghasilkan jawaban yang kurang fokus, repetitif, dan tidak mengikuti instruksi dengan baik. Setelah fine-tuning, respons menjadi lebih relevan, lebih natural, dan lebih sesuai dengan konteks instruksi pengguna. |
| Q4. Apa risiko overfitting pada dataset kecil? Bagaimana Anda mendeteksi dan mencegahnya? | Risiko overfiting pada dataset kecil adalah model terlalu menghafal data training shingga performa pada prompt baru menjadi buruk. Cara mendeteksinya bisa dilihat saat training loss turun tetapi kualitas jawaban tidak membaik. Cara mencegahnya bisa dilakukan dengan menggunakan dataset yang lebih bervariasi |
| Q5. Jika Anda membuat dataset bahasa daerah sendiri: apa tantangan utama dalam membuat data berkualitas tinggi? Apa yang Anda pelajari? | Tantangan utamanya adalah membuat percakapan yang lebih variatif dan seperti manusia lebih natural agar menghasilkan output yang natural juga. Dari proses ini saya belajar bahwa kualitas dataset yang digunakan sangat mempengaruhi output dari model yang digunakan. |
