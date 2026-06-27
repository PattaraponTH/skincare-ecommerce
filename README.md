# 🛍️ Skincare Shop

ระบบร้านค้าออนไลน์สำหรับจำหน่ายผลิตภัณฑ์ดูแลผิวพรรณ พัฒนาด้วย React.js และ Node.js

---

## 📋 รายละเอียดโครงงาน

| รายการ | รายละเอียด |
|--------|-----------|
| **วิชา** | CSI204 Digital Platform for Software Development |
| **ประเภทโครงงาน** | E-Commerce Website |
| **แพลตฟอร์ม** | Web Platform |

---

## 🎯 วัตถุประสงค์

- พัฒนาเว็บไซต์ขายสินค้า Skincare ออนไลน์
- รองรับการแสดงสินค้า ตะกร้าสินค้า และระบบคำสั่งซื้อ
- จัดการข้อมูลสินค้าและคำสั่งซื้อผ่าน Admin Dashboard
- ฝึกใช้งาน Git Workflow ผ่าน GitHub และ SourceTree

---

## ⚙️ Tech Stack

### Frontend
- **React.js** — UI Framework (Component-Based SPA)
- **CSS3** — Styling

### Backend
- **Node.js** — Runtime Environment
- **Express.js** — REST API Server
- **JWT** — Authentication & Authorization

### Database
- **PostgreSQL** — Relational Database (ข้อมูลสินค้า, คำสั่งซื้อ, ผู้ใช้)

### DevOps & Tools
- **GitHub** — Version Control & Repository Hosting
- **SourceTree** — Git GUI Client
- **GitHub Pages** — Frontend Deployment

---

## 📁 โครงสร้างโปรเจกต์

```
skincare-shop/
├── README.md               # เอกสารโครงงาน
├── diagram.mmd             # System Architecture Diagram (Mermaid)
├── markdown.html           # Project Overview (GitHub Pages)
└── doc/
    └── analysis.md         # Analysis & Design Document
```

---

## ✨ ฟีเจอร์หลัก

- **หน้าแสดงสินค้า** — รายการสินค้า Skincare พร้อมรูปภาพและราคา
- **ตะกร้าสินค้า** — เพิ่ม/ลบสินค้า และคำนวณราคารวม
- **ระบบสมาชิก** — สมัครสมาชิก / เข้าสู่ระบบ ด้วย JWT
- **ระบบคำสั่งซื้อ** — สร้างและติดตามสถานะคำสั่งซื้อ
- **ระบบชำระเงิน** — บันทึก Transaction และสถานะการชำระเงิน
- **ระบบรีวิวสินค้า** — ให้คะแนน 1–5 ดาว และแสดงความคิดเห็นหลังซื้อสินค้า
- **Admin Dashboard** — จัดการสินค้า หมวดหมู่ และคำสั่งซื้อ

---

## 🗄️ Database Schema

| Table | คำอธิบาย | คอลัมน์หลัก |
|-------|----------|------------|
| `users` | ข้อมูลผู้ใช้งาน | id, name, email, password, role |
| `products` | ข้อมูลสินค้า ราคา สต็อก | id, name, price, stock, category_id |
| `categories` | หมวดหมู่สินค้า | id, name |
| `orders` | คำสั่งซื้อและสถานะ | id, user_id, total, status |
| `order_items` | รายการสินค้าในคำสั่งซื้อ | id, order_id, product_id, qty, price |
| `payments` | ข้อมูลการชำระเงินและ transaction | id, order_id, method, status, paid_at |
| `reviews` | รีวิวและคะแนนสินค้าจากผู้ซื้อ | id, user_id, product_id, rating, comment |

---

## 🚀 การติดตั้งและใช้งาน

### ความต้องการของระบบ
- Node.js v18+
- npm v9+
- PostgreSQL v15+

### ขั้นตอนการติดตั้ง

```bash
# 1. Clone repository
git clone https://github.com/PattaraponTH/skincare-shop.git
cd skincare-shop

# 2. ติดตั้ง dependencies (Frontend)
cd frontend
npm install

# 3. ติดตั้ง dependencies (Backend)
cd ../backend
npm install

# 4. ตั้งค่า Environment Variables
cp .env.example .env
# แก้ไข DATABASE_URL, JWT_SECRET ใน .env

# 5. รันโปรเจกต์
npm run dev
```

---

## 🌐 GitHub Pages

เข้าถึงเว็บไซต์ได้ที่: `https://PattaraponTH.github.io/skincare-shop`

---

## 📄 เอกสารที่เกี่ยวข้อง

- [Analysis & Design Document](doc/analysis.md)
- [System Architecture Diagram](diagram.mmd)