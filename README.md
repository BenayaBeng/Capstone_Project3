# Customer Lifetime Value

1. Business Problem Understanding
2. Data Understanding
3. Data Preprocessing
4. Modeling
5. Conclusion
6. Recommendation

# 1.Business Problem Understanding

### 1.Stakeholder:

Tim Manajemen: Bertanggung jawab untuk pengambilan keputusan strategis terkait pemasaran, penjualan, dan keuangan.

Tim Pemasaran: Menggunakan informasi pelanggan untuk merancang kampanye pemasaran yang lebih efektif.

Tim Layanan Pelanggan: Membantu meningkatkan kepuasan pelanggan dengan pemahaman yang lebih baik tentang kebutuhan dan preferensi pelanggan.

Data Analyst: Bertanggung jawab untuk menganalisis data pelanggan dan 
menghasilkan wawasan yang berguna bagi stakeholder lainnya.

### 2.Masalah: 
Prediksi CLV: Apakah prediksi CLV itu akurat

Customer Retention: Menganalisis faktor-faktor yang mempengaruhi retensi pelanggan dan mengidentifikasi strategi yang efektif untuk meningkatkan retensi pelanggan.

Customer Segment: Mengidentifikasi segmen pelanggan yang berbeda berdasarkan atribut pelanggan yang tersedia, sehingga dapat menyusun strategi pemasaran yang lebih terarah.

### 3. Tujuan atau Solusi
Meningkatkan Akurasi Prediksi
Meningkatkan penjualan
Meningkatkan Kepuasan Pelanggan

# 2.Data Understanding

Dataset yang digunakan dalam proyek ini berisi fitur-fitur berikut:

Vehicle Class: Kelas kendaraan pelanggan.

Coverage: Jenis cakupan asuransi yang dimiliki pelanggan.

Renew Offer Type: Jenis penawaran perpanjangan yang diberikan kepada pelanggan.

Employment Status: Status pekerjaan pelanggan.

Marital Status: Status pernikahan pelanggan.

Education: Latar belakang pendidikan pelanggan.

Number of Policies: Jumlah kebijakan asuransi yang dimiliki pelanggan.

Monthly Premium Auto:  Premi bulanan yang dibayarkan pelanggan untuk asuransi otomatis.

Total Claim Amount:  Jumlah klaim total yang diajukan oleh pelanggan.

Income: Tingkat pendapatan pelanggan.

Customer Lifetime Value:  Variabel target yang mewakili nilai seumur hidup pelanggan.

# 3. Data Preprocessing

### Data Cleaning
1. Missing Value Analysis
2. Outlier Removal

### Data Transformation
One hot encoder

# 4. Modelling

### 1.Data Preparation
Data input untuk model disimpan dalam DataFrame yang disebut df2. Fitur-fitur diambil dari DataFrame menggunakan metode .iloc[:,:-1], yang memilih semua kolom kecuali yang terakhir. Variabel target, 'Customer Lifetime Value', diambil menggunakan metode .to_numpy(), yang mengonversi kolom DataFrame yang dipilih menjadi array NumPy. Fitur-fitur disimpan dalam variabel X, sedangkan variabel target disimpan dalam y.

### 2.Train-Test Split
Dataset dibagi menjadi subset latih dan uji menggunakan fungsi train_test_split dari library scikit-learn. Parameter test_size diatur menjadi 0.3, yang menandakan bahwa 30% data akan digunakan untuk pengujian, sedangkan 70% akan digunakan untuk pelatihan. Parameter random_state diatur menjadi 8 untuk memastikan pemisahan yang dapat direproduksi. Subset latih dan uji yang dihasilkan disimpan dalam variabel X_train, X_test, y_train, dan y_test, secara berturut-turut.

### 3.Model Training
Model SVR diinisialisasi dengan kelas SVR dari library scikit-learn. Parameter C diatur menjadi 111111, yang mengontrol penalitas kesalahan dalam model. Nilai C yang lebih tinggi mengindikasikan kekuatan regularisasi yang lebih kecil.

Pipeline dibuat menggunakan make_pipeline dari scikit-learn. Pipeline terdiri dari dua langkah: penskalaan fitur menggunakan MinMaxScaler dan penerapan model SVR. Pipeline ini memastikan bahwa transformasi penskalaan diterapkan secara konsisten selama pelatihan dan pengujian.

Model kemudian dilatih dengan data latih menggunakan metode fit. Fitur (X_train) dan variabel target yang sesuai (y_train) diberikan sebagai argumen kepada metode fit.

### 4.Model Evaluation
Evaluation Metric

Root Mean Squared Error (RMSE): RMSE mengukur deviasi rata-rata antara nilai prediksi dan nilai aktual. Semakin rendah nilai RMSE, semakin baik kualitas prediksi model. Nilai RMSE dihitung menggunakan fungsi mean_squared_error dari library scikit-learn.

Mean Absolute Error (MAE): MAE mengukur selisih rata-rata absolut antara nilai prediksi dan nilai aktual. MAE memberikan gambaran tentang seberapa besar kesalahan rata-rata dalam prediksi model. Nilai MAE dihitung menggunakan fungsi mean_absolute_error dari library scikit-learn.

R-squared (R2): R2 menunjukkan sejauh mana variasi dalam data target dapat dijelaskan oleh model. Nilai R2 berkisar antara 0 hingga 1, dengan 1 menunjukkan model yang sempurna sesuai dengan data. Nilai R2 dihitung menggunakan metode score pada objek regresi (regr).

Metrik evaluasi ini memberikan informasi penting tentang performa model regresi. Nilai-nilai tersebut dicetak sebagai hasil evaluasi dari model yang dijalankan pada data uji.

# 5. Conclusion
Setelah melakukan analisis dan pemodelan Customer Lifetime Value (CLV), berikut adalah beberapa kesimpulan yang dapat diambil dari proyek ini:

Terdapat variasi nilai seumur hidup pelanggan (CLV) di antara kelompok kendaraan, jenis cakupan asuransi, jenis penawaran perpanjangan, status pekerjaan, status pernikahan, latar belakang pendidikan, jumlah kebijakan asuransi, premi bulanan otomatis, jumlah klaim total, dan tingkat pendapatan.
Fitur-fitur seperti premi bulanan otomatis, jumlah kebijakan asuransi, dan jumlah klaim total memiliki pengaruh yang signifikan terhadap nilai seumur hidup pelanggan.
Model machine learning yang telah dikembangkan mampu memberikan prediksi CLV yang dapat digunakan untuk mengidentifikasi pelanggan bernilai tinggi dan rendah.

# 6. Recommendation
Setelah menganalisis Customer Lifetime Value (CLV) dan mendapatkan wawasan dari model CLV, kita dapat membuat rekomendasi berharga untuk meningkatkan strategi bisnis dan memaksimalkan nilai pelanggan. Berikut adalah beberapa rekomendasi berdasarkan temuan:

### 1 Customer Segmentation
Lakukan segmentasi pelanggan berdasarkan nilai seumur hidup pelanggan. Fokuskan upaya pemasaran dan retensi pada pelanggan bernilai tinggi untuk mempertahankan dan memperluas keterlibatan mereka.

### 2 Retention Strategies
Identifikasi pelanggan dengan risiko churn tinggi berdasarkan prediksi CLV. Ambil tindakan proaktif untuk mempertahankan pelanggan tersebut dengan penawaran khusus, program loyalitas, atau perbaikan pengalaman pelanggan.

### 3 Loyalty program
Gunakan wawasan CLV untuk menyesuaikan penawaran dan promosi untuk setiap pelanggan. Berikan insentif khusus kepada pelanggan bernilai tinggi untuk meningkatkan loyalitas mereka.

### 4 Customer Experience Enhancement
Tingkatkan pengalaman pelanggan dengan meningkatkan kualitas layanan dan responsifitas. Peningkatan kualitas layanan dapat membantu mempertahankan pelanggan dan meningkatkan CLV mereka.

### 5 Pricing Strategies
Gunakan informasi CLV untuk mengoptimalkan strategi penetapan harga. Sesuaikan harga untuk pelanggan dengan nilai seumur hidup tinggi dan pertimbangkan penawaran diskon atau paket untuk meningkatkan keterlibatan pelanggan dengan nilai rendah.
