# Lab10Web - Praktikum PHP OOP

## Nama : Lola Seftyliani
## NIM : 312410339
## Kelas : TI.24.A.4
## Matkul: Pemograman Web 1

## Tujuan Praktikum
- Memahami konsep OOP dasar di PHP.
- Membantu class, object, dan library modular (form, database).
- Mengimplementasikan modularisasi dalam proyek sederhana.

## Mobile.php
```html
<?php
class Mobil {
    public $warna;
    public $merk;
    public $harga;

    public function __construct($warna="Biru", $merk="BMW", $harga="10000000") {
        $this->warna = $warna;
        $this->merk = $merk;
        $this->harga = $harga;
    }

    public function gantiWarna($warnaBaru) {
        $this->warna = $warnaBaru;
    }

    public function info() {
        return "Merk: $this->merk, Warna: $this->warna, Harga: Rp " . number_format($this->harga, 0, ',', '.');
    }
}

// membuat objek mobil
$a = new Mobil(); 
$b = new Mobil("Hijau", "Toyota", 10000000);
?>

<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Contoh Class Mobil</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

<div class="container">
    <h1>Contoh Class Mobil</h1>

    <!-- Mobil pertama -->
    <h3>Mobil pertama</h3>
    <p>Warna: <b style="color:#007bff;"><?php echo $a->warna; ?></b></p>

    <?php $a->gantiWarna("Merah"); ?>

    <p>Setelah ganti warna:</p>
    <p>Warna: <b style="color:#d40046;"><?php echo $a->warna; ?></b></p>

    <hr>

    <!-- Mobil kedua -->
    <h3>Mobil kedua</h3>
    <p>Warna: <b style="color:#0f8b4c;"><?php echo $b->warna; ?></b></p>

    <div class="btn" style="display:inline-block; background:#ff8bbd; color:#5a1a2e;">
        <?php echo $b->info(); ?>
    </div>

</div>

</body>
</html>
```
Kode tersebut membuat sebuah class bernama Mobil yang memiliki properti warna, merk, dan harga. Constructor memberi nilai default ketika object dibuat, sedangkan method gantiWarna() digunakan untuk mengubah warna mobil. Method info() mengembalikan informasi lengkap tentang mobil dalam bentuk teks.

Setelah class dibuat, program membuat dua object: mobil pertama menggunakan nilai default, dan mobil kedua dengan warna Hijau dan merk Toyota. Di bagian HTML, nilai properti mobil pertama ditampilkan, lalu warnanya diubah menjadi Merah dan ditampilkan kembali. Mobil kedua juga ditampilkan bersama informasi lengkapnya melalui method info().
<img width="1919" height="828" alt="image" src="https://github.com/user-attachments/assets/c03e0bb4-6e32-4793-aa08-7432d205432a" />
