# GitHub Pages Site

โครงสร้างนี้พร้อมอัปขึ้น GitHub repo และเปิดใช้กับ GitHub Pages ได้ทันที

## โครงสร้างไฟล์

- `index.html` หน้าเว็บหลัก
- `assets/css/fonts.css` ฟอนต์ Sarabun แบบ local
- `assets/js/chart.umd.js` ไฟล์ Chart.js แบบ local
- `assets/fonts/*.woff2` ไฟล์ฟอนต์ที่ใช้จริง
- `assets/images/favicon.svg` ไอคอนเว็บ
- `assets/images/social-preview.svg` ภาพพรีวิวสำหรับ social share
- `site.webmanifest` metadata สำหรับ PWA/ไอคอน
- `.gitignore` ไฟล์ที่ไม่ต้องการให้ติด repo
- `.nojekyll` ปิดการประมวลผลแบบ Jekyll บน GitHub Pages

## วิธีใช้งานกับ GitHub Pages

1. อัปโหลดทุกไฟล์ในโฟลเดอร์นี้ขึ้น repo
2. ให้ `index.html` อยู่ที่ root ของ branch หรือ folder ที่ใช้ publish
3. เปิด `Settings > Pages`
4. เลือก branch ที่ต้องการ publish เช่น `main` และเลือก folder เป็น `/ (root)`

## หมายเหตุ

- เว็บไซต์นี้ไม่พึ่ง CDN ภายนอกแล้ว
- สามารถเปิดไฟล์ `index.html` จากเครื่องโดยตรงหรือผ่าน GitHub Pages ได้

## เตรียม repo และ push ขึ้น GitHub

รันคำสั่งต่อไปนี้ในโฟลเดอร์นี้

```powershell
cd C:\Users\PRAPAWADEE W\Downloads\boat-report-github-pages
git init
git add .
git commit -m "Initial GitHub Pages dashboard"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

จากนั้นไปที่ `Settings > Pages` แล้วเลือก branch `main` และ folder เป็น `/ (root)`

## ข้อควรทราบเรื่อง Social Preview

- ตอนนี้ใช้ไฟล์ local `assets/images/social-preview.svg` และ `favicon.svg`
- หากต้องการให้ social crawler บางระบบรองรับได้กว้างขึ้น แนะนำแปลง preview เป็น `.png` ขนาด `1200x630` แล้วเปลี่ยนค่า `og:image` และ `twitter:image` ให้ชี้ไปไฟล์ `.png`