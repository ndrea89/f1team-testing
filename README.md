# 🏎️ F1 Aerodynamic Part Validation - BPMN 2.0 Workflow

## 📌 Project Overview
Project ini mendokumentasikan alur kerja (business process) teknis dalam pengembangan komponen aerodinamika di tim Formula 1.

Model ini dibuat menggunakan **Camunda Modeler** dengan standar **BPMN 2.0**.

## 🛠️ Key Logic & Features
Dalam diagram ini, saya mengintegrasikan beberapa elemen teknis tingkat lanjut:
* **Error Boundary Events:** Menangani ketidakcocokan data (*correlation gap*) antara simulasi CFD dan tes Wind Tunnel.
* **Signal Events:** Mekanisme "Red Flag" untuk penghentian proses instan saat terjadi kendali teknis di lintasan.
* **Conditional Flows:** Validasi otomatis berdasarkan parameter fisik (Drag force & Downforce thresholds).

## 🔍 QA & Analytical Perspective
Mengapa alur ini dirancang seperti ini?
1. **Risk Mitigation:** Setiap tahapan memiliki "gerbang" validasi untuk mencegah komponen cacat sampai ke tahap balapan (Race).
2. **Negative Testing:** Saya mensimulasikan skenario kegagalan (cuaca buruk, sensor timeout) untuk memastikan sistem tetap memiliki *fallback plan*.
3. **Data Integrity:** Memastikan sinkronisasi data dari desain digital hingga hasil sensor fisik di sirkuit.

## 📂 Files in this Repo
* `/diagrams`: File mentah `.bpmn` (Bisa dibuka di Camunda).
* `/exports`: Hasil ekspor format `.svg` dan `.png` kualitas tinggi.
* `/docs`: Penjelasan detail mengenai skenario testing.

---
*Created by ATitanni, March 9, 2026*
**Senior QA Engineer & Aspiring Business Analyst**
