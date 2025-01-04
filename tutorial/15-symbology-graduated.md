[<< Back](../README.md)

# Symbology/Style Graduated

1. Symbology/Style Graduated merupakan simbologi berdasarkan kategori atau klasifikasi data **kuantitatif** dengan rentang tertentu misal < 2500, 2500 - 5000, > 5000.

2. Pastikan di dalam data GeoJSON sudah memiliki atribut yang digunakan sebagai dasar klasifikasi, misalnya atribut **`jumlah`**.

3. Pada script style, ubah script menjadi seperti ini.

```javascript
style: function (feature) {
	if (feature.properties.jumlah <= 2500) {
		return {
			opacity: 1,
			color: 'black',
			weight: 1.0,
			fillOpacity: 0.7,
			fillColor: '#ffffb2'
		}
	}
	if (feature.properties.jumlah > 2500 && feature.properties.jumlah <= 5000) {
		return {
			opacity: 1,
			color: 'black',
			weight: 1.0,
			fillOpacity: 0.7,
			fillColor: '#fd8d3c'
		}
	}
	if (feature.properties.jumlah > 5000) {
		return {
			opacity: 1,
			color: 'black',
			weight: 1.0,
			fillOpacity: 0.7,
			fillColor: '#bd0026'
		}
	}
},
```

5. Sesuaikan nama atribut yang digunakan sebagai dasar klasifikasi dengan nama atribut yang ada di dalam data GeoJSON yang Anda gunakan.

Reference:

1. [https://colorbrewer2.org/](https://colorbrewer2.org/)

2. [https://leafletjs.com/examples/choropleth/](https://leafletjs.com/examples/choropleth/)

---

> [unsorry@2024](https://unsorry.net)
