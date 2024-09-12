[<< Back](../README.md)

# GeoJSON Polyline

1. Setelah menambahkan library jQuery, tambahkan script berikut ini untuk membuat GeoJSON Polyline pada peta.

```javascript
// GeoJSON Polyline Jalan
var jalan = L.geoJSON(null, {
	// Style

	// onEachFeature

});
```

2. Tambahkan script untuk memanggil data GeoJSON file menggunakan jQuery.

```javascript
$.getJSON("data/jalan.geojson", function (data) {
	jalan.addData(data); // Menambahkan data ke dalam GeoJSON Polyline Jalan
	map.addLayer(jalan); // Menambahkan GeoJSON Polyline Jalan ke dalam peta
});
```

3. Tambahkan script untuk mengatur style pada GeoJSON Polyline ke dalam L.geoJSON.

```javascript
style: function (feature) {
	return {
		color: "red",
		opacity: 1,
		weight: 3,
	};
},
```

4. Tambahkan script untuk menampilkan Popup pada GeoJSON Polyline ketika *layer on* dan pada *event click*. Sesuaikan feature.properties dengan data GeoJSON file yang digunakan.

```javascript
onEachFeature: function (feature, layer) {
	// variable popup content
	var popup_content = "Fungsi: " + feature.properties.fungsi + "<br>" +
	"Panjang (m): " + feature.properties.panjang_m;

	layer.on({
		click: function (e) {
			jalan.bindPopup(popup_content);
		},
	});
},
```

5. Tambahkan script berikut ini untuk menambahkan tooltip ketika cursor berada di atas GeoJSON Polyline. Letakkan di dalam layer.on.

```javascript
mouseover: function (e) {
	jalan.bindTooltip(feature.properties.fungsi, {
		direction: "auto",
		sticky: true,
	});
},
```

Reference: [https://leafletjs.com/examples/geojson/](https://leafletjs.com/examples/geojson/)

---

> [unsorry@2024](https://unsorry.net)
