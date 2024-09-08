# Polyline

1. Tambahkan script berikut ini untuk membuat polyline pada peta.
```javascript
// Polyline
var vertexPolyline = [
	[-6.1995106, 106.8761802],
	[-6.1753924, 106.8271528],
	[-6.2184607, 106.8023014],
];
var polyline = L.polyline(vertexPolyline, {
	color: "red", // warna garis
	weight: 3, // ketebalan garis
	opacity: 1, // opacity garis
});

// Menambahkan polyline ke dalam peta
polyline.addTo(map);
```

2. Tambahkan script berikut ini untuk menambahkan popup pada polyline.
```javascript
// Popup
polyline.bindPopup("<b>Hallo</b><br>Ini adalah popup");
polyline.openPopup();
```

3. Tambahkan script berikut ini untuk menambahkan tooltip pada polyline.
```javascript
// Tooltip
polyline.bindTooltip("Ini adalah tooltip");
polyline.openTooltip();
```

Reference: [https://leafletjs.com/reference.html#polyline](https://leafletjs.com/reference.html#polyline)

---
> [unsorry@2024](https://unsorry.net)