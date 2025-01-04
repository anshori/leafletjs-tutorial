[<< Back](../README.md)

# Control Layer

1. Tambahkan script berikut ini untuk membuat control layer pada peta.
```javascript
// Control Layer
var baseMaps = {
	"OpenStreetMap": osm,
	"Esri World Imagery": Esri_WorldImagery,
	"Rupa Bumi Indonesia": rupabumiindonesia,
};

var overlayMaps = {
	"Marker": marker,
	"Circle": circle,
	"Polyline": polyline,
	"Polygon": polygon,
};

var controllayer = L.control.layers(baseMaps, overlayMaps);
controllayer.addTo(map);
```

Reference: [https://leafletjs.com/reference.html#control-layers](https://leafletjs.com/reference.html#control-layers)


### **_Contoh_**

[https://anshori.github.io/leafletjs-tutorial/sample/7-control-layer.html](https://anshori.github.io/leafletjs-tutorial/sample/7-control-layer.html)

---
> [unsorry@2024](https://unsorry.net)