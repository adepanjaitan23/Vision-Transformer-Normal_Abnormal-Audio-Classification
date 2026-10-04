## Vision Transformer Normal-Abnormal Audio Classification
# Respiratory Sound Segmentation and Preprocessing Pipeline

Proyek ini berisi *pipeline* pemrosesan data untuk menganalisis suara pernapasan menggunakan **Respiratory Sound Database**[cite: 3]. Repositori ini mencakup pengunduhan dataset otomatis, pemuatan data klinis pasien, *parsing* anotasi teks, serta segmentasi audio presisi tinggi berdasarkan label klinis[cite: 3].

## Fitur Utama
* **Otomasi Unduh Dataset**: Menggunakan pustaka `kagglehub` untuk mengunduh dataset *Respiratory Sound Database* secara langsung[cite: 3].
* **Eksplorasi & Konteks Diagnosis**: Membaca file metadata `patient_diagnosis.csv` untuk memetakan distribusi penyakit pasien[cite: 3].
* **Parsing Anotasi Presisi**: Membaca file anotasi `.txt` yang berisi waktu mulai (*start*), waktu selesai (*end*), penanda *crackle*, dan *wheeze*[cite: 3].
* **Segmentasi & Pelabelan Otomatis**: Memotong file audio mentah (`.wav`) secara presisi dan mengelompokkannya ke dalam kelas: `normal`, `crackle`, `wheeze`, atau `both`[cite: 3].
* **Penyimpanan Metadata**: Menyimpan hasil segmentasi ke dalam file CSV terstruktur (`metadata_segments_precise.csv`)[cite: 3].

## Prasyarat Pustaka (Libraries)
Pustaka Python yang digunakan dalam proyek ini meliputi[cite: 3]:
* `torch`, `torchvision`[cite: 3]
* `numpy`, `pandas`[cite: 3]
* `librosa`, `soundfile`[cite: 3]
* `scipy`[cite: 3]
* `matplotlib`, `seaborn`[cite: 3]
* `scikit-learn`[cite: 3]
* `kagglehub`[cite: 3]
* `tqdm`[cite: 3]

## Struktur Direktori Output
Setelah skrip dijalankan, direktori penyimpanan segmen audio akan terbentuk dengan struktur berikut[cite: 3]:
* `segmented_audio_precise/`
  * `normal/`
  * `crackle/`
  * `wheeze/`
  * `both/`
  * `metadata_segments_precise.csv`[cite: 3]
