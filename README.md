# Credit Card Fraud Detection using XGBoost
Project ini berfokus pada pengembangan model klasifikasi yang robust untuk mendeteksi anomali (penipuan) pada data transaksi kartu kredit, berhasil mencapai metrik Recall 82%.
# Ringkasan Eksekutif
Studi kasus ini mendemonstrasikan pipeline end-to-end dalam mengatasi masalah klasifikasi imbalanced pada data real-world.
# I. Data Preprocessing dan Tantangan
Data transaksi yang digunakan telah melalui anonimisasi PCA (Principal Component Analysis). Tantangan utama proyek ini adalah ketidakseimbangan kelas yang ekstrem, di mana kasus penipuan hanya merepresentasikan $0.2582\%$ dari total observasi, sehingga memaksa fokus pada metrik Recall sebagai kunci evaluasi.
Untuk persiapan data, Feature Engineering dilakukan dengan mengekstrak fitur Hour dari kolom Time. Selanjutnya, variabel Amount dan Hour diskalakan menggunakan RobustScaler untuk memitigasi dampak outlier sebelum pemodelan.
# II. Metodologi dan Kinerja Pemodelan
Model XGBoost (Extreme Gradient Boosting) diimplementasikan sebagai solusi klasifikasi biner.
1. Strategi Imbalance: Masalah imbalance ditangani dengan menyesuaikan bobot kelas minoritas menggunakan parameter scale_pos_weight (rasio $\approx 386:1$), yang meningkatkan sensitivitas model terhadap kasus penipuan.
2. Kinerja Kunci: Model mencapai Recall 82% pada testing set. Hasil ini meminimalkan False Negative (penipuan yang lolos) menjadi hanya 6 kasus, sebuah capaian krusial untuk menjaga integritas finansial.
# III. Wawasan dan Rekomendasi Bisnis
Analisis model memberikan wawasan yang dapat ditindaklanjuti (actionable insights) untuk mitigasi risiko:
1. Indikator Utama Risiko: Analisis Feature Importance mengidentifikasi fitur V14 dan V5 sebagai prediktor penipuan paling signifikan. Variabel-variabel PCA ini harus menjadi fokus investigasi lebih lanjut oleh tim fraud analytics.
2. Implementasi: Model direkomendasikan untuk diintegrasikan ke dalam sistem deteksi real-time untuk mengoptimalkan penanganan risiko dan mengurangi False Negative secara sistematis.
# Lihat Analisis Detail:
Untuk eksplorasi kode, visualisasi, dan output per langkah, silakan merujuk pada file [Credit_Card_Fraud_Detection_XGBoost.ipynb]
