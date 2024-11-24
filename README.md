# praktikum6

# CODINGAN 1

```
kontak = {
  "maulana": "083183266926",
  "ibrahim": "087815646769"
}
print("\nKontak maulana:", kontak["maulana"])

kontak["sintia"] = "082127150958"
kontak["ibrahim"] = "087815646769"

print("\nSemua Nama:")
for nama in kontak:
  print("- " + nama)

print("\nSemua Nomor:")
for nomor in kontak.values(): 
  print("- " + nomor)

print("\nDaftar Nama dan Nomornya:")
for nama, nomor in kontak.items():
  print("- " + nama + ": " + nomor)

del kontak["ibrahim"]
print("\nhapus[ ibrahim ]")

print("\nSemua Nama setelah penghapusan :")
for nama in kontak:
  print("- " + nama)

print("\nSemua Nomor setelah penghapusan :")
for nomor in kontak.values():
  print("- " + nomor)

print("\nDaftar Nama dan Nomornya penghapusan :")
for nama, nomor in kontak.items():
     print("- " + nama + ":"+ nomor)
```

# HASIL CODINGAN 1

![Cuplikan layar 2024-11-23 135134](https://github.com/user-attachments/assets/170cc49f-8605-4aa3-a5f4-f50861f60f3a)

# Penjelasan Coding 1

1. Pembuatan Dictionary:

       kontak = {
       "maulana": "083183266926",
       "ibrahim": "087815646769"
       }

- Ini membuat dictionary bernama kontak yang menyimpan nama sebagai key dan nomor telepon sebagai value
- Awalnya berisi 2 kontak: MAULANA dan IBRAHIM

2. Mengakses Value:

       print("\nKontak maulana:", kontak["maulana"])
   
- Menampilkan nomor telepon MAULANA dengan mengakses dictionary menggunakan key "MAULANA"

3. Menambah Data:

       kontak["sintia"] = "082127150958"

- Menambahkan kontak baru dengan nama "SINTIA" dan nomornya ke dalam dictionary

4. Menampilkan Semua Nama (Keys):

       print("\nSemua Nama:")
        for nama in kontak:
       print("- " + nama)

- Menggunakan loop untuk menampilkan semua nama (keys) dalam dictionary

5. Menampilkan Semua Nomor (Values):

        print("\nSemua Nomor:")
        for nomor in kontak.values(): 
        print("- " + nomor)


- Menggunakan loop dan method .values() untuk menampilkan semua nomor telepon

6. Menampilkan Nama dan Nomor (Key-Value Pairs):

       print("\nDaftar Nama dan Nomornya:")
       for nama, nomor in kontak.items():
       print("- " +nama + ": " + nomor)

- Menggunakan method .items() untuk mengakses pasangan key-value sekaligus
- Menampilkan nama dan nomor dalam format "nama: nomor"

7. Menghapus Data:

       del kontak["ibrahim"]
       print("\nhapus[ ibrahim ]")

- Menghapus kontak "IBRAHIM" dari dictionary menggunakan keyword del

8. Menampilkan Data Setelah Penghapusan:

- Program kemudian mengulangi proses menampilkan nama, nomor, dan pasangan nama-nomor
- Hasilnya menunjukkan bahwa data "IBRAHIM" sudah tidak ada dalam dictionary

Dari output yang ditampilkan:

- Awalnya ada 3 kontak (MAULANA, SINTIA, IBRAHIM)
- Setelah penghapusan tersisa 2 kontak (MAULANA dan SINTIA)
- Setiap informasi ditampilkan dengan format yang rapi dan terstruktur

Program ini mendemonstrasikan operasi dasar pada dictionary Python:

- Membuat dictionary
- Mengakses value dengan key
- Menambah data baru
- Menghapus data
- Mengiterasi melalui keys, values, dan items

  # FLOWCHART

  
