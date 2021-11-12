# Jarkom-Modul-2-A07-2021
Laporan resmi berisi dokumentasi soal Jarkom Modul 2.
---
Kelompok A-07:
- [Arkan Aulia Farhan](): 05111940000128
- [Muchamad Maroqi Abdul Jalil](https://github.com/maroqijalil): 05111940000143
- [Syamil Difaul Haq Sukur](https://github.com/Syamil28): 05111940000196
---

## Soal praktikum:

Luffy yang sudah menjadi Raja Bajak Laut ingin mengembangkan daerah
kekuasaannya dengan membuat peta seperti berikut:

![](./assets/image1.png)


Luffy bersama Zoro berencana membuat peta tersebut dengan kriteria
**EniesLobby** sebagai DNS Server, **Jipangu** sebagai DHCP Server,
**Water7** sebagai Proxy Server **(1)**, dan **Foosha** sebagai DHCP
Relay **(2)**. Luffy dan Zoro **menyusun peta tersebut dengan hati-hati
dan teliti**.

Ada beberapa kriteria yang ingin dibuat oleh Luffy dan Zoro, yaitu:

1.  Semua client yang ada **HARUS** menggunakan konfigurasi IP dari DHCP
    > Server.

2.  Client yang melalui Switch1 mendapatkan range IP dari \[prefix
    > IP\].1.20 - \[prefix IP\].1.99 dan \[prefix IP\].1.150 - \[prefix
    > IP\].1.169 **(3)**

3.  Client yang melalui Switch3 mendapatkan range IP dari \[prefix
    > IP\].3.30 - \[prefix IP\].3.50 **(4)**

4.  Client mendapatkan DNS dari EniesLobby dan client dapat terhubung
    > dengan internet melalui DNS tersebut. **(5)**

5.  Lama waktu DHCP server meminjamkan alamat IP kepada Client yang
    > melalui Switch1 selama 6 menit sedangkan pada client yang melalui
    > Switch3 selama 12 menit. Dengan waktu maksimal yang dialokasikan
    > untuk peminjaman alamat IP selama 120 menit. **(6)**

Luffy dan Zoro berencana menjadikan **Skypie** sebagai server untuk jual
beli kapal yang dimilikinya dengan **alamat IP yang tetap** dengan IP
\[prefix IP\].3.69 **(7)**. **Loguetown** digunakan sebagai client
**Proxy** agar transaksi jual beli dapat terjamin keamanannya, juga
untuk mencegah kebocoran data transaksi.

Pada Loguetown, proxy **harus bisa diakses** dengan nama
**jualbelikapal.yyy.com** dengan **port** yang digunakan adalah **5000
(8)**. Agar transaksi jual beli lebih aman dan pengguna website ada dua
orang, proxy dipasang **autentikasi user proxy dengan enkripsi MD5**[^1]
dengan **dua username,** yaitu luffybelikapalyyy dengan password
luffy\_yyy **dan** zorobelikapalyyy dengan password zoro\_yyy **(9)**.
Transaksi jual beli tidak dilakukan setiap hari, oleh karena itu akses
internet dibatasi hanya dapat diakses setiap hari **Senin-Kamis pukul
07.00-11.00** dan setiap hari **Selasa-Jum'at pukul 17.00-03.00**
keesokan harinya **(sampai Sabtu pukul 03.00)** **(10)**.

Agar transaksi bisa lebih fokus berjalan, maka dilakukan redirect
website agar mudah mengingat website transaksi jual beli kapal. Setiap
**mengakses google.com, akan diredirect menuju super.franky.yyy.com**
dengan website yang sama pada soal shift modul 2. Web server
super.franky.yyy.com berada pada node **Skypie (11)**.

Saatnya berlayar! Luffy dan Zoro akhirnya memutuskan untuk berlayar
untuk **mencari harta karun di super.franky.yyy.com**. Tugas pencarian
dibagi menjadi dua misi, Luffy bertugas untuk **mendapatkan gambar
(.png, .jpg)**, sedangkan Zoro **mendapatkan**[^2] **sisanya**. Karena
Luffy orangnya sangat teliti untuk mencari harta karun, ketika ia
berhasil mendapatkan gambar, ia mendapatkan gambar dan melihatnya dengan
kecepatan **10 kbps (12)**. Sedangkan, Zoro yang sangat bersemangat
untuk mencari harta karun, sehingga kecepatan kapal Zoro tidak dibatasi
ketika sudah mendapatkan harta yang diinginkannya **(13)**.

## Jawaban:

Karena kelompok kami adalah A07 maka kami menggunakan IP: 192.172.x.x

## Nomor 1
Konfigurasi Node

### Jawab
-   Foosha

Melakukan konfigurasi Foosha sebagai Router dari semua device nantinya.

![](./assets/image6.png)


Memasukkan perintah berikut agar node dapat terhubung internet.

![](./assets/image23.png)


-   Loguetown

Melakukan konfigurasi sebagai DHCP Client.

![](./assets/image5.png)


-   Alabasta

Melakukan konfigurasi sebagai DHCP Client.

![](./assets/image3.png)


-   EniesLobby

Melakukan konfigurasi sebagai DNS Server dengan alokasi IP yaitu
192.172.2.2.

![](./assets/image26.png)


Install kebutuhan DNS Server.

![](./assets/image24.png)


-   Water7

Melakukan konfigurasi sebagai Proxy Server dengan alokasi IP yaitu
192.171.2.3.

![](./assets/image4.png)


Install kebutuhan Proxy Server.

![](./assets/image15.png)


-   Jipangu

Melakukan konfigurasi sebagai DHCP Server dengan alokasi IP yaitu
192.171.2.4.

![](./assets/image25.png)


Install kebutuhan DHCP Server.

![](./assets/image12.png)


-   Skypie

Melakukan konfigurasi sebagai DHCP Client.

![](./assets/image22.png)


-   TottoLand

Melakukan konfigurasi sebagai DHCP Client.

![](./assets/image2.png)


## Nomor 2
Membuat Foosha sebagai DHCP Relay.
### Jawab

Menuliskan perintah-perintah yang digunakan ke dalam bash script di
Foosha. Perintah ini terdiri dari konfigurasi dhcp relay yang mengarah
ke IP Jipangu dengan semua interfae disambungkan.

![](./assets/image19.png)

## Nomor 3
Setting Client pada Switch 1
### Jawab
Menuliskan perintah-perintah yang digunakan ke dalam bash script di
Jipangu. Perintah ini adalah melakukan konfigurasi pada dhcp server
dengan interface pada eth0.

![](./assets/image20.png)


Kemudian mengatur konfigurasi untuk menentukan range IP pada Switch 1.

![](./assets/image21.png)


Melakukan testing dengan mencoba restart node Loguetown dan Alabasta,
kemudian membuka console dan melihat IPnya.

-   Loguetown

![](./assets/image16.png)


-   Alabasta

![](./assets/image10.png)

## Nomor 4
Setting Client pada Switch 3
### Jawab
Menambahkan konfigurasi yang digunakan ke dalam bash script di Jipangu.
Konfigurasi ini adalah mengatur konfigurasi untuk menentukan range IP
pada Switch 3.

![](./assets/image7.png)


Melakukan testing dengan mencoba restart node Tottoland dan Skypie,
kemudian membuka console dan melihat IPnya.

-   Tottoland

![](./assets/image11.png)


-   Skypie

![](./assets/image18.png)

## Nomor 5
Konfigurasi DNS Forwarder pada EniesLobby
### Jawab

Menuliskan perintah-perintah yang digunakan ke dalam bash script di
EniesLobby. Perintah ini adalah melakukan konfigurasi pada bind.

![](./assets/image13.png)


Melakukan testing dengan mencoba restart kemudian membuka console
Loguetown dan melakukan ping google.com.

![](./assets/image17.png)

## Nomor 6
Setting Lease Time untuk eth1 dan eth3
### Jawab

Menambahkan konfigurasi yang digunakan ke dalam bash script di Jipangu.
Konfigurasi ini adalah mengatur waktu alokasi IP pada Switch 1 dan
Switch 3.

![](./assets/image8.png)

## Nomor 7
Setting Fixed Adress untuk Skypie
### Jawab

Menambahkan konfigurasi yang digunakan ke dalam bash script di Jipangu.
Konfigurasi ini adalah mengatur alokasi IP untuk Skypie pada Switch 3.

![](./assets/image27.png)


Menambahkan static ethernet pada kofigurasi network di Skypie

![](./assets/image14.png)}

Melakukan testing dengan mencoba restart kemudian membuka console Skypie
kemudian mengecek IPnya.

![](./assets/image9.png)


[^1]: 1.0 → 1.1: Mengubah kalimat "**dengan enkripsi bcrypt**" menjadi
    "**dengan enkripsi MD5**"

[^2]: 1.0 → 1.1: Mengubah kalimat "Zoro mencari sisanya" menjadi "Zoro
    **mendapatkan sisanya**"
