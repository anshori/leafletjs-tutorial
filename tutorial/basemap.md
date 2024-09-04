# Basemap

1. Pada bagian script **Tile Layer Base Map** ubahlah variabel **basemap** menjadi beberapa jenis basemap misalnya OSM, ESRI Word Imagery, ESRI Topo, dll.
2. Ubah script **basemap.addTo(map)** sesuai dengan nama variabel basemap yang akan ditampilkan.

```javascript
// Tile Layer Base Map
var osm = L.tileLayer("https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png", {
		attribution:
				'&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors',
});

var Esri_WorldImagery = L.tileLayer('https://server.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer/tile/{z}/{y}/{x}', {
	attribution: 'Tiles &copy; Esri &mdash; Source: Esri, i-cubed, USDA, USGS, AEX, GeoEye, Getmapping, Aerogrid, IGN, IGP, UPR-EGP, and the GIS User Community'
});

var Esri_WorldShadedRelief = L.tileLayer('https://server.arcgisonline.com/ArcGIS/rest/services/World_Shaded_Relief/MapServer/tile/{z}/{y}/{x}', {
	attribution: 'Tiles &copy; Esri &mdash; Source: Esri',
	maxZoom: 13
});

// Menambahkan basemap ke dalam peta
Esri_WorldImagery.addTo(map);

```

Source tile layer basemap: [https://leaflet-extras.github.io/leaflet-providers/preview/](https://leaflet-extras.github.io/leaflet-providers/preview/)