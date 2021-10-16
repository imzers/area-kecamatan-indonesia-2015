# area-kecamatan-indonesia-2015
Jumlah area (desa/kelurahan) per Kecamatan di Indonesia, Data pada thn 2015

Untuk menampilkan jumlah area per kecamatan, menggunakan MySQL Query:

```
SELECT 
	ds.province_code, ds.province_name,
	ds.city_code, ds.city_name,
	ds.district_code,
	ds.district_name,
	COUNT(1) AS total_area
FROM **{TABLE_NAME}** AS ds
WHERE ds.country_code = 360
GROUP BY ds.country_code, ds.province_code, ds.city_code, 
	ds.district_code, ds.district_name
```
