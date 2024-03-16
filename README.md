# Konfigurasi-Sistem-Operasi-Jarak-Jauh-Dengan-SSH
## Peralatan Praktikum yang di Butuhkan 
#### 1. VirtualBox  `Virtual Machine`
#### 2. File Sistem Operasi Almalinux 
#### 3. File Sistem Operasi Ubuntu Linux
#### 4. Software Putty  `untuk remote server`

#### ________________________________________________________________________________________________________________________________________________________
## 1. VirtualBox
#### VirtualBox adalah virtualizer lengkap untuk keperluan umum untuk perangkat keras x86, ditargetkan untuk penggunaan server, desktop, dan tertanam.Untuk pengenalan menyeluruh tentang virtualisasi dan VirtualBox, silakan merujuk ke bab pertama Panduan Pengguna VirtualBox versi online .
#### Link Download VirtualBox  https://www.virtualbox.org/
####
![image](https://github.com/firmansultoni/Konfigurasi-Sistem-Operasi-Jarak-Jauh-Dengan-SSH/assets/113542409/5df947b9-eaf8-4feb-ae8d-1306c94a646d)

#### ________________________________________________________________________________________________________________________________________________________
## 2. File Sistem Operasi Almalinux 
#### VAlmaLinux OS adalah sistem operasi Linux open-source berbasis komunitas yang mengisi kesenjangan yang ditinggalkan oleh penghentian rilis stabil CentOS Linux. AlmaLinux OS adalah distro Enterprise Linux, biner yang kompatibel dengan RHEL®, dan dipandu serta dibangun oleh komunitas. Sebagai OS yang berdiri sendiri dan sepenuhnya gratis, AlmaLinux OS menikmati sponsor tahunan sebesar $1 juta dari CloudLinux Inc. dan dukungan dari lebih dari 25 sponsor lainnya. Upaya pembangunan yang sedang berlangsung diatur oleh anggota masyarakat. AlmaLinux OS Foundation adalah organisasi nirlaba 501(c)(6) yang dibuat untuk kepentingan komunitas OS AlmaLinux.
#### Link Download File Almalinux  https://almalinux.org/
####
![image](https://github.com/firmansultoni/Konfigurasi-Sistem-Operasi-Jarak-Jauh-Dengan-SSH/assets/113542409/59978fe1-9bdf-4819-9cd3-e97638ca46dd)

#### ________________________________________________________________________________________________________________________________________________________
## 3. File Sistem Operasi Ubuntu Linux
#### Sistem operasi desktop sumber terbuka yang mendukung jutaan PC dan laptop di seluruh dunia. Cari tahu lebih lanjut tentang fitur Ubuntu dan bagaimana kami mendukung pengembang dan organisasi di bawah ini.
#### Link Download File Ubuntu Linux  https://ubuntu.com/download/desktop
####
![image](https://github.com/firmansultoni/Konfigurasi-Sistem-Operasi-Jarak-Jauh-Dengan-SSH/assets/113542409/4b14dd97-3c02-43da-9c3f-9e0e063f1206)

#### ________________________________________________________________________________________________________________________________________________________
## 4. Software Putty
#### Link Download Putty https://putty.org/
#### 
![image](https://github.com/firmansultoni/Konfigurasi-Sistem-Operasi-Jarak-Jauh-Dengan-SSH/assets/113542409/f1d1de7f-5963-4f60-adb9-29137e7400ec)

#### ________________________________________________________________________________________________________________________________________________________
## Langkah-Langkah
### Buka Virtualbox 
![image](https://github.com/firmansultoni/Konfigurasi-Sistem-Operasi-Jarak-Jauh-Dengan-SSH/assets/113542409/799544b6-e2cc-4b08-af91-944a39b0a3b3)
### Buat Virtual Machine OS Almalinux dan Jalankan 
![image](https://github.com/firmansultoni/Konfigurasi-Sistem-Operasi-Jarak-Jauh-Dengan-SSH/assets/113542409/3a98509c-eb5a-4a87-bd00-c210b21a364b)
### Masuk Ke Terminal dan Cek Alamat IP  `ifconfig`
### Simpan Alamat IP Server Almalinux
![image](https://github.com/firmansultoni/Konfigurasi-Sistem-Operasi-Jarak-Jauh-Dengan-SSH/assets/113542409/f633d469-65e5-42c4-bd9e-7260aee3d6c6)

#### ________________________________________________________________________________________________________________________________________________________
### Buka Virtualbox 
![image](https://github.com/firmansultoni/Konfigurasi-Sistem-Operasi-Jarak-Jauh-Dengan-SSH/assets/113542409/799544b6-e2cc-4b08-af91-944a39b0a3b3)
### Buat Virtual Machine OS Ubuntu Linux dan Jalankan 
![image](https://github.com/firmansultoni/Konfigurasi-Sistem-Operasi-Jarak-Jauh-Dengan-SSH/assets/113542409/6122d1bb-4d1e-4616-b937-62dd54f30be7)
### Masuk Ke Terminal dan Cek Alamat IP  `ifconfig`
### Simpan Alamat IP Server Ubuntu Linux
![image](https://github.com/firmansultoni/Konfigurasi-Sistem-Operasi-Jarak-Jauh-Dengan-SSH/assets/113542409/dbb100bc-a2ad-46ea-bc5c-8c0ab1e1464e)

#### ________________________________________________________________________________________________________________________________________________________
### Buka Putty 
### Masukkan Alamat IP Kedua Server
![image](https://github.com/firmansultoni/Konfigurasi-Sistem-Operasi-Jarak-Jauh-Dengan-SSH/assets/113542409/e6e3d74f-3a96-4e9f-84bf-67e439af3705)
### Loging Di Kedua Server 
![image](https://github.com/firmansultoni/Konfigurasi-Sistem-Operasi-Jarak-Jauh-Dengan-SSH/assets/113542409/7ad7fb8a-edc8-41dc-ad62-06430fe135a6)

#### ________________________________________________________________________________________________________________________________________________________
### Instal SSH di Kedua Server Untuk Bisa Saling Berkomunikasi Antar Server
### Perintah intasll SSH di Server Almalinux 
#### `sudo dnf upgrade`
#### `sudo dnf install openssh-server`
![image](https://github.com/firmansultoni/Konfigurasi-Sistem-Operasi-Jarak-Jauh-Dengan-SSH/assets/113542409/ba3553a2-0e71-498b-bccc-2f318dbfc167)
#### `sudo systemctl enable sshd` mengaktifkan layanan SSH
#### `sudo systemctl start sshd` memulai layanan SSH
#### `sudo systemctl status sshd`  melihat status SSH
![image](https://github.com/firmansultoni/Konfigurasi-Sistem-Operasi-Jarak-Jauh-Dengan-SSH/assets/113542409/637f5e48-67ab-4cd1-ac11-854b99f70e05)
#### `sudo systemctl disable sshd`  menonaktifkan layanan SSH

#### ________________________________________________________________________________________________________________________________________________________
### Perintah intasll SSH di Server Ubuntu Linux 
#### `sudo apt update`
#### `sudo apt install openssh-server`
![image](https://github.com/firmansultoni/Konfigurasi-Sistem-Operasi-Jarak-Jauh-Dengan-SSH/assets/113542409/7b818bcd-0283-4acf-9d24-119d47f520ac)
#### `sudo systemctl start ssh` memulai layanan SSH
#### `sudo systemctl enable ssh` memulai layanan SSH secara otomatis ketika Boot
#### `sudo systemctl status ssh`  melihat status SSH
![image](https://github.com/firmansultoni/Konfigurasi-Sistem-Operasi-Jarak-Jauh-Dengan-SSH/assets/113542409/e1f9d607-bac6-418f-877b-69ffb777b1e4)
#### `sudo systemctl disable ssh` menonaktifkan layanan SSH

#### ________________________________________________________________________________________________________________________________________________________
## Tes Komunikasi Antar Server
#### pastikan kedua server berada pada jaringan yang sama 
### Tes Komunikasi di Server Almalinux
#### `ssh username@alamat_ip_server` ganti dengan username dan alamat ip yang di tuju
#### `ping alamat_ip_server` tes komunikasi saja tanpa login ke server
![image](https://github.com/firmansultoni/Konfigurasi-Sistem-Operasi-Jarak-Jauh-Dengan-SSH/assets/113542409/bf7ce740-d104-4835-96a8-d6d50dd44531)
