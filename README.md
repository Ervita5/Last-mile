# Last-mile
Optimasi Rute Pengiriman Barang pada Tahap _Last Mile_ dengan _Truck-Drone_ Menggunakan Metode _Mean Shift Clustering_ dan Algoritma Genetika

## Data Penelitian
Data penelitian yang digunakan meliputi informasi lokasi depot, lokasi pelanggan, 
armada pengiriman yang tersedia, jarak antar lokasi-lokasi, informasi waktu dan kecepatan 
pengiriman.

Lokasi pelanggan terdiri dari 90 titik yang mencakup rumah atau tempat yang menjadi tujuan pengiriman paket. Lokasi-lokasi ini tersebar di wilayah Jabodetabek. Diasumsikan bahwa setiap lokasi pelanggan hanya memiliki satu permintaan atau satu paket.

<div align="center">
    <img src="https://github.com/Ervita5/Issue/blob/main/Lokasi%20Pelanggan.png" alt="Customer Locations Map" width="250">
</div>

## Permasalahan
Pengiriman barang pada tahap _last mile_ sering dianggap sebagai tahap yang paling mahal 
dan kurang efisien. _Last mile_ dikatakan mahal karena dari total biaya pengiriman secara 
keseluruhan (_first mile_, _middle mile_, _last mile_) dapat mencapai 53% (Dolan, 2021). Oleh 
karena itu, _last mile_ menjadi fokus utama yang perlu diperhatikan dalam optimasi 
pengiriman barang. Penggunaan sistem _drone_ dalam _last mile delivery_ merupakan salah 
satu solusi untuk meningkatkan efektivitas pengiriman ini. Namun, _drone_ memiliki 
keterbatasan, yaitu radius jangkauan dan kapasitas angkut yang relatif kecil, sehingga 
menjadi pertimbangan yang perlu diatasi. Dengan adanya implementasi sistem _truck-drone_  menggunakan _mean shift clustering_ dan algoritma genetika, diharapkan dapat mengatasi permasalahan tersebut.

## Hasil dan Diskusi
Dalam membandingkan hasil dari metode _mean shift clustering_ dengan _clustering_ dengan 
metode intuitif kriteria dalam aspek jumlah cluster diterapkan untuk menilai efektivitas 
keduanya dalam konteks permasalahan _Parking Location Traveling Salesman Problem with Homogenous Drone_ (PLTSPHD).

<div align="center">
    <img src="https://github.com/Ervita5/Issue/blob/main/Clustering.png" alt="Customer Locations Map" width="800">
</div>
Berdasarkan hasil visualisasi pada  gambar di atas terlihat bahwa terdapat perbedaan signifikan dalam jumlah cluster yang dihasilkan oleh keduanya. Mean shift clustering menghasilkan 7 cluster, sementara solusi clustering dengan metode intuitif menghasilkan 19 cluster dan 2 outlier.

<div align="center">
    <img src="https://github.com/Ervita5/Issue/blob/main/Grafik%20Perbandingan.png" alt="Customer Locations Map" width="800">
</div>

Pada data ini, penggunaan mean shift clustering tampaknya lebih efisien dalam  membentuk kelompok data. Hal ini ditunjukan dari penurunan jumlah cluster yang dihasilkan oleh metode mean shift clustering sebesar 63% dibandingkahn metode intuitif. Jumlah cluster yang lebih sedikit yang dihasilkan dapat dianggap menguntungkan dalam konteks permasalahan PLTSPHD yang menekankan minimalisasi biaya transportasi. Berdasarkan gambar diatas mean shift clustering menghasilkan biaya yang lebih efisien dibandingkan dengan metode intutif. Hal ini ditunjukan dari penurunan biaya mean shift clustering sebesar 3,51 %. Selain itu, hasil juga menunjukkan bahwa mean shift clustering dapat mengurangi total jarak sebesar 27,93% dan waktu tempuh 
25,83 %. dibandingkan metode intuitif.

## Kesimpulan
Permasalahan pengiriman barang dengan sistem _truck-drone_ pada tahap _last mile_ dapat 
dimodelkan menjadi _Parking Location Traveling Salesman Problem with Homogenous Drone_
(PLTSPHD) dengan memperhatikan kendala jangkauan maksimum terbang _drone_ dan jam kerja 
pengiriman harian. Implementasi metode _mean shift clustering_ pada model PLTSPHD 
menghasilkan identifikasi _cluster_ yang optimal untuk pelanggan. Hasil eksperimen 
menunjukkan keefisienan metode ini dalam membentuk kelompok data dan menemukan lokasi 
parkir optimal. Kombinasi _mean shift clustering_ dan algoritma genetika 
membuktikan keunggulannya dalam mengoptimalkan rute pada konteks PLTSPHD. 
Keseluruhan, penelitian ini memberikan kontribusi positif dalam meningkatkan efisiensi 
pengiriman barang dengan memanfaatkan pendekatan clustering dan algoritma genetika.
