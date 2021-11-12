**PRAKTIKUM JARKOM MODUL 3**

Kelompok A07:

1.  Arkan Aulia Farhan (05111940000128)

2.  Muchamad Maroqi Abdul Jalil (05111940000143)

3.  Syamil Difaull Haq Sukur (05111940000196)

Soal praktikum:

Luffy yang sudah menjadi Raja Bajak Laut ingin mengembangkan daerah
kekuasaannya dengan membuat peta seperti berikut:

![](./assets/media/image1.png){width="6.283464566929134in"
height="4.611111111111111in"}

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

Jawaban:

Karena kelompok kami adalah A07 maka kami menggunakan IP: 192.171.x.x

1.  Konfigurasi Node

-   Foosha

Melakukan konfigurasi Foosha sebagai Router dari semua device nantinya.

![](./assets/media/image6.png){width="3.3958333333333335in"
height="2.8854166666666665in"}

Memasukkan perintah berikut agar node dapat terhubung internet.

![](./assets/media/image23.png){width="6.283464566929134in"
height="0.5in"}

-   Loguetown

Melakukan konfigurasi sebagai DHCP Client.

![](./assets/media/image5.png){width="2.6979166666666665in"
height="1.4375in"}

-   Alabasta

Melakukan konfigurasi sebagai DHCP Client.

![](./assets/media/image3.png){width="2.75in"
height="1.4583333333333333in"}

-   EniesLobby

Melakukan konfigurasi sebagai DNS Server dengan alokasi IP yaitu
192.172.2.2.

![](./assets/media/image26.png){width="2.6666666666666665in"
height="1.1458333333333333in"}

Install kebutuhan DNS Server.

![](./assets/media/image24.png){width="3.0208333333333335in"
height="0.5416666666666666in"}

-   Water7

Melakukan konfigurasi sebagai Proxy Server dengan alokasi IP yaitu
192.171.2.3.

![](./assets/media/image4.png){width="2.5104166666666665in"
height="0.9583333333333334in"}

Install kebutuhan Proxy Server.

![](./assets/media/image15.png){width="2.0729166666666665in"
height="0.5in"}

-   Jipangu

Melakukan konfigurasi sebagai DHCP Server dengan alokasi IP yaitu
192.171.2.4.

![](./assets/media/image25.png){width="2.5208333333333335in"
height="0.90625in"}

Install kebutuhan DHCP Server.

![](./assets/media/image12.png){width="3.3645833333333335in"
height="0.4479166666666667in"}

-   Skypie

Melakukan konfigurasi sebagai DHCP Client.

![](./assets/media/image22.png){width="2.53125in"
height="1.2916666666666667in"}

-   TottoLand

Melakukan konfigurasi sebagai DHCP Client.

![](./assets/media/image2.png){width="2.4583333333333335in"
height="1.34375in"}

2.  Membuat Foosha sebagai DHCP Relay.

Menuliskan perintah-perintah yang digunakan ke dalam bash script di
Foosha. Perintah ini terdiri dari konfigurasi dhcp relay yang mengarah
ke IP Jipangu dengan semua interfae disambungkan.

![](./assets/media/image19.png){width="6.208333333333333in"
height="2.5416666666666665in"}

3.  Setting Client pada Switch 1

Menuliskan perintah-perintah yang digunakan ke dalam bash script di
Jipangu. Perintah ini adalah melakukan konfigurasi pada dhcp server
dengan interface pada eth0.

![](./assets/media/image20.png){width="6.283464566929134in"
height="2.1805555555555554in"}

Kemudian mengatur konfigurasi untuk menentukan range IP pada Switch 1.

![](./assets/media/image21.png){width="5.979166666666667in"
height="3.6041666666666665in"}

Melakukan testing dengan mencoba restart node Loguetown dan Alabasta,
kemudian membuka console dan melihat IPnya.

-   Loguetown

![](./assets/media/image16.png){width="6.283464566929134in"
height="1.7916666666666667in"}

-   Alabasta

![](./assets/media/image10.png){width="6.283464566929134in"
height="1.7361111111111112in"}

4.  Setting Client pada Switch 3

Menambahkan konfigurasi yang digunakan ke dalam bash script di Jipangu.
Konfigurasi ini adalah mengatur konfigurasi untuk menentukan range IP
pada Switch 3.

![](./assets/media/image7.png){width="4.625in"
height="1.2291666666666667in"}

Melakukan testing dengan mencoba restart node Tottoland dan Skypie,
kemudian membuka console dan melihat IPnya.

-   Tottoland

![](./assets/media/image11.png){width="6.283464566929134in"
height="1.7638888888888888in"}

-   Skypie

![](./assets/media/image18.png){width="6.283464566929134in"
height="1.75in"}

5.  Konfigurasi DNS Forwarder pada EniesLobby

Menuliskan perintah-perintah yang digunakan ke dalam bash script di
EniesLobby. Perintah ini adalah melakukan konfigurasi pada bind.

![](./assets/media/image13.png){width="6.283464566929134in"
height="2.861111111111111in"}

Melakukan testing dengan mencoba restart kemudian membuka console
Loguetown dan melakukan ping google.com.

![](./assets/media/image17.png){width="6.283464566929134in"
height="2.5555555555555554in"}

6.  Setting Lease Time untuk eth1 dan eth3

Menambahkan konfigurasi yang digunakan ke dalam bash script di Jipangu.
Konfigurasi ini adalah mengatur waktu alokasi IP pada Switch 1 dan
Switch 3.

![](./assets/media/image8.png){width="4.5in"
height="3.4583333333333335in"}

7.  Setting Fixed Adress untuk Skypie

Menambahkan konfigurasi yang digunakan ke dalam bash script di Jipangu.
Konfigurasi ini adalah mengatur alokasi IP untuk Skypie pada Switch 3.

![](./assets/media/image27.png){width="4.208333333333333in"
height="0.7604166666666666in"}

Menambahkan static ethernet pada kofigurasi network di Skypie

![](./assets/media/image14.png){width="2.78125in" height="1.53125in"}

Melakukan testing dengan mencoba restart kemudian membuka console Skypie
kemudian mengecek IPnya.

![](./assets/media/image9.png){width="6.283464566929134in"
height="1.7916666666666667in"}

[^1]: 1.0 → 1.1: Mengubah kalimat "**dengan enkripsi bcrypt**" menjadi
    "**dengan enkripsi MD5**"

[^2]: 1.0 → 1.1: Mengubah kalimat "Zoro mencari sisanya" menjadi "Zoro
    **mendapatkan sisanya**"
