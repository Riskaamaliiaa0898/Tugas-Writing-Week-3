# JAVA SCRIPT INTERMEDIATE
## JavaScript - Array
> Mengorganisasi data dan menyimpan data adalah core concept dari programming. Array adalah tipe data list order yang dapat menyimpan tipe data apapun di dalamnya. Array dapat menyimpan tipe data String, Number, Boolean, dan lainnya.

Cara membuat Array

__Array__ didefinisikan menggunakan square brackets []

    // Cara mendefiniskan Array di JS

    let arrayData = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

    // Memanggil 1 data dari dalam array

    console.log("Sebelum Update", arrayData[0]);

    // Cara update nilai dalam suatu variable array (Update Tunggal)

    arrayData[0] = 15;
    console.log("Sesudah Update", arrayData[0]);

Const in Array

- Jika menggunakan let, kita dapat mengubah array  dengan array baru dan konten nilai yang ada di dalam array dengan nilai lain
- Const tidak bisa melakukan update data. Namun pada Array kita dapat melakukan update konten nilai di dalam array (mutable).
-    Yang tidak bisa adalah mengubah array dengan array yang baru jika menggunakan const


    Caranya menggunakan :

    // Array menggunakan Const
    const arrayDataConst = [10, 20, 30, 40, 50];
    console.log("Sebelum Update", arrayDataConst);

    arrayDataConst[2] = 10;
    console.log("Sesudah Update", arrayDataConst);

__Array Properties__ => Array memiliki 5 properti yang sering digunakan yaitu constructor, length, index, input, dan prototype.

__.length__ (length akan mengembalikan nilai dari jumlah panjang data suatu array.)

    // Melihat jumlah array dari suatu Variable Array
    // .length

    let panjangArrayData = arrayData.length;
    console.log("Jumlah Array Data", panjangArrayData);

Array Method => Array memiliki method atau biasa disebut built-in methods. Artinya Javascript sudah memudahkan kita dengan menyediakan function/method umum yang bisa kita gunakan.

Contoh Array Built-in Methods

__.push()__ adalah method untuk menambahkan item  array pada urutan yang paling akhir.

    let data = [];
    console.log("Sebelum di Push", data);

    data.push("H");
    data.push("J");

    console.log("Sesudah di Push", data);

__.pop()__ adalah method yang menghapus item array index terakhir.

    data.pop();
    data.pop();
    // console.log("Sesudah di Push", data);

__.shift()__ adalah method untuk menghapus item Array pada index pertama.

    // Contoh Shift
    console.log(antrianMinyak.shift());

__.unshift()__ adalah method untuk menambahkan item Array pada index pertama

    // Contoh Unshift
    antrianMinyak.unshift("Ujang");

__.sort()__ adalah method untuk mengurutkan secara Ascending atau Descending Alphanumeric.

    // Contoh Sort
    let number = [1, 45, 0, -2, 29, 11];
    console.log(number);
    console.log(number.sort());

Looping pada Array => Array memiliki built in methods untuk melakukan looping yaitu __.map() dan .forEach()__

__.ForEach()__ adalah method untuk melakukan looping pada setiap elemen array.

    // Perulangan Array menggunakan Foreach
    // Tidak memiliki nilai balikan atau return

    antrianMinyak.forEach((item, index) => {
    antrianMinyak[index] = item + " " + index;
    });

    console.log(antrianMinyak);

__.map()__ melakukan perulangan/looping dengan membuat array baru.

    // Perulangan Array menggunakan Map
    let antrianMinyakAsep = antrianMinyak.map((item) => {
    if (item === "Asep") {
        return true;
    } else {
        return false;
    }
    });

    console.log(antrianMinyakAsep);

## JavaScript - Multidimensional Array

> Multidimensional Array bisa dianalogikan dengan array of array. Ada array didalam array.

    let barang = [
        ["Kaos Putih" , 10],
        ["Kemeja Hitam" , 5],
        ["Sepatu" , 8],
        ["Celana" , 5],
    ] ;
    console.log(barang);

> Bayangkan multidimensional ini seperti Table. Baris pada table itu menunjukan jumlah array. Column pada table itu menunjukan isi dari tiap array.

### LOOPING FOR MULTIDIMENSIONAL ARRAY

    let barang = [
            ["Kaos Putih" , 10],
            ["Kemeja Hitam" , 5],
            ["Sepatu" , 8],
            ["Celana" , 5],
        ];

        barang.forEach((baris) => {
            baris.forEach ((column) => {
                console.log(column);
            });
        });

## JS- OBJECK
> object adalah sebuah tipe data pada variabel yang menyimpan properti dan fungsi (method). Properti adalah data lengkap dari sebuah object. Method adalah action dari sebuah object. Apa saja yang dapat dilakukan dari suatu object.


    let person = {
    name : "Riska",
    age : 23,
    onRelationShip : True,
    favoriteFood : ["boba", "es kopi gula aren", "shihlin"],
    address : {
        streetName : "Jl Kebayan",
        phone : 08582727727227
    }
    }

    // console.log(person);
    // person.name = "Riska Amalia"
    // console.log(person.address.streetName)

mengakses sebuah property dari obj memakai TITIK/DOT (.)


## Javascript - Recursive
> Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu. Recursive kebanyakan digunakan untuk case matematika, fisika, kimia, dan yang berhubungan dengan calculation.

    Sintaks untuk fungsi rekursif adalah:

    function recurse() {
        // function code
        recurse();
        // function code
    }

    recurse();

Paradigma Baru:
- procedural
- conditional
- looping
- modular (function)
- recursive

Ciri dari rekursif:

- Fungsi rekursif selalu memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. Kondisi ini harus dapat dibuktikan akan tercapai, karena jika tidak tercapai maka kita tidak dapat membuktikan bahwa fungsi akan berhenti, yang berarti algoritma kita tidak benar.
- Fungsi rekursif selalu memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya. karena tujuan utama dari rekursif ialah memecahkan masalah dengan mengurangi masalah tersebut menjadi masalah-masalah kecil.


Contoh sederhana dari fungsi rekursif adalah menghitung mundur nilainya menjadi 1.

    // program to count down numbers to 1

    function countDown(number) {

        // display the number
        console.log(number);

        // decrease the number value
        const newNumber = number - 1;

        // base case
        if (newNumber > 0) {
            countDown(newNumber);
        }
    }
    
    countDown(7);

Mencari hasil dari nilai pangkat dengan rekursif

    function pow (x, n){
        if ( n === 1){
            return x;
        } else {
            return x * pow(x, n - 1);
        }
        }

        console.log(pow(2, 3)); // 8

## JAVASCRIPT REGEX
> Regex adalah susunan karakter/deretan karakter spesial yang menggambarkan pattern/pola untuk pencarian text pada sebuah string atau document. Regex = Text matching.

Javascript regex punya beberapa built-in methods untuk Regex: 

1. __Literals__ adalah konsep regex yang paling sederhana dimana kita membuat regex sesuai dengan text yang ingin kita cari/match atau mengandung text yang kita cari.
2. __test()__  mengembalikan nilai BOOLEAN (TRUE/FALSE) untuk kecocokan sebuat text yang dicari.
3. __match()__ sama seperti test() yaitu sebuah method bawaan dari javascript. Namun match() mengembalikan nilai array dari karakter yang match.
4. __Flags__ Ada 6 flags dalam Javascript. Kita bahas 2 dahulu yang sering digunakan:
    - i = Untuk menghandle case-sensitive. Tidak mempermasalahkan besar kecilnya sebuah karakter. Tidak membedakan antara A dan a.
    - g = Untuk mencari kedalam seluruh string yang ingin dicari. Jika tidak menggunakan flags g, maka sistem akan mengembalikan nilai array pertama yang ditemukan saja atau tidak melanjutkan pencarian.

Karakter Set Short Syntax
Ada beberapa short syntax untuk kumpulan grup karakter.
- \d : Seluruh number/digit character. Contohnya [0-9]
- \w : Alphanumeric character (26 huruf abjad dan angka). Contohnya [A-Za-z0-9_]
- \s : Whitespace character (space, tab, newline, and similar). Contohnya [\t\r\n\f\v]

Negasi dari Karakter set short syntax
Kita juga bisa menggunakan negasi dari ketiga karakter set short syntax sebelumnya.
- \D : TIDAK mengandung seluruh number/digit character. Contohnya [^0-9]
- \W : TIDAK mengandung Alphanumeric character (26 huruf abjad dan angka). Contohnya [^A-Za-z0-9_]
- \S : TIDAK mengandung Whitespace character (space, tab, newline, and similar). Contohnya [^\t\r\n\f\v]
Icon set caret (^) merupakan negasi dari pattern regex yang dibuat.

5. __Anchors__ mencari karakter yang persis detail sama, kita bisa menggunakan Anchor.Diawali dengan (^) dan diakhiri dengan ($)
6. __Alternation__ Kita bisa menggunakan yang namanya Alternation. Menggunakan (|). Kalau kita ingin membuat beberapa kalimat yang exactly sama persis dengan pencarian


## JS - OOP & MODULES
### OOP 
> Object Oriented Programming (OOP) adalah suatu paradigma dalam pemrograman. Kita telah mempelajari paradigma seperti procedural, conditional, hingga function.

4 pilar pada OOP
- Encapsulation => adalah cara untuk membatasi akses langsung ke properti atau method dari sebuah objek.
- Abstraction => adalah sebuah teknik untuk menyembunyikan detail tertentu dari sebuah objek/method dan hanya menampilkan fungsionalitas atau fitur penting dari objek tersebut. Terkadang method yang tidak memiliki body pada parent class.

- Inheritance => adalah sebuah proses dimana sebuah class mewariskan property dan methodnya ke class lain atau childnya.
- Polymorpishm => berarti kemampuan dari suatu objek untuk memiliki banyak bentuk. 


Saat ini OOP dapat dibuat menggunakan:
- function
- class (ES6)

this keyword
> This adalah sebuah keyword khusus yang merujuk pada pada objek pemiliknya.Maksudnya adalah nilai dari this sangat bergantung pada di mana keyword this ini diletakkan atau di panggil. Jika this di gunakan dalam sebuah method maka ia merujuk pada objek pemiliknya.Jika this di dalam sebuah function maka ia merujuk pada global objek atau window. Dalam kasus function constructor dan class maka keyword this ini mengacu pada objek instannya.

### MODULES
> adalah sebuah teknik untuk menyembunyikan detail tertentu dari sebuah objek/method dan hanya menampilkan fitur penting dari objek tersebut. 


membuat Modules menggunakan ES6.
 Export dan import

    //importing 
    const doSomething = require('./doSomething.js'); 

    //exporting
    module.exports = function doSomething(n) {
    // do something
    }

## Web Storage 
Memahami localStorage vs sessionStorage
> __localStorage dan sessionStorage__ hampir identik dan memiliki API yang sama. Perbedaannya adalah bahwa dengan __sessionStorage__, data hanya bertahan sampai jendela atau tab ditutup. sedangkan __localStorage__, data dipertahankan hingga pengguna secara manual menghapus cache browser atau hingga aplikasi web Anda menghapus data. Tutorial ini menampilkan localStorage, tetapi sintaks untuk sessionStorage sama.

Jenis Web Storage
- Localstorage, session, IndexDB, Cookies, Trust Token, Web SQL
- Umumnya diguanakan FE : Local, Session, IndexDB
- Yang perlu di komunikasikan oleh BE : Cookies


### Localstorage

        let token = "12314123134dkjSBDlj;daelsdblaesblwescjsfkej";

        // Perintah menyimpan data kedalam localstorage
        localStorage.setItem("token", token);

        // Perintah mengambil data dari localstorage
        console.log(localStorage.getItem("Riska Amalia"));

        // Perintah menghapus data dari localstorage
        localStorage.removeItem("token");


### Session Storage

        // Set Item Token Session Storage
        sessionStorage.setItem("token", token);

        // Get data Session Storage
        sessionStorage.getItem("token");

        // Remove session
        // sessionStorage.removeItem("token");


## Synchronous dan Asynchronous Programming
> Synchronous adalah teknik pengerjaannya dilakukan secara rutut atau step bay step. sedangkan Asynchronous adalah teknil mengerjakannya secara pararel yaitu mengerjakan kegiatan 1 dan yang lain berbarengan dengan tujuan yang sama. 


### Basic Asynchronous of JavaScript
### Asynchronous - Promise
    // 1 Promise Chains

    const returnsAPromise = function (string) {
    return new Promise((resolve, reject) => {
        if (typeof string === "string") {
        resolve(`${string} is a resolved promise now`);
        } else {
        reject("Not a string!");
        }
    });
    };

    returnsAPromise("1").then((item) => {
    console.log(item);
    });

### Asynchronous - Async Await

    // 2 Async/Await

    // Synchronous

    const sayHello = (num, word) => {
    console.log(`Customer no.${num} says ${word}`);
    };

    sayHello(1, "Hi");
    sayHello(2, "Hello");

    // Async/Await
    const sayAsyncHello = async (num, word) => {
    await setTimeout(() => {
        console.log(`Customer no.${num} says ${word}`);
    }, 2000);
    };

    sayAsyncHello(3, "Yo");
    sayHello(4, "Yep");
    sayHello(5, "Never better");