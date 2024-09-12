[<< Back](../README.md)

# Geolocation

1. Tambahkan script berikut ini untuk membuat geolocation pada peta.
```javascript
// Geolocation
map.locate({
	setView: true,
	maxZoom: 16,
});

// Fungsi untuk menampilkan lokasi
function onLocationFound(e) {
	var radius = e.accuracy / 2;

	// Menampilkan marker pada lokasi 
	L.marker(e.latlng).addTo(map).bindPopup("Anda berada dalam radius " + radius + " meter dari titik ini").openPopup();

	// Menampilkan circle pada lokasi
	L.circle(e.latlng, radius).addTo(map);
}

map.on("locationfound", onLocationFound);

// Fungsi untuk menampilkan pesan error
function onLocationError(e) {
	alert(e.message);
}

map.on("locationerror", onLocationError);
```

Reference: [https://leafletjs.com/reference.html#locationevent](https://leafletjs.com/reference.html#locationevent)

---
> [unsorry@2024](https://unsorry.net)