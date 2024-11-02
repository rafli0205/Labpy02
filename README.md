## Membuat Program dan Flowchart dari program Tiket Bioskop dan juga Kalkulator
Nama : Rafli Dhiya Fadhaly

Nim : 312410251

Kelas : TI 24 A1
## 1. Membuat Program Tiket Bioskop
Program tiket bioskop ini adalah program untuk menghitung harga Tiket bioskop. Konsepnya adalah jika pengguna memiliki kartu member maka pengguna akan mendapatkan diskon 20%
## Flowcart Tiket Bioskop
![IMG-20241101-WA0001 1](https://github.com/user-attachments/assets/2ff2ac81-45c7-4399-89ab-008263effd67)
## Program akan meminta pengguna untuk menginputkan tipe tiket
```Python
Masukkan tipe tiket (reguler/vip): vip
Apakah Anda memiliki kartu member? (ya/tidak): ya
Harga tiket yang harus dibayar: 500000
```
## Penjelasan Kode
```Python
def hitung_harga_tiket():
  """Fungsi untuk menghitung harga tiket bioskop"""

  # Harga dasar tiket
  harga_reguler = 50000
  harga_vip = 100000
  diskon_member = 0.2 

  # Meminta input dari pengguna
  tipe_tiket = input("Masukkan tipe tiket (reguler/vip): ").lower()
  status_member = input("Apakah Anda memiliki kartu member? (ya/tidak): ").lower()

  # Menghitung harga tiket berdasarkan tipe tiket dan status member
  if tipe_tiket == "reguler":
    harga_awal = harga_reguler
  elif tipe_tiket == "vip":
    harga_awal = harga_vip
  else:
    print("Tipe tiket tidak valid.")
    return

  # Menghitung diskon jika pengguna adalah member
  diskon = harga_awal * diskon_member if status_member == "ya" else 0
  harga_akhir = harga_awal - diskon

  # Menampilkan hasil
  print("Harga tiket yang harus dibayar:", harga_akhir)

hitung_harga_tiket()
```
Harga Dasar Tiket Dua variabel Harga_Reguler dan Harga_vip menyimpan harga masing-masing. Diskon dihitung berdasarkan status keanggotaan. Jika pengguna adalah member (input "ya"), diskon 20% dari harga_awal dihitung. Jika tidak, diskon adalah 0. Program ini menghitung harga tiket dengan mempertimbangkan jenis tiket yang dibeli (reguler atau VIP) dan apakah pembeli memiliki kartu member yang memberikan diskon

Input Jenis Tiket: python tipe_tiket = input("Masukkan tipe tiket (reguler/VIP): ").strip().lower()

Program meminta pengguna untuk memasukkan jenis tiket yang diinginkan, yaitu "reguler" atau "VIP". Input tersebut diubah menjadi huruf kecil dan dihilangkan spasi di depan dan belakang untuk memastikan konsistensi, sehingga "VIP" atau "vip" tetap dianggap sama.

Input Status Member: python status_member = input("Apakah Anda memiliki kartu member? (ya/tidak): ").strip().lower()

Program meminta pengguna untuk memasukkan status apakah mereka memiliki kartu member ("ya" atau "tidak"). Penggunaannya mirip dengan input sebelumnya: diubah menjadi huruf kecil dan dihilangkan spasi.

Menentukan Harga Tiket: python if tipe_tiket == "reguler": harga_tiket = 35000 elif tipe_tiket == "vip": harga_tiket = 90000 else: print("Tipe tiket tidak valid.") harga_tiket = 0

Jika pengguna memilih tiket *reguler, maka harga_tiket diatur menjadi *35.000.
Jika pengguna memilih tiket *VIP, maka harga_tiket diatur menjadi *90.000.
Jika input tipe tiket tidak sesuai (bukan "reguler" atau "VIP"), program akan menampilkan pesan "Tipe tiket tidak valid." dan harga_tiket diatur menjadi 0.
Menghitung Diskon untuk Member: python if status_member == "ya" and harga_tiket > 0: diskon = harga_tiket * 0.3 total_harga = harga_tiket - diskon else: total_harga = harga_tiket

Jika pengguna adalah member (jawaban "ya") dan memilih tipe tiket yang valid (harga_tiket > 0), maka mereka mendapatkan diskon sebesar 30% dari harga_tiket.
Jika pengguna bukan member atau tipe tiket tidak valid, maka total_harga sama dengan harga_tiket tanpa diskon.
Menampilkan Total Harga: python if harga_tiket > 0: print(f"Total harga yang harus dibayar: Rp{total_harga:.2f}")

Jika harga tiket valid (harga_tiket > 0), program akan mencetak total harga yang harus dibayar, diformat hingga dua desimal (contoh: Rp35000.00).
Dengan struktur ini, program memastikan harga tiket dihitung dengan benar sesuai tipe tiket dan status keanggotaan pengguna.
## 2. Kalkulator sederhana
Program ini adalah program Kalkulator sederhana yang berfungsi untuk menghitung dua angka sesuai dengan operasi hitung yang dipilih.
## Flowchart dari Kalkulator Sederhana
![ticketflow 1](https://github.com/user-attachments/assets/eeb4d88c-26df-472a-bd8c-bc3c6265a956)
## Program akan meminta kita untuk memasukkan 3 angka untuk dibandingkan :
```Python
Masukkan angka pertama: 1000
Masukkan angka kedua: 100
Masukkan operator (+, -, *, /): *
Hasil: 100000.0
```
## Penjelasan Kode
```Python
def kalkulator():
  """Fungsi ini membuat kalkulator sederhana"""

  # Meminta input dari pengguna
  angka1 = float(input("Masukkan angka pertama: "))
  angka2 = float(input("Masukkan angka kedua: "))
  operator = input("Masukkan operator (+, -, *, /): ")

  # Melakukan operasi berdasarkan operator yang dipilih
  if operator == '+':
    hasil = angka1 + angka2
  elif operator == '-':
    hasil = angka1 - angka2
  elif operator == '*':
    hasil = angka1 * angka2
  elif operator == '/':
    if angka2 == 0:
      print("Tidak dapat membagi dengan nol")
    else:
      hasil = angka1 / angka2
  else:
    print("Operator tidak valid")

  # Menampilkan hasil
  if 'hasil' in locals():
    print("Hasil:", hasil)

kalkulator()
```
Kode program di atas adalah implementasi sederhana dari kalkulator yang dapat melakukan operasi dasar (penjumlahan, pengurangan, perkalian, dan pembagian) berdasarkan input pengguna. Mari kita bahas langkah-langkah kode ini:

## 1. Fungsi kalkulator
python def kalkulator(angka1, angka2, operator): if operator == "+": return angka1 + angka2 elif operator == "-": return angka1 - angka2 elif operator == "*": return angka1 * angka2 elif operator == "/": if angka2 != 0: return angka1 / angka2 else: return "Kesalahan: Pembagian dengan nol tidak diperbolehkan" else: return "Operator tidak valid"

Fungsi kalkulator mengambil tiga parameter:

angka1: bilangan pertama (float),
angka2: bilangan kedua (float),
operator: operasi yang ingin dilakukan (+, -, *, atau /).
Proses:

Fungsi memeriksa nilai operator dan menjalankan operasi yang sesuai.
Untuk pembagian, ada pengecekan tambahan untuk memastikan angka2 tidak nol, agar tidak terjadi error dalam perhitungan.
Jika operator tidak valid, fungsi mengembalikan pesan "Operator tidak valid".
## 2. Meminta Input dari Pengguna
python try: angka1 = float(input("Masukkan angka pertama: ")) operator = input("Masukkan operator (+, -, *, /): ") angka2 = float(input("Masukkan angka kedua: "))

Program meminta pengguna untuk memasukkan angka1, operator, dan angka2.
angka1 dan angka2 dikonversi ke float agar program bisa menerima angka desimal.
Error Handling:

Jika input tidak valid (misalnya pengguna memasukkan huruf untuk angka), blok try-except akan menangkap ValueError dan menampilkan pesan "Input tidak valid! Pastikan Anda memasukkan angka."
## 3. Menghitung Hasil dan Menampilkan
python hasil = kalkulator(angka1, angka2, operator) print(f"Hasil: {hasil}")

Setelah menerima input, program memanggil fungsi kalkulator dengan input yang diberikan dan menyimpan hasilnya dalam variabel hasil.
Program kemudian mencetak hasil.
## Contoh Output:
Input: angka pertama = 10, operator = +, angka kedua = 5

Output: Hasil: 15.0
Input: angka pertama = 10, operator = /, angka kedua = 0

Output: Kesalahan: Pembagian dengan nol tidak diperbolehkan
Program ini siap digunakan untuk operasi matematika dasar dengan penanganan error yang baik.
