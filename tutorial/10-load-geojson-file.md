[<< Back](../README.md)

# Load GeoJSON File

## using fetch

1. Tambahkan script berikut ini untuk memanggil data GeoJSON
```javascript
// Define layer groups
let jumlahpenduduk = L.layerGroup();

// Load geojson file
fetch('data/jumlah_penduduk.geojson')
    .then(response => response.json())
    .then(data => {
        L.geoJSON(data).addTo(jumlahpenduduk);
    });
```

## using jQuery

1. Tambahkan script berikut ini di dalam body untuk memanggil library jQuery.
```html
<script src="https://code.jquery.com/jquery-3.7.1.min.js"></script>
```

Reference: [https://jquery.com/](https://jquery.com/)

---
> [unsorry@2024](https://unsorry.net)