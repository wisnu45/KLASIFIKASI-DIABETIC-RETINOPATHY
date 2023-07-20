Studi kasus ini berdasarkan pada dataset Kaggle. - https://www.kaggle.com/c/aptos2019-blindness-detection/


This Research paper is summarized in the Research paper (summary doc).pdf

Contents of the Code Files are given below :-

| S No | Section  | Notebook (.ipynb) | Description | 
| ----  | --------- | --------- | --------- |
| 1 | Exploratory Data Analysis | 1_eda.ipynb | All Data Analysis & Insights on Images and classes |
| 2 | Image processing, Train/validation data | 2_process.ipynb | Image Resizing,preprocessing,data splitting |
| 3 | Transfer Learning using ResNet50 | 3_resnet50(colab).ipynb | Complete Model and Evaluation |
| 4 | Model ResNet50 224x224x3 | ResNet50_224x224x3.ipynb | PENERAPAN DEEP LEARNING MENGGUNAKAN CONVOLUTIONAL NEUTRAL NETWORK (CNN) UNTUK KLASIFIKASI DIABETIC RETINOPATHY |

DIAGRAM ALIR KERJA SISTEM
![Diagram Alir Kerja Sistem](https://github.com/wisnu45/KLASIFIKASI-DIABETIC-RETINOPATHY/assets/45603735/93f51aa2-a261-4dd1-9ff4-89ced578f512)

Pada tahap pembelajaran fitur ini, langkah pertama yang dilakukan yaitu menentukan ukuran matriks H dari nilai stride yang ditentukan menggunakan Persamaan. Pada perhitungan kali ini menggunakan ResNet50. Matriks citra input I berukuran 224 x 224 x 3 dengan padding = 3 dan stride = 2, matriks filter K berukuran 7 x 7 sebanyak 64. Matriks filter ini merupakan default dari arsitektur ResNet, dimana bobot pada matriks kernel merupakan filter yang optimal dengan edge detection pada suatu citra. Representasi matriks I dengan penambahan padding = 3 

uH = [(224 -7 + 2(3) ) / 2] + 1

Rumus yang digunakan adalah uH = [(I - K + 2P) / S] + 1, dengan nilai-nilai yang diberikan adalah I = 224, K = 7, P = 3, dan S = 2 
Ukuran matrik H dihitung seperti berikut: 
uH 	= 224-7+2(3)2+1
		= 2232+1
    = 112.5
Namun, karena ukuran feature map haruslah bilangan bulat, maka perlu membulatkannya. Dalam hal ini, akan membulatkannya ke bawah menjadi 112. Jadi, ukuran feature map yang diperoleh setelah melakukan konvolusi dengan parameter adalah 112 X 112.  
![image](https://github.com/wisnu45/KLASIFIKASI-DIABETIC-RETINOPATHY/assets/45603735/47f46df8-fd78-487b-b04b-79a7605dd38b)


AKURASI EFOCH 
![image](https://github.com/wisnu45/KLASIFIKASI-DIABETIC-RETINOPATHY/assets/45603735/f454578e-d713-4c62-8aba-0a7d19cb5c2f)

CONFUSION MATRIX

![image](https://github.com/wisnu45/KLASIFIKASI-DIABETIC-RETINOPATHY/assets/45603735/438fee0e-ed28-4437-bba5-e4e63136e392)

Countplot Distribusi Kelas Prediksi
![image](https://github.com/wisnu45/KLASIFIKASI-DIABETIC-RETINOPATHY/assets/45603735/51124e8a-862b-468c-b0d8-b7acd054883b)

Tabel Hasil Matrik Evaluasi Agregat Untuk Confusion Matrix
![image](https://github.com/wisnu45/KLASIFIKASI-DIABETIC-RETINOPATHY/assets/45603735/48f7ab71-6adc-4eb6-b77c-8152c3f3c28e)
Metrik evaluasi agregat dari confusion matrix menunjukkan bahwa model memiliki akurasi sekitar 95.1%, yang menggambarkan kemampuan model dalam mengklasifikasikan data secara benar secara keseluruhan. Namun, presisi rata-rata sekitar 57.7% menunjukkan bahwa model memiliki tingkat keakuratan yang lebih rendah dalam memberikan prediksi yang tepat untuk setiap kelas. Meskipun demikian, recall rata-rata mencapai sekitar 80.0%, menunjukkan bahwa model dapat mengidentifikasi dan menangkap sampel positif dengan baik. F1-score rata-rata sekitar 63.6% memberikan gambaran keseluruhan tentang kinerja model, yang mencerminkan keseimbangan antara presisi dan recall. Meskipun akurasi cukup tinggi, peningkatan presisi dan F1-score untuk beberapa kelas mungkin diperlukan. Evaluasi lebih lanjut dan penyesuaian model mungkin diperlukan untuk meningkatkan kinerja dalam mengklasifikasikan kelas-kelas yang memiliki presisi dan F1-score yang lebih rendah. 

Gambar Hasil Klasifikasi DR kelas 0-4 dengan Model ResNet50 244x224x3
![image](https://github.com/wisnu45/KLASIFIKASI-DIABETIC-RETINOPATHY/assets/45603735/a4ff040a-7979-4e78-9ce0-b828d15a1059)

