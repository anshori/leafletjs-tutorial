[<< Back](../README.md)

# Filter

1. Filter digunakan untuk menampilkan data GeoJSON berdasarkan kriteria tertentu.

2. setelah function onEachFeature, tambahkan script berikut.

```javascript
filter: function(feature, layer) {
	return feature.properties.kelas == 'Tinggi';
},
```

3. Ubah nilai `'Tinggi'` sesuai dengan nilai atribut yang akan dijadikan kriteria filter.

4. Gunakan || untuk menambahkan kriteria filter `OR` lainnya lebih dari satu.

5. Gunakan && untuk menambahkan kriteria filter `AND` lebih dari satu.

Reference: [https://leafletjs.com/reference.html#geojson-filter](https://leafletjs.com/reference.html#geojson-filter)

---
> [unsorry@2024](https://unsorry.net)