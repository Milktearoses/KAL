# Refleksi

**Refleksi matriks** (reflection matrix) adalah **matriks transformasi** yang mencerminkan (memantulkan) titik-titik dalam ruang terhadap **sumbu, garis, bidang, atau titik tertentu**.

Refleksi mengubah arah satu atau lebih komponen vektor, seperti bayangan di cermin.

---

### ✅ **Repleksi pada 2D (dua dimensi)**:

1. **Refleksi terhadap sumbu-x**:

$$
\begin{bmatrix}
1 & 0 \\
0 & -1
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix}
=
\begin{bmatrix}
x \\
-y
\end{bmatrix}
$$

→ Membalik titik terhadap sumbu-x (nilai y dibalik, x tetap).

2. **Refleksi terhadap sumbu-y**:

$$
\begin{bmatrix}
-1 & 0 \\
0 & 1
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix}
=
\begin{bmatrix}
-x \\
y
\end{bmatrix}
$$

→ Membalik titik terhadap sumbu-y.

3. **Refleksi terhadap garis y = x**:

$$
\begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix}
=
\begin{bmatrix}
y \\
x
\end{bmatrix}
$$

→ Menukar posisi x dan y.

---

### ✅ ** Repleksi pada 3D (tiga dimensi)**:

Refleksi bisa dilakukan terhadap bidang seperti $x=0$, $y=0$, atau $z=0$. Contoh refleksi terhadap bidang $x=0$:

$$
\begin{bmatrix}
-1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

---

### 🔧 **Aplikasi Refleksi Matriks**:

* Grafika komputer (cermin objek)
* Geometri transformasi
* Simulasi fisika (pantulan)





```python
%matplotlib inline  
from math import pi, sin, cos
import matplotlib.pyplot as plt
import numpy as np

titik = np.array([[0,0],[0.5,0.5],[0.5,1.5],[0,1],[0,0]])
koordinats = titik.transpose()
x = koordinats[0,:]
y = koordinats[1,:]


```


```python
B = np.array([[-1,0],[0,1]])
B_trans = B@koordinats

x_LT2 = B_trans[0,:]
y_LT2 = B_trans[1,:]

# Membuat gambar dan sumbu sumbu
fig, ax = plt.subplots()

# Ploting titik titik.  x dan y are vektor asal(domain) , x_LT1 dab y_LT1 bayangan (codomain)
ax.plot(x,y,'ro')
ax.plot(x_LT2,y_LT2,'bo')

# Menghubungkan titik dengan baris
ax.plot(x,y,'r',ls="--")
ax.plot(x_LT2,y_LT2,'b')

# menggambar sumbu sumbu
ax.axvline(x=0,color="k",ls=":")
ax.axhline(y=0,color="k",ls=":")
ax.grid(True)
ax.axis([-2,2,-1,2])
ax.set_aspect('equal')
ax.set_title("Refleksi sumbu Y");
```


    
![png](output_3_0.png)
    



```python
import numpy as np
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d import Axes3D

# Titik-titik objek asli (misalnya, segitiga 3D)
points = np.array([
    [1, 1, 1],
    [2, 1, 1],
    [1.5, 2, 1]
]).T  # bentuknya 3xN

# Matriks refleksi terhadap bidang x = 0
reflection_matrix = np.array([
    [-1, 0, 0],
    [ 0, 1, 0],
    [ 0, 0, 1]
])

# Lakukan refleksi
reflected_points = reflection_matrix @ points

# Buat plot
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')

# Gambar objek asli (biru)
ax.plot(points[0], points[1], points[2], 'bo-', label='Asli')

# Gambar objek setelah refleksi (merah)
ax.plot(reflected_points[0], reflected_points[1], reflected_points[2], 'ro-', label='Refleksi')

# Tambahkan garis bantu bidang x = 0
x_plane = np.zeros((2, 2))
y_plane, z_plane = np.meshgrid(np.linspace(0, 3, 2), np.linspace(0, 3, 2))
ax.plot_surface(x_plane, y_plane, z_plane, alpha=0.2, color='gray')

# Set aspek dan label
ax.set_xlabel('X')
ax.set_ylabel('Y')
ax.set_zlabel('Z')
ax.set_title('Refleksi terhadap bidang x = 0')
ax.legend()
ax.set_box_aspect([1,1,1])  # aspek rasio 1:1:1

plt.show()

```


    
![png](output_4_0.png)
    


## Latihan
1. Carilah matriks yang menggambarkan refleksi terhadap sumbu x. Kalikan matrik dengan 4 titik koordinat dan plot hasilnya
2. Carilah matriks yang menggambarkan refleksi terhadap sumbu y= -x. Kalikan matrik dengan 4 titik koordinat dan plot hasilnya

# Matrik Geser ( Shear Matrix)

**Shear matrix** atau **Matriks geser**. adalah jenis transformasi dalam **aljabar linear** dan **grafika komputer**, yang menggeser satu bagian dari objek ke arah tertentu tanpa mengubah volumenya.


Matriks shear "mendorong" titik-titik dalam suatu arah (biasanya horizontal atau vertikal), sedangkan titik-titik lain tetap relatif pada sumbu tertentu.

### Matrik Geser pada 2D:

Misalkan kita punya titik $(x, y)$. Jika kita terapkan **shear horizontal**, maka titiknya berubah menjadi:

$$
\begin{bmatrix}
1 & k \\
0 & 1
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix}
=
\begin{bmatrix}
x + ky \\
y
\end{bmatrix}
$$

Artinya, sumbu-x digeser sebanding dengan nilai y (terjadi "kemiringan" arah horizontal).

Jika shear vertikal:

$$
\begin{bmatrix}
1 & 0 \\
k & 1
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix}
=
\begin{bmatrix}
x \\
y + kx
\end{bmatrix}
$$

### Aplikasi:

* Dalam **grafika komputer** untuk menciptakan efek distorsi
* Dalam **mekanika** untuk menggambarkan deformasi material
* Dalam **transformasi geometris**  computer vision





```python
%matplotlib inline  
from math import pi, sin, cos
import matplotlib.pyplot as plt
import numpy as np

titik = np.array([[0,0],[0.5,0.5],[0.5,1.5],[0,1],[0,0]])
koordinats = titik.transpose()
x = koordinats[0,:]
y = koordinats[1,:]


S = np.array([[1,2],[0,1]])
S_coords = S@koordinats

x_LT4 = S_coords[0,:]
y_LT4 = S_coords[1,:]



fig, ax = plt.subplots()


ax.plot(x,y,'ro')
ax.plot(x_LT4,y_LT4,'bo')


ax.plot(x,y,'r',ls="--")
ax.plot(x_LT4,y_LT4,'b')


ax.axvline(x=0,color="k",ls=":")
ax.axhline(y=0,color="k",ls=":")
ax.grid(True)
ax.axis([-2,4,-1,2])
ax.set_aspect('equal')
ax.set_title("Shear");
```


    
![png](output_8_0.png)
    


# Matrik Rotasi

**Matriks rotasi** adalah **matriks transformasi linier** yang digunakan untuk **memutar vektor atau objek** di ruang 2D, 3D, atau lebih tinggi **tanpa mengubah bentuk atau ukurannya**.

---


Matriks rotasi memutar titik atau objek **sekitar asal (0,0)** atau sumbu tertentu, dengan **sudut tertentu** (biasanya dalam radian atau derajat).

---

## ✅  **Matriks Rotasi pada 2D**

Untuk memutar vektor sebesar sudut $\theta$ terhadap titik asal dalam bidang 2D:

$$
R(\theta) = 
\begin{bmatrix}
\cos\theta & -\sin\theta \\
\sin\theta & \cos\theta
\end{bmatrix}
$$

Jika kamu punya titik $(x, y)$, maka hasil rotasinya:

$$
\begin{bmatrix}
x' \\
y'
\end{bmatrix}
=
R(\theta) \cdot
\begin{bmatrix}
x \\
y
\end{bmatrix}
$$

---

## ✅  **Matriks Rotasi pada 3D**

Di 3D, rotasi bisa dilakukan terhadap sumbu X, Y, atau Z.

1. **Rotasi terhadap sumbu X (dengan sudut $\theta$)**:

$$
R_x(\theta) = 
\begin{bmatrix}
1 & 0 & 0 \\
0 & \cos\theta & -\sin\theta \\
0 & \sin\theta & \cos\theta
\end{bmatrix}
$$

2. **Rotasi terhadap sumbu Y**:

$$
R_y(\theta) = 
\begin{bmatrix}
\cos\theta & 0 & \sin\theta \\
0 & 1 & 0 \\
-\sin\theta & 0 & \cos\theta
\end{bmatrix}
$$

3. **Rotasi terhadap sumbu Z**:

$$
R_z(\theta) = 
\begin{bmatrix}
\cos\theta & -\sin\theta & 0 \\
\sin\theta & \cos\theta & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

---

## 🛠️ **Aplikasi Matriks Rotasi:**

* Grafika komputer (animasi, rotasi objek)
* Robotika (pergerakan lengan robot)
* Pemrosesan citra (rotasi gambar)
* Navigasi (GPS, drone, pesawat)
* Ilmu data spasial dan geometri

---




```python
%matplotlib inline  
from math import pi, sin, cos
import matplotlib.pyplot as plt
import numpy as np

titik = np.array([[0,0],[0.5,0.5],[0.5,1.5],[0,1],[0,0]])
koordinats = titik.transpose()
x = koordinats[0,:]
y = koordinats[1,:]

```


```python
theta = pi/6
R = np.array([[cos(theta),-sin(theta)],[sin(theta),cos(theta)]])
R_koordinats = R@koordinats

x_LT3 = R_koordinats[0,:]
y_LT3 = R_koordinats[1,:]

# membuat gambar
fig, ax = plt.subplots()

# ploting titik titik.  x dan y adalah vektor asal (domain), x_LT1 dab y_LT1 adalah bayangan (codomain)
ax.plot(x,y,'ro')
ax.plot(x_LT3,y_LT3,'bo')

# menghubungkan titik dengan baris
ax.plot(x,y,'r',ls="--")
ax.plot(x_LT3,y_LT3,'b')

# menggambar sumbu sumbu koordinat
ax.axvline(x=0,color="k",ls=":")
ax.axhline(y=0,color="k",ls=":")
ax.grid(True)
ax.axis([-2,2,-1,2])
ax.set_aspect('equal')
ax.set_title("Rotasi");
```


    
![png](output_12_0.png)
    


# Komposisi transformasi

**Komposisi transformasi** (Composition of Transformations) adalah proses **menggabungkan dua atau lebih transformasi** geometris (seperti translasi, rotasi, refleksi, dan dilatasi) menjadi satu transformasi yang lebih kompleks.

Dalam komposisi transformasi, **transformasi pertama** diterapkan terlebih dahulu, dan kemudian **transformasi kedua** diterapkan pada hasil dari transformasi pertama. Jika lebih dari dua transformasi, proses ini dilakukan secara berurutan.


Misalnya, jika kita memiliki dua transformasi:

1. $T_1$ (seperti rotasi)
2. $T_2$ (seperti translasi)

Maka komposisi transformasi $T_1 \circ T_2$ berarti:

1. Terlebih dahulu **aplikasikan $T_2$** pada titik atau objek.
2. Setelah itu, **aplikasikan $T_1$** pada hasil transformasi sebelumnya.

### Matriks dan Komposisi:

Jika kita bekerja dengan **matriks transformasi**, komposisi dapat dilakukan dengan **perkalian matriks**. Misalnya, jika $A$ adalah matriks transformasi pertama dan $B$ adalah matriks transformasi kedua, maka komposisi transformasi tersebut adalah:

$$
C = A \times B
$$

Dengan catatan:

* Matriks $A$ diterapkan setelah $B$.
* Urutan perkalian matriks sangat penting, karena perkalian matriks **tidak komutatif** (yaitu $A \times B \neq B \times A$).

---

### Contoh Komposisi Transformasi:

Misalnya, kita ingin menggabungkan dua transformasi:

1. **Rotasi 90°** terhadap titik asal.
2. **Translasi (geser) 5 satuan ke kanan dan 3 satuan ke atas.**

Langkah-langkah:

1. **Rotasi**: Matriks rotasi 90°:

   $$
   R = 
   \begin{bmatrix}
   0 & -1 \\
   1 & 0
   \end{bmatrix}
   $$

2. **Translasi**: Matriks translasi 5 satuan ke kanan dan 3 satuan ke atas:

   $$
   T = 
   \begin{bmatrix}
   1 & 0 & 5 \\
   0 & 1 & 3 \\
   0 & 0 & 1
   \end{bmatrix}
   $$

Jika kita komposisikan translasi dan rotasi, kita harus menggabungkan matriks translasi dan rotasi ke dalam satu matriks transformasi. Hasil akhirnya akan memberikan rotasi **diikuti oleh translasi**.

---

### Aplikasi dalam Dunia Nyata:

* **Grafika komputer**: Untuk menggambar dan memanipulasi objek 3D (rotasi, translasi, zooming, dll.).
* **Robotika**: Untuk mengarahkan robot melalui serangkaian pergerakan.
* **Geometri**: Untuk mempelajari bentuk dan perubahan posisi dalam ruang.

---




## Latihan
1. Buatlah beberapa operasi  komposisi shear, rotasi dan reflesi  pada 2D untuk titik koordinat (2,2)
2. Buatlah beberapa operasi  komposisi shear, rotasi dan reflesi  pada 2D untuk titik koordinat (2,2) sehingga titik tersebut kembali lagi ke (2,2)

# Matrik Translasi

**Matriks translasi** adalah matriks yang digunakan untuk **mentranslasi** (menggeser) titik atau objek dalam ruang. Translasi memindahkan titik dengan **jarak tertentu** di sepanjang sumbu tertentu, tanpa mengubah bentuk atau orientasi objek.

---

### ✅ **Matriks Translasi pada 2D**

Dalam ruang dua dimensi (2D), matriks translasi biasanya dituliskan sebagai:

$$
T =
\begin{bmatrix}
1 & 0 & tx \\
0 & 1 & ty \\
0 & 0 & 1
\end{bmatrix}
$$

* $tx$ adalah jarak translasi sepanjang sumbu **x** (horizontal).
* $ty$ adalah jarak translasi sepanjang sumbu **y** (vertikal).

Jika kita memiliki titik $(x, y)$, maka hasil translasi menjadi:

$$
\begin{bmatrix}
x' \\
y' \\
1
\end{bmatrix}
=
T \cdot
\begin{bmatrix}
x \\
y \\
1
\end{bmatrix}
$$

Dimana:

* $x' = x + tx$
* $y' = y + ty$

Jadi, titik $(x, y)$ akan digeser ke posisi baru $(x + tx, y + ty)$.

---

### ✅ **Matriks Translasi pada 3D**

Untuk translasi di ruang tiga dimensi (3D), matriks translasi dapat dituliskan sebagai:

$$
T =
\begin{bmatrix}
1 & 0 & 0 & tx \\
0 & 1 & 0 & ty \\
0 & 0 & 1 & tz \\
0 & 0 & 0 & 1
\end{bmatrix}
$$

* $tx$, $ty$, dan $tz$ adalah jarak translasi sepanjang sumbu **x**, **y**, dan **z**.

Jika kita memiliki titik $(x, y, z)$, maka hasil translasi menjadi:

$$
\begin{bmatrix}
x' \\
y' \\
z' \\
1
\end{bmatrix}
=
T \cdot
\begin{bmatrix}
x \\
y \\
z \\
1
\end{bmatrix}
$$

Dimana:

* $x' = x + tx$
* $y' = y + ty$
* $z' = z + tz$

---

### ✅ **Aplikasi Matriks Translasi:**

* **Grafika komputer**: Untuk menggeser objek atau gambar di layar.
* **Robotika**: Untuk memindahkan posisi lengan robot.
* **Geometri**: Untuk memindahkan titik atau bentuk dalam ruang tanpa merubah ukuran atau orientasi.

---





```python
import numpy as np
import matplotlib.pyplot as plt

# Titik-titik objek (misalnya segitiga)
x = np.array([1, 2, 3])  # Koordinat X
y = np.array([1, 3, 2])  # Koordinat Y

# Matriks translasi (misalnya translasi 2 unit ke kanan dan 1 unit ke atas)
tx, ty = 2, 1
translation_matrix = np.array([[1, 0, tx],
                               [0, 1, ty],
                               [0, 0, 1]])

# Menambahkan baris 1 untuk koordinat homogen (x, y, 1)
coordinates = np.vstack((x, y, np.ones_like(x)))

# Menghitung hasil translasi
translated_coordinates = translation_matrix @ coordinates

# Titik-titik hasil translasi
x_translated = translated_coordinates[0, :]
y_translated = translated_coordinates[1, :]

# Plot objek asli dan hasil translasi
plt.figure(figsize=(6, 6))
plt.plot(x, y, 'bo-', label='Objek Asli')  # Titik objek asli (biru)
plt.plot(x_translated, y_translated, 'ro-', label='Objek Setelah Translasi')  # Titik objek setelah translasi (merah)

# Menambahkan label dan judul
plt.xlabel('X')
plt.ylabel('Y')
plt.title('Matriks Translasi pada Objek 2D')
plt.axhline(0, color='black',linewidth=1)
plt.axvline(0, color='black',linewidth=1)
plt.grid(True)
plt.legend()
plt.axis('equal')  # Agar skala X dan Y sama

plt.show()

```


    
![png](output_17_0.png)
    

