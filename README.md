# praktikum.8
## Nama : Avrillia Nur Hidayah
## NIM : 312210309
## Kelas : TI.22.A3
 
 # Soal Tugas Praktikum.
 
![WhatsApp Image 2022-12-10 at 17 46 48](https://user-images.githubusercontent.com/115686359/206853338-0ae32af9-e590-4479-9c3a-7d569c24e288.jpeg)

## Code dan langkah-langkah sebagai berikut:

## Panduan dalam menjalankan Outpunya:
#### L=Lihat data
#### T=Tambah data
#### U=Ubah data
#### C=Cari data
#### H=Hapus data
#### K=keluar dari program 

### 1. Buat dictionary kosong
```Mahasiswa {}```

### 2. Menu di program utama
```
def menu():
    print("\n")
    print("====================================================")
    print("      \t\t Program input nilai       ")
    print("====================================================\n")

    x = input("[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar]: ")
    print("\n")

    if x == 'L':
        show()
    elif x == 'T':
        add()
    elif x == 'U':
        update()
    elif x == 'H':
        delete()
    elif x == 'C':
        search()
    elif x == 'K':
        print("==========================================================================")
        print('\n')
        print("> You exit the code                        ")
        print("\n")
        print("==========================================================================")

        exit()

    else:
        print("            KODE YANG ANDA MASUKKAN TIDAK VALID !!!!!!!!!!!")


while True:
  menu()
```  

### 3. Program untuk menambah data
```
def add():
    print("Tambah Data")
    nama = input("Nama\t         : ")
    nim = input("NIM\t         : ")
    uts = int(input("Nilai UTS\t : "))
    uas = int(input("Nilai UAS\t : "))
    tugas = int(input("Nilai Tugas\t : "))
    akhir = (tugas * 30 / 100) + (uts * 35 / 100) + (uas * 35 / 100)
    mahasiswa[nama] = nim, tugas, uts, uas, akhir
```

### Outputnya adalah

Saya akan menambahkan 2 data:

![Screenshot (655)](https://user-images.githubusercontent.com/115686359/206855047-0cb1c4dc-61e8-4e2a-be35-3bef09b9fc71.png)

![Screenshot (656)](https://user-images.githubusercontent.com/115686359/206855115-270e8b7f-9b90-4d70-a30f-174ec01934f2.png)

### 4. Program melihat data yang sudah di tambahkan
```
def show():
    if mahasiswa.items():
        print("Daftar Nilai")
        print("=================================================================================")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("=================================================================================")
        i = 0
        for a in mahasiswa.items():
            i += 1
            print("| {no:2d} | {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} |      {5:6.2f} |"
                  .format(a[0][: 14], a[1][0], a[1][1], a[1][2], a[1][3], a[1][4], no=i))
        print("=================================================================================")
```

### Outputnya adalah:

![Screenshot (658)](https://user-images.githubusercontent.com/115686359/206855255-637c1c4e-d835-403e-99bd-ace26626fbe7.png)

### 5. Program untuk mengubah data
```
def update():
    print("Ubah Data")
    nama = input("Masukkan Nama : ")
    if nama in mahasiswa.keys():
        nim = input("NIM\t : ")
        uts = int(input("Nilai UTS\t : "))
        uas = int(input("Nilai UAS\t : "))
        tugas = int(input("Nilai Tugas\t : "))
        akhir = (tugas * 30 / 100) + (uts * 35 / 100) + (uas * 35 / 100)
        mahasiswa[nama] = nim, tugas, uts, uas, akhir
```

### Outputnya adalah

![Screenshot (659)](https://user-images.githubusercontent.com/115686359/206855415-2683092b-36cf-46a3-8db9-cac1c89645d6.png)

Kemudian data akan terubah jjika kita mengetik ```L``` yaitu Lihat

![Screenshot (660)](https://user-images.githubusercontent.com/115686359/206855454-602f3555-4e27-4ffa-aca0-a8b74b75e652.png)

### 6. Program untuk menghapus data
```
def delete():
    print("Hapus Data")
    nama = input("Masukkan Nama : ")

    if nama in mahasiswa.keys():
        del mahasiswa[nama]

    else:
        print("Nama tidak ditemukan")
```

### Outputnya adalah

![Screenshot (662)](https://user-images.githubusercontent.com/115686359/206855556-fea52c23-e47a-4a7b-afca-a447d98d03f2.png)

### 7. Program untuk mencari data
```
def search():
    print("Cari Data")
    a = input("Masukkan Nama : ")
    if a in mahasiswa.keys():
        print("===========================================================================")
        print("|      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir   |")
        print("===========================================================================")
        print("| {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} |     {5:6.2f} |"
              .format(a, mahasiswa[a][0], mahasiswa[a][1], mahasiswa[a][2], mahasiswa[a][3], mahasiswa[a][4]))
        print("===========================================================================")

    else:
        print("=================================================================================")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("=================================================================================")
        print("|                          DATA TIDAK DITEMUKAN                                 |")
        print("=================================================================================")

```

### Outpunya adalah

![Screenshot (661)](https://user-images.githubusercontent.com/115686359/206855693-83206462-79bd-4367-81d5-fb49aaee425f.png)

### Flowchart nya
