[<< Back](../README.md)

# GeoJSON Polygon

1. Setelah menambahkan library jQuery, tambahkan script berikut ini untuk membuat GeoJSON Polygon pada peta.

```javascript
// GeoJSON Polygon Jumlah Penduduk
var jumlah_penduduk = L.geoJSON(null, {
	// Style

	// onEachFeature

});
```

2. Tambahkan script untuk memanggil data GeoJSON file menggunakan jQuery.

```javascript
$.getJSON("data/jumlah_penduduk.geojson", function (data) {
	jumlah_penduduk.addData(data); // Menambahkan data ke dalam GeoJSON Polygon Jumlah Penduduk
	map.addLayer(jumlah_penduduk); // Menambahkan GeoJSON Polygon Jumlah Penduduk ke dalam peta
});
```

3. Tambahkan script untuk mengatur style pada GeoJSON Polygon ke dalam L.geoJSON.

```javascript
style: function (feature) {
	return {
		color: "gray",
		opacity: 1,
		weight: 1,
		fillColor: "#ff0000",
		fillOpacity: 0.8,
	};
},
```

4. Tambahkan script untuk menampilkan Popup pada GeoJSON Polygon ketika *layer on* dan pada *event click*. Sesuaikan feature.properties dengan data GeoJSON file yang digunakan.

```javascript
onEachFeature: function (feature, layer) {
	// variable popup content
	var popup_content = "Kecamatan: " + feature.properties.kecamatan + "<br>" +
	"Jumlah Penduduk: " + feature.properties.jumlah_penduduk;

	layer.on({
		click: function (e) {
			jumlah_penduduk.bindPopup(popup_content);
		},
	});
},
```

5. Tambahkan script berikut ini untuk menambahkan tooltip ketika cursor berada di atas GeoJSON Polygon. Letakkan di dalam layer.on.

```javascript
mouseover: function (e) {
	jumlah_penduduk.bindTooltip(feature.properties.desa, {
		direction: "auto",
		sticky: true,
	});
},
```

Reference: [https://leafletjs.com/examples/geojson/](https://leafletjs.com/examples/geojson/)

---

> [unsorry@2024](https://unsorry.net)
