# 🚀 ข้อสอบปฏิบัติรายวิชาเขียนลายวงจรอิเล็กทรอนิกส์ด้วย KiCad 🛠️

## 📌 คำชี้แจง  
✅ ให้นักศึกษาดำเนินการออกแบบวงจรและแผ่น PCB ตามหัวข้อที่กำหนด  
💻 ใช้ **KiCad** เป็นซอฟต์แวร์หลักในการออกแบบ  
📜 ให้แนบ **ไฟล์โปรเจกต์, ภาพแคปหน้าจอ และ Gerber Files**  
✅ คะแนนเต็ม **40 คะแนน**  

---

## 🟢 1. สร้างโปรเจค (2 คะแนน) 
📌 สร้างโปรเจคใหม่โดยใช้ชื่อ **CE67xx_Test_ชื่อนักศึกษา**  
**ตัวอย่าง:** `CE6741_Test_Phoori`  

---

## 🔵 2. ออกแบบ Schematic Diagram (15 คะแนน)  

### 📝 2.1 กำหนดข้อมูล Schematic  
- อ้างอิงตามรูปด้านล่าง  
  - ![sch-info](imgs/sch-info.png)  

### 📡 2.2 ต่อวงจรตามภาพตัวอย่าง  
- ![sch-zoom](imgs/sch-zoom.png)  

### 🔧 2.3 กำหนด Footprint ตาม BOM  
- ![bom](imgs/bom.png)  

### 🎯 2.4 เมื่อออกแบบสำเร็จควรได้ผลลัพธ์ดังนี้  
- ![sch](imgs/sch.png)  

### ✅ 2.5 ตรวจสอบ Electrical Rules Checker (ERC)  
- ตรวจสอบข้อผิดพลาดของวงจร  
- ![sch-check](imgs/sch-check.png)  
---

## 🔵 3. ออกแบบ PCB Layout (15 คะแนน)  
### 📝 3.1 กำหนดข้อมูล Schematic  
- ![pcb-info](imgs/pcb-info.png)
### 3.2 กำหนดให้นักศึกษา กำหนดขนาด ผ่าน PCB ไม่เกิน 16mm x 45mm
- ![pcb-size](imgs/pcb-size.png)
### 3.3 กำหนดขนาดเส้น ดังต่อไปนี้
- ![pcb-net](imgs/pcb-netclasses.png)
### 3.4 Draw filled zone และ เพิ่มชื่อ นักศึกษา B.Silkscreen ดังภาพ 
- ![pcb-3d-back](imgs/pcb-3d-back.png)
### 3.5 กำหนดค่าการตรวจเช็ค และตรวจสอบ ความถูกต้อง
- ![pcb-con](imgs/pcb-constraints.png)
- ![pcb-check](imgs/pcb-check.png)

---

## 🟠 4. การสร้างไฟล์สำหรับการผลิต JLCPCB (8 คะแนน)  

### 🏗 4.1 การส่งออก Gerber Files 
### 4.2 สั่งผลิต JLCPCB ด้วยใช้ Gerber Files 
- ![jlcpcb-t](imgs/jlcpcb-top.png)
- ![jlcpcb-b](imgs/jlcpcb-bot.png)

---

## ✅ จบข้อสอบ  
