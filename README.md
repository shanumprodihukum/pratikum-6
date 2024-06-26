# pratikum-6
1. Tampilkan data karyawan yang bekerja pada departemen yang sama dengan karyawan yang bernama Dika
SELECT nik, nama, id_dept FROM Karyawan WHERE id_dept = (SELECT id_dept FROM Karyawan WHERE nama = 'Dika');
Script :
![6](https://github.com/shanumprodihukum/pratikum-6/assets/148035386/244f257f-b59c-454b-b3ed-ce942fbf7b4c)
2. Tampilkan data karyawan yang gajinya lebih besar dari rata-rata gaji semua karyawan. Urutkan menurun berdasarkan besaran gaji
Script :
![7](https://github.com/shanumprodihukum/pratikum-6/assets/148035386/3396a6bf-7e3d-4137-a90f-5b2d2db1aab6)
SELECT nik, nama, id_dept, gaji_pokok FROM karyawan WHERE gaji_pokok > (SELECT AVG(gaji_pokok) FROM Karyawan) ORDER BY gaji_pokok DESC;
3. Tampilkan nik dan nama karyawan untuk semua karyawan yang bekerja di departmen yang sama dengan karyawan dengan nama yang mengandung huruf 'K'.
Script :
![8](https://github.com/shanumprodihukum/pratikum-6/assets/148035386/f18c9116-f5c4-427a-8539-4c554b163432)
4. Tampilkan data karyawan yang bekerja pada departemen yang ada di Kantor pusat.
Script :
![9](https://github.com/shanumprodihukum/pratikum-6/assets/148035386/9f0d5973-d31b-4e21-9d53-0d3803c16eef)
5. Tampilkan nik dan nama karyawan untuk semua karyawan yang bekerja di departmen yang sama dengan karyawan dengan nama yang mengandung huruf 'K' dan yang gajinya lebih besar dari rata-rata gaji semua karyawan
SELECT DISTINCT k1.nik, k1.nama FROM karyawan k1 JOIN karyawan k2 ON k1.id_dept = k2.id_dept WHERE k1.gaji_pokok > (SELECT AVG(gaji_pokok) FROM karyawan WHERE nama LIKE '%K%');
Script :
![10](https://github.com/shanumprodihukum/pratikum-6/assets/148035386/cf164dd3-0674-4d56-ba05-45113105d901)
