# CurrencyApps
Mengkonversi Dollar $
Aplikasi ini berfungsi untuk perhitungan nilai tukar mata uang dolar menjadi rupiah. Yang mana 1 dollar di konfersikan menjadi rupiah akan bernilai Rp 15.000 

## Scope & Functionalities
- User dapat memasukkan angka(nilai dolar) yang akan di convert menjadi rupiah
- User dapat mengeklik tombol hitung untuk mengetahui konfersi
- User mendapat info invalid jika memasukkan berupa teks/huruf karena,memang tidak di peruntukan teks / huruf

## How does it works
Diawali dari method "MainWindow" pada class window.xaml.cs dideklarasikan dengan:

``` csharp
public MainWindow()
        {
            InitializeComponent();
            Currency = new CurrencyController();
        }
```
logika perhitungan terdapat pada CurrencyController.cs sebagai berikut:
``` csharp
public string usdToIdr(string nominal)
        {
            var nominalDouble = Convert.ToDouble(nominal);
            var result = nominalDouble * 15000;
            return Convert.ToString(result);
        }
```
