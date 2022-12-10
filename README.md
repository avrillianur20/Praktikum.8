# praktikum.8
## Nama : Avrillia Nur Hidayah
## NIM : 312210309
## Kelas : TI.22.A3
 
 # Soal Tugas Praktikum.
 
![WhatsApp Image 2022-12-10 at 17 46 48](https://user-images.githubusercontent.com/115686359/206853338-0ae32af9-e590-4479-9c3a-7d569c24e288.jpeg)

## Code dan langkah-langkah sebagai berikut:

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
