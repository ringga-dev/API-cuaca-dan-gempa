# BMKG

BMKG web content scraper, mengambil konten cuaca dan gempa dan menampilkan data dalam bentuk JSON

## Getting Started

Untuk mengakses API ini dapat langsung menggunakan url:

```
http://your.server.com/bmkg/?menu=%menu%&wilayah=%wilayah%
```

Dengan paramater

- menu: cuaca | gempa
- wilayah: bisa diisi nama provinsi seperti "dki jakarta", atau diisi "list" untuk melihat list provinsi yang terdaftar.
  contoh:

```
http://your.server.com/bmkg/?menu=cuaca&wilayah=aceh
http://your.server.com/bmkg/?menu=cuaca&wilayah=list
```

dan akan menghasilkan data JSON

```
	[
		{
			"kota": "Aceh Barat",
			"malam": "Berawan",
			"dini_hari": "Cerah Berawan",
			"suhu": "23 - 28",
			"kelembaban": "80 - 95"
		},
		{
			"kota": "Aceh Barat Daya",
			"malam": "Cerah Berawan",
			"dini_hari": "Berawan",
			"suhu": "23 - 27",
			"kelembaban": "80 - 95"
		},
	]

untuk gempa:

```

http://your.server.com/bmkg/?menu=gempa

```

yang akan menampilkan 200 data realtime gempa berdasarkan pengukuran (tanpa pemeriksaan data)

```

    [
    	{
    		"stts": "preliminary",
    		"tgl": "2021/11/19",
    		"jam": "06:01:56.504 (UTC)",
    		"lintang": "-6.86",
    		"bujur": "129.56",
    		"kedalaman": "193",
    		"m": "4.7",
    		"mt": "-",
    		"region": "Banda Sea"

    	},{
    		"stts": "preliminary",
    		"tgl": "2021/11/19",
    		"jam": "02:19:40.212 (UTC)",
    		"lintang": "-1.35",
    		"bujur": "120.52",
    		"kedalaman": "10",
    		"m": "2.6",
    		"mt": "-",
    		"region": "Sulawesi, Indonesia"
    	}
    ]

```

## Demo Page

List Provinsi

```

http://iotcampus.net/bmkg/?menu=cuaca&wilayah=list

```

Prakiraan Cuaca Daerah Jambi

```

http://iotcampus.net/bmkg/?menu=cuaca&wilayah=jambi

```

200 Gempa Yang Terdeteksi

```

http://iotcampus.net/bmkg/?menu=gempa

```

## Sumber Data

- [Data Gempa](https://inatews.bmkg.go.id/light/?act=realtimeev) - 200 data realtime gempa
- [Data Cuaca](https://www.bmkg.go.id/cuaca/prakiraan-cuaca-indonesia.bmkg?Prov=07&NamaProv=DKI%20Jakarta) - Data cuaca DKI Jakarta hari ini

## Authors

- **Ringga Septia Pribadi**

_APPS ini merupakan pengembangan dari repo yang di miliki oleh Hudzaifah Al Jihad selaku pemilik code_

- **Hudzaifah Al Jihad** - _Initial work_ - [bangjii](https://github.com/bangjii)
```
