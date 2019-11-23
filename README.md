# **Praktikum 4**
# Program Menghitung Nilai Mahasiswa

Pada praktek kali ini, saya mencoba membuat program menentukan nilai mahasiswa dengan menggunakan list.

- Source Code dan Penjelasan
```
print("==================================================================")
print("|                 PROGRAM INPUT NILAI MAHASISWA                  |")
print("==================================================================")

nilai = []                                                            ## Membuat list nilai kosong
perulangan = True                                                     ## Membuat variable perulangan "true" untuk logika looping

while perulangan:                                                     ## Looping
    nama = input("Masukkan Nama: ")                                   ## Membuat variable nama untuk list dan menginputkan datanya
    nim = input("Masukkan NIM: ")                                     ## Membuat variable nim untuk list dan menginputkan datanya
    nilaiTugas = int(input("Masukkan Nilai Tugas: "))                 ## Membuat variable nilaiTugas untuk list dan menginputkan datanya
    nilaiUts = int(input("Masukkan Nilai UTS: "))                     ## Membuat variable nilaiUts untuk list dan menginputkan datanya
    nilaiUas = int(input("Masukkan Nilai UTS: ")                      ## Membuat variable nilaiUas untuk list dan menginputkan datanya
    nilaiAkhir = (nilaiTugas * 30/100) + (nilaiUts * 35/100) + (nilaiUas * 35/100) ## Membuat variable nilaiAkhir untuk list dan menggabungkan nilaiTugas, uts, dan uas dengan syarat yang sudah ditentukan.

    nilai.append([nama, nim, nilaiTugas, nilaiUts, nilaiUas, int(nilaiAkhir)])  ## Menambahkan semua list nama sampai nilaiAkhir ke list nilai.
    if (input("Tambah data (y/t)? ") == 't'):                         ## Jika kita tidak menambahkan data ketik "t" untuk mengakhiri
        perulangan = False                                            ## Looping selesai

print("\n                      DAFTAR NILAI MAHASISWA                    ")
print("==================================================================")
print("| No |     Nama     |    NIM    | Tugas |  UTS  |  UAS  |  Akhir |")
print("==================================================================")
i = 0                                                                         ## looping dimulai dari angka nol untuk mengurutkan data
for item in nilai:                                                            ## looping dari list nilai
    i += 1
    print("| {no:2d} | {nama:12s} | {nim:9s} | {nilaiTugas:5d} | {nilaiUts:5d} | {nilaiUas:5d} | {nilaiAkhir:6.2f} |"           ## Mengatur posisi tabel
          .format(no=i, nama=item[0], nim=item[1], nilaiTugas=item[2], nilaiUts=item[3], nilaiUas=item[4], nilaiAkhir=item[5])) ## Mengambil list yg sudah diinputkan didalam list nilai.
print("==================================================================")
```

- Screenshot Input
![Input](https://user-images.githubusercontent.com/22215113/69473008-eccfcc80-0de3-11ea-8174-26729aa0c3b9.png)

- Screenshot Ouput
![Output](https://user-images.githubusercontent.com/22215113/69473016-feb16f80-0de3-11ea-9ea0-8bbd5b837d0b.png)

```
                                 Veno Setyoaji Wiratama
                                        311910363
                                        TI.19.A.2
                                Universitas Pelita Bangsa
```
