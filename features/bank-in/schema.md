# Schema

## Database

### Bank Header

| Kolom         | Kolom Frontend                                                                                                   | Requirement                                                                                                                      | Tujuan                                                                                                                                                                  | Contoh Data                                                      |
| ------------- | ---------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| id            | — (tidak ditampilkan; digunakan secara internal sebagai key/route record)                                        | Primary key, auto increment, unsigned integer                                                                                    | Nomor pengenal unik untuk sistem saja. User tidak pernah melihat atau mengisi ini.                                                                                      | 1, 2, 3, 4, 5                                                    |
| formulir\_id  | Form Number                                                                                                      | Wajib diisi · unsigned int · FK → formulir.id · ON UPDATE cascade · ON DELETE cascade                                            | Nomor bukti transaksi yang bisa dicari & dilacak di halaman List/Detail. Contoh: `BANK-IN/0004/VIII/26`.                                                                | BANK-OUT/0001/VIII/26, BANK-IN/0004/VIII/26)                     |
| coa\_id       | Bank Account                                                                                                     | Wajib diisi · unsigned int · FK → coa.id · ON UPDATE cascade · ON DELETE cascade                                                 | Rekening bank mana yang dipakai — misalnya BCA Giro atau Mandiri. Ini yang muncul di dropdown "Bank Account" saat user buat transaksi baru.                             | 20122, 20130                                                     |
| person\_id    | Payment From                                                                                                     | Wajib diisi · unsigned int · FK → person.id (idx: point\_finance\_bank\_person\_index) · ON UPDATE restrict · ON DELETE restrict | Siapa pihak yang terlibat: customer yang **membayar** (untuk Bank In)                                                                                                   | 501, 502, 503, 504, 505                                          |
| payment\_flow | — (bukan field langsung; menentukan kolom List — Received atau Disbursed — tempat nominal baris ini ditampilkan) | Wajib diisi · string · nilai yang diharapkan: "in" atau "out" (divalidasi di level aplikasi — bukan enum di database)            | Penanda apakah ini uang **MASUK** atau **KELUAR**. Inilah yang membuat nominal transaksi muncul di kolom **Received** atau **Disbursed** pada halaman List              | "out", "out", "in", "out", "in"                                  |
| total         | Amount                                                                                                           | Wajib diisi · decimal(16,4)                                                                                                      | Jumlah total uang dalam transaksi ini. **Dihitung otomatis** dari penjumlahan semua baris rincian akun di bawahnya — user tidak perlu isi manual, sistem yang jumlahkan | 310000.0000, 320100.0000, 2500000.0000, 313600.0000, 750000.0000 |

### Bank Detail

| Kolom                    | Kolom Frontend                                                            | Aturan                                                                                                                               | Tujuan                                                                                                                                            | Contoh Data                                                                      |
| ------------------------ | ------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| id                       | — (tidak ditampilkan)                                                     | Primary key, auto increment, unsigned integer                                                                                        | Pengenal unik untuk setiap baris item dalam satu transaksi bank.                                                                                  | 1, 2, 3, 4, 5                                                                    |
| point\_finance\_bank\_id | — (tidak ditampilkan langsung; mengelompokkan baris pada tabel line-item) | Wajib diisi · unsigned int · FK → point\_finance\_bank.id (idx: point\_finance\_bank\_index) · ON UPDATE cascade · ON DELETE cascade | Menghubungkan baris rincian ini ke transaksi (Header) induknya. Kalau Header-nya dihapus, semua baris rincian di bawahnya ikut terhapus otomatis. | 1, 1, 1, 2, 2                                                                    |
| coa\_id                  | Account                                                                   | Wajib diisi · unsigned int · FK → coa.id · ON UPDATE restrict · ON DELETE restrict                                                   | Akun akuntansi spesifik untuk baris ini — misalnya "Beban Bensin Kendaraan" atau "Beban Cetak Banner"                                             | 53101, 53106, 53103, 41001, 53115                                                |
| allocation\_id           | Allocation                                                                | opsional                                                                                                                             | Cost center / cabang / alokasi tempat baris item ini dibebankan.                                                                                  | 1, 1, 2, (dalam praktiknya nullable untuk baris bank-in — lihat Catatan)         |
| notes\_detail            | Notes                                                                     | opsional · text                                                                                                                      | Catatan bebas yang menjelaskan peruntukan baris item ini.                                                                                         | "Testing", "Bensin mobil box kiriman HB Mojokerto", "Pelunasan invoice INV-2201" |
| amount                   | Amount                                                                    | Wajib diisi · decimal(16,4)                                                                                                          | Nominal untuk baris rincian ini secara spesifik. Semua Amount di sini otomatis dijumlahkan menjadi Total di Header.                               | 100000.0000, 120100.0000, 200000.0000, 2500000.0000, 313600.0000                 |

## Sample Database

### Bank Header

| id | formulir\_id | coa\_id (Bank Account) | person\_id (Payment From/To) | payment\_flow | total   |
| -- | ------------ | ---------------------- | ---------------------------- | ------------- | ------- |
| 1  | 201          | 20122                  | 501                          | **in**        | 100000  |
| 2  | 202          | 20130                  | 502                          | **in**        | 275000  |
| 3  | 203          | 20122                  | 501                          | **out**       | 100000  |
| 4  | 204          | 20130                  | 503                          | **out**       | 2500000 |
| 5  | 205          | 20122                  | 504                          | **out**       | 1285948 |
| 6  | 206          | 20130                  | 505                          | **out**       | 313600  |

### Bank Detail

| id | point\_finance\_bank\_id | coa\_id (Account)            | allocation\_id | notes\_detail     | amount  |
| -- | ------------------------ | ---------------------------- | -------------- | ----------------- | ------- |
| 1  | 1                        | 53101 (ACCOUNT PAYABLE)      | NULL           | Testing           | 100000  |
| 2  | 3                        | 53103 (HUTANG DAGANG)        | NULL           | Retur pembayaran  | 275000  |
| 3  | 3                        | 53101 (ACCOUNT PAYABLE)      | NULL           | Testing           | 100000  |
| 4  | 4                        | 53102 (PIUTANG USAHA)        | NULL           | Pelunasan invoice | 2500000 |
| 5  | 5                        | 53101 (ACCOUNT PAYABLE)      | NULL           | Reimburse kas     | 1285948 |
| 6  | 6                        | 53105 (HONORARIUM KONSULTAN) | NULL           | Cetak banner      | 313600  |
