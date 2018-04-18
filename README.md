# smsid 

**Smsid | Mengirim sms dengan termux  (Java program)**
======================================

> Mengirim sms dari terminal (termux) ?
> Tak perlu pulsa, cukup koneksi internet untuk menggunakan ini.
> Tak perlu **python**, **php**, **ruby**, **perl**, **golang** ataupun program interpreter lainnya, untuk menjalankan ini, karna ini berjalan langsung pada dalvikVM (android virtual mechine).



## Cara Penggunaan 
===================

1. Menapilkan pesan help.
   Menampilkan text help sangatlah mudah,
   cukup ketik ini di command prompt:
   ```bash
   smsid
   ```
   Atau juga bisa dengan:
   ```bash
   smsid --help
   ```
   bisa juga dengan POSIX style:
   ```bash
   smsid -h
   ```

2. Mengirim pesan tunggal.
   ```
   smsid send [phone-number] [message]
   ```
   **[phone-number]** harus berupa angka,
   dan jumlanya harus 9 sampai dengan 13 angka, 
   harus di awali dengan 08 dan **bukan** 62
   jika nomor tidak valid akan muncul input prompt
   intuk memasukan ulang nomor.

   **[message]** harus valid, dimana character
   ("@"  "/" "\" ":"") akan dihapus otomatis (jika ada).
   jumlah character **[message]** harus lebih besar
   dari 0 dan lebih kecil dari 122.
   Jika ingin menyertakan pesan text pada parameter
   command, harus menggunakan tanda kutip pada pesan,
   agar pesan yang di kirim tidak terpotong.

   contoh:
   ```bash
   smsid send 081234567890 "Ini pesan saya"
   ```

   Bisa juga mengosongkan parameter **[message]**
   seperti:
   ```bash
   smsid send 081234557890
   ```
   command di atas akan menampilkan input prompt 
   guna memasukan pesan yang akan di kirim.

   Bahkan parameter **[phone-number]** dan juga **[messae]**
   bisa di kosongkan keduanya, seperti:
   ```bash
  smsid send 
   ```
   command diatas akan menampilkan input prompt guna 
   memasukan nomor tujuan dan pesan yang akan dikirim.


3. Mengirim pesan multi
   bisa juga di sebut spam karna mengirim hal yang sama.
   bedanya disini textnya dapat di custom  sesuai 
   kehendak (yang terpenting valid).

   Jika ingin mengirim pesan multi,bisa menggunakan
   command ini.

   ```bash
   smsid boom [-y] [phone-number] [message] [max-send]
   ```
   **[-y]** menkonfirmasi setuju jika pesan text
   akan di format ulang guna validasi.
   untuk parameter **[phone-number]** dan **[message]**
   sama seperti di atas.
   **[max-send]** jumlah pesan yang akan dikirim pada 
   nomor yang sama.


## INSTALLATION
1. Dengan **git clone** .
   Cara ini mengharuskan sudah menginstall program git,
   Jika belum mempunyai program git pada prangkat,
   bisa menggunakan command di bawah untuk menginstall.

   ```bash
   pkg install git
   ```

   Jika susah, bisa ketahap berikutnya,
   yaitu menginstall program ini dengan mengetik 
   command seperti ini :

   ```bash
   git clone https://github.com/amsitlab/smsid-java.git
   ```
   Tunggu beberapa saat hingga program gite selesai
   menyalin, jika sudah lanjut kethap berikutnya,
   yaitu pindah ke directory ./smsid-java dengan
   cara:

   ```bash
   cd ./smsid-java
   ```

   lalu beri akses **x** untuk file ./install dengan
   cara:
   > NB: sebelum menggunakan command di bawah 
   pastikan directory sekarang berada di dalam 
   */data/data/com.termux/files/* guna menghindari
   terjadinya error "**permission denied**"

   ```bash
   chmod +x ./install 
   ```

   atau bisa juga dengan menggunakan **apt**:

   ```bash
   apt install ./smsid_x.x_all.deb
   ```


   > "**x.x**" adalah version package yg telah di
   > download. untuk melihat versi berapa yg telah di
   > install bisa menggunakan command "**ls**" untuk
   > melihat file.

   jika file yg telah di download/clone adalah 
   *smsid_1.1_all.deb* maka ketik seperti ini 
   di commandline:


   ```bash
   apt install
   ```

## Author
----------


[@amsitlab](https://amsitlab.github.io)


## Buildwith
------------


 [picocli](https://github.com/ramkop/picocli) 

 [Ecj Batch Compiler](https://eclipse.org/jdt/core)

 Android dx tools


## Changelog
------------
1.1 Adding Subcommand.

1.0 Working Progress.
