---
title: Transformasi Refleksi dengan Matriks

---

## TRANSFORMASI REFLEKSI DENGAN MATRIKS
### Pendahuluan

Pada materi ini, kita akan mempelajari bagaimana transformasi refleksi bekerja dalam konteks geometri dan bagaimana menerapkannya menggunakan matriks. Refleksi merupakan salah satu jenis transformasi linier penting dalam matematika dan grafika komputer.

Apa Itu Refleksi dalam Transformasi Geometri?
Refleksi adalah salah satu jenis transformasi linier yang “memantulkan” titik terhadap garis tertentu, seperti sumbu-x, sumbu-y, garis y = x, garis y = -x, atau titik asal (0, 0). Dalam matematika, refleksi dapat direpresentasikan sebagai perkalian antara matriks refleksi dan vektor posisi.

### Tujuan
Diberikan titik $(x, y)$, kita ingin mencari hasil refleksinya $(x', y')$ dengan menggunakan:

$$\begin{bmatrix}x'\\ y'\end{bmatrix} = M.\begin{bmatrix}x\\ y\end{bmatrix}$$
 
 
di mana $M$ adalah matriks transformasi refleksi.

### Cara Mengalikan Matriks dengan Vektor
Misalkan:

$$M = \begin{bmatrix}a&b\\c&d\end{bmatrix}, v^\rightarrow = \begin{bmatrix}x\\y\end{bmatrix}$$
 
 
Maka:

$$M.v^\rightarrow = \begin{bmatrix}a.x+b.y\\c.x+d.y\end{bmatrix}$$
 
### Contoh Refleksi Titik (2, 3)
Kita ambil contoh titik (2,3), dan kita coba refleksikan terhadap beberapa garis berikut ini:

**1. Refleksi terhadap sumbu-x**
Matriks:

$$M = \begin{bmatrix}1&0\\0&-1\end{bmatrix}$$

$$v^\rightarrow = M.v^\rightarrow = \begin{bmatrix}1&0\\0&-1\end{bmatrix}.\begin{bmatrix}2\\3\end{bmatrix} = \begin{bmatrix}2\\-3\end{bmatrix}$$

Hasil : **(2, -3)**

### 2. Refleksi terhadap sumbu-y
Matriks:

$$\begin{bmatrix}-1&0\\0&-1\end{bmatrix}$$

$$M.\begin{bmatrix}2\\3\end{bmatrix} = \begin{bmatrix}-2\\3\end{bmatrix}$$

Hasil: **(-2, 3)**

3. Refleksi terhadap garis y = x
Matriks:

$$M = \begin{bmatrix}0&1\\1&0\end{bmatrix}$$

$$\begin{bmatrix}0&1\\1&0\end{bmatrix}.\begin{bmatrix}2\\3\end{bmatrix} = \begin{bmatrix}3\\2\end{bmatrix}$$

Hasil: **(3, 2)**

### 4. Refleksi terhadap garis y = -x
Matriks:

$$M = \begin{bmatrix}0&-1\\-1&0\end{bmatrix}$$

$$\begin{bmatrix}0&-1\\-1&0\end{bmatrix}.\begin{bmatrix}2\\3\end{bmatrix} = \begin{bmatrix}-3\\-2\end{bmatrix}$$

Hasil: **(-3, -2)**

5. Refleksi terhadap titik asal (0, 0)
Matriks:

$$M = \begin{bmatrix}-1&0\\0&-1\end{bmatrix}$$

$$\begin{bmatrix}-1&0\\0&-1\end{bmatrix}.\begin{bmatrix}2\\3\end{bmatrix} = \begin{bmatrix}-3\\-2\end{bmatrix}$$

Hasil: **(-2, -3)**

### Kesimpulan
Transformasi refleksi dapat dihitung dengan cara mengalikan vektor posisi dengan matriks refleksi yang sesuai. Setiap jenis refleksi memiliki bentuk matriks yang berbeda, tetapi prinsip perhitungannya tetap sama yaitu menggunakan perkalian matriks biasa.