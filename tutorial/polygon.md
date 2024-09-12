[<< Back](../README.md)

# Polygon

1. Tambahkan script berikut ini untuk membuat polygon pada peta.
```javascript
// Polygon
var vertexPolygon = [
	[-6.1574398,106.7968941],
	[-6.1569275,106.8614388],
	[-6.1849327,106.8506241],
	[-6.1999592,106.8593788],
	[-6.2119118,106.7901993]
];
var polygon = L.polygon(vertexPolygon, {
	color: "purple", // warna garis
	weight: 3, // ketebalan garis
	opacity: 1, // opacity garis
	fillColor: "#0f3", // warna fill
	fillOpacity: 0.5, // opacity fill
});

// Menambahkan polygon ke dalam peta
polygon.addTo(map);
```

2. Tambahkan script berikut ini untuk menambahkan popup pada polygon.
```javascript
// Popup
polygon.bindPopup("<b>Hallo</b><br>Ini adalah popup");
polygon.openPopup();
```

3. Tambahkan script berikut ini untuk menambahkan tooltip pada polygon.
```javascript
// Tooltip
polygon.bindTooltip("Ini adalah tooltip");
polygon.openTooltip();
```

Reference: [https://leafletjs.com/reference.html#polygon](https://leafletjs.com/reference.html#polygon)

---
> [unsorry@2024](https://unsorry.net)