# Soal 1
## query
```sql
     id_guru int(10) primary key not null,
     nama_depan varchar(40) not null unique,
     nama_belakaCREATE TABLE tabel_guru(
     id_gng varchar(40) not null,
     mapel varchar(40) not null,
     usia int(10) not null,
     tanggal_lahir varchar(20) not null);
```

## hasil
![image](asetremd/s1.png)

## Analisis
1. Tabel yang dibuat bernama "tabel_guru" dengan menggunakan perintah `CREATE TABLE`.
    
2. Struktur kolom yang didefinisikan dalam tabel adalah sebagai berikut:
    
    - `id_gng`: Kolom dengan tipe data `int(10)` digunakan untuk menyimpan ID guru. Kolom ini dinyatakan sebagai primary key (`PRIMARY KEY`) yang berarti nilainya harus unik dan tidak boleh kosong (`NOT NULL`).
    - `nama_depan`: Kolom dengan tipe data `varchar(40)` digunakan untuk menyimpan nama depan guru. Kolom ini juga dinyatakan sebagai kolom yang unik (`UNIQUE`) yang berarti setiap nilai yang dimasukkan harus berbeda. Kolom ini juga tidak boleh kosong (`NOT NULL`).
    - `nama_belaka`: Kolom dengan tipe data default yang tidak didefinisikan. Dalam contoh ini, tipe data kolom tidak ditentukan.
    - `mapel`: Kolom dengan tipe data `varchar(40)` digunakan untuk menyimpan mata pelajaran yang diajar oleh guru. Kolom ini tidak boleh kosong (`NOT NULL`).
    - `usia`: Kolom dengan tipe data `int(10)` digunakan untuk menyimpan usia guru. Kolom ini tidak boleh kosong (`NOT NULL`).
    - `tanggal_lahir`: Kolom dengan tipe data `varchar(20)` digunakan untuk menyimpan tanggal lahir guru. Kolom ini tidak boleh kosong (`NOT NULL`).
3. Setiap kolom memiliki batasan validasi dan aturan seperti `NOT NULL` untuk memastikan bahwa kolom-kolom tersebut harus diisi dengan nilai yang valid pada saat memasukkan data ke dalam tabel.
    
4. Tabel "tabel_guru" akan dibuat dengan struktur kolom yang telah didefinisikan.


# soal 2

## query

```sql
insert into tabel_guru
values (1, "Adrianty", null, "Pemograman web","Ketua jurusan", 34, "1982-06-29"),
(2, "Ibrahim", "mallombasang", "Basis Data,"Kepala sekolah", 21, "2000-09-21"),
 (3, "Muhammad", "Yusuf", "Pemodelan perangkat lunak", null, 28, "1992-12-24"),
 (4, "Rusdyansya", null, "Pemograman berorientitas","Asisten kepala sekolah", 25, "1996-01-21");

```
## hasil
![image](asetremd/s2.png)

## Analisis
Perintah `INSERT INTO` digunakan untuk memasukkan data ke dalam tabel `tabel_guru`. Pada perintah ini, kita memasukkan empat baris data ke dalam tabel dengan menggunakan perintah `VALUES`.

Setiap baris data didefinisikan dalam tanda kurung dan dipisahkan oleh tanda koma. Setiap kolom pada tabel `tabel_guru` harus memiliki nilai yang sesuai dalam urutan yang benar.

Analisis nilai-nilai yang dimasukkan untuk setiap baris:

1. Baris pertama:
    
    - `id_guru`: 1
    - `nama_depan`: 'Adrianty'
    - `nama_belakang`: NULL
    - `mapel`: 'Pemograman web'
    - `jabatan`: 'Ketua jurusan'
    - `usia`: 34
    - `tanggal_lahir`: '1982-06-29'
2. Baris kedua:
    
    - `id_guru`: 2
    - `nama_depan`: 'Ibrahim'
    - `nama_belakang`: 'mallombasang'
    - `mapel`: 'Basis Data'
    - `jabatan`: 'Kepala sekolah'
    - `usia`: 21
    - `tanggal_lahir`: '2000-09-21'
3. Baris ketiga:
    
    - `id_guru`: 3
    - `nama_depan`: 'Muhammad'
    - `nama_belakang`: 'Yusuf'
    - `mapel`: 'Pemodelan perangkat lunak'
    - `jabatan`: NULL
    - `usia`: 28
    - `tanggal_lahir`: '1992-12-24'
4. Baris keempat:
    
    - `id_guru`: 4
    - `nama_depan`: 'Rusdyansya'
    - `nama_belakang`: NULL
    - `mapel`: 'Pemograman berorientitas'
    - `jabatan`: 'Asisten kepala sekolah'
    - `usia`: 25
    - `tanggal_lahir`: '1996-01-21'
# soal 3

## query
```sql
insert into tabel_guru
values (5,"hansar", null, "Bahasa indonesia", null, 17,"2006-06-06);
```

## Hasil
![image](asetremd/s3.png)

## Analisis
- `id_guru`: 5
- `nama_depan`: 'hansar'
- `nama_belakang`: NULL
- `mapel`: 'Bahasa indonesia'
- `jabatan`: NULL
- `usia`: 17
- `tanggal_lahir`: '2006-06-06'

Setelah melakukan perintah `INSERT INTO`, Anda kemudian menjalankan perintah SQL `SELECT * FROM tabel_guru;`. Perintah ini digunakan untuk mengambil dan menampilkan semua data yang ada dalam tabel `tabel_guru`.

Hasil dari perintah `SELECT *` akan menampilkan semua kolom dan nilai-nilai yang ada dalam tabel `tabel_guru`, termasuk data yang telah dimasukkan sebelumnya serta data baru yang ditambahkan.


# soal 4
## query
```sql
select * from tabel_guru;
```

## Hasil
![image](asetremd/s4.png)
## Analisis
Hasil dari perintah `SELECT *` akan menampilkan semua kolom dan nilai-nilai yang ada dalam tabel `tabel_guru`.

# soal 5

## query
```sql
select * from tabel_guru
where id_guru = "4";
```
## Hasil
![image](asetremd/s5.png)
## Analisis
dari perintah `SELECT *` dengan kondisi `WHERE id_guru = "4"` akan bergantung pada data yang ada dalam tabel tersebut. Jika terdapat baris dengan nilai `id_guru` sama dengan "4", maka baris tersebut akan dipilih dan ditampilkan.

# soal 6
## query
```sql
update tabel_guru set nama_belakang="ganteng" where id_guru="2";
```
## Hasil

![image](asetremd/s6.png)

## Analisis
1. `UPDATE tabel_guru`: Mengindikasikan bahwa kita akan melakukan operasi pembaruan (update) pada tabel `tabel_guru`.
2. `SET nama_belakang = "ganteng"`: Menentukan kolom yang akan diperbarui dan nilai baru yang akan diberikan. Dalam hal ini, kolom `nama_belakang` akan diubah menjadi "ganteng".
3. `WHERE id_guru = "2"`: Menentukan kondisi untuk baris data yang akan diperbarui. Hanya baris dengan nilai `id_guru` sama dengan "2" yang akan mengalami perubahan.

Jika terdapat baris dalam tabel `tabel_guru` dengan `id_guru` sama dengan "2", maka baris tersebut akan mengalami perubahan. Kolom `nama_belakang` pada baris tersebut akan diubah menjadi "ganteng".
# soal 7

## query
```sql
delete from tabel_guru id_guru=5;
```
## Hasil
![image](asetremd/s7.png)
## Analisis
1. `DELETE FROM tabel_guru`: Mengindikasikan bahwa kita akan melakukan operasi penghapusan (delete) pada tabel `tabel_guru`.
2. `WHERE id_guru = 5`: Menentukan kondisi untuk baris data yang akan dihapus. Hanya baris dengan nilai `id_guru` sama dengan 5 yang akan dihapus.

Jika terdapat baris dalam tabel `tabel_guru` dengan nilai `id_guru` sama dengan 5, maka baris tersebut akan dihapus dari tabel.
# soal 8

## query
```sql
select * from tabel_guru
where mapel LIKE 'pem%' and usia <30
ORDER BY usia ASC;
```
## Hasil
![image](asetremd/s8.png)
## Analisis
1. `SELECT * FROM tabel_guru`: Mengindikasikan bahwa kita akan mengambil semua kolom dan data dari tabel `tabel_guru`.
2. `WHERE mapel LIKE 'pem%' AND usia < 30`: Menentukan kondisi untuk pengambilan data. Hanya baris yang memenuhi kondisi tersebut yang akan ditampilkan. Kondisi ini memfilter data dengan dua syarat: kolom `mapel` dimulai dengan kata "pem" dan kolom `usia` kurang dari 30.
3. `ORDER BY usia ASC`: Menyusun hasil pengambilan data secara menaik (ascending) berdasarkan kolom `usia`. Artinya, data akan ditampilkan mulai dari yang memiliki nilai usia terkecil hingga yang memiliki nilai usia terbesar.

Hasil dari perintah `SELECT *` dengan kondisi `WHERE mapel LIKE 'pem%' AND usia < 30 ORDER BY usia ASC` akan bergantung pada data yang ada dalam tabel `tabel_guru`. Hanya baris yang memenuhi kedua kondisi tersebut yang akan ditampilkan, dan data akan disusun berdasarkan usia secara menaik.
# soal 9 
## query 
```sql
select id_guru, nama_depan from tabel_guru
where nama_depan LIKE '_%i%';
```

## Hasil
![image](asetremd/s9.png)
## Analisis
1. `SELECT id_guru, nama_depan FROM tabel_guru`: Mengindikasikan bahwa kita akan mengambil kolom `id_guru` dan `nama_depan` dari tabel `tabel_guru`.
2. `WHERE nama_depan LIKE '_%i%'`: Menentukan kondisi untuk pengambilan data. Hanya baris yang memenuhi kondisi tersebut yang akan ditampilkan. Kondisi ini memfilter data dengan satu syarat: kolom `nama_depan` mengandung karakter "i" di suatu posisi kecuali di awal kata, karena pola '_%i%' mengharuskan ada minimal satu karakter sebelum "i".

Hasil dari perintah `SELECT id_guru, nama_depan` dengan kondisi `WHERE nama_depan LIKE '_%i%'` akan bergantung pada data yang ada dalam tabel `tabel_guru`. Hanya baris yang memenuhi kondisi tersebut yang akan ditampilkan, dan hanya kolom `id_guru` dan `nama_depan` yang akan ditampilkan.

# soal 10
## query
```sql
select concat_ws("",nama_depan, nama_belakang) AS nama_lengkap from tabel_guru;
```
## Hasil
![image](asetremd/s10.png)
## Analisis 
1. `SELECT CONCAT_WS("", nama_depan, nama_belakang) AS nama_lengkap`: Mengindikasikan bahwa kita akan membuat kolom baru yang disebut `nama_lengkap` dengan menggabungkan (concatenating) nilai dari kolom `nama_depan` dan `nama_belakang` dalam tabel `tabel_guru` menggunakan fungsi `CONCAT_WS()`. Fungsi `CONCAT_WS()` digunakan untuk menggabungkan nilai-nilai kolom dengan pemisah yang ditentukan di dalam tanda kutip kosong ("").
2. `FROM tabel_guru`: Menunjukkan bahwa kita akan mengambil data dari tabel `tabel_guru`.

Hasil dari perintah `SELECT CONCAT_WS("", nama_depan, nama_belakang) AS nama_lengkap FROM tabel_guru` akan menghasilkan satu kolom baru yang disebut `nama_lengkap`, yang berisi hasil penggabungan nilai dari kolom `nama_depan` dan `nama_belakang` dalam tabel `tabel_guru`. Setiap nilai dalam kolom `nama_lengkap` akan berisi kombinasi dari `nama_depan` dan `nama_belakang` tanpa ada pemisah di antara keduanya.
# soal 11
## query
```sql
alter table tabel_guru
add status enum("PNS", "pppk", "Honorer");
```
## Hasil
![image](asetremd/s11.png)
## Analisis
1. `ALTER TABLE tabel_guru`: Mengindikasikan bahwa kita akan mengubah struktur tabel `tabel_guru`.
2. `ADD status ENUM("PNS", "pppk", "Honorer")`: Menentukan perubahan yang akan dilakukan pada tabel. Perintah `ADD` digunakan untuk menambahkan kolom baru ke dalam tabel, dalam hal ini `status`. Tipe data kolom baru ini adalah `ENUM`, yang berarti nilainya terbatas pada sekumpulan nilai yang telah ditentukan. Nilai-nilai yang diperbolehkan untuk kolom `status` adalah "PNS", "pppk", dan "Honorer".

Setelah perintah tersebut dieksekusi, tabel `tabel_guru` akan mengalami perubahan dengan penambahan kolom `status` yang memiliki tipe data `ENUM`. Kolom ini akan membatasi nilai yang dapat dimasukkan ke dalamnya hanya pada nilai yang telah ditentukan ("PNS", "pppk", dan "Honorer").

# soal 12
## query
```sql
select nama_depan, max(usia) as usia from tabel_guru;
```

## Hasil
![image](asetremd/s12.png)

## Analisis
1. `SELECT nama_depan, MAX(usia) AS usia`: Mengindikasikan bahwa kita akan mengambil kolom `nama_depan` dan nilai maksimum dari kolom `usia` dalam tabel `tabel_guru`. Alias `AS usia` digunakan untuk memberi nama kolom hasil agregasi (nilai maksimum) sebagai "usia".

Hasil dari perintah `SELECT nama_depan, MAX(usia) AS usia FROM tabel_guru` akan menghasilkan satu baris data yang berisi nilai dari kolom `nama_depan` yang diambil dari tabel `tabel_guru`, serta nilai maksimum dari kolom `usia` dalam tabel tersebut. Alias `usia` digunakan sebagai nama kolom hasil agregasi.
