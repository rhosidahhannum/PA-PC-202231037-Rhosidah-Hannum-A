
# Deteksi Tepi Pola Objek

Deteksi tepi adalah salah satu teknik penting dalam pengolahan citra yang digunakan untuk mengidentifikasi perubahan tajam dalam intensitas piksel. Yang membantu dalam memisahkan objek dari latar belakangnya atau dalam analisis struktur objek dalam citra.

### Pengenalan Deteksi Tepi
Deteksi tepi dalam pengolahan citra adalah proses kritis untuk menemukan lokasi perubahan tajam dalam intensitas piksel, yang mengindikasikan batas-batas atau kontur objek dalam citra. Perubahan tersebut menandai transisi yang signifikan antara objek dan latar belakang atau antara bagian-bagian yang berbeda dari objek yang sama. Dengan mengidentifikasi tepi, kita dapat menyoroti struktur geometris, tekstur, atau fitur lain yang penting dalam citra, memungkinkan analisis yang lebih mendalam terhadap properti dan karakteristik objek yang diamati. Deteksi tepi memiliki peran penting dalam segmentasi citra, pengenalan pola, dan aplikasi lain yang memerlukan pemahaman detail tentang struktur visual dari objek dalam citra digital.
### Tujuan Deteksi Tepi dalam Pengolahan citra
- **Segmentasi Citra**: Deteksi tepi membantu memisahkan objek dari latar belakang dalam citra. Ini sangat penting dalam aplikasi seperti pengenalan objek dan pemrosesan citra medis, di mana kita perlu mengidentifikasi dan memisahkan bagian-bagian yang berbeda dari gambar untuk analisis lebih lanjut.
- **Mengidentifikasi Struktur Objek**: Dengan menemukan tepi atau batas-batas objek dalam citra, kita dapat mengidentifikasi struktur geometris atau tekstur yang ada. Misalnya, dalam pengenalan wajah, deteksi tepi dapat membantu dalam menentukan lokasi mata, hidung, dan mulut.
- **Ekstraksi Fitur**: Tepi dalam citra sering kali menunjukkan perubahan tajam dalam intensitas piksel, yang dapat digunakan sebagai fitur untuk analisis lebih lanjut seperti pengenalan pola atau klasifikasi objek.
- **Meningkatkan Presisi Segmentasi**: Dengan memisahkan objek dan latar belakang dengan lebih baik melalui deteksi tepi, kita dapat meningkatkan presisi segmentasi citra. Ini membantu dalam pengolahan citra untuk aplikasi seperti penglihatan mesin atau analisis medis, di mana ketepatan dalam memisahkan elemen-elemen objek sangat penting.
- **Reduksi Informasi**: Deteksi tepi juga dapat digunakan untuk mengurangi jumlah informasi yang tidak relevan atau noise dalam citra. Dengan fokus pada fitur-fitur yang penting seperti tepi, kita dapat meningkatkan efisiensi dalam analisis dan pengolahan selanjutnya.
###  Metode Deteksi Tepi
**1. Metode Sobel**: Menggunakan operator Sobel untuk menghitung gradien citra secara horizontal dan vertikal. Operator Sobel ini mengaplikasikan kernel konvolusi untuk mengekstraksi perubahan tajam dalam intensitas piksel di sekitar setiap titik dalam citra.
Metode Prewitt: Serupa dengan Sobel, menggunakan kernel Prewitt untuk menghitung gradien citra. Kernel ini juga bekerja dalam arah horizontal dan vertikal, menyoroti perbedaan intensitas piksel yang signifikan.

**2.Metode Prewitt**: Serupa dengan Sobel, menggunakan kernel Prewitt untuk menghitung gradien citra. Kernel ini juga bekerja dalam arah horizontal dan vertikal, menyoroti perbedaan intensitas piksel yang signifikan.

**3. Metode Canny**: Menggunakan beberapa langkah proses, termasuk filter Gaussian untuk mengurangi noise, perhitungan gradien untuk menemukan arah perubahan tajam, non-maximum suppression untuk menyaring tepi maksimal, dan hysteresis thresholding untuk mempertahankan tepi yang signifikan.

**4.Metode Laplacian of Gaussian (LoG)**: Menggabungkan operasi Laplacian dengan Gaussian blur. Langkah ini menghasilkan citra yang di-blur terlebih dahulu untuk mengurangi noise, diikuti dengan deteksi tepi menggunakan operator Laplacian untuk menemukan titik maksimum perubahan kedua dalam intensitas piksel.
### Aplikasi Deteksi Tepi dalam Pengolahan Citra
Deteksi tepi memiliki berbagai aplikasi penting, termasuk:
- **Segmentasi Citra**: Memisahkan objek dari latar belakang.Dengan menemukan tepi atau batas-batas objek, kita dapat membuat maska atau region-of-interest (ROI) yang memungkinkan untuk fokus pada area tertentu dalam citra untuk analisis lebih lanjut. Ini penting dalam aplikasi seperti pengenalan objek, segmentasi medis, dan robotika.
- **Pengenalan Objek**: Membantu dalam pengenalan pola dan pengklasifikasian objek.Dengan mengidentifikasi dan memisahkan fitur-fitur penting menggunakan deteksi tepi, sistem dapat membedakan antara objek dan latar belakang dengan lebih baik. Misalnya, dalam visi komputer untuk pengenalan wajah, deteksi tepi digunakan untuk menemukan garis-garis karakteristik seperti tepi mata, hidung, dan mulut.
- **Peningkatan Kualitas Citra**: Mengurangi noise dan meningkatkan kejelasan objek dalam citra.Dengan menyoroti perubahan tajam dalam intensitas piksel, deteksi tepi membantu dalam memisahkan sinyal yang relevan dari noise atau gangguan dalam citra. Ini bisa dilakukan dengan menerapkan filter Gaussian sebelum deteksi tepi untuk meratakan citra dan menghilangkan noise, sehingga memperbaiki kualitas gambar yang dihasilkan.
### Tantangan dan Pertimbangan
**1. Noise**:Deteksi tepi rentan terhadap noise atau gangguan dalam citra. Noise dapat muncul dari berbagai sumber, seperti sensor citra yang tidak sempurna atau kondisi pencahayaan yang buruk.Noise dapat mempengaruhi akurasi deteksi tepi dengan memunculkan tepi palsu atau mengaburkan tepi yang sebenarnya. Ini dapat mengurangi kualitas segmentasi objek dan analisis citra secara keseluruhan.

**2. Parameter**:engaturan parameter seperti threshold sangat penting dalam deteksi tepi. Threshold digunakan untuk menentukan apakah perbedaan intensitas antara dua piksel akan dianggap sebagai tepi atau bukan. Pemilihan threshold yang tidak tepat bisa menghasilkan deteksi tepi yang tidak akurat atau kehilangan informasi tepi yang relevan. Oleh karena itu, memahami karakteristik citra dan melakukan penyetelan parameter secara cermat sangat penting untuk mencapai hasil yang diinginkan.

**3. Orientasi**:Beberapa metode deteksi tepi mungkin lebih cocok untuk menangkap tepi dalam orientasi tertentu, seperti vertikal atau horizontal.Orientasi tepi yang signifikan dalam citra dapat mempengaruhi pilihan metode yang digunakan. Misalnya, dalam citra dengan orientasi garis vertikal yang dominan, metode seperti Sobel atau Prewitt yang fokus pada gradien vertikal mungkin lebih efektif daripada deteksi tepi umum.

## Tahapan Penyelesaian Projek
### 1. Pengambilan Foto
- Ambil foto diri dengan jarak minimal 2 meter dari objek(diri sendiri)
- Simpan foto dalam format jpeg atau pengenalan
### 2. Implementasi Kode Untuk Deteksi Tepi Pola Objek
**Import Library**
~~~
import cv2  
import numpy as np  
import matplotlib.pyplot as plt 
~~~
**Penjelasan**:
 

Kode di atas digunakan untuk mengimpor tiga pustaka penting untuk pengolahan gambar dan plotting di Python. Pertama, pustaka OpenCV (`import cv2`) diimpor, yang merupakan pustaka terkenal untuk visi komputer. OpenCV menyediakan berbagai fungsi untuk pengolahan gambar dan video, seperti membaca dan menulis gambar, deteksi tepi, deteksi objek, dan banyak lagi. Kedua, pustaka NumPy (`import numpy as np`) diimpor, yang merupakan pustaka untuk operasi numerik. NumPy mendukung array multidimensi dan berbagai fungsi matematika yang efisien, yang sangat berguna dalam pengolahan citra untuk menangani piksel gambar sebagai array. Terakhir, pustaka Matplotlib (`import matplotlib.pyplot as plt`) diimpor, yang merupakan pustaka untuk plotting dan visualisasi data. Matplotlib memungkinkan pembuatan grafik yang interaktif dan publikasi berkualitas tinggi, termasuk plot gambar dan hasil pengolahan citra yang dilakukan oleh OpenCV. Dengan menggabungkan ketiga pustaka tersebut, kita dapat membaca gambar, mengolahnya, dan menampilkan hasilnya dalam bentuk visual yang mudah dipahami.

**Edge Detection**
~~~
image = cv2.imread('foto.jpeg')
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)


edges = cv2.Canny(image, 100, 50)
~~~
**Penjelasan**:

Kode di atas digunakan untuk membaca dan memproses gambar dengan menggunakan pustaka OpenCV. Pertama, gambar dibaca dari file bernama `foto.jpeg` menggunakan fungsi `cv2.imread()` dan disimpan dalam variabel `image`. Secara default, gambar dibaca dalam format BGR (Blue, Green, Red). Selanjutnya, gambar dikonversi dari format BGR ke format RGB (Red, Green, Blue) menggunakan fungsi `cv2.cvtColor()` untuk memastikan kesesuaian dengan pustaka lain yang mungkin digunakan untuk visualisasi gambar, seperti Matplotlib, yang menggunakan format RGB. Setelah itu, gambar dikonversi lagi menjadi skala abu-abu dengan `cv2.cvtColor()` menggunakan parameter `cv2.COLOR_BGR2GRAY`. Konversi ini mengubah gambar menjadi versi yang lebih sederhana dengan hanya satu saluran warna, yang sangat berguna dalam banyak algoritma pemrosesan gambar. Terakhir, algoritma deteksi tepi Canny diterapkan pada gambar dengan menggunakan fungsi `cv2.Canny()`. Algoritma ini mendeteksi tepi dalam gambar berdasarkan perubahan intensitas piksel yang tajam. Dua parameter tambahan, yaitu threshold bawah dan threshold atas, digunakan untuk menentukan seberapa kuat perubahan intensitas yang harus dideteksi sebagai tepi. Dalam kode ini, threshold bawah diatur ke 100 dan threshold atas diatur ke 50. Hasil dari deteksi tepi ini disimpan dalam variabel `edges`. Secara keseluruhan, kode ini memuat gambar, mengonversinya ke format yang sesuai, dan menerapkan deteksi tepi untuk mengidentifikasi tepi-tepi dalam gambar tersebut.
~~~
fig, axs = plt.subplots(1, 2, figsize=(10, 10))


ax = axs.ravel()


ax[0].imshow(image)
ax[0].set_title("Original Image")  


ax[1].imshow(edges, cmap="gray")
ax[1].set_title("Canny Edge Detection") 


plt.show()
~~~
**Penjelasan**:

Kode di atas menggunakan pustaka Matplotlib untuk membuat dan menampilkan subplot yang berisi gambar asli dan hasil deteksi tepi Canny. Pertama, baris `fig, axs = plt.subplots(1, 2, figsize=(10, 10))` membuat sebuah figure dengan dua subplot yang disusun secara horizontal (1 baris, 2 kolom) dan mengatur ukuran figure menjadi 10x10 inci. Variabel `axs` adalah array yang berisi dua objek subplot. Baris `ax = axs.ravel()` meratakan array `axs` sehingga mudah diakses sebagai array datar. Selanjutnya, gambar asli (`image`) ditampilkan pada subplot pertama (`ax[0]`) menggunakan `ax[0].imshow(image)`, dan judul "Original Image" ditambahkan dengan `ax[0].set_title("Original Image")`. Kemudian, hasil deteksi tepi Canny (`edges`) ditampilkan pada subplot kedua (`ax[1]`) dengan `ax[1].imshow(edges, cmap="gray")`, yang menampilkan gambar dalam skala abu-abu menggunakan colormap `gray`. Judul "Canny Edge Detection" ditambahkan pada subplot kedua dengan `ax[1].set_title("Canny Edge Detection")`. Kemudian, `plt.show()` digunakan untuk menampilkan figure yang berisi kedua subplot tersebut. Secara keseluruhan, kode di atas digunakan untuk menampilkan perbandingan antara gambar asli dan hasil deteksi tepi Canny dalam satu figure dengan dua subplot yang disusun secara horizontal.

**Contours Detection**
~~~
contours, hierarchy = cv2.findContours(edges, cv2.RETR_TREE, cv2.CHAIN_APPROX_SIMPLE)
contour_image = cv2.cvtColor(gray_image, cv2.COLOR_GRAY2BGR)
cv2.drawContours(contour_image, contours, -1, (0, 255, 0), 2)
~~~
**Penjelasan**:


Kode di atas menggunakan pustaka OpenCV untuk mendeteksi kontur dalam gambar dan menggambar kontur tersebut pada gambar. Pertama, baris `contours, hierarchy = cv2.findContours(edges, cv2.RETR_TREE, cv2.CHAIN_APPROX_SIMPLE)` mendeteksi kontur dalam gambar tepi yang dihasilkan sebelumnya (`edges`) menggunakan fungsi `cv2.findContours()`. Parameter `cv2.RETR_TREE` digunakan untuk mengambil semua kontur dan membangun hierarki penuh dari kontur yang ditemukan, sedangkan `cv2.CHAIN_APPROX_SIMPLE` digunakan untuk menyederhanakan kontur dengan menghilangkan titik-titik yang tidak diperlukan. Hasilnya adalah daftar kontur (`contours`) dan hierarki kontur (`hierarchy`). Selanjutnya, gambar skala abu-abu (`gray_image`) dikonversi kembali ke format gambar berwarna BGR dengan `cv2.cvtColor(gray_image, cv2.COLOR_GRAY2BGR)` untuk memungkinkan menggambar kontur berwarna pada gambar tersebut. Hasil konversi ini disimpan dalam variabel `contour_image`. Kemudian, fungsi `cv2.drawContours(contour_image, contours, -1, (0, 255, 0), 2)` digunakan untuk menggambar semua kontur yang ditemukan pada gambar `contour_image`. Parameter `-1` menunjukkan bahwa semua kontur harus digambar, `(0, 255, 0)` adalah warna hijau dalam format BGR, dan `2` adalah ketebalan garis kontur. Secara keseluruhan, kode di atas digunakan untuk mendeteksi kontur dalam gambar tepi, mengonversi gambar skala abu-abu ke gambar berwarna, dan menggambar kontur yang terdeteksi pada gambar berwarna tersebut dengan warna hijau.
~~~
fig, axs = plt.subplots(1, 3, figsize=(15, 5))

# Original Image
axs[0].imshow(image)
axs[0].set_title('Original Image')

# Canny Edge Detection
axs[1].imshow(edges, cmap='gray')
axs[1].set_title('Canny Edge Detection')

# Contours Detection
axs[2].imshow(contour_image)
axs[2].set_title('Contours Detection')


plt.show()
~~~
**Penjelasan**:

Kode di atas menggunakan pustaka Matplotlib untuk membuat dan menampilkan tiga subplot yang berisi gambar asli, hasil deteksi tepi Canny, dan hasil deteksi kontur. Pertama, `fig, axs = plt.subplots(1, 3, figsize=(15, 5))` membuat sebuah figure dengan tiga subplot yang disusun secara horizontal (1 baris, 3 kolom) dan mengatur ukuran figure menjadi 15x5 inci. Variabel `axs` adalah array yang berisi tiga objek subplot. Selanjutnya, gambar asli (`image`) ditampilkan pada subplot pertama (`axs[0]`) menggunakan `axs[0].imshow(image)`, dan judul "Original Image" ditambahkan dengan `axs[0].set_title('Original Image')`. Kemudian, hasil deteksi tepi Canny (`edges`) ditampilkan pada subplot kedua (`axs[1]`) dengan `axs[1].imshow(edges, cmap='gray')`, yang menampilkan gambar dalam skala abu-abu menggunakan colormap `gray`. Judul "Canny Edge Detection" ditambahkan pada subplot kedua dengan `axs[1].set_title('Canny Edge Detection')`. Terakhir, gambar hasil deteksi kontur (`contour_image`) ditampilkan pada subplot ketiga (`axs[2]`) dengan `axs[2].imshow(contour_image)`, dan judul "Contours Detection" ditambahkan dengan `axs[2].set_title('Contours Detection')`. Kemudian, `plt.show()` digunakan untuk menampilkan figure yang berisi ketiga subplot tersebut. Secara keseluruhan, kode di atas digunakan untuk menampilkan perbandingan antara gambar asli, hasil deteksi tepi Canny, dan hasil deteksi kontur dalam satu figure dengan tiga subplot yang disusun secara horizontal.






