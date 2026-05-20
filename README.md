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



Model setelah fine-tuning menghasilkan respons yang lebih relevan dan lebih fokus dalam membahas topik yang ada dibandingkan base model.


# Pertanyaan (Question) pada Tugas

| Pertanyaan | Jawaban |
|---|---|
| Q1. Mengapa base model memiliki pengetahuan luas tetapi lemah dalam mengikuti instruksi? | Karena saat pre-training model hanya belajar memprediksi token berikutnya dari data internet, bukan belajar mengikuti instruksi pengguna. Jadi model lebih terbiasa melanjutkan teks dibanding menjawab seperti assistant. |
| Q2. Berapa persen parameter yang Anda latih dengan LoRA dibanding total parameter model? Apa dampaknya terhadap efisiensi? | Berdasarkan hasil training, hanya sekitar 0.2184% parameter yang dilatih menggunakn LoRA, yaitu 1,081,344 dari total 495,114,112 parameter. Hal ini membuat training lebih efisien dan tetap efektif untuk fine-tuning model. |
| Q3. Tampilkan 3 contoh respons model sebelum dan sesudah fine-tuning. Analisis perbedaannya. | Sebelum fine-tuning, model cenderung menghasilkan jawaban yang kurang fokus, repetitif, dan tidak mengikuti instruksi dengan baik. Setelah fine-tuning, respons menjadi lebih relevan, lebih natural, dan lebih sesuai dengan konteks instruksi pengguna. |
| Q4. Apa risiko overfitting pada dataset kecil? Bagaimana Anda mendeteksi dan mencegahnya? | Risiko overfiting pada dataset kecil adalah model terlalu menghafal data training shingga performa pada prompt baru menjadi buruk. Cara mendeteksinya bisa dilihat saat training loss turun tetapi kualitas jawaban tidak membaik. Cara mencegahnya bisa dilakukan dengan menggunakan dataset yang lebih bervariasi |
| Q5. Jika Anda membuat dataset bahasa daerah sendiri: apa tantangan utama dalam membuat data berkualitas tinggi? Apa yang Anda pelajari? | - |
