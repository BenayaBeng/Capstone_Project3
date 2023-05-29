# Customer Lifetime Value

1. Business Problem Understanding
2. Data Understanding
3. Data Preprocessing
4. Modeling
5. Conclusion
6. Recommendation

# 1.Business Problem Understanding

Project ini bertujuan untuk memprediksi Customer Lifetime Value/CLV bagi sebuah perusahaan.

CLV merupakan ukuran seberapa berharga pelanggan bagi perusahaan, yang mengindikasikan total keuntungan yang dihasilkan oleh seorang pelanggan selama masa hidupnya sebagai pelanggan.

Dengan memahami CLV, perusahaan dapat menilai profitabilitas dalam mendapatkan dan mempertahankan pelanggan, serta merancang strategi *marketing* yang efektif untuk menargetkan pelanggan berharga.

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
