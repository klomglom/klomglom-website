# วิธี Deploy klomglom.com บน GitHub + Vercel

## ขั้นตอนทั้งหมด (ทำครั้งเดียว ใช้ได้ตลอด)

---

### ขั้นตอนที่ 1 — สร้าง GitHub Repository

1. ไปที่ https://github.com แล้ว Login (ถ้ายังไม่มี account ให้สมัครฟรี)
2. กดปุ่ม **"New"** (สีเขียว) มุมบนซ้าย
3. ตั้งชื่อ Repository เช่น `klomglom-website`
4. เลือก **Public**
5. กด **"Create repository"**

---

### ขั้นตอนที่ 2 — Upload ไฟล์ขึ้น GitHub

1. ใน Repository ที่เพิ่งสร้าง กด **"uploading an existing file"**
2. ลาก **ไฟล์ `index.html`** จากคอมขึ้นไป
3. กด **"Commit changes"** (ปุ่มสีเขียวด้านล่าง)

---

### ขั้นตอนที่ 3 — เชื่อม Vercel กับ GitHub

1. ไปที่ https://vercel.com แล้ว Login ด้วย **GitHub account เดียวกัน**
2. กด **"Add New Project"**
3. เลือก Repository `klomglom-website` ที่เพิ่งสร้าง
4. กด **"Deploy"** — รอประมาณ 30 วินาที
5. Vercel จะให้ URL ชั่วคราวเช่น `klomglom-website.vercel.app` → ทดสอบได้เลย

---

### ขั้นตอนที่ 4 — ผูก Domain klomglom.com

1. ใน Vercel Project กด **"Settings"** → **"Domains"**
2. พิมพ์ `klomglom.com` แล้วกด **"Add"**
3. Vercel จะแสดง DNS records ที่ต้องตั้งค่า เช่น:
   - **Type A** → `76.76.21.21`
   - **Type CNAME** → `cname.vercel-dns.com`
4. ไปที่ผู้ให้บริการ Domain ของคุณ (เช่น Cloudflare, GoDaddy, หรือ จดทะเบียน.com)
5. แก้ไข DNS ตาม records ที่ Vercel แจ้ง
6. รอ 5–30 นาที DNS จะอัพเดต

---

### ขั้นตอนที่ 5 — อัพเดตเนื้อหาในอนาคต

เมื่อต้องการแก้ไขเนื้อหา:
1. เปิดไฟล์ `index.html` บนคอม แก้ไขได้เลย
2. ไปที่ GitHub Repository → กดชื่อไฟล์ `index.html`
3. กดปุ่มดินสอ (Edit) มุมขวา
4. วางเนื้อหาใหม่ → กด **"Commit changes"**
5. Vercel จะ Deploy ให้อัตโนมัติ ภายใน 30 วินาที ✅

---

## ทำไม GitHub + Vercel ถึงดีกว่า Google Sites?

| | Google Sites | GitHub + Vercel |
|---|---|---|
| SEO | ❌ แย่ (JS-rendered) | ✅ ดีมาก (HTML สะอาด) |
| Speed | ❌ ช้า | ✅ เร็วมาก (CDN ทั่วโลก) |
| Custom Domain | ⚠️ ได้แต่ซับซ้อน | ✅ ง่าย |
| Meta Tags | ❌ ควบคุมไม่ได้ | ✅ ควบคุมได้ทั้งหมด |
| Schema/JSON-LD | ❌ ไม่รองรับ | ✅ รองรับ |
| ราคา | ฟรี | ฟรี (plan ฟรีเพียงพอ) |

---

## SEO Keywords ที่ใส่ไว้แล้ว

- ซุปไก่บำรุงสุขภาพ (Primary)
- ซุปไก่ตุ๋น
- ของเยี่ยมไข้
- ซุปไก่สมุนไพร
- อาหารบำรุงผู้สูงอายุ
- ซุปบำรุงร่างกาย
- ซุปไก่ไม่ปรุงรส
- ซุปไก่โสม

---

*สร้างโดย Claude สำหรับ klomglom.com*
