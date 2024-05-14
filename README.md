# Last-mile
Optimasi Rute Pengiriman Barang pada Tahap _Last Mile_ dengan _Truck-Drone_ Menggunakan Metode _Mean Shift Clustering_ dan Algoritma Genetika

## Data Penelitian
Data penelitian yang digunakan meliputi informasi lokasi depot, lokasi pelanggan, 
armada pengiriman yang tersedia, jarak antar lokasi-lokasi, informasi waktu dan kecepatan 
pengiriman.

Lokasi pelanggan terdiri dari 90 titik yang mencakup rumah atau tempat yang menjadi tujuan pengiriman paket. Lokasi-lokasi ini tersebar di wilayah Jabodetabek. Diasumsikan bahwa setiap lokasi pelanggan hanya memiliki satu permintaan atau satu paket.

<div align="center">
    <img src="https://github.com/Ervita5/Issue/blob/main/Screenshot%20(92).png" alt="Customer Locations Map" width="250">
</div>

## Permasalahan
Pengiriman barang pada tahap _last mile _sering dianggap sebagai tahap yang paling mahal 
dan kurang efisien. _Last mile_ dikatakan mahal karena dari total biaya pengiriman secara 
keseluruhan (_first mile_, _middle mile_, _last mile_) dapat mencapai 53% (Dolan, 2021). Oleh 
karena itu, _last mile_ menjadi fokus utama yang perlu diperhatikan dalam optimasi 
pengiriman barang. Penggunaan sistem _drone_ dalam _last mile delivery_ merupakan salah 
satu solusi untuk meningkatkan efektivitas pengiriman ini. Namun, _drone _memiliki 
keterbatasan, yaitu radius jangkauan dan kapasitas angkut yang relatif kecil, sehingga 
menjadi pertimbangan yang perlu diatasi. Dengan adanya implementasi sistem _truck-drone_  menggunakan _mean shift clustering_ dan algoritma genetika, diharapkan dapat mengatasi permasalahan tersebut.

## Hasil dan Diskusi


<div align="center">
    <img src="https://github.com/Ervita5/Issue/blob/main/Grafik%20Perbandingan.png" alt="Customer Locations Map" width="800">
</div>

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
