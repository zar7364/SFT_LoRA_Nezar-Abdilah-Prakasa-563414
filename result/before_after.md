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
