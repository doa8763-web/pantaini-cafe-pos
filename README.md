# PANTAINI CAFÉ POS Online

ระบบ POS ออนไลน์แบบหลายเครื่อง ใช้ Supabase Auth + PostgreSQL + Realtime

## สิ่งที่มี
- Login ด้วย Email/Password
- สิทธิ์ Admin / Staff
- เมนูออนไลน์จากฐานข้อมูล
- POS และตะกร้าสินค้า
- เงินสด / QR
- คำนวณเงินทอน
- บันทึกออเดอร์และรายการสินค้า
- Dashboard ยอดขาย
- ประวัติการขาย
- Admin จัดการเมนู
- Realtime: เครื่องอื่นเห็นการเปลี่ยนแปลงของเมนู/ยอดขายเมื่อรีเฟรชข้อมูล

## ตั้งค่า Supabase
1. สร้างโปรเจกต์ใน Supabase
2. ไปที่ SQL Editor แล้ววางไฟล์ `supabase.sql` ทั้งหมดและกด Run
3. ไปที่ Authentication > Providers เปิด Email
4. สร้าง user สำหรับ Admin และ Staff ใน Authentication > Users
5. รันคำสั่งท้ายไฟล์ SQL เพื่อเปลี่ยนเจ้าของร้านเป็น `admin`
6. ไปที่ Project Settings > API คัดลอก Project URL และ anon key
7. ใส่ลงใน `config.js`

> ห้ามใส่ `service_role key` ในเว็บไซต์เด็ดขาด ใช้เฉพาะ anon key

## เปิดใช้งานบน Vercel
1. อัปโหลดโฟลเดอร์นี้ไป GitHub
2. Import Project ใน Vercel
3. Deploy

หรืออัปโหลดไฟล์ static ไปยังผู้ให้บริการ static hosting ที่รองรับ HTTPS

## หมายเหตุ
ระบบ Auth ของ Supabase อาจเปิด email confirmation ตามการตั้งค่าโปรเจกต์ ถ้าต้องการให้พนักงานล็อกอินได้ทันที ให้ตั้งค่าตามนโยบายของร้านใน Authentication
