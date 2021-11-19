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
Dan jika data Kurang dari 200 Maka data yang setelanya akan berisi null

```

http://iotcampus.net/bmkg/?menu=gempa

```

## Sumber Data

- [Data Gempa](https://inatews.bmkg.go.id/light/?act=realtimeev) - 200 data realtime gempa
- [Data Cuaca](https://www.bmkg.go.id/cuaca/prakiraan-cuaca-indonesia.bmkg?Prov=07&NamaProv=DKI%20Jakarta) - Data cuaca DKI Jakarta hari ini

## Authors

- **Ringga Septia Pribadi**

*APPS ini merupakan pengembangan dari repo yang di miliki oleh Hudzaifah Al Jihad selaku pemilik code*
*Pengembangan ini bertujuan untuk memperbaiki model penampilan data agar lebih ramah bagi code dan penguna api itu sendiri*
*

- **Hudzaifah Al Jihad** - _Initial work_ - [bangjii](<a href="https://github.com/bangjii">cek di sini</a>)
```



  <img style="width:500px;height:600px;" src="https://scontent-sin6-4.xx.fbcdn.net/v/t1.6435-9/201128546_342438534115223_6657857503935702476_n.jpg?_nc_cat=100&cb=c578a115-c1c39920&ccb=1-5&_nc_sid=e3f864&_nc_eui2=AeGoJIpFiea0UOdynZIP_SgmiouWZ4ejUW6Ki5Znh6NRbrjA6HV0fSu9ire9C0SZwZ4nnDHTomblnMPiN1AF7580&_nc_ohc=iytVO3_Q_R8AX8-WES0&_nc_ht=scontent-sin6-4.xx&oh=c35ca4a29e0289c2ebba9f26302c6921&oe=61BDC988" />
