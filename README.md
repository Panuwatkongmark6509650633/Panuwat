# Strapi คืออะไร
Strapi คือระบบ Content Management System (CMS) แบบ Headless ที่ถูกพัฒนาโดยใช้ JavaScript และ Node.js ซึ่งมีความยืดหยุ่นสูง ผู้ใช้สามารถสร้างและจัดการเนื้อหาต่างๆ ผ่าน API ได้อย่างง่ายดายโดยไม่ต้องผูกพันกับรูปแบบการแสดงผลเฉพาะแพลตฟอร์มใดๆ
# สารบัญ
 - [รายละเอียดของ Strapi](#%E0%B8%A3%E0%B8%B2%E0%B8%A2%E0%B8%A5%E0%B8%B0%E0%B9%80%E0%B8%AD%E0%B8%B5%E0%B8%A2%E0%B8%94%E0%B8%82%E0%B8%AD%E0%B8%87%20Strapi)
 - [ขั้นตอนการติดตั้ง](#%E0%B8%82%E0%B8%B1%E0%B9%89%E0%B8%99%E0%B8%95%E0%B8%AD%E0%B8%99%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B8%95%E0%B8%B4%E0%B8%94%E0%B8%95%E0%B8%B1%E0%B9%89%E0%B8%87)
 - [กรณีการใช้งาน](#%E0%B8%81%E0%B8%A3%E0%B8%93%E0%B8%B5%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B9%83%E0%B8%8A%E0%B9%89%E0%B8%87%E0%B8%B2%E0%B8%99)
 - [เกี่ยวกับ .gitignore](#%E0%B9%80%E0%B8%81%E0%B8%B5%E0%B9%88%E0%B8%A2%E0%B8%A7%E0%B8%81%E0%B8%B1%E0%B8%9A%20.gitignore)
 - [Deployment](#Deployment)
## รายละเอียดของ Strapi
CMS หรือ **Content Management System** คือระบบที่ช่วยในการจัดการเนื้อหาเว็บไซต์หรือแอปพลิเคชันโดยไม่จำเป็นต้องมีความรู้ทางการเขียนโค้ดมากนัก ผู้ใช้สามารถสร้าง, แก้ไข, และจัดการเนื้อหาผ่านอินเทอร์เฟซที่ใช้งานง่าย เช่น แดชบอร์ดหรือแผงควบคุม ซึ่งช่วยให้การจัดการเนื้อหาสะดวกและรวดเร็วขึ้น

**Strapi** เป็นหนึ่งใน CMS ที่ได้รับความนิยม โดย Strapi เป็น CMS แบบ Headless ซึ่งหมายความว่า มันแยกส่วนของการจัดการเนื้อหาออกจากส่วนของการแสดงผล ทำให้สามารถเชื่อมต่อกับ Frontend หรือแอปพลิเคชันใด ๆ ผ่าน API เช่น REST หรือ GraphQL ได้อย่างยืดหยุ่น นอกจากนี้ Strapi ยังเป็น Open Source ซึ่งหมายความว่าผู้ใช้สามารถปรับแต่งและขยายการทำงานได้ตามความต้องการ

### กรณีใช้งาน Strapi

 1. กรณีการใช้งานของ Strapi:

1.  **เว็บไซต์และบล็อก**: ใช้ Strapi เพื่อจัดการเนื้อหา เช่น บทความ, ข่าวสาร, และโพสต์บล็อก โดยเชื่อมต่อกับ Frontend ที่สร้างด้วยเทคโนโลยีต่าง ๆ เช่น React, Vue, หรือ Angular
    
2.  **แอปพลิเคชันมือถือ**: Strapi สามารถให้บริการเนื้อหาผ่าน API สำหรับแอปพลิเคชันมือถือ (iOS หรือ Android) ทำให้สามารถจัดการข้อมูลที่แสดงในแอปได้ง่าย
    
3.  **ระบบจัดการเนื้อหา eCommerce**: ใช้ Strapi เพื่อจัดการข้อมูลผลิตภัณฑ์, หมวดหมู่, คำสั่งซื้อ, และข้อมูลลูกค้า สำหรับเว็บไซต์หรือแอปพลิเคชัน eCommerce
    
4.  **แพลตฟอร์มการเรียนรู้**: สร้างและจัดการเนื้อหาเกี่ยวกับหลักสูตร, บทเรียน, และข้อสอบ โดย Strapi สามารถเชื่อมต่อกับ Frontend ที่ใช้ในการสอนและเรียนรู้
    
5.  **ระบบการจัดการเนื้อหาภายในองค์กร**: ใช้ Strapi เพื่อจัดการข้อมูลที่ต้องการแบ่งปันภายในองค์กร เช่น เอกสาร, ข่าวสารภายใน, และฐานข้อมูลทรัพยากร
    
6.  **โปรเจกต์ที่ต้องการ API ที่กำหนดเอง**: Strapi ช่วยในการสร้าง API ที่กำหนดเองตามความต้องการของโปรเจกต์ ทำให้สามารถจัดการและให้บริการเนื้อหาได้อย่างยืดหยุ่น

# ขั้นตอนการติดตั้ง
ความต้องการขั้นต่ำของระบบ

 -  **NodeJS**  v.18 upto v.20
 - **npm**  < v.6

ขั้นตอน

 1. สร้าง folder ที่ต้องการเก็บ Strapi
 2. กด `Win + R` บนแป้นพิมพ์ แล้วพิมพ์ `cmd` จากนั้นกด Enter เพื่อเปิด Command Prompt
 3. นำทางไปยังโฟลเดอร์ที่สร้างไว้โดย `cd` เข้าไปใน folder ที่สร้างไว้
 4. ทำการ Download และติดตั้ง Strapi ตามคำสั่งดังนี้ 
```
npx create-strapi-app@latest my-project --quickstart
#เมื่อรันจะขึ้นข้อความให้เลือก Login/Sign up หรือ Skip แนะนำให้เลือก Login
```

5. `cd` เข้าไปใน `my-project` จากนั้นทำการตรวจสอบ version ด้วยคำสั่ง`npm -v`
6. เริ่มต้นใช้งาน Strapi ด้วยคำสั่ง `npm run develop` จะเด้งเข้าสู่หน้าสมัคร admin `localhost:1337/admin/registe` อัตโนมัติ

![image](https://github.com/user-attachments/assets/f301945f-3591-435b-9297-f60fae73a832)

7. สามารถทำการ Register เพื่อเข้าใช้งานได้





## Deployment

Strapi gives you many possible deployment options for your project including [Strapi Cloud](https://cloud.strapi.io). Browse the [deployment section of the documentation](https://docs.strapi.io/dev-docs/deployment) to find the best solution for your use case.

```
yarn strapi deploy
```

## 📚 Learn more
##ขั้นตอนในการติดตั้ง

- [Resource center](https://strapi.io/resource-center) - Strapi resource center.
- [Strapi documentation](https://docs.strapi.io) - Official Strapi documentation.
- [Strapi tutorials](https://strapi.io/tutorials) - List of tutorials made by the core team and the community.
- [Strapi blog](https://strapi.io/blog) - Official Strapi blog containing articles made by the Strapi team and the community.
- [Changelog](https://strapi.io/changelog) - Find out about the Strapi product updates, new features and general improvements.

Feel free to check out the [Strapi GitHub repository](https://github.com/strapi/strapi). Your feedback and contributions are welcome!

## ✨ Community

- [Discord](https://discord.strapi.io) - Come chat with the Strapi community including the core team.
- [Forum](https://forum.strapi.io/) - Place to discuss, ask questions and find answers, show your Strapi project and get feedback or just talk with other Community members.
- [Awesome Strapi](https://github.com/strapi/awesome-strapi) - A curated list of awesome things related to Strapi.

---

<sub>🤫 Psst! [Strapi is hiring](https://strapi.io/careers).</sub>
