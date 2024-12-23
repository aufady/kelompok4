![Gambar 1](https://github.com/aufady/kelompok4_Project_SPS/blob/main/Tampilan%20GUI%20suara%20dari%20speaker%20berfungsi%20normal.PNG)  
*Tampilan Qt Designer Hasil Rekaman Suara dari Speaker Laptop yang Berfungsi Normal*

![Gambar 2](https://github.com/aufady/kelompok4_Project_SPS/blob/main/Tampilan%20GUI%20suara%20dari%20speaker%20laptop%20rusak.PNG)  
*Tampilan Qt Designer Hasil Rekaman Suara dari Speaker Laptop yang Rusak*

# Pendeteksian Kerusakan Speaker Laptop Melalui Analisis Sinyal Suara

Proyek ini mengembangkan sebuah aplikasi berbasis PyQt5 untuk mendeteksi kerusakan pada speaker laptop melalui analisis sinyal suara. Aplikasi ini memungkinkan pengguna merekam suara dari speaker laptop, memvisualisasikan pola sinyal dalam domain waktu dan domain frekuensi melalui antarmuka GUI yang dirancang menggunakan Qt Designer, serta menganalisis perbedaan karakteristik antara speaker yang berfungsi normal dan yang rusak. Data suara dapat terunggah secara otomatis ke platform Edge Impulse untuk pelatihan model machine learning.

## Authors
1. Zudan Rizky Aditya (2042231007)  
2. Muhammad Aufa Affandi (2042231011)  
3. Ziyad Zakiy Permana (2042231077) 
4. Ahmad Radhy (Supervisor)

Teknik Instrumentasi - Institut Teknologi Sepuluh Nopember Surabaya

## Features

1. **Voice Recording**: Rekam sinyal suara speaker laptop secara real-time.
2. **Real-Time Visualization**:  
   - **Domain Waktu**: Menampilkan pola amplitudo sinyal terhadap waktu.  
   - **Domain Frekuensi**: Menganalisis spektrum frekuensi menggunakan Discrete Fourier Transform (DFT).  
3. **Audio Playback**: Memutar ulang rekaman untuk verifikasi.  
4. **Data Upload**: Unggah data rekaman ke platform Edge Impulse untuk pelatihan model.

## Requirements

### Software
1. Python 3.8+
2. Visual studio code dan Qt Designer (untuk menulis dan menjalankan kode yang diperlukan supaya menampilkan sinyal dalam domain waktu dan domain frekuensi (DFT).
3. Platform Edge Impulse (untuk mengelola dataset, melakukan pra-pemrosesan sinyal, dan melatih model pembelajaran mesin untuk klasifikasi suara).
4. PyQt5
5. Sounddevice
6. Pyqtgraph
7. Wavio
8. Requests (untuk unggah data ke Edge Impulse)

### Hardware
- Dua laptop
- Speaker laptop (salah satu laptop harus memiliki speaker yang berfungsi dengan
baik dan laptop lainnya memiliki speaker yang tidak berfungsi atau rusak untuk
membedakan sumber suara)
- Earphone (digunakan untuk merekam suara secara lebih jelas dan mengurangi
gangguan noise dari lingkungan)

### Mekanisme Urutan
1.	Memastikan semua perangkat, termasuk laptop, earphone, dan koneksi internet untuk menggunakan platform Edge Impulse, telah siap.
2.	Membuka Qt Designer untuk membuat antarmuka dengan elemen-elemen seperti tombol rekam, tombol putar ulang, serta dua grafik untuk menampilkan sinyal dalam domain waktu dan domain frekuensi (DFT).
3.	Membuka Visual Studio Code yang sudah berisi kode untuk menampilkan sinyal dalam domain waktu dan domain frekuensi (DFT) pada GUI yang dirancang dengan Qt Designer. Pastikan kode ini telah terhubung dengan Qt Designer dan Edge Impulse.
4.	Memasukkan API key dan Project ID pada kode di Visual Studio Code agar data rekaman dapat dikirim dan masuk ke dataset di platform Edge Impulse.
5.	Menjalankan kode untuk merekam suara dari speaker laptop yang berfungsi dan yang rusak, serta memastikan data berhasil dikirim ke Edge Impulse.
6. Melakukan pra-pemrosesan sinyal di platform Edge Impulse dengan mengubah
hasil rekaman suara menjadi spektrogram atau menggunakan metode MFCC (Mel
Frequency Cepstral Coefficients) untuk ekstraksi fitur yang lebih relevan.
7. Gunakan dataset yang sudah diproses untuk melatih model machine learning yang
dapat mengenali pola suara dari kedua jenis speaker (yang berfungsi dan rusak).
8. Evaluasi akurasi dan performa klasifikasi model dengan menggunakan dataset
untuk memastikan model dapat mengenali pola suara dengan baik.

## Installation

### 1. Clone the Repository
```bash
git clone https://github.com/aufady/kelompok4_Project_SPS 
```

### 2. Install Python Dependencies
```bash
pip install PyQt5 sounddevice pyqtgraph wavio requests
```

## Usage

### 1. Run the Application
Jalankan aplikasi GUI:
```bash
python main.py
```

### 2. Record Audio
-Klik tombol "Start Recording" untuk merekam suara speaker laptop.

-Visualisasi sinyal akan diperbarui secara real-time dalam domain waktu dan frekuensi.

### 3. Save and Analyze
- Rekaman suara disimpan dalam format WAV.
- Data suara dapat terunggah ke Edge Impulse untuk melatih model machine learning.

### 4. Playback
- Gunakan tombol "Replay Audio" untuk memutar ulang rekaman

## Project Structure
```
speaker-damage-detection/
├── main.py             # PyQt5 GUI Application
├── recorder.py         # Audio recording and processing logic
├── edge_impulse.py     # Integration with Edge Impulse API
├── visualizer.py       # Logic for real-time visualization
├── recordings/         # Directory for saved audio files
├── README.md           # Project documentation
└── LICENSE             # Project license
```

## Future Improvements
- Tambahkan fitur untuk analisis lebih mendalam, seperti deteksi noise atau spektrum harmonik.
- Kembangkan model machine learning untuk meningkatkan akurasi deteksi kerusakan.
- Integrasikan sistem untuk penggunaan real-time dalam diagnosa perangkat audio.

## Contributions
Kontribusi untuk memperbaiki atau mengembangkan proyek ini sangat diterima. Silakan fork repository ini dan kirimkan pull request Anda.

## License
Proyek ini dilisensikan di bawah Lisensi MIT. Lihat file LICENSE untuk detailnya.
