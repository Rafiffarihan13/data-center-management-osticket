# Implementasi IT Service Management (ITSM) pada Infrastruktur Pusat Data

Proyek ini merupakan simulasi infrastruktur Pusat Data untuk mata kuliah **Manajemen Pusat Data** di **Universitas Sriwijaya**, yang berfokus pada penyediaan layanan *IT Helpdesk* berskala *enterprise* menggunakan osTicket di atas sistem operasi peladen Linux.

**Disusun oleh:** M. Rafif Farihan

---

## 🛠️ Arsitektur & Teknologi (Tech Stack)
Infrastruktur dibangun dari tingkat *hypervisor* hingga aplikasi dengan tumpukan teknologi berikut:
* **Hypervisor:** Proxmox VE
* **Sistem Operasi:** AlmaLinux 10.2 (Virtual Machine)
* **Web Server:** Apache (httpd)
* **Database:** MariaDB
* **Bahasa Pemrosesan:** PHP 8.x
* **Keamanan:** SELinux & SSH Access
* **Aplikasi Utama:** osTicket (IT Helpdesk & Ticketing System)

---

## 🖥️ Dokumentasi Sistem

### 1. Fondasi Infrastruktur (Proxmox, AlmaLinux, & LAMP Stack)
Server dijalankan secara virtual di dalam lingkungan Proxmox. Konfigurasi awal mencakup pengaturan jaringan lokal, modifikasi kebijakan SELinux agar Apache memiliki akses tulis secara penuh, serta pembukaan akses *remote* via protokol SSH untuk administrasi jarak jauh. Gambar di bawah menunjukkan akses sistem operasi melalui terminal PuTTY.

![Infrastruktur Server](Screenshot%202026-10-14%20062304.png)

### 2. Portal Layanan Klien (Client Helpdesk)
Sebagai simulasi SOP operasional Data Center, klien dapat melaporkan insiden (seperti *server down* atau *request storage*) melalui antarmuka web. Aplikasi osTicket memisahkan akses pengguna umum dengan teknisi untuk menjaga keamanan sistem.

![Portal Klien](Screenshot%202026-10-14%20062958.png)

### 3. Sistem Manajemen Insiden (Admin/Staff Control Panel)
Laporan dari klien masuk secara *real-time* ke dasbor teknisi. Setiap pengaduan memiliki nomor tiket unik untuk pelacakan. Teknisi dapat memberikan balasan, mengubah status perbaikan, dan memantau histori perbaikan infrastruktur.

![Dashboard Teknisi](Screenshot%202026-10-14%20062844.png)

---

## 📌 Kesimpulan
Penggunaan LAMP Stack pada distro *enterprise* seperti AlmaLinux memberikan stabilitas tinggi, sementara implementasi osTicket mendemonstrasikan pemahaman mendalam terkait Standar Operasional Prosedur (SOP) pelayanan IT di dalam sebuah Pusat Data nyata.
