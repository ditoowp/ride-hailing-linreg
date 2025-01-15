# **Uber vs. Lyft** : Linear Regression Model 

By [Dito Wicaksana P.](https://github.com/ditoowp) | Data Resource: [Kaggle](https://www.kaggle.com/datasets/brllrb/uber-and-lyft-dataset-boston-ma)

<center><img src="https://imgtr.ee/images/2024/07/14/d4d61da3c007124e92a2305c005dc0af.png" width=65% /></center>

---

## Introduction
<p style="text-align: justify;">
Uber dan Lyft merupakan dua perusahaan <em>ride-hailing</em>  terbesar yang menyediakan layanan transportasi melalui aplikasi seluler. Didirikan di San Francisco, Uber pada tahun 2009 dan Lyft pada tahun 2012, keduanya menawarkan alternatif transportasi yang nyaman dibandingkan dengan taksi tradisional atau transportasi umum. Uber telah berkembang menjadi perusahaan global yang beroperasi di ratusan kota di seluruh dunia, menawarkan berbagai layanan mulai dari UberX yang terjangkau hingga UberBLACK yang mewah. Lyft, meskipun beroperasi di lebih sedikit negara dibandingkan Uber, telah memperluas jangkauannya ke banyak kota di Amerika Serikat dan Kanada, dengan fokus pada pengalaman pengguna yang ramah dan layanan yang kompetitif. Keduanya bersaing ketat dalam hal harga, ketersediaan kendaraan, dan fitur tambahan seperti program loyalitas dan opsi berbagi perjalanan.
</p>

---

## Objective
<p style="text-align: justify;">
Tujuan utama dari proyek ini adalah mengembangkan model regresi linear untuk memprediksi <strong>price</strong> atau biaya <em>ride-hailing</em>  untuk Uber dan Lyft. Model prediktif ini bertujuan untuk mengidentifikasi dan mengukur hubungan antara biaya perjalanan dan beberapa faktor yang mempengaruhinya, yang meliputi:
</p>

* **Jam Kerja**: Waktu dalam sehari dan apakah termasuk dalam jam kerja atau periode permintaan tinggi.
* **Kondisi Cuaca**: Berbagai parameter cuaca seperti suhu, curah hujan, dan visibilitas yang mungkin mempengaruhi biaya perjalanan.
* **Jarak**: Total jarak yang ditempuh selama perjalanan.
* **Destinasi**: Destinasi spesifik atau jenis area (misalnya, bandara, pusat kota, pinggiran kota) yang menjadi tujuan perjalanan.

<p style="text-align: justify;">
Dengan menganalisis faktor-faktor ini, model ini bertujuan untuk memberikan prediksi biaya perjalanan yang akurat, memberikan wawasan berharga bagi pelanggan dan penyedia layanan di industri ride-hailing. Tujuan utamanya adalah untuk meningkatkan pemahaman tentang bagaimana berbagai variabel mempengaruhi penetapan harga, sehingga memungkinkan pengambilan keputusan yang lebih baik dan mungkin mengoptimalkan strategi penetapan harga.
</p>

---

## Conclusion

**EDA**

Berdasarkan EDA, diantara kedua aplikasi ride-hailing Uber memiliki penggunaan yang lebih banyak dibandingkan dengan Lyft. Orang-orang lebih banyak memesan aplikasi ride-hailing pada jam 11 dan 12 malam. Temperatur rata-ratanya adalah 39°F atau apabila dikonversikan sekitar 3.98°C. Ini dikarenakan dataset diambil pada bulan November dan Desember yang mana ini adalah musim dingin di Kota New York. Namun, pada dataset cuaca ini tidak berkorelasi terhadap harga aplikasi ride-hailing. Yang menentukan naik-turunnya harga adalah jarak, surge multiplier, dan jenis kendaraan. Contohnya, apabila jarak yang ditempuh semakin tinggi maka semakin tinggi juga harganya.

**Model Evaluation**

MSE dan RMSE digunakan karena yang ingin diprediksi adalah harga, yang mana lebih baik tidak ada error untuk memprediksinya.

**Model Analysis**

Hasil MSE dan RMSE menunjukkan bahwa tidak ada perbedaan yang signifikan pada Train-Set dan Test-Set yang menunjukkan bahwa model adalah `Good Fit`. Adapun kelebihan dan kelemahan **Linear Regression**:

* Kelebihan :
1. Mudah untuk diinterpretasikan
2. Dasar untuk metode lainnya
* Kekurangan :
1. Sensitif terhadap outliers
2. Mudah overfit apabila jumlah independent variable-nya banyak.

Untuk improvement selanjutnya, bisa meng-handle outliernya atau coba menggunakan **Polynomial Regression** karena dapat melihat kurva dan pola yang lebih kompleks pada data.
