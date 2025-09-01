# Tugas-Praktikum1 
1. Apa yang dimaksud dengan kelas dalam PBO?
    
    kelas adalah blueprint (cetakan) atau rancangan untuk membuat objek. Di dalam kelas terdapat atribut (data/properti) dan method (fungsi/perilaku).

2. Bagaimana cara kerja atribut dan method dalam kelas?

    Dalam kelas:

       - Atribut = data atau ciri-ciri dari objek (misalnya: nama, umur, saldo).
       - Method = perilaku atau tindakan yang bisa dilakukan objek (misalnya: berjalan, menyimpan uang, menampilkan data).

    Cara kerjanya:

       - Saat kita membuat objek dari kelas, objek itu akan memiliki atribut sendiri (data tersimpan di dalamnya).
       - Method bisa dipanggil untuk mengolah atau menampilkan data dari atribut tersebut.
       - Atribut dan method saling bekerja sama: atribut menyimpan informasi, method memproses atau mengubah informasi itu.

3. Apa perbedaan antara method yang mengembalikan nilai dan yang tidak?

    Dalam PBO (atau pemrograman umum), method bisa dibagi menjadi dua:

       1. Method yang mengembalikan nilai

           - Setelah dijalankan, method ini menghasilkan sebuah nilai untuk dipakai lagi.
           - Ditulis dengan tipe data pengembalian (misalnya int, String, double).
           - Harus ada kata kunci return.

       2. Method yang tidak mengembalikan nilai

           - Tidak menghasilkan nilai, hanya menjalankan aksi.
           - Ditulis dengan kata kunci void.
           - Tidak memakai return (kecuali untuk keluar dari method).

4. Bagaimana method berinteraksi dengan atribut dalam kelas?

    Method berinteraksi dengan atribut dalam kelas dengan cara:

       - Membaca nilai atribut → method bisa mengambil data dari atribut untuk ditampilkan atau dihitung.
       - Mengubah nilai atribut → method bisa mengisi atau memperbarui data dalam atribut.
       - Mengendalikan akses atribut → biasanya atribut dibuat private, lalu method (getter & setter) dipakai untuk mengatur cara membaca/menulis atribut tersebut.
5. Pada percobaan 1, definisikan bagian kode program sesuai prinsip SOLID.

    1. Single Responsibility Principle (SRP)
    - Kelas Puppy hanya bertugas menyimpan data (nama, umur) dan menyediakan method untuk mengubah serta membaca umur.
    - Tidak ada tanggung jawab lain, sehingga sudah sesuai SRP.

    2. Open/Closed Principle (OCP)
    - Kode terbuka untuk pengembangan. Misalnya jika ingin menambahkan atribut baru seperti berat badan atau ras, bisa ditambahkan tanpa harus mengubah logika utama.
    - Dengan cara ini kelas tetap tertutup untuk modifikasi besar.

    3. Liskov Substitution Principle (LSP)
    - Jika nanti Puppy dijadikan superclass, subclass seperti Bulldog atau GoldenRetriever tetap dapat digunakan sebagai objek Puppy.
    - Karena fungsi setAge() dan getAge() konsisten, prinsip ini tidak akan dilanggar.

    4. Interface Segregation Principle (ISP)
    - Saat ini belum ada interface.
    - Jika dibuat interface Animal dengan method dasar seperti makeSound(), eat(), sleep(), maka Puppy bisa memilih hanya mengimplementasikan yang relevan.
    - Perbaikan ini akan membuat kode lebih fleksibel.

    5. Dependency Inversion Principle (DIP)
    - Pada main(), objek Puppy dibuat langsung (new Puppy("tommy")).
    - Artinya program bergantung pada kelas konkrit, bukan abstraksi.
    - Agar sesuai DIP, sebaiknya gunakan interface/abstraksi seperti IAnimal sehingga kode tidak bergantung pada implementasi spesifik.

6. Compile program pada percobaan 2 dan 3 dan lakukan analisa anda.

    1. Analisis Percobaan 2
    - Kelas Contoh memiliki method cetak() yang bersifat static untuk mencetak "Saya Suka".
    - Method main() sudah benar ditulis public static void main(String[] args).
    - Di dalam main(), method cetak() dipanggil lalu mencetak "Java".

    Program ini adalah contoh sederhana pemanggilan method static dari main dan sudah berjalan dengan benar.

    2. Analisis Percobaan 3
    - myStaticMethod() → static, bisa dipanggil langsung dari main() tanpa objek.
    - myPublicMethod() → non-static, harus dipanggil lewat objek (myObj.myPublicMethod()).
    - Alur program: jalankan myStaticMethod(), buat objek Main, lalu panggil myPublicMethod().

    Program ini memperlihatkan perbedaan pemanggilan antara static method dan public (non-static) method.


