# Marker

1. Tambahkan script berikut ini untuk membuat marker pada peta.
```javascript
// Marker
var marker = L.marker([-6.1753924, 106.8271528]);

// Menambahkan marker ke dalam peta
marker.addTo(map);
```

2. Tambahkan script berikut ini untuk menambahkan popup pada marker.
```javascript
// Popup
marker.bindPopup("<b>Hallo</b><br>Ini adalah popup");
marker.openPopup();
```

3. Tambahkan script berikut ini untuk menambahkan tooltip pada marker.
```javascript
// Tooltip
marker.bindTooltip("Ini adalah tooltip");
marker.openTooltip();
```

Reference: [https://leafletjs.com/reference.html#marker](https://leafletjs.com/reference.html#marker)

---
> [unsorry@2024](https://unsorry.net)