# Tugas Manajemen Pusat Data: Enterprise Server Provisioning, IT Service Management, & Remote Administration

**Nama:** M. Rafif Farihan  
**NIM:** 09011282328042
**Kelas:** SK7
**Mata Kuliah:** Manajemen Pusat Data  
**Dosen Pengampu:** Adi Hermansyah, M.T.  

---

## Deskripsi Proyek

Proyek ini merupakan persiapan infrastruktur *Enterprise Data Center* berbasis virtualisasi. Fokus utama pada tahap ini adalah melakukan *provisioning* server mandiri (*Standalone Server*) menggunakan arsitektur *Virtual Machine* (VM AlmaLinux 10.2), pengaktifan layanan *Database & Web Server* (LAMP Stack), implementasi sistem *IT Service Management* atau *IT Helpdesk* (osTicket), serta akses administrasi jarak jauh (*Remote SSH*).

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
Laporan dari klien masuk secara *real-time* ke dasbor teknisi. Setiap pengaduan memiliki nomor tiket unik untuk pelacakan. Teknisi dapat memberikan balasan, mengubah status perbaikan menjadi *Closed*, dan memantau histori perbaikan infrastruktur.

![Dashboard Teknisi](Screenshot%202026-10-14%20062844.png)

---

## 📌 Kesimpulan
Penggunaan LAMP Stack pada distro *enterprise* seperti AlmaLinux memberikan stabilitas tinggi, sementara implementasi osTicket mendemonstrasikan pemahaman mendalam terkait Standar Operasional Prosedur (SOP) pelayanan IT di dalam sebuah Pusat Data nyata.
