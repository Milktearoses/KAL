---
title: Pembuktian Transformasi Linier

---

## PEMBUKTIAN TRANSFORNASI LINIER
Diberikan transformasi berikut:

**T(v1, v2) = (v1 + v2, v1)**

Kita ingin membuktikan bahwa ini adalah transformasi linier, yaitu transformasi yang memenuhi dua sifat penting:

### Definisi Transformasi Linier
Suatu transformasi T disebut linier jika memenuhi dua sifat:

1. **Aditifitas (Penjumlahan tetap berlaku)**
T(u + v) = T(u) + T(v)

2. **Homogenitas (Perkalian skalar tetap berlaku)**
T(c * v) = c * T(v)

### Langkah 1: Uji Aditifitas
Misalkan:

- u = (u1, u2)
- v = (v1, v2)

Maka:
- u + v = (u1 + v1, u2 + v2)
- T(u + v) = (u1 + v1 + u2 + v2, u1 + v1)

Sementara:
- T(u) = (u1 + u2, u1)
- T(v) = (v1 + v2, v1)
- T(u) + T(v) = (u1 + u2 + v1 + v2, u1 + v1)

**Karena T(u + v) = T(u) + T(v), sifat aditifitas terpenuhi.**

### Langkah 2: Uji Homogenitas
Misalkan:
- v = (v1, v2)
- c adalah skalar

Maka:
- c * v = (c * v1, c * v2)
- T(c * v) = (c * v1 + c * v2, c * v1)
- T(v) = (v1 + v2, v1)
- c * T(v) = (c * (v1 + v2), c * v1)

**Karena T(c * v) = c * T(v), sifat homogenitas juga terpenuhi.**

### Kesimpulan
Karena transformasi T memenuhi dua sifat utama transformasi linier (aditifitas dan homogenitas), maka:

**T(v1, v2) = (v1 + v2, v1) adalah transformasi linier.**