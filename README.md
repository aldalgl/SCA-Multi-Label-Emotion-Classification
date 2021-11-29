### STA-Multi-Label-Emotion-Classification

# Analysis Emotion Of Comment Topic Reddit With Multi-label Classification Using SVM Algorithm

## Deskripsi proyek
* Menilai kualitas komentar yang diposting pada reddit dengan emotion analysis
* Acuan bagi para redditors untuk memposting konten yang baik, membuat komentar yang bermanfaat dan juga memberikan umpan balik yang relevan [Anderson (2015)]
* Memahami opini publik dapat membantu kreator dalam mengambil keputusan [Jitendra Kumar (2018)]

## Latar Belakang
Proyek ini akan menggunakan metode klasifikasi Support Vector Machine (SVM). Pada dasarnya SVM digunakan untuk menentukan decision boundary atau hyperplane antar dua kelas, sehingga akan menjadi tantangan apabila diimplementasikan pada multilabel classification karena secara native cara kerja pengklasifikasian SVM berbeda dengan klasifikasi multilabel. Sehingga, untuk mengatasi tantangan tersebut dapat digunakan NB-SVM (Naive Bayes - Suport Vector Machine) dengan Logistic Regression oleh machine learning open source library berbasis python yaitu Scikit-learn. Strategi ini merupakan pengklasifikasian multi target yang dapat digunakan untuk mendukung klasifikasi multilabel dengan SVM.

## Tujuan
* Berkontribusi memecahkan tantangan multilabel classification menggunakan metode SVM.
* Menerapkan metode SVM dalam menganalisis emosi pada komentar di reddit dengan multilabel classification.
* Untuk mengetahui bagaimana tingkat akurasi menggunakan metode SVM dalam melakukan emotion analysis.

### Adapun tahap implementasi yang dilakukan yaitu:
* Data preparation
* Data Cleaning
  * Pengecekan terhadap data null
  * Menghapus nilai yang sama/unnique pada dataset
  * Drop atribut yang tidak dibutuhkan
* Text Preprocessing
  * Case folding
  * Removal of punctuation
  * Stopwords Removal
  * Stemming
  * Lemmatization
* Feature Extraction menggunakan TF IDF
* Modling with SVM dengan komposisi pembagian 80% data train dan 20% data set
* Kemudian, melakukan evaluasi untuk menghitung _confussion matrix_ terhadap 27 label emosi yang akan diprediksi.

### Kesimpulan
Proyek ini menganalisis emosi komentar pada platform reddit dengan multi-label classification menggunakan algoritma SVM. Data set semula terbagi atas 3 dokumen .csv yang digabungkan dengan 211225 rows. Kemudian data dibersihkan dengan pengecekan data null, penghapusan nilai yang sama/ununique, dan memisahkan atribut yang tidak dibutuhkan. Kemudian  pada text processing dilakukan case folding, removal of punctuation, stopwords removal, stemming,dan lemmatization. Dilanjutkan kembali dengan melakukan feature extraction terhadap teks komentar menggunakan TF IDF dan modeling. Pada modeling dataset dibagi atas 80% data train dan 20% data test, dan dibangun dengan NB-SVM dengan Logistic Regression oleh machine learning open source library berbasis python untuk menangani pengkalsifikasian multilabel. Meskipun NB-SVM dapat menyelesaikan pengkalsifikasian multilabel tetapi nilai akurasi sangat rendah yaitu  0.04918925316605515. Rendahnya nilai akurasi ini disebabkan oleh label yang digunakan berjumlah cukup banyak yaitu 27 label, sehingga tingkat akurasi model yang dihasilkan sangat rendah.

### Referensi 
[1] Anderson, "Ask me anything: what is Reddit?," Library Hi Tech News, vol. 32, pp. 8-11, 2015. 
[2] S. Aman and S. S. , "Identifying expressions of emotion in text," in International Conference on Text, Speech and Dialogue, Springer, Berlin, Heidelberg, 2007. 
[3] J. K. Rout, "A model for sentiment and emotion analysis of unstructured social media text," Electron Commer Res , no. 18, pp. 181-199, 2017. 
[4] K. I. Gunawan and J. Santoso, "Multilabel Text Classification Menggunakan SVM dan Doc2Vec Classification pada Dokumen Berita Bahasa Indonesia," Journal of Information System, Graphics, Hospitality and Technology, vol. 3, no. 1, pp. 29-38, 2021. 
[5] JEREMY HOWARD. (2018, February). NB-SVM strong linear baseline. Retrieved December 29, 2021 from https://www.kaggle.com/jhoward/nb-svm-strong-linear-baseline.

