# Last-mile
Optimasi Rute Pengiriman Barang pada Tahap Last Mile dengan Truck-Drone Menggunakan Metode Mean Shift Clustering dan Algoritma Genetika

## Data Penelitian
Data penelitian yang digunakan meliputi informasi lokasi depot, lokasi pelanggan, 
armada pengiriman yang tersedia, jarak antar lokasi-lokasi, informasi waktu dan kecepatan 
pengiriman.

Lokasi pelanggan terdiri dari 90 titik yang mencakup rumah atau tempat yang menjadi tujuan pengiriman paket. Lokasi-lokasi ini tersebar di wilayah Jabodetabek. Diasumsikan bahwa setiap lokasi pelanggan hanya memiliki satu permintaan atau satu paket.

<div align="center">
    <img src="https://github.com/Ervita5/Issue/blob/main/Screenshot%20(92).png" alt="Customer Locations Map" width="250">
</div>

## Permasalahan
Pengiriman barang pada tahap last mile sering dianggap sebagai tahap yang paling mahal 
dan kurang efisien. Last mile dikatakan mahal karena dari total biaya pengiriman secara 
keseluruhan (first mile, middle mile, last mile) dapat mencapai 53% (Dolan, 2021). Oleh 
karena itu, last mile menjadi fokus utama yang perlu diperhatikan dalam optimasi 
pengiriman barang. Penggunaan sistem drone dalam last mile delivery merupakan salah 
satu solusi untuk meningkatkan efektivitas pengiriman ini. Namun, drone memiliki 
keterbatasan, yaitu radius jangkauan dan kapasitas angkut yang relatif kecil, sehingga 
menjadi pertimbangan yang perlu diatasi. Dengan adanya implementasi sistem truckdrone dan optimasi pengiriman PLTSPHD menggunakan mean shift clustering dan 
algoritma genetika, diharapkan dapat mengatasi permasalahan tersebut.

## Hasil dan Diskusi



## Kesimpulan
Permasalahan pengiriman barang dengan sistem truck-drone pada tahap last mile dapat 
dimodelkan menjadi Parking Location Traveling Salesman Problem with Homogenous Drone
(PLTSPHD) dengan memperhatikan kendala jangkauan maksimum terbang drone dan jam kerja 
pengiriman harian. Implementasi metode mean shift clustering pada model PLTSPHD 
menghasilkan identifikasi cluster yang optimal untuk pelanggan. Hasil eksperimen 
menunjukkan keefisienan metode ini dalam membentuk kelompok data dan menemukan lokasi 
parkir optimal. Kombinasi mean shift clustering dan algoritma genetika 
membuktikan keunggulannya dalam mengoptimalkan rute pada konteks PLTSPHD. 
Keseluruhan, penelitian ini memberikan kontribusi positif dalam meningkatkan efisiensi 
pengiriman barang dengan memanfaatkan pendekatan clustering dan algoritma genetika.
