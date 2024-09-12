[<< Back](../README.md)

# Symbology/Style Categorized

1. Symbology/Style Categorized merupakan simbologi berdasarkan kategori atau klasifikasi data **kualitatif** misal kelas Tinggi, Sedang, Rendah.

2. Pastikan di dalam data GeoJSON sudah memiliki atribut yang digunakan sebagai dasar klasifikasi, misalnya atribut **`kelas`**.

3. Buat *variable object* untuk simbologi berdasarkan kategori, misalnya dengan nama **`symbologyCategorized`**.

```javascript
var symbologyCategorized = {"Tinggi": "#d95f0e", "Sedang": "#fec44f", "Rendah": "#fff7bc" };
```

4. Pada script style di bagian fillColor, ubah script menjadi seperti ini.

```javascript
fillColor: symbologyCategorized[feature.properties.kelas],
```

5. Sesuaikan nama atribut yang digunakan sebagai dasar klasifikasi dengan nama atribut yang ada di dalam data GeoJSON yang Anda gunakan.

Reference: [https://colorbrewer2.org/](https://colorbrewer2.org/)

---
> [unsorry@2024](https://unsorry.net)