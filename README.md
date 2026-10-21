Deskripsi
klasifikasimhs.csv adalah dataset berbentuk CSV yang berisi data
kondisi tempat tinggal dan sosial-ekonomi orang tua, serta label
kelayakan keringanan Uang Kuliah Tunggal (UKT). Dataset ini dapat
digunakan sebagai bahan latihan eksplorasi data, prapemrosesan data, dan
klasifikasi sederhana.
Catatan: Dataset ini tidak menjelaskan sumber data, periode
pengumpulan, maupun definisi resmi kode kategori. Jangan gunakan data
ini untuk mengambil keputusan nyata tentang kelayakan bantuan sebelum
asal-usul dan aturan labelnya diverifikasi.

Isi dataset
Dataset berisi 100 baris data dan 6 kolom.
  Kolom                           Deskripsi               Tipe data yang
                                                          disarankan
  Tempat Tinggal                Kode kategori tempat    Kategorikal/biner
                                  tinggal; arti kode 0
                                  dan 1 belum
                                  dijelaskan dalam file   

  Pekerjaan Orang Tua           Jenis pekerjaan orang   Kategorikal
                                  tua                     

  Penghasilan Orang Tua         Penghasilan orang tua   Numerik
                                  dalam angka;
                                  satuan/periode tidak
                                  dicantumkan secara
                                  eksplisit               

  Jumlah Tanggungan Orang Tua   Jumlah tanggungan orang Bilangan bulat
                                  tua                     

  Kendaraan                     Kode jumlah/kategori    Kategorikal atau
                                  kendaraan; arti kode    bilangan bulat, setelah
                                  0, 1, dan 2 belum definisi dikonfirmasi
                                  dijelaskan dalam file   

  Kelayakan Keringanan UKT      Label target kelayakan; Kategorikal/biner
                                  arti 0 dan 1 perlu  setelah dibersihkan
                                  dikonfirmasi dari
                              pembuat dataset         
Persiapan penggunaan
1. Simpan klasifikasimhs.csv di folder proyek.
2. Baca file menggunakan aplikasi spreadsheet atau pustaka Python
   seperti pandas.
3. Periksa nilai kategori dan tipe data sebelum analisis.
4. Bersihkan anomali data yang tercatat pada DATASHEET.md.
5. Pastikan definisi setiap kode kategori dan label telah dikonfirmasi
   sebelum melatih model.
Contoh membaca file dengan Python:
import pandas as pd

data = pd.read_csv("klasifikasimhs.csv")
print(data.head())
print(data.info())
print(data.isna().sum())
Struktur berkas
project/
├── klasifikasimhs.csv
├── README.md
└── DATASHEET.md
Batasan
- Tidak ada keterangan sumber, lisensi, tanggal pengumpulan, atau
  metode pengumpulan data.
- Arti kode kategori belum dijelaskan.
- Dataset memiliki anomali yang perlu diperiksa sebelum analisis atau
  pemodelan.
- Dataset sebaiknya dianggap sebagai data latihan sampai validitas dan
  izin penggunaannya dikonfirmasi.