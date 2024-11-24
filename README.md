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

  ![flowchart praktikum6](https://github.com/user-attachments/assets/3b59495a-b106-409c-9532-1a9b843eee3c)

   # coding 2
```
    # Dictionary untuk menyimpan data mahasiswa
    data_mahasiswa = {}

    # Fungsi untuk menambahkan data mahasiswa
    def tambah_data():
      nim = input("Masukkan NIM: ")
    if nim in data_mahasiswa:
        print("Data dengan NIM ini sudah ada!")
        return
    nama = input("Masukkan Nama: ")
    tugas = float(input("Masukkan Nilai Tugas: "))
    uts = float(input("Masukkan Nilai UTS: "))
    uas = float(input("Masukkan Nilai UAS: "))
    akhir = (0.3 * tugas) + (0.35 * uts) + (0.35 * uas)
    data_mahasiswa[nim] = {"nama": nama, "tugas": tugas, "uts": uts, "uas": uas, "akhir": akhir}
    print("Data berhasil ditambahkan!")

    # Fungsi untuk mengubah data mahasiswa
    def ubah_data():
      nim = input("Masukkan NIM yang ingin diubah: ")
    if nim not in data_mahasiswa:
        print("Data tidak ditemukan!")
        return
    print("Data ditemukan: ", data_mahasiswa[nim])
    nama = input("Masukkan Nama baru: ")
    tugas = float(input("Masukkan Nilai Tugas baru: "))
    uts = float(input("Masukkan Nilai UTS baru: "))
    uas = float(input("Masukkan Nilai UAS baru: "))
    akhir = (0.3 * tugas) + (0.35 * uts) + (0.35 * uas)
    data_mahasiswa[nim] = {"nama": nama, "tugas": tugas, "uts": uts, "uas": uas, "akhir": akhir}
    print("Data berhasil diubah!")

    # Fungsi untuk menghapus data mahasiswa
    def hapus_data():
      nim = input("Masukkan NIM yang ingin dihapus: ")
    if nim in data_mahasiswa:
        del data_mahasiswa[nim]
        print("Data berhasil dihapus!")
    else:
        print("Data tidak ditemukan!")

    # Fungsi untuk mencari data mahasiswa
    def cari_data():
      nim = input("Masukkan NIM yang ingin dicari: ")
    if nim in data_mahasiswa:
        print("Data ditemukan: ", data_mahasiswa[nim])
    else:
        print("Data tidak ditemukan!")

    # Fungsi untuk menampilkan semua data mahasiswa
    def tampilkan_data():
      if not data_mahasiswa:
        print("TIDAK ADA DATA")
        return
    print("Daftar Nilai")
    print("=" * 63)
    print("| NO |    NIM    |      NAMA      | TUGAS | UTS | UAS | AKHIR |")
    print("=" * 63)
    for i, (nim, data) in enumerate(data_mahasiswa.items(), start=1):
        print(f"| {i:<2} | {nim:<9} | {data['nama']:<13} | {data['tugas']:<5} | {data['uts']:<3} | {data['uas']:<3} | {data['akhir']:<5.2f} |")
    print("=" * 63)

    # Program utama
    def main():
      while True:
        print("\n[L]ihat, [T]ambah, [U]bah, [H]apus, [C]ari, [K]eluar")
        pilihan = input("Pilihan: ").lower()
        if pilihan == "l":
            tampilkan_data()
        elif pilihan == "t":
            tambah_data()
        elif pilihan == "u":
            ubah_data()
        elif pilihan == "h":
            hapus_data()
        elif pilihan == "c":
            cari_data()
        elif pilihan == "k":
            print("Keluar dari program. Terima kasih!")
            break
        else:
            print("Pilihan tidak valid!")

    if __name__ == "__main__":
         main()
```

# HASIL CODINGAN 2

![Cuplikan layar 2024-11-24 234506](https://github.com/user-attachments/assets/adb6a5a8-d536-48fa-9c62-b5d8add41c88)

# Penjelasan 

Berikut adalah ringkasan ulang program manajemen data mahasiswa:  

1.Menu Utama:  
   Program dimulai dengan menampilkan pilihan berikut:  
   - Lihat data mahasiswa: Menampilkan daftar mahasiswa yang ada.  
   - Tambah data mahasiswa: Menambahkan informasi mahasiswa baru.  
   - Ubah data mahasiswa: Memperbarui informasi mahasiswa tertentu.  
   - Hapus data mahasiswa: Menghapus data mahasiswa berdasarkan NIM.  
   - Cari data mahasiswa: Mencari data mahasiswa dengan NIM tertentu.  
   - Keluar: Mengakhiri program.  

2. Lihat Data Mahasiswa:  
   Jika pengguna memilih opsi ini, program akan menampilkan daftar mahasiswa. Jika tidak ada data, program akan menampilkan pesan "TIDAK ADA DATA".  

3. Tambah Data Mahasiswa:  
   - Program meminta pengguna memasukkan NIM.  
   - Jika NIM sudah ada, program akan memberi pesan "DATA SUDAH ADA".  
   - Jika NIM belum ada, program meminta pengguna mengisi data tambahan seperti nama, nilai tugas, nilai UTS, dan nilai UAS.  
   - Program akan menghitung nilai akhir dan menyimpan data tersebut.  

4. Ubah Data Mahasiswa:  
   - Pengguna diminta memasukkan NIM mahasiswa yang ingin diperbarui.  
   - Jika NIM ditemukan, program meminta pengguna mengedit data seperti nama, nilai tugas, nilai UTS, dan nilai UAS.  
   - Program akan menghitung ulang nilai akhir dan menyimpan perubahan.  

5. Hapus Data Mahasiswa:  
   - Pengguna diminta memasukkan NIM mahasiswa yang ingin dihapus.  
   - Jika NIM ditemukan, data akan dihapus dari database.  

6. Cari Data Mahasiswa:  
   - Pengguna diminta memasukkan NIM mahasiswa yang ingin dicari.  
   - Jika NIM ditemukan, program akan menampilkan informasi mahasiswa.  
   - Jika tidak ditemukan, program akan memberi pesan "DATA TIDAK DITEMUKAN".  

7. Keluar:  
   Program akan berhenti ketika opsi ini dipilih.  

Informasi Tambahan:  
- Input NIM: Digunakan untuk memasukkan NIM mahasiswa.  
- Pengecekan Data: Program memastikan apakah NIM sudah ada atau belum.  
- Tampilkan Data: Data mahasiswa akan ditampilkan di layar.  
- Input Informasi Tambahan: Pengguna akan mengisi nama, nilai tugas, nilai UTS, dan nilai UAS.  
- Hitung Nilai Akhir: Program menghitung nilai akhir berdasarkan data yang dimasukkan.  
- Simpan atau Hapus: Data akan disimpan atau dihapus sesuai perintah pengguna.
