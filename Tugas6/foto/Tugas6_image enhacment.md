## Tugas 6 Pemerosesan Citra Digital
Nama   : Sesilia Miranda<br>
Nim    : 2110131220010

<h2 align="center">IMAGE ENHACMENT</h2>

Image enhacment atau perbaikan kualitas citra gambar (image enhancement) merupakan salah satu proses awal dalam pengolahan citra gambar (image preprocessing). Perbaikan kualitas diperlukan karena seringkali citra gambar yang dijadikan obyek pembahasan mempunyai kualitas yang kurang baik (buruk), misalnya citra gambar mengalami noise (derau) pada saat pengiriman informasi melalui saluran transmisi, citra gambar mungkin terlalu terang atau gelap, atau citra gambar kurang tajam, kabur dan sebagainya. Melalui operasi pemrosesan awal inilah kulitas citra gambar diperbaiki sehingga citra gambar dapat digunakan untuk aplikasi lebih lanjut, misalnya untuk aplikasi pengenalan (recognition) obyek didalam citra gambar tersebut.

1. Spatial domain

    Metode-metode image enhancement dalam ranah spasial dilakukan dengan memanipulasi secara langsung pixel-pixel di dalam citra.

    Metode diantaranya ialah:

    + Grey scale manipulation

        Bentuk operasi yang paling sederhana adalah ketika operator T hanya bekerja pada lingkungan piksel pada citra masukan, yaitu $\hat{F}(x,y)$hanya bergantung pada nilai F pada ( x , y ). Ini adalah transformasi atau pemetaan skala abu-abu.

        Kasus paling sederhana adalah ambang batas di mana profil intensitas diganti dengan fungsi langkah, aktif pada nilai ambang yang dipilih. Dalam hal ini setiap piksel dengan tingkat keabuan di bawah ambang batas pada gambar input dipetakan ke 0 pada gambar output. Piksel lain dipetakan ke 255.

    + Histogram equalization

        Histogram equalization adalah teknik umum untuk meningkatkan tampilan gambar. Misalkan kita memiliki gambar yang didominasi gelap. Kemudian histogramnya akan dimiringkan ke ujung bawah skala abu-abu dan semua detail gambar dikompresi ke ujung gelap histogram. Jika kita bisa `memperpanjang' tingkat abu-abu di ujung gelap untuk menghasilkan histogram yang terdistribusi lebih seragam maka gambar akan menjadi jauh lebih jelas.

    + Image smoothing

        Tujuan penghalusan gambar adalah untuk mengurangi efek derau kamera, nilai piksel palsu, nilai piksel yang hilang, dll. Ada banyak teknik berbeda untuk penghalusan gambar; kita akan mempertimbangkan rata-rata lingkungan dan perataan tepi-pemeliharaan.

    + Image sharpening

        Tujuan utama penajaman gambar adalah untuk menonjolkan detail halus pada gambar, atau untuk menyempurnakan detail yang telah diburamkan (mungkin karena noise atau efek lain, seperti gerakan). Dengan penajaman gambar, kita ingin meningkatkan komponen frekuensi tinggi; ini menyiratkan bentuk filter spasial yang memiliki komponen positif tinggi di tengahnya (lihat gambar 4 di bawah).

    + High boost filtering

        Kita dapat memikirkan pemfilteran lolos tinggi dalam hal mengurangi gambar lolos rendah dari gambar asli, yaitu,
        
        High pass = Original - Low pass.
        
        Namun, dalam banyak kasus di mana gambar high pass diperlukan, kita juga ingin mempertahankan beberapa komponen frekuensi rendah untuk membantu interpretasi gambar. Jadi, jika kita mengalikan gambar asli dengan faktor amplifikasi A sebelum mengurangkan gambar low pass, kita akan mendapatkan high boost atau filter penekanan frekuensi tinggi . Dengan demikian,

2. Frequency domain

    Metode-metode image enhancement dalam ranah frekuensi dilakukan dengan mengubah citra terlebih dahulu dari ranah spasial ke ranah frekuensi, baru kemudian memanipulasi nilai-nilai frekuensi tersebut.

    Metode diantaranya ialah:

    + Transformasi fourier

        Tranformasi fourier adalah suatu model transformasi yang memindahkan domain spasial atau domain waktu menjadi domain frekuensi. Dengan menggunakan transformasi fourier, sinyal atau citra dapat dilihat sebagai suatu objek dalam domain frekuensi.
        Analisis dalam domain frekuensi banyak digunakan seperti filtering. 
        
        Low pass filtering melibatkan penghapusan komponen frekuensi tinggi dalam gambar. Ini menghasilkan kekaburan gambar (dan dengan demikian pengurangan transisi tajam yang terkait dengan kebisingan). Filter low pass yang ideal akan mempertahankan semua komponen frekuensi rendah, dan menghilangkan semua komponen frekuensi tinggi. Namun, filter ideal memiliki dua masalah: blurring dan ringing . Masalah-masalah ini disebabkan oleh bentuk filter domain spasial yang terkait, yang memiliki sejumlah besar undulasi. Transisi yang lebih halus dalam filter domain frekuensi, seperti filter Butterworth, mencapai hasil yang jauh lebih baik.