[<< Back](../README.md)

# Scale

1. Tambahkan script berikut ini untuk membuat skala (scale) pada peta.
```javascript
// Scale
var scale = L.control.scale();
scale.addTo(map);
```

2. Untuk mengatur letak posisi skala (scale) pada peta, ubah script menjadi seperti berikut ini.
```javascript
// Scale 
var scale = L.control.scale({
	position: "bottomright",
});
```

3. Untuk mengatur satuan skala (scale) pada peta, misal hanya akan menampilkan satian metrik saja, ubah script menjadi seperti berikut ini.
```javascript
// Scale 
var scale = L.control.scale({
	imperial: false,
});
```
Reference: [https://leafletjs.com/reference.html#control-scale](https://leafletjs.com/reference.html#control-scale)

---
> [unsorry@2024](https://unsorry.net)