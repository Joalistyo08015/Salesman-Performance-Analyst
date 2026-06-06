# 📊 Salesman Performance Analysis Dashboard

## 📌 Latar Belakang

Project ini dibuat untuk menganalisis performa tenaga penjualan (salesman) berdasarkan revenue, jumlah transaksi, quantity penjualan, dan tren penjualan dari waktu ke waktu.

Analisis dilakukan menggunakan MySQL sebagai database management system untuk membangun relational database dan Power BI sebagai tools visualisasi data. Dashboard yang dihasilkan bertujuan membantu perusahaan dalam memonitor performa salesman, mengidentifikasi top performer, serta mendukung pengambilan keputusan berbasis data.

> **Catatan:** Dataset asli tidak disertakan dalam repository ini karena alasan kerahasiaan dan privasi data perusahaan. Repository ini berfokus pada proses perancangan database, pembuatan query SQL, pengembangan dashboard, dan analisis bisnis.

---

# 🎯 Tujuan Analisis

Analisis ini dilakukan untuk menjawab beberapa pertanyaan bisnis berikut:

* Siapa salesman dengan revenue tertinggi?
* Siapa salesman dengan jumlah transaksi terbanyak?
* Siapa salesman dengan quantity penjualan tertinggi?
* Bagaimana tren revenue salesman dari tahun ke tahun?
* Berapa kontribusi revenue masing-masing salesman terhadap total revenue perusahaan?
* Bagaimana distribusi performa penjualan antar salesman?
* Strategi apa yang dapat dilakukan untuk meningkatkan performa tim penjualan?

---

# 🛠️ Tools & Technologies
![MySQL](https://img.shields.io/badge/MySQL-SQL%20Query%20%26%20Data%20Modeling-blue)
![Excel](https://img.shields.io/badge/Excel-Data%20Preparation-green)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard%20%26%20Visualization-yellow)

| Tools    | Fungsi                         |
| -------- | ------------------------------ |
| MySQL    | Database Management System     |
| SQL      | Data Query & Transformation    |
| Power BI | Dashboard & Data Visualization |

---

# 📂 Struktur Repository
```text
Salesman-Performance-Analysis-Dashboard

│

├── Dashboard

│ └── Salesman Performance Dashboard.png

│

├── SQL

│ ├── Create Table.sql

│ ├── Primary Key.sql

│ ├── Foreign Key.sql

│ ├── Master Table.sql

│ └── Full Query.sql

│

├── Database Schema

│ └── ERD.png

│

└── README.md
```
---

# 🔄 Alur Pengolahan Data

### 1. Database Design

Membuat struktur database yang terdiri dari empat tabel utama:

* Customer
* Product
* Salesman
* Sales Transaction

### 2. Data Modeling

Menentukan Primary Key dan Foreign Key untuk membangun hubungan antar tabel dan menjaga integritas data.

### 3. Data Transformation

Menggabungkan data transaksi dan data master menggunakan SQL JOIN untuk membentuk Master Table yang siap digunakan untuk analisis.

### 4. Data Analysis

Melakukan analisis terhadap:

* Revenue per Salesman
* Transaction per Salesman
* Quantity Sold per Salesman
* Revenue Trend
* Revenue Contribution

### 5. Data Visualization

Membangun dashboard interaktif menggunakan Power BI untuk memudahkan monitoring performa salesman.

---

# 🗄️ Struktur Database

## Customer

| Kolom            |
| ---------------- |
| Customer_Account |
| Region           |
| Customer_Name    |

## Product

| Kolom         |
| ------------- |
| Product_ID    |
| Item_Category |
| Product       |
| Price         |

## Salesman

| Kolom         |
| ------------- |
| Salesman_ID   |
| Salesman_Name |

## Sales Transaction

| Kolom               |
| ------------------- |
| Invoice_ID          |
| Invoice_Date        |
| Invoice_Year        |
| Branch              |
| Salesman_ID         |
| Customer_Account    |
| Product_ID          |
| Qty                 |
| Payment_Per_Month   |
| Booking_Fee         |
| Monthly_Installment |
| Delivery_Fee        |

---

# 🔗 Relasi Antar Tabel

## Primary Key

| Tabel             | Primary Key      |
| ----------------- | ---------------- |
| Customer          | Customer_Account |
| Product           | Product_ID       |
| Salesman          | Salesman_ID      |
| Sales Transaction | Invoice_ID       |

## Relationship

* Customer (1) → (M) Sales Transaction
* Product (1) → (M) Sales Transaction
* Salesman (1) → (M) Sales Transaction

---

# 📈 Dashboard Overview

Dashboard menampilkan beberapa KPI utama, yaitu:

### KPI

* Total Salesman
* Total Quantity Sold
* Total Transactions
* Average Revenue per Salesman

### Visualisasi

* Revenue by Salesman
* Transaction by Salesman
* Quantity Sold by Salesman
* Top 5 Revenue Trend by Year
* Top 5 Revenue Contribution by Salesman
* Salesman Performance Table

### Filter

* Tahun
* Salesman
* Kategori Produk
* Wilayah

---

# 📊 Hasil Analisis

## Revenue Performance

Tim penjualan yang terdiri dari 14 salesman berhasil menghasilkan total revenue sebesar Rp4,19 miliar, dengan rata-rata revenue per salesman sebesar Rp299,25 juta.

## Top Salesman Performance

Darman Sitorus menjadi salesman dengan performa terbaik dengan total revenue sebesar Rp604,16 juta, atau sekitar 14,42% dari total revenue perusahaan. Nilai tersebut berada sekitar 2 kali lebih tinggi dibandingkan rata-rata revenue per salesman.

## Transaction & Quantity Performance

Selama periode analisis, tercatat 432 transaksi dan 432 unit penjualan. Darman Sitorus juga mencatat performa tertinggi dengan 63 transaksi dan 63 unit penjualan, menunjukkan kontribusi yang signifikan terhadap aktivitas penjualan perusahaan.

## Revenue Distribution

Terdapat perbedaan performa yang cukup signifikan antar salesman. Sebagian salesman menghasilkan revenue jauh di atas rata-rata tim, sementara sebagian lainnya masih berada di bawah rata-rata revenue per salesman.

## Revenue Trend

Analisis tren menunjukkan bahwa performa revenue antar salesman mengalami fluktuasi selama periode analisis, sehingga diperlukan monitoring berkala untuk menjaga konsistensi pencapaian target penjualan.

---

# 💡 Rekomendasi Bisnis

* Mengembangkan program insentif untuk mempertahankan performa salesman terbaik.
* Mengidentifikasi strategi penjualan yang digunakan oleh top performer dan menerapkannya kepada anggota tim lainnya.
* Memberikan pelatihan tambahan bagi salesman dengan performa rendah.
* Melakukan monitoring performa secara berkala menggunakan dashboard interaktif.
* Mengevaluasi distribusi wilayah dan peluang pasar untuk meningkatkan produktivitas tim penjualan.

---

# 👤 Author

Project ini dibuat sebagai bagian dari portfolio Data Analyst dengan fokus pada:

* Database Design
* Relational Database
* SQL Query
* Data Transformation
* Data Visualization
* Business Analysis
* Power BI Dashboard
