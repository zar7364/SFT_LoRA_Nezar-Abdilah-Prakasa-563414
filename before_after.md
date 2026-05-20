# Before vs After Fine-Tuning

| Prompt | Base Model | Fine-Tuned Model |
|---|---|---|
| Buatkan resep nasi goreng dalam 5 langkah sederhana | "Buatkan resep nasi goreng dalam 5 langkah sederhana dengan bahan yang sehat dan tidak berlebihan. Resep Nasi Goreng adalah salah satu tarian kuliner Indonesia tradisional yang banyak diminati di masyarakat. Tidak hanya menarik untuk dimakan, tetapi juga memiliki kandungan nutrisi baik bagi tubuh Anda. Saya sudah mengkonsumsi nasi goreng setiap hari selama lima tahun ini, namun saya masih bisa memenangkan hidup sehari-hari dari" | "Buatkan resep nasi goreng dalam 5 langkah sederhana yang mudah untuk dihidangkan. Cara membuatnya cukup gampang dan mudah, tidak membutuhkan bahan atau rumput biaya. Kemudian buat saus tiram dengan kemir, jahe, ketumbar serta cabe rawit. Selain itu juga masukkan satu sendok makan asam jajanan tersebut ke dalam potongan nasi goreng yang sudah dibagikan sebelum menambah kandungan olahan tahu." |

## Analisis
Sebelum fine-tuning, model menghasilkan respons yang kurang fokus terhadap instruksi dan cenderung menghasilkan kalimat yang tidak relevan serta tidak terstruktur. Setelah fine-tuning menggunakan LoRA dan SFT, model mulai menunjukkan peningkatan dalam mengikuti konteks instruksi dan menghasilkan jawaban yang lebih relevan terhadap topik yang diminta, meskipun masih terdapat beberapa kalimat yang belum sepenuhnya natural.
