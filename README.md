<div align="center">

<img src="Exam/imgs/CE.jpg" width="120" alt="CE Logo"/>

# 🖥️ KiCad PCB Design

**วิชาการออกแบบ PCB ด้วย KiCad**  
สาขาวิศวกรรมคอมพิวเตอร์ · CE6841/21 · มหาวิทยาลัย KSU

<br/>

[![KiCad](https://img.shields.io/badge/KiCad-9.0-blue?style=for-the-badge&logo=kicad&logoColor=white)](https://www.kicad.org/)
[![Platform](https://img.shields.io/badge/Platform-Win%20%7C%20Mac%20%7C%20Linux-lightgrey?style=for-the-badge&logo=windows&logoColor=white)](https://www.kicad.org/download/)
[![GitHub](https://img.shields.io/badge/GitHub-alfaXphoori-181717?style=for-the-badge&logo=github)](https://github.com/alfaXphoori/KiCad)

<br/>

[📝 ข้อสอบ](#-เนื้อหาในแต่ละโฟลเดอร์) · [📦 Library](#-library-และ-symbol) · [🏭 ผลิต PCB](#-การผลิต-pcb) · [🚀 เริ่มต้น](#-เริ่มต้นใช้งาน)

</div>

---

## 📁 โครงสร้างโปรเจกต์

```
KiCad/
├── 📂 Exam/               ← เอกสารและรูปประกอบสอบปฏิบัติ
│   ├── imgs/              ← รูปภาพประกอบข้อสอบ
│   ├── Exam_SCH.pdf       ← Schematic ตัวอย่าง
│   ├── Exam_PCB.pdf       ← PCB Layout ตัวอย่าง
│   └── README.md
└── 📂 Material/           ← เอกสารประกอบการสอน
    ├── 📂 Test/           ← ชุดทดสอบ
    │   ├── imgs/
    │   └── README.md
    └── 📂 Trainnig/       ← ชุดฝึกปฏิบัติ
        ├── Libraries/
        └── README.md
```

---

## 📚 เนื้อหาในแต่ละโฟลเดอร์

| | โฟลเดอร์ | เนื้อหา |
|:---:|:---------|:--------|
| 📝 | [**Exam**](Exam/README.md) | ข้อสอบปฏิบัติ RP2350A Dev Board · 4-Layer PCB |
| 🧪 | [**Material/Test**](Material/Test/README.md) | ข้อสอบปฏิบัติ ESP32 LED/LDR Circuit |
| 🎓 | [**Material/Trainnig**](Trainnig/README.md) | เอกสารและวงจรตัวอย่างสำหรับฝึกปฏิบัติ |

---

## 🌐 เว็บไซต์ที่เกี่ยวข้อง

### 🛠️ ซอฟต์แวร์และเครื่องมือ

| ชื่อ | รายละเอียด | ลิงก์ |
|:----|:-----------|:-----:|
| **KiCad EDA** | โปรแกรมออกแบบ PCB หลัก (ฟรี / Open Source) | [🔗](https://www.kicad.org/) |
| **KiCad Docs** | คู่มือการใช้งาน KiCad อย่างเป็นทางการ | [🔗](https://docs.kicad.org/) |
| **TinkerCAD** | จำลองวงจรออนไลน์ก่อน Route PCB | [🔗](https://www.tinkercad.com/) |

### 📦 Library และ Symbol

| ชื่อ | รายละเอียด | ลิงก์ |
|:----|:-----------|:-----:|
| **SnapEDA** | ดาวน์โหลด Symbol + Footprint + 3D Model | [🔗](https://www.snapeda.com/) |
| **Ultra Librarian** | คลัง Symbol และ Footprint สำหรับชิปต่าง ๆ | [🔗](https://www.ultralibrarian.com/) |
| **Component Search Engine** | ค้นหา Footprint จากชื่อ Part Number | [🔗](https://componentsearchengine.com/) |

### 🏭 การผลิต PCB

| ชื่อ | รายละเอียด | ลิงก์ |
|:----|:-----------|:-----:|
| **JLCPCB** | ผลิต PCB ราคาถูก รองรับ Gerber จาก KiCad | [🔗](https://jlcpcb.com/) |
| **PCBWay** | ผลิต PCB + Assembly บริการครบวงจร | [🔗](https://www.pcbway.com/) |

### 📖 เรียนรู้เพิ่มเติม

| ชื่อ | รายละเอียด | ลิงก์ |
|:----|:-----------|:-----:|
| **KiCad Forum** | ชุมชนผู้ใช้ KiCad ตั้งคำถาม/ตอบปัญหา | [🔗](https://forum.kicad.info/) |
| **Raspberry Pi RP2350** | Datasheet RP2350A MCU | [🔗](https://datasheets.raspberrypi.com/rp2350/rp2350-datasheet.pdf) |
| **IPC Standards** | มาตรฐานการออกแบบ PCB (IPC-2221) | [🔗](https://www.ipc.org/) |

---

## 🚀 เริ่มต้นใช้งาน

> [!TIP]
> ทำตามขั้นตอนด้านล่างเพื่อเริ่มใช้งานโปรเจกต์ได้ทันที

1. **ดาวน์โหลด KiCad 9.0** → [kicad.org/download](https://www.kicad.org/download/)
2. **โหลด Library เพิ่มเติม** → ดูรายละเอียดใน [Exam/README.md](Exam/README.md)
3. **เปิดไฟล์โปรเจกต์** → ไฟล์นามสกุล `.kicad_pro`

---

<div align="center">

*KiCad PCB Design · Computer Engineering CE6841/21 · KSU · 2026*

</div>
