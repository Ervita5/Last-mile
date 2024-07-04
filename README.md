# Last-mile
Optimasi Rute Pengiriman Barang pada Tahap _Last Mile_ dengan _Truck-Drone_ Menggunakan Metode _Mean Shift Clustering_ dan Algoritma Genetika

## Permasalahan
Pengiriman barang pada tahap _last mile_ sering dianggap sebagai tahap yang paling mahal dan kurang efisien. _Last mile_ dikatakan mahal karena dari total biaya pengiriman secara keseluruhan (_first mile_, _middle mile_, _last mile_) dapat mencapai 53% (Dolan, 2021). Oleh karena itu, _last mile_ seringkali menjadi fokus utama yang harus diperhatikan dalam optimasi pengiriman barang. Salah satu solusi yang dapat digunakan untuk meningkatkan efektivitas pengiriman ini adalah dengan menggunakan sistem _drone_. Namun, _drone_ memiliki keterbatasan, yaitu radius jangkauan dan kapasitas angkut yang relatif kecil, sehingga 
menjadi pertimbangan yang perlu diatasi. Dengan adanya implementasi sistem _truck-drone_  menggunakan _mean shift clustering_ dan algoritma genetika, diharapkan dapat mengatasi permasalahan tersebut.

## Data Penelitian
Data penelitian yang digunakan meliputi informasi lokasi depot, lokasi pelanggan, armada pengiriman yang tersedia, jarak antar lokasi-lokasi, informasi waktu dan kecepatan pengiriman.

Lokasi pelanggan terdiri dari 90 titik yang mencakup rumah atau tempat yang menjadi tujuan pengiriman paket. Lokasi-lokasi ini tersebar di wilayah Jabodetabek. Diasumsikan bahwa setiap lokasi pelanggan hanya memiliki satu permintaan atau satu paket.

<div align="center">
    <img src="https://github.com/Ervita5/Issue/blob/main/Lokasi%20Pelanggan.png" alt="Customer Locations Map" width="250">
</div>

_Truck_ yang digunakan berjumlah satu dan berbentuk box. _Drone_ yang digunakan berjumlah 15 _drone_ yang homogen dan identik. Jenis _drone_ yang digunakan adalah _drone wings_. Berikut adalah beberapa spesifikasi untuk _drone wings_:

- Panjang drone 1,3 meter, panjang sayap 1 meter, dan berat sekitar 5,2 kg tanpa 
paket.
- Jarak maksimum yang dapat ditempuh oleh drone wings dalam satu misi 
pengiriman adalah 4 km.
65
- Kecepatan rata – rata drone wings dalam melakukan pengiriman adalah 104,4 
km/jam atau sekitar 0,57 menit/km
- Kapasitas muatan yang dapat diangkut oleh drone dalam satu misi pengiriman
adalah 5 kg.

## Hasil dan Diskusi
Dalam membandingkan hasil dari metode _mean shift clustering_ dengan _clustering_ dengan metode _intuitif_ kriteria dalam aspek jumlah cluster diterapkan untuk menilai efektivitas 
keduanya dalam konteks permasalahan _Parking Location Traveling Salesman Problem with Homogenous Drone_ (PLTSPHD).

<div align="center">
    <img src="https://github.com/Ervita5/Issue/blob/main/Clustering.png" alt="Customer Locations Map" width="600">
</div>

Berdasarkan hasil visualisasi pada  gambar di atas terlihat bahwa terdapat perbedaan signifikan dalam jumlah _cluster_ yang dihasilkan oleh keduanya. _Mean shift clustering_ menghasilkan 7 _cluster,_ sementara _clustering_ dengan metode _intuitif_ menghasilkan 19 _cluster_ dan 2 _outlier_. Setelah melakukan proses _clustering_ dan didapatkan _centroid-centroid_, selanjutnya melakukan proses _routing_ untuk mencari rute optimal pengiriman barang menggunakan kendaraan _truck_ dengan metode algoritma genetika. Proses _routing_ diimplementasikan melalui program dengan bahasa _Python_ yang dijalankan pada Google Collab.

<div align="center">
    <img src="https://github.com/Ervita5/Issue/blob/main/Routing.png" alt="Customer Locations Map" width="800">
</div>

Membangkitkan populasi awal terlebih dahulu menggunakan ANN (_All Nearest Neighbors_). Didapatkan rute 0 – 2 – 5 – 1 – 6 – 3 – 7 – 4 – 0, menunjukkan jarak terpendek dengan nilai 55,42 km. 

Proses algoritma genetika dalam program dengan bahasa python dijalankan sebanyak 100 generasi. Setelah 100 generasi didapatkan solusi rute optimal yaitu 0 – 5 – 2 – 1 – 6 – 3 – 7 – 4 – 0 dengan nilai fitness 0,018440002685214583 dan total jarak 54,22 km.

Solusi ini lebih baik dibandingkan solusi yang diperoleh melalui metode ANN namun tidak terlalu signifikan.

<div align="center">
    <img src="https://github.com/Ervita5/Issue/blob/main/Grafik%20Perbandingan.png" alt="Customer Locations Map" width="800">
</div>

Pada data ini, penggunaan _mean shift clustering_ tampaknya lebih efisien dalam  membentuk kelompok data. Hal ini ditunjukan dari penurunan jumlah _cluster_ yang dihasilkan oleh metode _mean shift clustering_ sebesar 63% dibandingkah metode _intuitif_. Jumlah _cluster_ yang lebih sedikit yang dihasilkan dapat dianggap menguntungkan dalam konteks permasalahan PLTSPHD yang menekankan minimalisasi biaya transportasi. Berdasarkan gambar diatas _mean shift clustering_ menghasilkan biaya yang lebih efisien dibandingkan dengan metode _intutif_. Hal ini ditunjukan dari penurunan biaya _mean shift clustering_ sebesar 3,51 %. Selain itu, hasil juga menunjukkan bahwa _mean shift clustering_ dapat mengurangi total jarak sebesar 27,93% dan waktu tempuh 25,83 %. dibandingkan metode _intuitif_.



## Kesimpulan
Permasalahan pengiriman barang dengan sistem _truck-drone_ pada tahap _last mile_ dapat dimodelkan menjadi _Parking Location Traveling Salesman Problem with Homogenous Drone_ (PLTSPHD) dengan memperhatikan kendala jangkauan maksimum terbang _drone_ dan jam kerja pengiriman harian. Implementasi metode _mean shift clustering_ pada model PLTSPHD menghasilkan identifikasi _cluster_ yang optimal untuk pelanggan. Hasil eksperimen menunjukkan keefisienan metode ini dalam membentuk kelompok data dan menemukan lokasi parkir optimal. Kombinasi _mean shift clustering_ dan algoritma genetika membuktikan keunggulannya dalam mengoptimalkan rute pada konteks PLTSPHD. Keseluruhan, penelitian ini memberikan kontribusi positif dalam meningkatkan efisiensi 
pengiriman barang dengan memanfaatkan pendekatan clustering dan algoritma genetika.
