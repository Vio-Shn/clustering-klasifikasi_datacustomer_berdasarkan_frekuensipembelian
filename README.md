# Analisis Clustering dan Klasifikasi Pelanggan

Repository ini berisi analisis clustering dan klasifikasi pada data pelanggan, dengan tujuan untuk mengidentifikasi pola pembelian dan mengklasifikasikan pelanggan berdasarkan frekuensi dan jumlah pembelian.

## Hasil Clustering

Data telah dikelompokkan menjadi empat cluster berdasarkan frekuensi pembelian dan jumlah pengeluaran. Berikut adalah deskripsi masing-masing cluster:

### Cluster 1
- **Centroid**: Frekuensi = 1.30, Purchase Amount = 44,419.63
- **Karakteristik**: Cluster ini memiliki frekuensi pembelian yang mirip dengan kluster lainnya (sekitar 1.30) tetapi dengan jumlah pembelian yang tertinggi (sekitar 44,419.63).Hal ini menunjukkan bahwa pelanggan dalam cluster ini mungkin tidak sering berbelanja, namun setiap kali berbelanja, mereka melakukan pembelian dalam jumlah besar.

### Cluster 2
- **Centroid**: Frekuensi = 1.29, Purchase Amount = 21,861.11
- **Karakteristik**: Frekuensi pembelian di cluster ini hampir sama dengan cluster lainnya, namun jumlah pembelian mereka berada di tengah-tengah (sekitar 21,861.11). Ini menunjukkan bahwa pelanggan di cluster ini mungkin memiliki pola pembelian yang konsisten tetapi dalam jumlah sedang.

### Cluster 3
- **Centroid**: Frekuensi = 1.30, Purchase Amount = 10,560.62
- **Karakteristik**: Frekuensi pembelian sama seperti cluster lainnya, namun jumlah pembelian paling rendah (sekitar 10,560.62). Pelanggan di cluster ini berbelanja dalam jumlah yang lebih kecil, mungkin menunjukkan segmen pelanggan dengan daya beli yang lebih rendah atau preferensi untuk pembelian kecil.

### Cluster 4
- **Centroid**: Frekuensi = 1.31, Purchase Amount = 33,219.90
- **Karakteristik**: Frekuensi pembelian paling tinggi (1.31) meskipun perbedaannya kecil, dengan jumlah pembelian yang juga tinggi (sekitar 33,219.90). Ini menunjukkan bahwa pelanggan dalam cluster ini sedikit lebih sering berbelanja dan juga mengeluarkan uang dalam jumlah yang besar setiap kali berbelanja, meski tidak sebesar Cluster 1.

### Analisis Lanjutan
#### Segmentasi Berdasarkan Daya Beli:
1. **Cluster 1 dan Cluster 4** memiliki jumlah pembelian yang relatif tinggi. Hal ini dapat mengindikasikan pelanggan dengan daya beli yang lebih tinggi atau preferensi untuk berbelanja dalam jumlah besar. Strategi promosi atau produk premium dapat difokuskan pada dua cluster ini.
2. **Cluster 2 dan Cluster 3** memiliki jumlah pembelian yang lebih rendah, terutama Cluster 3, yang menunjukkan adanya kelompok pelanggan dengan daya beli rendah. Strategi diskon atau promosi bundling bisa lebih efektif untuk menarik pelanggan dalam cluster ini.

#### Kesempatan untuk Meningkatkan Frekuensi Pembelian:
  - Frekuensi pembelian di semua cluster cukup konsisten dan rendah, sekitar 1.3. Hal ini menunjukkan peluang untuk meningkatkan frekuensi pembelian melalui strategi pemasaran yang mendorong kunjungan berulang, seperti loyalty programs atau penawaran berbasis waktu (misalnya, diskon bulanan).

#### Potensi untuk Penargetan Khusus:

  1. **Cluster 1** bisa ditargetkan dengan produk-produk atau layanan kelas atas yang berharga tinggi, karena pelanggan di cluster ini cenderung melakukan pembelian besar.
  2. **Cluster 4** juga dapat menerima penawaran serupa namun dengan opsi untuk pembelian lebih sering. Program langganan atau layanan berbasis keanggotaan dapat menarik pelanggan ini untuk berbelanja lebih sering.
  3. **Cluster 3** mungkin lebih sensitif terhadap harga, sehingga promosi diskon atau penawaran dengan harga terjangkau bisa menjadi cara untuk mendorong lebih banyak pembelian dari kelompok ini.

#### Strategi Berdasarkan Pengeluaran:

  - Melalui pengetahuan tentang pembelian rata-rata setiap cluster, tim pemasaran dapat menyesuaikan rekomendasi produk dan layanan sesuai preferensi masing-masing kelompok pelanggan. Misalnya, produk bernilai tinggi dapat dipromosikan kepada Cluster 1 dan Cluster 4, sementara produk dengan harga lebih rendah dan promosi diskon dapat diarahkan pada Cluster 2 dan Cluster 3.

## Hasil Klasifikasi

Algoritma yang digunakan dan hasil evaluasi sebagai berikut:

1. **K-Nearest Neighbors (KNN)**
   - **Akurasi**: 0.96745
   - **Catatan**:     Precision dan Recall cukup baik, tetapi tidak setinggi Decision Tree atau Random Forest, yang menunjukkan bahwa KNN mungkin mengalami sedikit kesalahan dalam mengklasifikasikan beberapa sampel positif atau negatif.

2. **Decision Tree (DT)**
   - **Akurasi**: 1.000
   - **Precision**: 1.000
   - **Recall**: 1.000
   - **F-1 Score**: 1.000
   - **Catatan**: Model ini memiliki akurasi, precision, recall, dan F1-score sempurna (1.000). Hasil yang sempurna ini mungkin menunjukkan model mengalami overfitting, terutama jika data uji memiliki karakteristik yang sama dengan data latih..

3. **Random Forest (RF)**
   - **Akurasi**: 0.99995
   - **F-1 Score**: 0.99902
   - **Catatan**: Hampir sempurna dalam seluruh metrik dengan akurasi 0.99995 dan F1-score 0.99902, yang juga menunjukkan potensi overfitting ringan, meskipun model ensemble seperti Random Forest umumnya lebih baik dalam menghindari overfitting dibandingkan Decision Tree.

4. **Support Vector Machine (SVM)**
   - **Akurasi**: 0.98185
   - **Precision**: 0.946243
   - **Catatan**: Meski SVM menunjukkan performa yang bagus, penurunan recall dapat berarti bahwa model ini sedikit kurang sensitif terhadap deteksi positif, sehingga ada beberapa kasus positif yang mungkin tidak terdeteksi dengan baik..

5. **Naive Bayes (NB)**
   - **Akurasi**: 0.95665
   - **Precision**: 0.963307
   - **Recall**: 0.837534
   - **Catatan**: Recall rendah ini mengindikasikan kelemahan dalam mengidentifikasi kelas positif dengan benar. Sehingga, Naive Bayes memiliki kecenderungan untuk menghasilkan banyak false negatives. perbaiki lah kalimat-kalimat ini untuk dilampirkan pada readme file github agar terilihat menarik.

---

### Berdasarkan hasil clustering dan klasifikasi ini perusahaan bisa mengambil keputusan terkait pola pembelian dan meningkatkan tingkat penjualan dari perusahaan dengan metode-metode pengelompokan dan klasifikasi tipe pembeli. :wink:

