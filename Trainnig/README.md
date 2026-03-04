## อบรมการทำแผ่น PCB ด้วย โปรแกรม KiCad
### วงจรตัวอย่าง 
วงจรตัวอย่างสำหรับการออกแบบวงจร PCB ด้วย Thinkercad
- https://www.tinkercad.com/things/eSUcswWTFzh-ledldr?sharecode=JfBLzF_0L9jgbdxzz1LCe_89Y2LhkJQhNdCu0lRxLeg
![t0](https://github.com/user-attachments/assets/8e69e0ec-dfc7-4d61-a3cd-85a739e22710)
![esp32 pin](https://github.com/user-attachments/assets/befdf9ab-9e73-42b1-82ec-ba1d9e9a0179)

### อุปกรณ์อิเล็กทรอนิกส์
- ESP32 C3 Super Mini (ส่วนประมวลผล)
  - ![esp32 bak bak](https://github.com/user-attachments/assets/ad510dd9-e1c6-43c7-a7f2-dede058a4d55)   ![esp32 c3 bak bak](https://github.com/user-attachments/assets/e3ff696d-ea86-488e-9baa-d51a653e5871)
- ปุ่มกด
  - ![btn](https://github.com/user-attachments/assets/fdfcbe7f-2956-4075-96ac-ddc428b21e3c)
- หลอด LED
  - ![led](https://github.com/user-attachments/assets/066509de-0232-4343-87b9-503fbe5afb4e)
- ตัวรับแสง LDR
  - ![LDR](https://github.com/user-attachments/assets/7039e88f-f174-420f-bd35-d0a435fa26d8)
- ตัวต้านทาน (R)
  - ![R](https://github.com/user-attachments/assets/2de20a5d-d331-4426-898e-c0de57905a1f)
- ตัวต่อไฟ Terminal
  - ![terminal](https://github.com/user-attachments/assets/b0b5b466-7c3b-4ede-87fd-14785ebb415f)

### การใช้งานโปรแกรม KiCad EDA
#### KiCad Schmatic Editor 
- https://www.kicad.org/
1. เปิดโปรแกรมจากปุ่ม Start และ ค้นหา Kicad
 - ![Screenshot 2025-01-23 211224](https://github.com/user-attachments/assets/000366e6-a9db-40fb-8763-ecdff5a4c994)
2. สร้าง Project ใหม่ 
 - ![1](https://github.com/user-attachments/assets/1cf80bfb-8ba5-4041-9a9b-b5ddfbf5faf9)
3. ตั้งชื่อ และ save
 - ![Screenshot 2025-01-23 211854](https://github.com/user-attachments/assets/42b8cbfe-58cf-427b-a15e-cc486225bc08)
4. ได้ Project ที่มี ไฟล์ .kicad_sch และ .kicad_pcb
 - ![Screenshot 2025-01-23 212054](https://github.com/user-attachments/assets/0a94ece5-1284-4ae3-98ea-407abf2ae4c4)
5. เข้าไปยัง .kicad_sch
 - ![Screenshot 2025-01-23 212349](https://github.com/user-attachments/assets/bbd1d232-1c4c-437e-9963-1e5791e7e2e1)
6. กำหนดข้อมูลชิ้นงาน
 - ![Screenshot 2025-01-23 213152](https://github.com/user-attachments/assets/ad6ddade-2754-408b-b74d-89327ce35c34)
7. Add อุปกรณ์ สำหรับการต่อวงจร (Add Symbol (A))
 - ![Screenshot 2025-01-23 213233](https://github.com/user-attachments/assets/1d236909-1b19-41c4-9b28-bc3a4de206ba)
8. ค้นหาอุปกรณ์ ตัวต้านทาน R
 - ![Screenshot 2025-01-23 213354](https://github.com/user-attachments/assets/4e35fff1-951d-4505-a876-3166afc96336)
9. กดเลือกตัวอุปกรณ์ R
 - ![Screenshot 2025-01-23 213425](https://github.com/user-attachments/assets/7b5b17db-0b55-4b27-b21f-63074fa02fb8)
10. ทำการตั้งค่าให้กับ R ที่เพิ่มเข้ามา
 - ![Screenshot 2025-01-23 213506](https://github.com/user-attachments/assets/5b9a569e-3815-4057-9b4a-518d2b774843)
11. ทำการเลือก Footprint สำหรับอุปกรณ์ R
 - ![Screenshot 2025-01-23 213636](https://github.com/user-attachments/assets/b72c9f49-844e-43ca-a6b2-7fd19f04dc60)
12. Add ส่วน GND (Ground) (Add Power (P))
 - ![Screenshot 2025-01-23 213832](https://github.com/user-attachments/assets/e56f471b-7a09-40ac-bc97-f2e91cfafe15)

#### Add New Libraries
13. ทำการเพิ่มอุปกรณ์ ESP32 C3 และ ปุ่มกด TS13-1212-73 ใน Manage Symbol Libraries
 - ![Screenshot 2025-01-23 214642](https://github.com/user-attachments/assets/f7413409-2dc7-4452-88a1-27a2459d79f6)
14. กดปุ่ม Add existing library to table 
 - ![Screenshot 2025-01-23 214457](https://github.com/user-attachments/assets/be4ecd21-65e9-46db-8c2c-fd45b9f7e4fd)
15. เลือกไฟล์ นามสกุล .kicad_sym
 - ![Screenshot 2025-01-23 214531](https://github.com/user-attachments/assets/a8cf0941-b0a3-4dd1-88bc-343c166db7b9)
16. ทำการเพิ่มอุปกรณ์ ESP32 C3 และ ปุ่มกด TS13-1212-73 ใน Manage Footprint Libraries
 - ![Screenshot 2025-01-23 214642](https://github.com/user-attachments/assets/a9fd3db3-6553-41bd-8a1a-a84113d4d647)
17. กดปุ่ม Add existing 
 - ![Screenshot 2025-01-23 214710](https://github.com/user-attachments/assets/ee7701b7-82d7-46dd-babd-327161057822)
18. เลือก Folder ที่อยู่ของ ไฟล์
 - ![Screenshot 2025-01-23 214721](https://github.com/user-attachments/assets/bdb6650a-a791-4b53-84c1-1b878ba1db22)
19. เข้าไปยัง Footprint Editor
 - ![Screenshot 2025-01-23 214753](https://github.com/user-attachments/assets/a1fed986-18c5-44f1-bfe3-db8b7647c6fc)
20. ค้นหา Footprint ESP32 C3
 - ![Screenshot 2025-01-23 214823](https://github.com/user-attachments/assets/61108079-1ac7-4692-814c-5b9c5c54dc5f)
21. เข้า File -> Footprint Properties
 - ![Screenshot 2025-01-23 214914](https://github.com/user-attachments/assets/a245ff0f-a43d-4e8b-bba7-c00c2fa1a781)
22. ทำการเลือก หน้าต่าง 3D Models
 - ![Screenshot 2025-01-23 214936](https://github.com/user-attachments/assets/b33e581e-ecce-4552-9013-ff28b73821fc)
23. ทำการลบ 3D เก่าใช้ไม่ได้ และทำการ Add 3D ตัวใหม่
 - ![Screenshot 2025-01-23 215004](https://github.com/user-attachments/assets/af98c17e-c2f0-4c48-a859-4a129ef95b79)
 - ![Screenshot 2025-01-23 215209](https://github.com/user-attachments/assets/fbcf0259-32da-423b-99f7-28695a94003b)
24. จัดตำแหน่งให้ตรงกับรู
 - ![Screenshot 2025-01-23 215425](https://github.com/user-attachments/assets/e3220ccb-0f00-40ad-bc34-41235b277837)
25. อุปกรณ์ทั้งหมดของวงจร PCB นี้
 - ![Screenshot 2025-01-23 220243](https://github.com/user-attachments/assets/a1fd43c9-909a-4c66-8bf7-7743fddbb7fc)

#### Wiring & Checker
26. ทำการลากเส้น เชื่อมต่อ อุปกรณ์ (Add Wire (W))
 - ![Screenshot 2025-01-23 213914](https://github.com/user-attachments/assets/13cad75e-d41e-4298-a46f-2bdf14b1e489)
27. เมื่อต่อวงจรเสร็จ ทำการตรวจสอบ กดปุ่ม Electrical Rules Checker
 - ![Screenshot 2025-01-23 220411](https://github.com/user-attachments/assets/a3857265-848f-4268-82ec-0af2580fad5b)
28. กด Run ERC
 - ![Screenshot 2025-01-23 220435](https://github.com/user-attachments/assets/87a01fac-0f02-43d9-8b5a-b050d6e4d3a0)
29. เมื่อเจอ Error Input Power pin no driven 
 - ![Screenshot 2025-01-23 220435](https://github.com/user-attachments/assets/a39c428c-628f-4853-b9cf-6684d8408792)
30. เพื่อแก้ Error ทำการเพิ่ม PWR_FLAG ที่ตำแหน่ง 5V และ GND 
 - ![Screenshot 2025-01-23 220521](https://github.com/user-attachments/assets/98f7c412-3b4f-4a31-8952-2e3633b5ad0e)
31. Run Electrical Rules Checker อีกครั้ง เพื่อไม่ให้มี Error
 - ![Screenshot 2025-01-23 220608](https://github.com/user-attachments/assets/d965ff8c-7c92-4845-ad0a-f363eb1b8441)
32. Save & Go Tools -> Update PCB from Schematic
 - ![Screenshot 2025-01-23 220649](https://github.com/user-attachments/assets/922bd10e-69ba-49db-b4a0-84fb1bf2c05d)

#### KiCad PCB Editor 
33. กด Update เพิ่มทำการเพิ่มอุปกรณ์ยัง PCB Editor
 - ![Screenshot 2025-01-23 220839](https://github.com/user-attachments/assets/cf6cc13b-b73b-4c04-8688-ee72c841426b)
34. กด Click 1 ครั้งวางทั้งหมด
 - ![Screenshot 2025-01-23 220933](https://github.com/user-attachments/assets/6a6ac362-ae53-422d-9753-0ed86b2b19d8)
35. กำหนดข้อมูลชิ้นงาน PCB
 - ![Screenshot 2025-01-23 221039](https://github.com/user-attachments/assets/1e31b366-6797-4ae6-820d-769d1194aca0)
36. สร้างกรอบ สำหรับตัดขอบ กด Appearance -> Edge.Cuts -> Draw Rectangle
 - ![Screenshot 2025-01-23 221153](https://github.com/user-attachments/assets/2191eb6a-56d6-45be-b7ab-1eb12a98e157)
37. กำหนดขนาดกรอบ และ ขนาดเส้นกรอบ
 - ![Screenshot 2025-01-23 221403](https://github.com/user-attachments/assets/2e2c17d1-3468-4a14-9799-a645f85435d2)
38. จัดอุปกรณ์ให้อยู่ในกรอบที่กำหนดไว้
 - [Screenshot 2025-01-23 221709](https://github.com/user-attachments/assets/3c095b4f-8d59-4c17-ad4b-059f3ef67a3f)
39. กำหนดขนาดของเส้น และ ระยะห่างเส้น กด Board Setup 
 - ![Screenshot 2025-01-23 221739](https://github.com/user-attachments/assets/0d67f444-0860-4576-8a21-982154854a30)
40. กด Net Classes และแก้ไขค่า
 - ![Screenshot 2025-01-23 221818](https://github.com/user-attachments/assets/c082efd6-0f0e-47f5-922b-1887933168cc)
41. กด Violation Severity แก้ไข Clearance violation to Warning และ Courtyards overlap to Warning
 - ![Screenshot 2025-01-23 221859](https://github.com/user-attachments/assets/608b9b19-88b9-4920-8ce4-0afac007617e)
42. เดินลายวงจร โดยเลือก B.CU ที่ Bottom Layer
 - ![Screenshot 2025-01-23 221928](https://github.com/user-attachments/assets/397f4b2a-0a4a-44fe-996c-657c2026a5c2)
43. เลือก Route tracks (X) เดินลายวงจร
 - ![Screenshot 2025-01-23 221955](https://github.com/user-attachments/assets/756840f7-d7c2-4d60-9e01-0464a6fb55d1)

#### Add Plugin to Kicad
44. กด Plugin and Content Manager
 - ![Screenshot 2025-01-23 222132](https://github.com/user-attachments/assets/432f7ee7-ac68-4090-bd56-5f7b64f3a5c2)
45. ค้นหา Freerouting & Fabrication Toolkit และ ติดตั้ง
 - ![Screenshot 2025-01-23 222236](https://github.com/user-attachments/assets/16d8c0de-ca28-4833-a4a1-5915b1617b99)
 - ![Screenshot 2025-01-23 222323](https://github.com/user-attachments/assets/e142cd51-4543-4b68-ac02-441deb7a31e5)
46. ใช้งาน Auto Route Tracks โดยกดที่ Freerouting
 - ![Screenshot 2025-01-23 222401](https://github.com/user-attachments/assets/84eba2ec-2dac-4412-8a17-351486e12baf)
47. สำหรับ Routing 1 layer กด Cancel
 - ![Screenshot 2025-01-23 222554](https://github.com/user-attachments/assets/325e09a8-1940-4fdc-8d9e-83cda4242ab8)
48. เลือก Open the settings 
 - ![Screenshot 2025-01-23 222629](https://github.com/user-attachments/assets/849ecbff-c4e2-49b7-b628-f4dfcb721878)
49. ตั่งค่า Auto-Router Settings ดังนี้
 - ![Screenshot 2025-01-23 222644](https://github.com/user-attachments/assets/4a739852-02fb-4e39-b2ed-64f1f231b8b4)
50. กดปุ่ม Start the auto-router
 - ![Screenshot 2025-01-23 222752](https://github.com/user-attachments/assets/c6ff6949-099c-4972-80ce-c230658c8a33)
51. กด Design Rules Checker เพื่อตรวจสอบ
 - ![Screenshot 2025-01-23 223222](https://github.com/user-attachments/assets/171acd4e-70cc-44ca-a4ab-584cefd0cba4)
52. กด 3D Viewer เพื่อดู 3D PCB Board
 - ![Screenshot 2025-01-23 223748](https://github.com/user-attachments/assets/490c6274-3a9c-4c4d-a0bd-8ad816a11f64)

#### Generate Gerber Files
53. กด Fabrication toolkit 
 - ![Screenshot 2025-01-23 223246](https://github.com/user-attachments/assets/a2a7b18d-656f-47d7-a843-31620335ab64)
54. กด Generate 
 - ![Screenshot 2025-01-23 223305](https://github.com/user-attachments/assets/8a2e0175-caaa-47dd-8633-3cf3f1513d17)
55. จะได้ Gerber Zip File 
 - ![Screenshot 2025-01-23 223324](https://github.com/user-attachments/assets/8dd25329-fd51-490b-9e80-705aa71580e8)

#### JLCPCB
- https://www.jlcpcb.com/
56. สั่งผลิต PCB จาก JLCPCB
 - ![Screenshot 2025-01-23 223350](https://github.com/user-attachments/assets/37f5802f-658d-45f0-a332-4cea600b2b50)
57. ลาก Gerber File ที่ได้ไปยัง Add Gerber บนเวปไซต์
 - ![Screenshot 2025-01-23 223506](https://github.com/user-attachments/assets/f089d185-12d0-4c6f-b393-fe7a144cee29)
58. ดูลาย 3D จาก JLCPCB
 - ![Screenshot 2025-01-23 223649](https://github.com/user-attachments/assets/dc4665b4-03bf-4544-9e0b-363c73383c4e)

https://www.canva.com/design/DAGdEUbxk0E/IqLkosl9fwG4LXA7SQ4JsQ/view?utm_content=DAGdEUbxk0E&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h1f56214bf2
