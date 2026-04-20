# 🚀 Deploy to Railway (1 Click)

ผู้อื่นสามารถใช้ระบบได้ผ่าน Railway ที่ deploy โดยอัตโนมัติจาก GitHub

## การ Deploy บน Railway

### ขั้นตอน:

1. **ไปที่ Railway**
   - https://railway.app

2. **Sign up ด้วย GitHub**
   - Click "Sign up with GitHub"

3. **Create New Project**
   - Click "New Project"
   - Select "Deploy from GitHub repo"

4. **เลือก Repository**
   - Search `kanoon254569-cell/store` (หรืออีกชื่อ repo)
   - Click "Deploy"

5. **Railway จะ Auto Deploy**
   - รอ build เสร็จ (3-5 นาที)
   - Get public URL อัตโนมัติ

6. **ส่ง URL ให้ผู้อื่นใช้**
   - เช่น: `https://store-abc123.railway.app`

---

## ✨ Auto Deploy Features

✅ **Automatic Deployment** - ทุกครั้ง push ไป GitHub  
✅ **Environment Variables** - ตั้งได้ใน Railway Dashboard  
✅ **Free Tier** - ทำงานได้ฟรี  
✅ **Public URL** - ผู้อื่นเข้าถึงได้  
✅ **Logs** - ดูได้ใน Railway Panel  

---

## การเข้าใช้งาน

### Login
- Email: `admin@ecommerce.local`
- Password: (ตั้งตอนสร้าง admin user)

### Features
- Dashboard - ดูยอดขายและสต็อก
- Products - เพิ่มสินค้าขายหรือจัดการสต็อก
- Orders - ดูรายการสั่งซื้อ

---

## Environment Variables (ตั้งใน Railway Dashboard)

```
MONGODB_URL=your_db_url
JWT_SECRET=your_secret_key
ADMIN_EMAIL=admin@ecommerce.local
```

---

## Troubleshooting

**Q: Deploy ไม่สำเร็จ?**
- ดู Logs ใน Railway Dashboard
- ตรวจสอบ Dockerfile
- เช็ค requirements.txt มี dependency ครบไหม

**Q: Database ไม่เชื่อมต่อ?**
- ตั้ง MONGODB_URL ใน Environment Variables

**Q: สามารถใช้ฟรีตลอดไป?**
- Railway free tier: $5/month free credits
- ราคาต่อสินค้า: $0.001 - $0.005 per request
- Recommended สำหรับ Demo

---

## ลิงก์ที่ต้องจำ

- 📱 **Repository**: https://github.com/kanoon254569-cell/store
- 🚀 **Railway**: https://railway.app
- 📚 **API Docs**: `https://your-domain.railway.app/docs`
- 🎨 **Dashboard**: `https://your-domain.railway.app` (หลังจาก deploy)

---

## Share เพื่อให้ผู้อื่นใช้

1. บอกผู้อื่นไปที่ Railway URL ที่ได้
2. ป้อน admin credentials
3. เข้าใช้ Dashboard ได้เลย!

---

### Railway ดีกว่าตัวเลือกอื่นช่วง?

| Platform | Setup | Cost | Auto-Deploy |
|----------|-------|------|-------------|
| Railway | ⭐⭐⭐⭐⭐ | $5/mo free | ✅ |
| Heroku | ⭐⭐⭐⭐ | Free (limited) | ✅ |
| Vercel | ⭐⭐⭐⭐ | Free | ✅ (frontend only) |
| AWS/GCP | ⭐⭐⭐ | Pay-as-you-go | ⚙️ Manual |

Railway เหมาะที่สุดสำหรับ Demo + Production + Budget friendly! 🎯
