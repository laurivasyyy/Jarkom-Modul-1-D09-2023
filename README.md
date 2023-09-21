# Jarkom-Modul-1-D09-2023
## **Lapres Praktikum Jarkom Modul 1 Kelompok D-09**
### **Nama Kelompok**
|**Nama**|**NRP**|
|--------|-------|
|Laurivasya Gadhing Syahafidh|5025211136|
|Dafarel Fatih Wirayudha     |5025211120|


## **Nomor 1**
**User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.**

**Solusi :**

Karena user ingin melakukan aktivitas denggan menggunakan protokol FTP (File Transfer Protocol), maka kita akan melakukan display filter protocol ftp saja. Setelah kita melakukan filter, kita akan mencari message info dengan perintah STOR yang diikuti oleh nama file(karena user ingin mengunggah suatu file).

![no1a-b](https://github.com/laurivasyyy/Jarkom-Modul-1-D09-2023/blob/ff10549ffe14ad992f2e20d70c75ed11e2cc85a5/img/no.1a-b.png)

#### Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut?
---
Dapat dilihat melalui gambar diatas bahwa sequence number (raw) pada frame ke-147 adalah <ins>**258040667**</ins>

#### Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut?
---
Berdasarkan gambar diatas, acknowledge number (raw) pada frame ke-147 adalah <ins>**1044861039**</ins>

Lalu, untuk melihat response dari aktivitas STOR tersebut kita hanya perlu mencari message info dengan nama file yang diunggah. Pada kasus ini, response ditunjukkan pada frame ke-149.

![no1c-d](https://github.com/laurivasyyy/Jarkom-Modul-1-D09-2023/blob/ff10549ffe14ad992f2e20d70c75ed11e2cc85a5/img/no.1c-d.png)

#### Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
---
Dapat dilihat melalui gambar diatas bahwa sequence number (raw) pada frame ke-149 adalah <ins>**1044861039**</ins> sama seperti acknowledge number (raw) pada frame ke-147.

#### Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
---
Berdasarkan gambar diatas, acknowledge number (raw) pada frame ke-149 adalah <ins>**258040696**</ins>

## **Nomor 2**
Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!

## **Nomor 3**
**Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:**

**Solusi :**
Untuk melihat banyaknya packet yang didisplay dengan IP source/destination 239.255.255.250 dan port 3702, maka kita perlu melakukan display filter dengan perintah ```(ip.src == 239.255.255.250 || ip.dst == 239.255.255.250) && (tcp.port == 3702 || udp.port == 3702)```

![no.3](https://github.com/laurivasyyy/Jarkom-Modul-1-D09-2023/blob/b08ab3a56de07a40ebc25ede8704a8e95ef52ccb/img/no.3.png)

#### Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?
---
Berdasarkan gambar diatas, banyaknya packet yang didisplay setelah dilakukan display filter adalah <ins>**21**<ins>

#### Protokol layer transport apa yang digunakan?
---
Protokol layer transport yang digunakan adalah User Datagram Protocol (<ins>**UDP**<ins>)

## **Nomor 4**
**Berapa nilai checksum yang didapat dari header pada paket nomor 130?**

**Solusi :**
Untuk melihat nilai checksum yang didapat dari header pada paket nomor 130, kita hanya perlu mengklik paket ke-130 dan melakukan analisis pada bagian UDP (User Datagram Protocol). Kemudian kita bisa melihat hasil checksumnya yaitu <ins>**0x18e5**<ins>

![no.4](https://github.com/laurivasyyy/Jarkom-Modul-1-D09-2023/blob/d71bcdbc958d1fe0a7e91544434e119a105fea59/img/no.4.png)



### **Nomor 5**
**Elshe menemukan suatu file packet capture yang menarik. Bantulah Elshe untuk menganalisis file packet capture tersebut.**

**Solusi :**
Untuk memperoleh password dari file.zip yang disediakan kita perlu mencari packet no berapakah yang menyimpan password dari file.zip yang ada. Lalu, saya menemukan bahwa password terletak pada packet no. 14. Setelah itu, saya melakukukan follow untuk melihat isi dari TCP stream packet 14.

![no.5](https://github.com/laurivasyyy/Jarkom-Modul-1-D09-2023/blob/a554b899f4de80493edbde98153d4e40c41ae239/img/no.5.png)

Password yang diperoleh adalah NWltcGxlUGFzNXdvcmQ= lalu kita decode di [Base64](https://www.base64decode.org) menjadi 5implePas5word. Password inilah yang bisa kita gunakan untuk membuka file.zip file yang ada.

#### Berapa banyak packet yang berhasil di capture dari file pcap tersebut?
---
![no.5-1](https://github.com/laurivasyyy/Jarkom-Modul-1-D09-2023/blob/a554b899f4de80493edbde98153d4e40c41ae239/img/no.%205a.png)

Terdapat <ins>**60**</ins> packet yang berhasil di capture dari file pcap tersebut.

https://github.com/laurivasyyy/Jarkom-Modul-1-D09-2023/blob/a554b899f4de80493edbde98153d4e40c41ae239/img/no.%205b-c.png

#### Port berapakah pada server yang digunakan untuk service SMTP?**
---
Berdasarkan gambar diatas, port yang digunakan server untuk service SMTP adalah <ins>**25**</ins>

#### Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?**
---
Berdasarkan gambar diatas, IP yang merupakan public IP adalah <ins>**74.53.140.153**</ins>

### **Nomor 6**
**Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.**

**Solusi :**

### **Nomor 7**
**Berapa jumlah packet yang menuju IP 184.87.193.88?**

**Solusi :**

### **Nomor 8**
**Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)**

**Solusi :**

![no.8](https://github.com/laurivasyyy/Jarkom-Modul-1-D09-2023/blob/d71bcdbc958d1fe0a7e91544434e119a105fea59/img/no.%208.png)

### **Nomor 9**
**Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!**

**Solusi :**

### **Nomor 10**
**Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet**

**Solusi :**






