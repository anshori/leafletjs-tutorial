[<< Back](../README.md)

# Pane

1. Pane adalah layer yang digunakan untuk mengatur tata letak layer pada peta di atas atau di bawah layer lainnya.

2. Sebelum variabel `geojsonLayer` tambahkan script berikut.

```javascript
map.createPane('paneNamaLayer');
map.getPane("paneNamaLayer").style.zIndex = 401;
```

3. Nilai zIndex semakin besar maka layer akan semakin di atas layer lainnya.

4. Gunakan nilai zIndex lebih dari 200 supaya berada di atas basemap.

5. Di dalam variabel `geojsonLayer` tambahkan fungsi script berikut.

```javascript
pane: 'paneNamaLayer',
```

Reference: [https://leafletjs.com/reference.html#geojson-pane](https://leafletjs.com/reference.html#geojson-pane)

---
> [unsorry@2024](https://unsorry.net)