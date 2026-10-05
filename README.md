# 🧠 PromptVault v2.1

ระบบจัดการ Prompt AI พร้อม Light/Dark Mode + Admin Login  
เก็บข้อมูลผ่าน Google Sheets

## ✨ ฟีเจอร์

### 🌓 โหมดสี
- **เริ่มต้นเป็นโหมดสว่าง (Light Mode)**
- สลับเป็นโหมดมืดได้ตลอดเวลา
- บันทึก preference อัตโนมัติ

### 🔐 Admin Login
- ต้องใส่รหัสผ่านเพื่อเข้า Admin Panel
- รหัสเริ่มต้น: `admin123`
- เปลี่ยนรหัสผ่านได้ใน Admin Panel → แท็บ "ความปลอดภัย"
- รหัสผ่านเก็บใน Google Sheets (Settings Sheet)

### 👨‍💼 Admin Panel
- 📊 ภาพรวม: สถิติ, กราฟ, Quick Actions
- 📝 จัดการ Prompts (Table view)
- 📂 หมวดหมู่
- 🔐 ความปลอดภัย: เปลี่ยนรหัสผ่าน
- ⚙️ ตั้งค่า: API URL, โหมดสี
- 📜 Logs: บันทึกการใช้งาน

### 🎯 ฟีเจอร์หลัก
- ✅ CRUD Prompts
- 🔧 ตัวแปร `{{variable}}`
- 📋 คัดลอก Prompt
- 📂 หมวดหมู่ + แท็ก
- ⭐ รายการโปรด
- 🔍 ค้นหา + เรียงลำดับ
- 📊 สถิติการใช้งาน
- 📥 Import/Export JSON
- 🔄 ซิงค์ Google Sheets

## 🚀 การติดตั้ง

### ขั้นตอนที่ 1: สร้าง Google Sheets
1. ไปที่ [sheets.google.com](https://sheets.google.com)
2. สร้าง Spreadsheet ใหม่

### ขั้นตอนที่ 2: เปิด Apps Script
1. เมนู **ส่วนขยาย → Apps Script**

### ขั้นตอนที่ 3: วางโค้ด
1. คัดลอกโค้ดจาก `code.gs` ทั้งหมด
2. วางใน Apps Script Editor
3. บันทึก (Ctrl+S)

### ขั้นตอนที่ 4: Deploy
1. **Deploy → New deployment**
2. Type: **Web app**
3. Execute as: **Me**
4. Who has access: **Anyone**
5. คัดลอก Web App URL

### ขั้นตอนที่ 5: เชื่อมต่อ Frontend
1. เปิด `index.html` (หรือ Deploy บน GitHub Pages)
2. กดปุ่ม 🔐 → ใส่รหัส `admin123` → Login
3. ไปที่ ⚙️ ตั้งค่า → วาง URL → บันทึก

## 🔑 การจัดการรหัสผ่าน

### ผ่าน Admin Panel
1. Login ด้วยรหัสปัจจุบัน
2. ไปที่แท็บ **🔐 ความปลอดภัย**
3. ใส่รหัสปัจจุบัน + รหัสใหม่ → เปลี่ยน

### ผ่าน Google Sheets โดยตรง
1. เปิด Google Sheets
2. ไปที่ Sheet ชื่อ **Settings**
3. แก้ไขค่าในคอลัมน์ `value` ของ row `admin_password`
4. บันทึก → ใช้รหัสใหม่ได้ทันที

## 📁 โครงสร้าง Google Sheets

ระบบจะสร้าง 3 Sheets อัตโนมัติ:
- **Prompts** - ข้อมูล prompts
- **Logs** - บันทึกการใช้งาน
- **Settings** - ตั้งค่า (รวมถึงรหัสผ่าน)

## 🌐 Deploy บน GitHub Pages

1. สร้าง Repository ใหม่บน GitHub
2. อัพโหลดไฟล์ `index.html`
3. ไปที่ **Settings → Pages**
4. Source: **Deploy from a branch** → `main` / `/ (root)`
5. เว็บไซต์จะอยู่ที่ `https://username.github.io/repo-name/`

## 📄 License

MIT License - ใช้งานได้อย่างอิสระ
