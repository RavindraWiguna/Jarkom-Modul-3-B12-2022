# Jarkom-Modul-3-B12-2022

## Soal 1
Loid bersama Franky berencana membuat peta tersebut dengan kriteria WISE sebagai DNS Server, Westalis sebagai DHCP Server, Berlint sebagai Proxy Server (1)
### Cara Pengerjaan
<img src="https://github.com/RavindraWiguna/Jarkom-Modul-3-B12-2022/blob/main/images/no 1/picture1.png" style="width:86%;height:86%;"><br>
<img src="https://github.com/RavindraWiguna/Jarkom-Modul-3-B12-2022/blob/main/images/no 1/picture2.png" style="width:86%;height:86%;"><br>
<img src="https://github.com/RavindraWiguna/Jarkom-Modul-3-B12-2022/blob/main/images/no 1/picture3.png" style="width:86%;height:86%;"><br>
## Soal 2
 dan Ostania sebagai DHCP Relay (2)
### Cara Pengerjaan
<img src="https://github.com/RavindraWiguna/Jarkom-Modul-3-B12-2022/blob/main/images/no 2/picture1.png" style="width:86%;height:86%;"><br>
## Soal 3
Ada beberapa kriteria yang ingin dibuat oleh Loid dan Franky, yaitu:
Semua client yang ada HARUS menggunakan konfigurasi IP dari DHCP Server.
Client yang melalui Switch1 mendapatkan range IP dari [prefix IP].1.50 - [prefix IP].1.88 dan [prefix IP].1.120 - [prefix IP].1.155 (3)

### Cara Pengerjaan
<img src="https://github.com/RavindraWiguna/Jarkom-Modul-3-B12-2022/blob/main/images/no 3/picture1.png" style="width:86%;height:86%;"><br>
<img src="https://github.com/RavindraWiguna/Jarkom-Modul-3-B12-2022/blob/main/images/no 3/picture2.png" style="width:86%;height:86%;"><br>
## Soal 4
Client yang melalui Switch3 mendapatkan range IP dari [prefix IP].3.10 - [prefix IP].3.30 dan [prefix IP].3.60 - [prefix IP].3.85 (4)

### Cara Pengerjaan
<img src="https://github.com/RavindraWiguna/Jarkom-Modul-3-B12-2022/blob/main/images/no 4/picture1.png" style="width:86%;height:86%;"><br>
<img src="https://github.com/RavindraWiguna/Jarkom-Modul-3-B12-2022/blob/main/images/no 4/picture2.png" style="width:86%;height:86%;"><br>
<img src="https://github.com/RavindraWiguna/Jarkom-Modul-3-B12-2022/blob/main/images/no 4/picture3.png" style="width:86%;height:86%;"><br>
## Soal 5
Client mendapatkan DNS dari WISE dan client dapat terhubung dengan internet melalui DNS tersebut. (5)
### Cara Pengerjaan
<img src="https://github.com/RavindraWiguna/Jarkom-Modul-3-B12-2022/blob/main/images/no 5/picture1.png" style="width:86%;height:86%;"><br>
<img src="https://github.com/RavindraWiguna/Jarkom-Modul-3-B12-2022/blob/main/images/no 5/picture2.png" style="width:86%;height:86%;"><br>
<img src="https://github.com/RavindraWiguna/Jarkom-Modul-3-B12-2022/blob/main/images/no 5/picture3.png" style="width:86%;height:86%;"><br>
<img src="https://github.com/RavindraWiguna/Jarkom-Modul-3-B12-2022/blob/main/images/no 5/picture4.png" style="width:86%;height:86%;"><br>
<img src="https://github.com/RavindraWiguna/Jarkom-Modul-3-B12-2022/blob/main/images/no 5/picture5.png" style="width:86%;height:86%;"><br>
## Soal 6
Lama waktu DHCP server meminjamkan alamat IP kepada Client yang melalui Switch1 selama 5 menit sedangkan pada client yang melalui Switch3 selama 10 menit. Dengan waktu maksimal yang dialokasikan untuk peminjaman alamat IP selama 115 menit. (6)
### Cara Pengerjaan
<img src="https://github.com/RavindraWiguna/Jarkom-Modul-3-B12-2022/blob/main/images/no 6/picture1.png" style="width:86%;height:86%;"><br>
## Soal 7
Loid dan Franky berencana menjadikan Eden sebagai server untuk pertukaran informasi dengan alamat IP yang tetap dengan IP [prefix IP].3.13 (7).
### Cara Pengerjaan
<img src="https://github.com/RavindraWiguna/Jarkom-Modul-3-B12-2022/blob/main/images/no 7/picture1.png" style="width:86%;height:86%;"><br>
## Soal 8
SSS, Garden, dan Eden digunakan sebagai client Proxy agar pertukaran informasi dapat terjamin keamanannya, juga untuk mencegah kebocoran data.

Pada Proxy Server di Berlint, Loid berencana untuk mengatur bagaimana Client dapat mengakses internet. Artinya setiap client harus menggunakan Berlint sebagai HTTP & HTTPS proxy. Adapun kriteria pengaturannya adalah sebagai berikut:

### Cara Pengerjaan
==============================================
	Note: 
Sebelum melakukan konfigurasi proxy pada client, server proxy harus dikonfigurasi terlebih dahulu (no. 9 dan seterusnya).

	Konfigurasi Client Proxy SSS
	```
	> export http_proxy="http://10.9.2.3:8080"
```
Konfigurasi Client Proxy Garden
```
	> export http_proxy="http://10.9.2.3:8080"
```
Konfigurasi Client Proxy Eden
```
	> export http_proxy="http://10.9.2.3:8080"
```
	==============================================

## Soal 9
Adapun pada hari dan jam kerja sesuai nomor (1), client hanya dapat mengakses domain loid-work.com dan franky-work.com (IP tujuan domain dibebaskan)
### Cara Pengerjaan
Jadikan Berlint sebagai Proxy Server sehingga dapat mengakses internet. 
==============================================
Install proxy squid pada Berlint
```
apt-get update
apt-get install squid
service squid start

service squid status

Konfigurasi squid
b.1 backup file config default squid
```
> mv /etc/squid/squid.conf /etc/squid/squid.conf.bak
```
b.2 buat konfigurasi squid baru pada file /etc/squid/squid.conf
b.3 pada file config baru dengan command
```
> nano /etc/squid/squid.conf
```
masukkan script:
```
http_port 8080
visible_hostname Berlint
```
b.4 restart squid
```
> service squid restart
```


## Soal 10
Saat akses internet dibuka, client dilarang untuk mengakses web tanpa HTTPS. (Contoh web HTTP: http://example.com)

### Cara Pengerjaan

```
	
WISE
nano /etc/bind/named.conf.local dan masukan

zone "loid-work.com" {
  type master;
  file "/etc/bind/jarkom/loid-work.com";
};

zone "franky-work.com" {
  type master;
  file "/etc/bind/jarkom/franky-work.com";
};

mkdir /etc/bind/jarkom/  

nano /etc/bind/jarkom/loid-work.com dan masukan

$TTL 604800
@ IN SOA loid-work.com. root.loid-work.com. (
                20211108 ; Serial
                604800 ; Refresh
                86400 ; Retry
                2419200 ; Expire
                604800 ) ; Negative Cache TTL
;
@ IN NS loid-work.com.
@ IN A 10.9.2.3
@ IN AAAA ::1
www IN CNAME loid-work.com.

nano /etc/bind/jarkom/franky-work.com dan masukan

$TTL 604800
@ IN SOA franky-work.com. root.franky-work.com. (
                20211108 ; Serial
                604800 ; Refresh
                86400 ; Retry
                2419200 ; Expire
                604800 ) ; Negative Cache TTL
;
@ IN NS franky-work.com.
@ IN A 10.9.2.3
@ IN AAAA ::1
www IN CNAME franky-work.com.


Berlint
nano /etc/squid/squid.conf dan tambahkan

  http_port 5000
    visible_hostname loid-work.com
    visible_hostname franky-work.com
    http_access allow all
    
  ```
dan lakukan service squid restart

## Soal 11
Agar menghemat penggunaan, akses internet dibatasi dengan kecepatan maksimum 128 Kbps pada setiap host (Kbps = kilobit per second; lakukan pengecekan pada tiap host, ketika 2 host akses internet pada saat bersamaan, keduanya mendapatkan speed maksimal yaitu 128 Kbps)
### Cara Pengerjaan

```

Berlin
nano /etc/squid/acl-bandwidth.conf dan masukan

delay_pools 2
delay_class 1 1
delay_class 1 2
delay_access 1 allow all
delay_access 2 allow all
delay_parameters 2 128000/128000 128000/128000


nano /etc/squid/squid.conf dan masukan

include /etc/squid/acl-bandwidth.conf
```
lakukan service squid restart

====================================================================

## Soal 12
Setelah diterapkan, ternyata peraturan nomor (4) mengganggu produktifitas saat hari kerja, dengan demikian pembatasan kecepatan hanya diberlakukan untuk pengaksesan internet pada hari libur
### Cara Pengerjaan
