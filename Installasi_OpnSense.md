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