# praktikum5 Membuat list, menambahkan, mengedit, mengambil elemen pada list di Python.

#### Repository ini sebagai tugas Mata kuliah Bahasa Pemrogramman.

1. Baik Pertama-tama buatlah sebuah Folder `Praktikum5` 

    `Note Untuk penamaan folder dan file bisa sesuai keinginan kalian`
   
![5a026d59-d577-4635-827a-65586afa6ec3](https://user-images.githubusercontent.com/115473865/202857633-3ada68ef-94bc-4106-9f53-6d48de14ef46.jpg)

2. Selanjutnya buka file `List.py` lalu masukan code dibawah ini :

   ```Python
   # membuat 5 list dengan type data yang berbeda

    # membuat list
print("Buat sebuah list sebanyak 5 elemen dengan nilai bebas")
list = [1, 2, 3, 4, 5]
print(list)

# mengakses list
print("Menampilkan elemen 3")
print(list[2])

print("ambil nilai elemen 2 sampai ke 4")
print(list[1:4])

print("ambil elemen terakhir")
print(list[-1])

# mengubah elemen list
print("ubah elemen 4 dengan nilai lainnya")
list[4]=10
print(list[3])

print("ubah elemen 4 sampai dengan elemen terakhir")
list[4:5]=[20,11]
print(list)

# Tambah elemen list
print("Ambil 2 bagian dari list pertama(A) dan jadikan list ke 2(B)")
list_pertama=list[3:5]
print(list_pertama)

print("tambah list B dengan nilai string")
list_pertama.append("guest")
print(list_pertama)

print("Tambah list B dengan 3 nilai")
list_pertama.append(["guest",7,8])
print(list_pertama)

print("Menggabungkan list B dengan list A")
gabung=list_pertama+list
print(gabung)

3. Selanjutnya jalankan file dengan cara buka terminal lalu ketikan `python List.py` dan berikut hasilnya :

   


## Membuat program input data mahasiswa beserta nilai dan disimpan didalam List.

  Berikut Flowchart program yang akan kita buat :

  ![flowchart program](img/flowchart.png)

#### Requirement
- Pip [install pip](https://pypi.org/project/pip/)
- Cara install pip [cara install pip](https://www.anbidev.com/python-pip/)
- Package Tabulate

1. Pertama kita install Package `Tabulate` dengan cara buka terminal lalu copas `pip install tabulate` sebagai berikut :

    ![tabulate](img/tabulate.png)

2. Lalu buka file `Praktikum5.py` dan masukan code berikut

    ```Python
    # import package tabulate
    from tabulate import tabulate

    # membuat list kosong untuk menampung data
    dataMahasiswa = []
    no = 0
    # melakukan perulangan input sesuai keinginan sampai pertanyaan tambah data dimunculkan kembali
    while(True):
    # membuat variable untuk menampung inputan
    no += 1
    nama = input("Masukan Nama : ")
    nim = input("Masukan NIM : ")
    kelas = input("Masukan Kelas : ")
    matkul = input("Masukan Mata Kuliah : ")

    # mengkonversi string ke integer
    tugas = int(input("Masukan Nilai Tugas : "))
    uts = int(input("Masukan Nilai UTS : "))
    uas = int(input("Masukan Nilai UAS : "))

    # menjumlahkan nilai dari tugas,uts dan uas
    nilai_akhir = (tugas * 30 / 100) + (uts * 35 / 100) + (uas * 35 / 100)

    # lakukan pengecekan jika nilai_akhir lebih besar dari 50 maka Lulus selain itu tidak lulus dan mengulang mata kuliah
    if (nilai_akhir > 50):
        keterangan = "Lulus"
    else:
        keterangan = "Tidak Lulus, Mengulang Mata kuliah"
    # menambahkan data input ke list dataMahasiswa
    dataMahasiswa.append(
        [no, nama, nim, kelas, matkul, tugas, uts, uas, nilai_akhir, keterangan])

    # input tambah data jika tekan y maka input kembali, selain itu berhenti dan tampilkan data
    tambah_data_lagi = input("Tambah Data lagi ? (y/t) : ")
    if(tambah_data_lagi == "t"):
        break

    # tampilkan dataMahasiswa menggunakan tabulate package agar tampilan berbentuk table
    print(tabulate(dataMahasiswa, headers=[
          "No", "Nama", "Nim", "Kelas", "Mata Kuliah", "Tugas", "UTS", "UAS", "Nilai Akhir", "Keterangan"], tablefmt="fancy_grid"))
    ```

3. Selanjutnya jalankan file dengan cara buka terminal lalu ketikan `python Praktikum5.py` dan berikut hasilnya :

    ![hasil praktium5](img/praktikum5.png)

    `Selesai terima kasih`

    [saweria](https://saweria.co/adamwebdev)
