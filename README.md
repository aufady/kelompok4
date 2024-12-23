(Aplikasi Qt nya belum diupload)

Peralatan & Bahan 
Peralatan yang dibutuhkan untuk mini project ini adalah :
1. Dua laptop.
2. Speaker laptop (salah satu laptop harus memiliki speaker yang berfungsi dengan
baik dan laptop lainnya memiliki speaker yang tidak berfungsi atau rusak untuk
membedakan sumber suara).
3. Earphone (digunakan untuk merekam suara secara lebih jelas dan mengurangi
gangguan noise dari lingkungan).
4. Software visual studio code dan Qt Designer (untuk menulis dan menjalankan kode yang diperlukan supaya menampilkan sinyal dalam domain waktu dan domain frekuensi (DFT).
5. Platform Edge Impulse (untuk mengelola dataset, melakukan pra-pemrosesan sinyal, dan melatih model pembelajaran mesin untuk klasifikasi suara).

Mekanisme Urutan Kerja :
1.	Memastikan semua perangkat, termasuk laptop, earphone, dan koneksi internet untuk menggunakan platform Edge Impulse, telah siap.
2.	Membuka Qt Designer untuk membuat antarmuka dengan elemen-elemen seperti tombol rekam, tombol putar ulang, serta dua grafik untuk menampilkan sinyal dalam domain waktu dan domain frekuensi (DFT).
3.	Membuka Visual Studio Code yang sudah berisi kode untuk menampilkan sinyal dalam domain waktu dan domain frekuensi (DFT) pada GUI yang dirancang dengan Qt Designer. Pastikan kode ini telah terhubung dengan Qt Designer dan Edge Impulse.
4.	Memasukkan API key dan Project ID pada kode di Visual Studio Code agar data rekaman dapat dikirim dan masuk ke dataset di platform Edge Impulse.
5.	Menjalankan kode untuk merekam suara dari speaker laptop yang berfungsi dan yang rusak, serta memastikan data berhasil dikirim ke Edge Impulse.
6. Melakukan pra-pemrosesan sinyal di platform Edge Impulse dengan mengubah hasil rekaman suara menjadi spektrogram atau menggunakan metode MFCC (Mel Frequency Cepstral Coefficients) untuk ekstraksi fitur yang lebih relevan.
7. Gunakan dataset yang sudah diproses untuk melatih model machine learning yang dapat mengenali pola suara dari kedua jenis speaker (yang berfungsi dan rusak).
8. Evaluasi akurasi dan performa klasifikasi model dengan menggunakan dataset untuk memastikan model dapat mengenali pola suara dengan baik.
