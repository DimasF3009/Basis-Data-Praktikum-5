# Basis-data-praktikum-5

```
Latihan
1 Lakukan join table Mahasiswa dan Dosen
2 Lakukan join tabel Matakuliah dan Dosen
3 Lakukan join table JadwalMengajar, Dosen, dan Matakuluan
4 Lakukan join tabel KrsMahasiswa, Mahasiswa, Matakuliah, dan Dosen
```
# LATIHAN

1 Lakukan join table Mahasiswa dan Dosen
![tg1](https://github.com/DimasF3009/Basis-Data-Praktikum-5/assets/115356128/2014b9f4-5535-46a6-bb23-13092d4dc9c8)


2 Lakukan join tabel Matakuliah dan Dosen
![tg2](https://github.com/DimasF3009/Basis-Data-Praktikum-5/assets/115356128/a742c559-a51e-43ca-ad5c-0e5c5e50a5d0)
```
Pada kode ini hasilnya empty karena kedua tabel tidak saling ber relasi
```


3 Lakukan join table JadwalMengajar, Dosen, dan Matakuluan
![tg3](https://github.com/DimasF3009/Basis-Data-Praktikum-5/assets/115356128/2abdbb33-7af2-4631-a508-b1c1d65bfde2)


4 Lakukan join tabel KrsMahasiswa, Mahasiswa, Matakuliah, dan Dosen
![tg4](https://github.com/DimasF3009/Basis-Data-Praktikum-5/assets/115356128/7b5a1c72-176d-46e7-b63f-7c6d29d74972)

# LATIHAN

1. JOIN table Mahasiswa dan Dosen
```
SELECT Mahasiswa.nim, Mahasiswa.nama, Mahasiswa.jenis_kelamin, Dosen.nama AS 'Dosen' 
FROM Mahasiswa 
JOIN Dosen ON Dosen.kd_ds=Mahasiswa.kd_ds;
```
![vs1](https://github.com/DimasF3009/Basis-Data-Praktikum-5/assets/115356128/7ae17c02-9129-43ac-85ae-789e08268952)


2. LEFT JOIN table Mahasiswa dan Dosen
```
SELECT Mahasiswa.nim, Mahasiswa.nama, Mahasiswa.jenis_kelamin, Dosen.nama AS 'Dosen'
FROM Mahasiswa
LEFT JOIN Dosen ON Dosen.kd_ds=Mahasiswa.kd_ds;
```
![vs2](https://github.com/DimasF3009/Basis-Data-Praktikum-5/assets/115356128/d85a9a75-cbe1-4b7f-98da-f8305ac007a8)


3. JOIN table JadwalMengajar, Dosen, dan Matakuliah
```
SELECT jadwalMengajar.kd_mk, matakuliah.nama AS 'Mata kuliah', matakuliah.sks, Dosen.nama AS 'Dosen Pengampu'
FROM jadwalMengajar
JOIN Dosen ON jadwalMengajar.kd_ds = Dosen.kd_ds
JOIN matakuliah ON jadwalMengajar.kd_mk = matakuliah.kd_mk;
```
![vs3](https://github.com/DimasF3009/Basis-Data-Praktikum-5/assets/115356128/cc7cddcb-85fe-460d-b3af-91e00c6bcdf4)


4. JOIN table JadwalMengajar, Dosen, dan Matakuliah
```
SELECT jadwalMengajar.kd_mk, matakuliah.nama AS 'Mata kuliah', matakuliah.sks, Dosen.nama AS 'Dosen Pengampu', jadwalMengajar.hari, jadwalMengajar.jam, jadwalMengajar.ruang
FROM jadwalMengajar
JOIN Dosen ON jadwalMengajar.kd_ds = Dosen.kd_ds
JOIN matakuliah ON jadwalMengajar.kd_mk = matakuliah.kd_mk;
```
![vs4](https://github.com/DimasF3009/Basis-Data-Praktikum-5/assets/115356128/96032c37-3b49-45db-8888-5f49a6c8f114)

















