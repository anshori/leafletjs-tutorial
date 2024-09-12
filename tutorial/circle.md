[<< Back](../README.md)

# Circle

1. Tambahkan script berikut ini untuk membuat circle pada peta.
```javascript
// Circle
var circle = L.circle([-6.1753924, 106.8271528], {
	color: "red", // warna garis
	opacity: 1, // opacity garis
	fillColor: "#f03", // warna fill
	fillOpacity: 0.5, // opacity fill
	radius: 1000, // radius dalam meter
});

// Menambahkan circle ke dalam peta
circle.addTo(map);
```

2. Tambahkan script berikut ini untuk menambahkan popup pada circle.
```javascript
// Popup
circle.bindPopup("<b>Hallo</b><br>Ini adalah popup");
circle.openPopup();
```

3. Tambahkan script berikut ini untuk menambahkan tooltip pada circle.
```javascript
// Tooltip
circle.bindTooltip("Ini adalah tooltip");
circle.openTooltip();
```

Reference: [https://leafletjs.com/reference.html#circle](https://leafletjs.com/reference.html#circle)

---
> [unsorry@2024](https://unsorry.net)