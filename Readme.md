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





