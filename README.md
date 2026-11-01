# TCG Meta Hub

รวมผลการแข่งขันและเด็คลิสต์ของ Riftbound และ Marvel Hero Rush
สร้างด้วย Next.js 15, Tailwind CSS, Prisma และ PostgreSQL

> ข้อมูลทัวร์นาเมนต์ ผู้เล่น และการ์ดในโปรเจกต์นี้เป็นข้อมูลสมมติ (mock) ทั้งหมด

## เริ่มใช้งาน

    npm install
    npm run dev

## หน้าต่าง ๆ

- `/riftbound`, `/marvel-hero-rush`: Dashboard
- `/[game]/tournaments`: รายชื่อทัวร์นาเมนต์ + ตัวกรอง
- `/[game]/tournaments/[slug]`: Top 3 + Decklist
- `/[game]/decks`: ค้นหาเด็ค
- `/[game]/decks/[deckId]`: หน้าเด็คเดี่ยว
- `/admin/import`: นำเข้าเด็คลิสต์ (ต้องเชื่อมฐานข้อมูลก่อน)
- `GET /api/decks?game=riftbound&q=fury`
- `POST /api/revalidate`

## Deploy ขึ้น Vercel

1. Push repo ขึ้น GitHub
2. ไปที่ vercel.com แล้วกด Add New, Project, เลือก repo, กด Deploy
3. ถ้าจะใช้ฐานข้อมูล ให้ใส่ Environment Variables ตาม `.env.example` แล้วรัน `npx prisma migrate deploy`
