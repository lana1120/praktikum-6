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

