<div align="center">

### TUGAS 3
### PEMROSESAN CITRA DIGITAL
### (ABKC6306)
 
<img src="lambangULM2021warna.png" alt="drawing" width="200"/> 

### DISUSUN OLEH:
Akhmad Rizki Rahmatullah (2310131210017)
### DOSEN PENGAMPU:
Dr. Harja Santana Purba, M.Kom./Novan A.B. Saputra, S.Kom., M.T

### PROGRAM STUDI PENDIDIKAN KOMPUTER
### FAKULTAS KEGURUAN DAN ILMU PENDIDIKAN
### UNIVERSITAS LAMBUNG MANGKURAT
### 2024
<br>
<br>
<br>

### Pembahasan

#### Pengertian Halftoning

Pemrosesan gambar halftone adalah proses yang umum digunakan untuk mengompresi informasi yang terkandung dalam suatu gambar.Fakta ini memungkinkan untuk mencetak atau menampilkan gambar dalam berbagai format. Contoh penggunaan halftone adalah penerbitan cetak offset, seperti surat kabar, majalah, dan buku. Jenis offset ini paling banyak digunakan di industri untuk menjangkau khalayak dalam skala besar. Dengan menggunakan titik-titik untuk membentuk objek dalam gambar,  persepsi dapat dikelabui dan menampilkan tingkat abu-abu yang berbeda.

Proses halftoning dilakukan melalui gambar dengan mengikuti lintasan dari atas ke bawah dan dari kiri ke kanan. Selama prosedur ini, piksel dievaluasi dengan kernel. Tujuannya adalah untuk mendistribusikan kesalahan P(i,j) karena piksel yang dibinerisasi menghasilkan kesalahan akumulatif. Kesalahan didistribusikan antara lingkungan bawah dan kiri.

#### Method Pada Halftoning
1. **_Error diffusion_**

_Error diffusion_ merupakan salah satu method halftoning yang populer yang mengasumsikan gambar yang diberikan dengan ukuran MxN dalam skala abu-abu, perlakuan setiap piksel dalam pendekatan ini adalah dari atas ke bawah dan dari kiri ke kanan. Teknik ini digunakan untuk mengkompensasi kesalahan pada proses _thresholding_. Berikut ini penjabaran mengenai metode _error diffusion_ oleh Floyd-Steinberg:

![Errror diffusion](errordiffusion.png)

Berikut contoh filter yang dikembangkan oleh Floyd-Steinberg:

![Errror diffusion](errordiffusion2.png)

Keterangan:

![Errror diffusion](errordiffusion_rumus1.png) 
 = _pixel_ pada posisi (i,j) yang diinputkan

![Errror diffusion](errordiffusion_rumus2.png) 
 = penjumlahan dari _input pixel_ dan _diffused error_

![Errror diffusion](errordiffusion_rumus3.png) 
 = _quantized pixel value_

![Errror diffusion](errordiffusion_rumus4.png) 
 = _diffusion filter_ yang dimana ![Errror diffusion](errordiffusion_rumus5.png) 

![Errror diffusion](errordiffusion_rumus6.png) 
 = selisih dari nilai dari _pixel_ baru dengan
_quantized pixel_ value  

2. **_Ordered Dithering_**

_Ordered dithering_ dilakukan dengan membandingkan tiap blok dari citra asli dengan sebuah matriks pembatas (matriks threshold) yang disebut dengan matriks dither. Masing-masing elemen dari blok asli dikuantisasi sesuai dengan nilai batas pada pola dither. Nilai-nilai pada matriks dither adalah tetap, tetapi bisa bervariasi sesuai dengan jenis citra.

Untuk setiap matriks pembatas, terdapat _threshold_ matriks yang sesuai digunakan untuk membuat citra _halftone_. Nilai threshold matriks dapat ditentukan dari pembatas matriks I (i,j) dengan persamaan:

![Ordered Dithering](ordereddithering1.png)

Keterangan:

T(i,j) = Matriks _threshold_

I(i,j) = Matriks pembatas/_dither_

N<sup>2</sup> = Jumlah elemen pada matriks

Citra asli memiliki matriks lebih besar dari pada matriks _threshold_, maka pola dither dilakukan berkala atau secara terus menerus terhadap seluruh _pixel_ citra. Secara spesifik operasi dapat dilihat pada persamaan:

![Ordered Dithering](ordereddithering2.png)

Keterangan:

b(i,j) = Matriks hasil _halftoning_

T(i,j) = Matriks _threshold_

f(i,j) = Matriks citra

<br>
<br>
<br>

### DAFTAR PUSTAKA

Ortega-Sánchez, N, et al. (2020).  An Evolutionary Approach to Improve the Halftoning Process._Mathematics_,  _8(9)_, 1-23.

Raharjo, W. S. & Aguswahyudi, D. (2016). Implementasi Skema Meaningful Sharing pada Kriptografi Visual Berwarna untuk Digital Safe Deposit Box. _ULTIMATICS_, _8(1)_, 16-22.

Stefanus, Tony, & Teny H. (2016). APLIKASI HALFTONE QR-CODE DENGAN METODE ORDERED DITHERING. _Seminar Nasional Sistem Informasi Indonesia_, 353-358.

