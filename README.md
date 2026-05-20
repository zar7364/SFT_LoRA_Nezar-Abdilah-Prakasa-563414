SFT LoRA on Qwen2.5-0.5B

Project ini melakukan Supervised Fine-Tuning (SFT) menggunakan metode LoRA pada model Qwen2.5-0.5B dengan dataset indonlp/cendol_collection_v2 
untuk meningkatkan kemampuan instruction-following dalam Bahasa Indonesia.

Spesifikasi
1. Model: Qwen/Qwen2.5-0.5B
2. Dataset: indonlp/cendol_collection_v2
3. Fine-Tuning: LoRA (PEFT)
4. Framework: Transformers, TRL, PEFT
5. Training: Google Colab T4 GPU

Model setelah fine-tuning menghasilkan respons yang lebih relevan dan lebih focus dalam membahas topik yang ada dibandingkan base model.
