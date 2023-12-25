# Konfigurasi OPNsense dan Installasi

## Alur Installasi OPNsense
Tatacara installasi OPNsense beserta langkah-langkah konfigurasi untuk OPNSense

### Download ISO image OPNsense
Untuk Link website download bisa dilihat dibawah berikut
- https://opnsense.org/download/
- https://sourceforge.net/projects/opnsense/

### Konfigurasi OPNsense
Untuk menkonfigurasi OPNsense terlebih dahulu untuk membuat atau menginstall OPNsense di Virtual machine.

Langkah-langkah konfigurasi :
- A. Pilih Option 2 karena kita mau set interface IP addressnya.
  
  B. Setelah itu pilih nomer 1 yaitu LAN (le1 - dhcp)
  
  C. Configurasi ipv4 via dhcp pilih opsi Y

  ![konfigurasi](img/konfigurasi%201.jpeg)


- selebihnya pilih opsi no semua, karena kita tidak menggunakan ipv6 lalu dia akan mulai memproses

  ![konfigurasi](img/konfigurasi%202.jpeg)


- Setelah selesai memproses, kita akan mendapatkan URL yang akan kita gunukan untuk masuk kehalaman dashboard login opnsense. (https://IP_OPNsense)

  ![konfigurasi](img/konfigurasi%203.jpeg)


- Untuk username & Password jika dalam penginstalan awal kita tidak merubah passwordnya sama sekali, login saja menggunakan password default dari Opnsense yaitu 
  
  Username: root

  Password: opnsense 

  ![konfigurasi](img/konfigurasi%204.jpeg)


### Konfigurasi IDS pada OPNsense
Konfigurasi IDS OPNsense

- Pada bagian ini menjelaskan mengenai tahapan konfigurasi IDS pada OPNSense, Langkah-langkahnya sebagai berikut :
  A. klik pada menu “service” pilih sub menu “Intrusion Detection”. 
  
  B. Kemudian pada bar menu, pilih “Download”, setelah itu beri tanda centang pada semua paket suricata yang akan di download. 
  
  C. lalu klik “enable selected”. Kemudian klik “Download & Update Rules”

  ![IDS](img/Gambar%201.JPG)


- Lihat pada tab rules sudah terlihat paket suricata yang sudah ter Download.

  ![IDS](img/Gambar%202.JPG)


- kemudian beralih ke tab setting. 
  A. Beri tanda  centang pada “Enable”, “IPS Mode”, dan "Promiscuous mode”
  
  B. Pada bagian pattern matcher lalu pilih “Hyperscan”, pada bagian interfaces pilih “LAN, WAN” lalu Apply. IDS Siap digunakan

  ![IDS](img/Gambar%203.JPG)


- Kita melakukan PING terlebih dahulu Web server yang telah kita buat, jika berhasil maka OPNsense akan mendeteksi adanya aktivitas yang sedang terjadi pada web server kita.

  ![IDS](img/Gambar%204.1.JPG)

  ![IDS](img/Gambar%204.2.JPG)


- Kita lihat pada bagian tab alert sudah ada beberapa packet yang telah terdeteksi oleh OPNsense

  ![IDS](img/Gambar%205.JPG)

