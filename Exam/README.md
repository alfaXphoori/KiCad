# สอบปฏิบัติ: การออกแบบวงจร PCB ด้วย KiCad

**เวลาในการทำข้อสอบ:** 3 ชั่วโมง

---

> ## คำชี้แจงการสอบปฏิบัติ
> 1. ให้นักศึกษาสร้างโครงการ KiCad ใหม่ ตั้งชื่อว่า **`StudentID_Exam`** เช่น `Phoori_Exam`
> 2. ออกแบบ **Schematic** และ **PCB Layout** ตามข้อกำหนดในแต่ละงาน
> 3. ต้องผ่าน **ERC และ DRC โดยไม่มี Error** ก่อนส่งงาน
> 4. ส่งไฟล์ทั้ง **Zip Folder** และ **Screenshot** ทั้งหมดตามที่กำหนด
> 5. **ห้าม** Copy งานคนอื่น ต้องวาดและต่อวงจรเองทั้งหมด

---

## ก่อนเริ่มสอบ: โหลด Symbol และ Footprint Library

> ⚠️ **อุปกรณ์บางตัวไม่มีใน KiCad Library มาตรฐาน ต้องโหลดเพิ่มก่อนเริ่มทำข้อสอบ**

### ขั้นตอนที่ 1 – ดาวน์โหลด Library Files

เข้าลิงก์ด้านล่าง แล้วดาวน์โหลดไฟล์ทั้งหมดในโฟลเดอร์:

**📁 [Library Files](https://drive.google.com/drive/u/3/folders/1tgE6V-60Cr-DjqShTD6DQ9Ks3JGPzj9w)**

แตกไฟล์ไว้ที่โฟลเดอร์ที่จำง่าย เช่น `C:\KiCad_Lib\`

### ขั้นตอนที่ 2 – เพิ่ม Symbol Library ใน KiCad

1. เปิด KiCad → **Preferences → Manage Symbol Libraries**
2. คลิกแท็บ **Global Libraries** (ใช้ได้กับทุกโครงการ)
3. คลิกปุ่ม **Add existing library to table** (ไอคอนโฟลเดอร์)
4. เลือกไฟล์ `.kicad_sym` ที่ดาวน์โหลดมา
5. คลิก **OK**

### ขั้นตอนที่ 3 – เพิ่ม Footprint Library ใน KiCad

1. เปิด KiCad → **Preferences → Manage Footprint Libraries**
2. คลิกแท็บ **Global Libraries**
3. คลิกปุ่ม **Add existing library to table**
4. เลือกโฟลเดอร์ `.pretty` ที่ดาวน์โหลดมา
5. คลิก **OK**

### ขั้นตอนที่ 4 – เพิ่ม 3D Model ใน KiCad

1. ไฟล์ 3D Model จะอยู่ในรูปแบบ **`.step`** หรือ **`.wrl`** ในโฟลเดอร์ที่ดาวน์โหลดมา
2. วางไฟล์ 3D ไว้ที่โฟลเดอร์ **`C:\KiCad_Lib\3D\`**
3. การผูก 3D Model กับ Footprint:
   - เปิด **Footprint Editor** → เลือก Footprint ที่ต้องการ
   - ไปที่ **Edit → Footprint Properties** → แท็บ **3D Models**
   - คลิก **Add 3D Model** → เลือกไฟล์ `.step` หรือ `.wrl`
   - ปรับค่า Offset / Scale / Rotation ให้ตรงกับ Component จริง
   - คลิก **OK**
4. ตรวจสอบ 3D View ใน PCB Editor: **View → 3D Viewer** (กด `Alt+3`)

### อุปกรณ์ที่ต้องโหลด Library เพิ่ม:

| อุปกรณ์ | Symbol/Footprint |
|---------|-----------------|
| RP2350A-QFN60 | RP2350A Symbol + QFN-60 Footprint + `.step` 3D Model |
| ME6217C33M5G | LDO Symbol + SOT-23-5 Footprint + `.step` 3D Model |
| W25Q16JVUXIQ | Flash Symbol + WSON-8 Footprint + `.step` 3D Model |
| C3E-12.000-12-3030-R | Crystal Symbol + SMD 3.2×2.5 Footprint + `.step` 3D Model |

---

## งานที่ 1: สร้างโครงการและ Board Setup

### ขั้นตอน:
1. เปิด KiCad 9.0 → สร้าง New Project ชื่อ **`StudentID_Exam`**
2. กรอก Title Block ใน Schematic ดังนี้:

| ช่อง | ข้อมูลที่ต้องกรอก |
|------|-----------------|
| Title | Exam |
| Date | 2026-03-04 |
| Revision | V1.0 |
| Company | ชื่อ-นามสกุลนักศึกษา |
| Comment 1 | รหัสนักศึกษา |
| Comment 2 | สาขา CE6841/21 |

3. ตั้งค่า PCB Board Setup ตามนี้:

| พารามิเตอร์ | ค่าที่ต้องตั้ง |
|-------------|--------------|
| Board Layers | 4 Layer (F.Cu / In1.Cu / In2.Cu / B.Cu) |
| Board Thickness | 1.6 mm |
| Min Track Width | 0.2 mm |
| Min Clearance | 0.2 mm |
| Min Via Hole Diameter | 0.3 mm |
| Min Via Annular Width | 0.1 mm |

> **ตัวอย่าง Board Setup – Physical:**  
> ![Physical Board Setup](imgs/Physical_Board_Setup.png)

> **ตัวอย่าง Board Setup – Constraints:**  
> ![Constraints Board Setup](imgs/Constraints_Board_Setup.png)

> **ตัวอย่าง Board Setup – Violations:**  
> ![Violation Board Setup](imgs/Violation_Board_Setup.png)

---

## ERC และ Annotation

### ขั้นตอนปฏิบัติ:
1. ไปที่เมนู **Tools -> Annotate Schematic** -> คลิก Annotate All
2. เพิ่ม `PWR_FLAG` Symbol บน Net `VBUS` และ `+3V3` เพื่อแก้ ERC Warning
3. รัน **Inspect -> Electrical Rules Checker (ERC)**
4. แก้ไข Error ทุกรายการจนกว่าจะไม่มี Error เหลือ
5. บันทึก Schematic

**สิ่งที่ต้องส่ง:** Screenshot ของหน้าต่าง ERC ที่แสดง **0 Errors, 0 Warnings** บันทึกชื่อ `SCH_ERC_0Error.png`

พร้อมถ่ายภาพ Schematic ภาพรวมทั้งหมด บันทึกชื่อ `SCH_Full.png`

> **ตัวอย่างผล ERC ที่ผ่าน (0 Errors):**  
> ![SCH Error Check](imgs/SCH_Error_Check.png)

---

##  PCB Layout - Import Netlist และ Component Placement

### ขั้นตอนที่ 1 - Update PCB จาก Schematic:
1. ใน Schematic Editor -> **Tools -> Update PCB from Schematic**
2. ตรวจสอบว่า Component ทุกตัวถูก Import เข้า PCB Editor

### ขั้นตอนที่ 2 - กำหนดขนาด Board:
1. วาด Board Outline บน Layer **Edge.Cuts**
2. ขนาด Board: **ไม่เกิน 35 mm x 35 mm** (กำหนดเองในช่วง 20–35 mm)
3. ใช้ Line Width: **0.05 mm**

> ⚠️ **Board ต้องมีขนาดไม่เกิน 35×35 mm มิฉะนั้นถือว่าไม่ผ่านเงื่อนไขขนาดบอร์ด**

### เพิ่มชื่อและโลโก้ CE บน Silkscreen ด้านหลัง:

**ส่วนที่ 1 – พิมพ์ชื่อตัวเอง (Text):**
1. เลือก Layer **B.SilkS**
2. ไปที่ **Place -> Add Text** (หรือกด `T`)
3. พิมพ์ **ชื่อ-นามสกุลภาษาอังกฤษ** ของตัวเอง เช่น `PHOORI`
   - ขนาด Text: **3.0 mm** ขึ้นไป ให้เห็นชัดเจน
   - วางบริเวณด้านบนของ Board ด้านหลัง (B.SilkS)

**ส่วนที่ 2 – เพิ่มรูปโลโก้ CE (Bitmap Image):**
1. เตรียมไฟล์รูปโลโก้ **CE** ในรูปแบบ **PNG (สีขาวบนพื้นดำ)** ขนาดแนะนำ 200×200 px ขึ้นไป
2. ใน PCB Editor ไปที่ **Place -> Add Image** (หรือ **File -> Import -> Bitmap Image**)
3. เลือกไฟล์รูปโลโก้ CE แล้วคลิก OK
4. เลือก Layer เป็น **B.SilkS** และปรับ Scale ให้เหมาะสม
5. วางรูปโลโก้ CE ใต้ชื่อ ให้เห็นชัดเจนบนด้านหลัง Board

> 💡 **เคล็ดลับการเตรียมรูป:** ให้ใช้รูปโลโก้ CE ที่มีพื้นหลังสีดำ และส่วนที่ต้องการพิมพ์เป็นสีขาว เพื่อให้ KiCad แปลงเป็น Silkscreen ได้ถูกต้อง

---

## งานที่ 8: PCB Layout - Routing

### Net Classes ที่ต้องตั้งค่าก่อน Route:

| Net Class | Net ที่รวมอยู่ | Track Width | Clearance |
|-----------|-------------|------------|-----------|
| USB_DIFF | USB_DP, USB_DM | 0.2 mm | 0.2 mm |
| POWER | VBUS, +3V3 | 0.5 mm | 0.3 mm |
| Default | ทุก Net อื่น | 0.2 mm | 0.2 mm |

### ขั้นตอนที่ 1 - ตั้งค่า Net Classes:
1. **Board Setup -> Net Classes** -> เพิ่ม Class `USB_DIFF` และ `POWER`
2. กำหนด Track Width และ Clearance ตามตาราง

> **ตัวอย่าง Net Classes ใน Board Setup:**  
> ![Net Classes Board Setup](imgs/Net_Classes_Board_Setup.png)

### ขั้นตอนที่ 2 - Copper Pour / Fill Zone (บังคับ):

ต้องทำ Fill Zone ครบทั้ง **4 Layer** ต่อไปนี้:

**ขั้นตอนสำหรับแต่ละ Layer:**
1. เลือก Layer เป้าหมาย (F.Cu / In1.Cu / In2.Cu / B.Cu)
2. ไปที่ **Place -> Add Filled Zone** (หรือกด `Ctrl+Shift+Z`)
3. วาด Zone ให้ครอบ Board ทั้งหมดภายใน Edge.Cuts
4. ในกล่อง Zone Properties:
5. กด `B` เพื่อ **Fill All Zones** ทุกครั้งหลังแก้ไข
6. ตรวจสอบว่า GND Fill ครอบคลุมพื้นที่ > 70% ของแต่ละ Layer

> **ตัวอย่าง Copper Zone Properties:**  
> ![Copper Zone Properties](imgs/Fill_Zone.png)

> ⚠️ **ต้องมี Fill Zone ครบทุก Layer ที่กำหนด มิฉะนั้นถือว่าไม่ผ่านเงื่อนไข GND Plane**

---

## DRC และ 3D View

### ขั้นตอนที่ 1 - Design Rule Check:
1. ไปที่ **Inspect -> Design Rules Checker (DRC)**
2. คลิก **Run DRC**
3. แก้ไข Error ทุกรายการจนกว่าจะไม่เหลือ Error
4. เป้าหมาย: **0 Errors**
5. บันทึก Screenshot ชื่อ `PCB_DRC_0Error.png`

> **ตัวอย่างผล DRC ที่ผ่าน (0 Errors):**  
> ![PCB Error Check](imgs/PCB_Error_Check.png)

### ขั้นตอนที่ 2 - ตรวจสอบ 3D View (บังคับ):
1. ใน PCB Editor กด **`Alt+3`** หรือไปที่ **View → 3D Viewer**
2. ตรวจสอบว่า Component ทุกตัวแสดง 3D Model ครบถ้วน **ไม่มีอุปกรณ์ที่ขาด 3D Model**
3. บันทึก Screenshot ของ 3D View จำนวน **2 มุม** คือ:
   - มุมมอง **Top (ด้านบน)**
   - มุมมอง **Bottom (ด้านล่าง)**
4. บันทึกภาพชื่อ `3D_Top.png` และ `3D_Bottom.png`

นอกจากนี้ ให้ถ่ายภาพ PCB Layout เพิ่มเติม 2 รูป:
- `PCB_Layout_Top.png` — แสดง Layer **F.Cu** (หน้า PCB)
- `PCB_Layout_Bottom.png` — แสดง Layer **B.Cu** (หลัง PCB)

> ⚠️ **Component ทุกตัวต้องมี 3D Model ครบถ้วน**

---

## สรุปการส่งงาน

### ลิงก์การส่งงาน:
[คลิกที่นี่เพื่อส่งงาน](https://docs.google.com/forms/d/e/1FAIpQLSdr00fWbVABh_uF_Hmt_Hmi3ux_y0vmjzFsGliQYqPfY1zKxA/viewform?usp=dialog)

### ไฟล์ที่ต้องส่ง:
```
StudentID_Exam.zip                   ← Zip โฟลเดอร์โครงการทั้งหมด
├── StudentID_Exam.kicad_pro
├── StudentID_Exam.kicad_sch
└── StudentID_Exam.kicad_pcb

Screenshots_Schematic/               
└── SCH_Full.png                     ← ภาพรวม Schematic ทั้งหมด

Screenshots_PCB/                     
└── PCB_Full.png                     ← ภาพรวม PCB ทั้งหมด

Screenshots_3D/                      
├── 3D_Top.png                       ← มุมมองด้านบน (Top)
└── 3D_Bottom.png                    ← มุมมองด้านล่าง (Bottom)
```

### ตัวอย่างรูปที่ใช้ส่งงาน:

> **Schematic (SCH_Full.png):**  
> ![Schematic Full](imgs/SCH_Pic.png)

> **PCB Layout (PCB_Full.png):**  
> ![PCB Full](imgs/PCB_Pic.png)

> **3D Top (3D_Top.png):**  
> ![3D Top](imgs/3D_F_Pic.png)

> **3D Bottom (3D_Bottom.png):**  
> ![3D Bottom](imgs/3D_B_Pic.png)

---


*สอบปฏิบัติ KiCad | CE6841/21 | 4 มีนาคม 2026*
