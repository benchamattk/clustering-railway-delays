# Railway Delay Clustering

> This repository contains the research code and analysis for a study on clustering railway delay incidents, submitted to **IEEE BigData 2025 – Industry & Government Track**.

> Repository นี้รวบรวมซอร์สโค้ดและข้อมูลการวิเคราะห์สำหรับงานวิจัยเรื่องการจัดกลุ่มเหตุการณ์ความล่าช้าของรถไฟ (Clustering Railway Delay Incidents) ซึ่งได้นำเสนอในงานประชุมวิชาการ  **IEEE BigData 2025 – Industry & Government Track**

---

## Project Description

This project investigates patterns of railway delay incidents using clustering techniques on mixed-type data. The objective is to identify station-level delay patterns by jointly analyzing numerical and categorical features from open government datasets.

โครงการนี้ศึกษารูปแบบของเหตุการณ์ความล่าช้าของรถไฟ โดยใช้เทคนิคการจัดกลุ่ม (Clustering) บนข้อมูลแบบผสม (Mixed-type data) วัตถุประสงค์เพื่อระบุรูปแบบความล่าช้าในระดับสถานี ผ่านการวิเคราะห์ร่วมกันระหว่างข้อมูลเชิงตัวเลขและข้อมูลเชิงกลุ่ม ซึ่งรวบรวมจากชุดข้อมูลเปิดของภาครัฐ

The study applies **K-Prototypes clustering** for mixed-type data and benchmarks its performance against two alternative methods:
- **K-Means** with one-hot encoding
- **Agglomerative clustering** using Gower distance

งานวิจัยนี้ประยุกต์ใช้อัลกอริทึม **K-Prototypes clustering** สำหรับข้อมูลแบบผสม และเปรียบเทียบ (Benchmark) กับอีก 2 วิธีทางเลือก ได้แก่:
- **K-Means** ร่วมกับการทำ One-hot encoding
- **Agglomerative clustering** โดยใช้ระยะห่างแบบ Gower (Gower distance)

**Key Finding:** The results show how incorporating categorical attributes (e.g., cause types, time-of-day categories, and calendar effects) enables insights that are not accessible through numerical-only clustering approaches.

**ข้อค้นพบหลัก:** ผลการศึกษาแสดงให้เห็นว่าการนำคุณลักษณะเชิงกลุ่ม (Categorical attributes) เช่น ประเภทสาเหตุ, ช่วงเวลาของวัน และวันที่ มาร่วมวิเคราะห์ด้วยนั้น ช่วยให้ค้นพบข้อมูลเชิงลึกที่ไม่อาจพบได้หากใช้วิธีการจัดกลุ่มที่พึ่งพาเพียงข้อมูลเชิงตัวเลขเพียงอย่างเดียว
---

## 🛠️ Methodology

The analysis workflow includes:

- 🧹 **Data cleaning and validation**
- 🔗 **Data integration** of passenger volume and incident records
- ⚙️ **Feature engineering** for:
  - Time-of-day categories
  - Weekend and public-holiday flags
  - Intermodal connectivity indicators
- 📊 **Clustering analysis** using three methods for comparison
- 📏 **Evaluation** using Silhouette scores *(computed via Gower distance)*
- 📝 **Cluster profiling and interpretation**

---

## 📂 Repository Structure

```text
railway-delay-clustering/
│
├── notebooks/
│   └── railway_delay_clustering_analysis.ipynb
│
├── data/
│   ├── passenger_arl.csv
│   └── incident_data.csv
│
├── README.md
└── LICENSE
