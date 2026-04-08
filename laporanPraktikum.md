# <h1 align="center">Laporan Praktikum Modul 1 - ... </h1>
<p align="center">[MUHAMMADTETUKOKEMALPASHA] - [109082500181]</p>

## Unguided 

### 1. [Soal]
#### soal1.go

```go

package main

import "fmt"

func fibonacci(n int) int {
	if n == 0 {
		return 0
	}
	if n == 1 {
		return 1
	}
	return fibonacci(n-1) + fibonacci(n-2)
}

func main() {
	var n int
	fmt.Print("Masukkan nilai n: ")
	fmt.Scan(&n)

	fmt.Print("n  ")
	for i := 0; i <= n; i++ {
		fmt.Printf("%d  ", i)
	}
	fmt.Println() 
                                     
	fmt.Print("Sn ")
	for i := 0; i <= n; i++ {
		
		fmt.Printf("%d  ", fibonacci(i))
	}
	fmt.Println()
}
```
### Output Unguided :

##### Output 
![Screenshot Output Unguided 1_1]
[penjelasan] :Program ini ditulis dalam bahasa Go dan berfungsi untuk menampilkan deret Fibonacci hingga nilai ke-n yang dimasukkan oleh pengguna. Fungsi `fibonacci(n int)` menggunakan metode rekursif, yaitu memanggil dirinya sendiri untuk menghitung nilai Fibonacci dengan aturan dasar: jika n = 0 maka hasilnya 0, jika n = 1 maka hasilnya 1, dan untuk nilai lainnya dihitung dari penjumlahan dua bilangan sebelumnya (`fibonacci(n-1) + fibonacci(n-2)`). Pada fungsi `main`, program meminta input nilai n dari pengguna, lalu mencetak baris pertama berupa indeks dari 0 sampai n, dan baris kedua berupa nilai deret Fibonacci yang sesuai untuk setiap indeks tersebut.


## Unguided 

### 2. [Soal]
#### soal2.go

```go
package main

import "fmt"

func main() {
	var n int
	fmt.Scan(&n)
	bintang(n, 0)
}

func bintang(n, i int) {
	if i != n {
		baris(i,0)
		fmt.Println("")
		bintang(n, i+1)
	}else{
		baris(i,0)
	}
}

func baris(i, a int) {
	if a != i {
		fmt.Print("*")
		baris(i, a+1)
	}
}

```
### Output Unguided :

##### Output 
![Screenshot Output Unguided 1_1]
[penjelasan] : Program ini ditulis dalam bahasa Go dan berfungsi untuk mencetak pola bintang menggunakan konsep rekursif. Pada fungsi `main`, program menerima input berupa angka n yang menentukan jumlah baris pola, lalu memanggil fungsi `bintang(n, 0)` untuk mulai mencetak. Fungsi `bintang` bekerja secara rekursif untuk mengatur jumlah baris, di mana setiap baris dicetak dengan memanggil fungsi `baris(i, 0)` yang bertugas mencetak sejumlah bintang sesuai nilai i pada baris tersebut. Fungsi `baris` juga menggunakan rekursi untuk mencetak karakter "*" satu per satu hingga mencapai jumlah yang diinginkan. Hasil akhirnya adalah pola segitiga bintang yang jumlah bintangnya bertambah di setiap baris dari 0 hingga n.

## Unguided 

### 3. [Soal]
#### soal3.go

```go
package main

import "fmt"

func cariFaktor(n, i int) {
	if i <= n {
		if n%i == 0 {
			fmt.Printf("%d ", i)
		}
		cariFaktor(n, i+1)
	}
}

func main() {
	var n int
	fmt.Print("Masukkan N: ")
	fmt.Scan(&n)
	fmt.Print("Faktor: ")
	cariFaktor(n, 1)
	fmt.Println()
}
```
### Output Unguided :

##### Output 
![Screenshot Output Unguided 1_1]
[penjelasan] :Program ini ditulis dalam bahasa Go dan berfungsi untuk mencari serta menampilkan semua faktor dari sebuah bilangan yang dimasukkan oleh pengguna. Pada fungsi `main`, program meminta input nilai N, kemudian memanggil fungsi `cariFaktor(n, 1)` untuk mulai mengecek faktor dari angka 1 hingga N. Fungsi `cariFaktor` menggunakan rekursi, di mana setiap nilai i dicek apakah merupakan faktor dari n dengan kondisi `n % i == 0`; jika iya, maka nilai i akan dicetak. Proses ini terus berlanjut dengan memanggil fungsi yang sama dengan i+1 hingga i lebih besar dari n, sehingga semua faktor dari bilangan tersebut berhasil ditampilkan.


### 4. [Soal]
#### soal4.go

```go
package main

import "fmt"

func main() {
	var n,i int = 0,1
	fmt.Scan(&n)
	turun(n,i)
	naik(n,i)
}

func turun(n, i int) {
	if n != i{
	fmt.Print(n)
	fmt.Print(" ")
	turun(n-1,i)
	}
}

func naik(n,i int){
	if i <= n{
		fmt.Print(i)
		fmt.Print(" ")
		naik(n,i+1)
	}
}

```
### Output Unguided :

##### Output 
![Screenshot Output Unguided 1_1]
[penjelasan] :Program ini ditulis dalam bahasa Go dan berfungsi untuk mencetak angka secara menurun lalu menaik menggunakan rekursi. Pada fungsi `main`, program membaca input nilai n, lalu memanggil dua fungsi yaitu `turun(n, i)` dan `naik(n, i)` dengan nilai awal i = 1. Fungsi `turun` mencetak angka dari n ke bawah hingga mendekati 1 dengan cara mengurangi nilai n secara rekursif selama n tidak sama dengan i. Setelah itu, fungsi `naik` mencetak angka dari 1 hingga n dengan cara menambah nilai i secara rekursif selama i kurang dari atau sama dengan n. Hasil akhirnya adalah deretan angka yang ditampilkan turun dari n ke 1, kemudian naik kembali dari 1 ke n.


### 5. [Soal]
#### soal5.go

```go
package main

import "fmt"

func cetakGanjil(n, i int) {
	if i <= n {
		if i%2 != 0 {
			fmt.Printf("%d ", i)
		}
		cetakGanjil(n, i+1)
	}
}

func main() {
	var n int
	fmt.Print("Masukkan N: ")
	fmt.Scan(&n)
	cetakGanjil(n, 1)
	fmt.Println()
}


```
### Output Unguided :

##### Output 
![Screenshot Output Unguided 1_1]
[penjelasan] :Program ini ditulis dalam bahasa Go dan berfungsi untuk menampilkan bilangan ganjil dari 1 hingga N menggunakan rekursi. Pada fungsi `main`, program meminta pengguna memasukkan nilai N, lalu memanggil fungsi `cetakGanjil(n, 1)` untuk memulai dari angka 1. Fungsi `cetakGanjil` akan mengecek setiap angka i apakah ganjil dengan kondisi `i % 2 != 0`; jika benar, maka angka tersebut dicetak. Selanjutnya fungsi memanggil dirinya sendiri dengan nilai i+1 hingga i lebih besar dari n, sehingga semua bilangan ganjil dari 1 sampai N berhasil ditampilkan.


### 6. [Soal]
#### soal6.go

```go
package main

import "fmt"

func main() {
	var x, y int
	var hasil int = 1
	fmt.Scan(&x,&y)
	pangkat(x,y,hasil)
}

func pangkat(x, y, hasil int){
	if y > 0{
		hasil = x * hasil
		pangkat(x,y-1,hasil)
	}else{
		fmt.Print(hasil)
	}
}

```
### Output Unguided :

##### Output 
![Screenshot Output Unguided 1_1]
[penjelasan] :Program ini ditulis dalam bahasa Go dan berfungsi untuk menghitung hasil perpangkatan suatu bilangan menggunakan rekursi. Pada fungsi `main`, program menerima dua input yaitu x sebagai bilangan dasar dan y sebagai pangkat, serta menginisialisasi variabel `hasil` dengan nilai 1, kemudian memanggil fungsi `pangkat(x, y, hasil)`. Fungsi `pangkat` bekerja secara rekursif dengan cara mengalikan `hasil` dengan x selama nilai y masih lebih dari 0, sambil mengurangi nilai y di setiap pemanggilan. Ketika y sudah mencapai 0, proses berhenti dan nilai `hasil` yang merupakan hasil akhir dari x pangkat y akan dicetak.
