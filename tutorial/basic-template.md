# Basic Template

1. Buat folder kerja baru dengan nama **leafletjs-tutorial**
2. Buat file **index.html** di dalam folder kerja Anda
3. Tuliskan kode berikut ke dalam file **index.html**

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>Leaflet JS</title>
		<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" integrity="sha256-p4NxAoJBhIIN+hmNHrzRCf9tD/miZyoHS5obTRR9BMY=" crossorigin="" />
		<style>
			#map {
				width: 100%;
				height: 600px;
			}
		</style>
	</head>
	<body>
		<div id="map"></div>

		<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js" integrity="sha256-20nQCchB9co0qIjJZRGuk2/Z9VM+kNiyxNV1lvTlZBo=" crossorigin=""></script>
		<script>
			// Inisialisasi peta
			var map = L.map("map").setView([-6.1753924, 106.8271528], 13);

			// Tile Layer Base Map
			var basemap = L.tileLayer("https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png", {
				attribution:
					'&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors',
			});

			// Menambahkan basemap ke dalam peta
			basemap.addTo(map);
		</script>
	</body>
</html>
```

---
> [unsorry@2024](https://unsorry.net)