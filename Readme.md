# Currency Apps
Aplikasi ini mencakup fungsi nilai perhitungan nilai tukar mata uang dari dollar ke rupiah.
Satu dollar dianggap senilai dengan 15.000

## Scope & Functionalities
- User dapat memasukkan angka
- User dapat menggunakan tombol hitung
- User mendapat info invalid jika yang diinputkan berupa text

## How does it works?

Diawali dengan method `MainWindow` pada class Mainwindow.xaml.cs, kita mendeklarasikan sebuah...

```Csharp
 public MainWindow()
        {
            InitializeComponent();
            Currency = new CurrencyController();
        }
```

Logika perhitungan  terdapat pada `CurrencyController.cs` sebagai berikut 
cara kerjanya yaitu nilai atau angka yang diinputkan akan dikalikan dengan harga dollar ke rupiah yaitu 15000. 

```csharp

        public string UsdToIdr(string nominal)
        {
            var nominalDouble = Convert.ToDouble(nominal);
            var result = nominalDouble * 15000;
            return Convert.ToString(result);
        }
```

### Latihan 

1. Percobaan

   - Pada percobaan 1 nomer 4 saat diinputkan angka atau huruf maka hasil output akan sesuai dengan yang diinputkan.
   - Pada percobaan 2 nomer 2 angka yaang diinputkan akan dikali dengan 10000.
   - Pada percobaan 2 nomor 3 saat diinputkan angka atau huruf akan terjadi  error karena string tidak dapat dikonversi ke double.
   - Pada percobaan 3 nomor 2 angka yang diinputkan akan ditampilkan setelah dikali 4.
   - Pada percobaan 3 nomor 3 saat diinputkan huruf atau string maka akan ditampilkan invalid.
   
2. `CurrencyController.cs` berfungsi memisahkan antara program dan logic agar mudah dibaca.
3. Method isAllowed berfungsi mengecek variabel nominal input yang dimasukkan oleh user berupa string atau integer
4. Regex berfungsi mengetahui karakter yang diinputkan user berupa angka atau selain angka, jika yang diinputkan bukan berupa angka maka akan mengeluarkan output invalid.
5. Class Diagram
     





