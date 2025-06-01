
# Ansible Role: NGINX Deployment

**Ansible Role untuk Mengelola Instalasi dan Operasi NGINX Secara Otomatis**

Repository ini menyediakan serangkaian playbook Ansible yang dirancang untuk mempermudah proses instalasi, konfigurasi, dan manajemen layanan NGINX pada server berbasis Linux Debian dan Ubuntu. Dengan pendekatan modular dan deklaratif, Anda dapat mengotomatisasi life cycle NGINX mulai dari instalasi hingga penghapusan.

## Features

- **Instalasi Otomatis**: Playbook `install.yml` untuk menginstal NGINX beserta dependensinya.
- **Manajemen Layanan**: Playbook `start.yml` dan `stop.yml` untuk memulai dan menghentikan layanan NGINX.
- **Penghapusan**: Playbook `uninstall.yml` untuk menghapus NGINX dari sistem.
- **Struktur Modular**: Menggunakan struktur role Ansible yang memisahkan tugas, variabel, dan handler untuk kemudahan pemeliharaan.

## Project Structure
```
ansible-nginx/
├── ansible.cfg
├── hosts.ini
├── install.yml
├── start.yml
├── stop.yml
├── uninstall.yml
└── roles/
    └── nginx/
        ├── tasks/
        ├── handlers/
        └── templates/
```
- `ansible.cfg`: Konfigurasi Ansible.
- `hosts.ini`: Inventori host target.
- `install.yml`: Playbook untuk instalasi NGINX.
- `start.yml`: Playbook untuk memulai layanan NGINX.
- `stop.yml`: Playbook untuk menghentikan layanan NGINX.
- `uninstall.yml`: Playbook untuk menghapus NGINX.
- `roles/nginx/`: Direktori role Ansible untuk NGINX.

## Prerequisites

- Ansible versi terbaru (disarankan menggunakan `pip install ansible`)
- Akses SSH ke server target dengan hak akses sudo
- Sistem operasi berbasis Linux (Debian/Ubuntu)

## How to Use

1. **Clone Repository**

   ```bash
   git clone https://github.com/anang4di/ansible-nginx.git
   cd ansible-nginx
   ```
   
2. **Sesuaikan Inventori**

	Edit file `hosts.ini` dan sesuaikan dengan host target Anda.

4. **Instalasi NGINX**
	```bash
	ansible-playbook install.yml
	```
5. **Start NGINX**
	```bash
	ansible-playbook start.yml
	```
6. **Stop NGINX**
	```bash
	ansible-playbook stop.yml
	```
7. **Uninstall NGINX**
	```bash
	ansible-playbook uninstall.yml
	```
